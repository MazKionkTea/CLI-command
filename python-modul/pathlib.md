| Command                      | Deskripsi                                                                                   | Contoh                                                            |
| ---------------------------- | ------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| `from pathlib import Path`   | Mengimpor class `Path` untuk bekerja dengan path file/direktori secara object-oriented.     | `from pathlib import Path`                                        |
| `Path()`                     | Membuat objek path baru.                                                                    | `p = Path("data/file.txt")`                                       |
| `Path.cwd()`                 | Mengembalikan current working directory.                                                    | `Path.cwd()`                                                      |
| `Path.home()`                | Mengembalikan direktori home user.                                                          | `Path.home()`                                                     |
| `Path("...")`                | Membuat path dari string.                                                                   | `p = Path("data/file.txt")`                                       |
| `Path / "nama"`              | Menggabungkan path menggunakan operator `/`.                                                | `Path("data") / "file.txt"`                                       |
| `Path.joinpath()`            | Menggabungkan satu atau beberapa bagian path.                                               | `Path("data").joinpath("file.txt")`                               |
| `Path.name`                  | Mendapatkan nama file/direktori terakhir dari path.                                         | `Path("data/test.txt").name`                                      |
| `Path.stem`                  | Mendapatkan nama file tanpa ekstensi.                                                       | `Path("test.txt").stem`                                           |
| `Path.suffix`                | Mendapatkan ekstensi file terakhir.                                                         | `Path("test.txt").suffix`                                         |
| `Path.suffixes`              | Mendapatkan semua ekstensi file.                                                            | `Path("archive.tar.gz").suffixes`                                 |
| `Path.parent`                | Mendapatkan direktori induk.                                                                | `Path("data/test.txt").parent`                                    |
| `Path.parents`               | Mendapatkan seluruh parent path sebagai sequence.                                           | `Path("a/b/c").parents[1]`                                        |
| `Path.anchor`                | Mendapatkan bagian anchor/root dari path.                                                   | `Path("/home/user").anchor`                                       |
| `Path.parts`                 | Memecah path menjadi tuple bagian-bagiannya.                                                | `Path("a/b/c.txt").parts`                                         |
| `Path.as_posix()`            | Mengubah path menjadi format POSIX dengan `/`.                                              | `Path("a\\b.txt").as_posix()`                                     |
| `Path.as_uri()`              | Mengubah path absolut menjadi URI `file://`.                                                | `Path("/home/user/a.txt").as_uri()`                               |
| `Path.absolute()`            | Menghasilkan path absolut tanpa harus melakukan resolving symlink.                          | `Path("data/a.txt").absolute()`                                   |
| `Path.resolve()`             | Menghasilkan path absolut yang telah di-resolve, termasuk symlink.                          | `Path("data/a.txt").resolve()`                                    |
| `Path.is_absolute()`         | Mengecek apakah path merupakan absolute path.                                               | `Path("/home/user").is_absolute()`                                |
| `Path.is_relative_to()`      | Mengecek apakah path berada di bawah path tertentu.                                         | `Path("a/b").is_relative_to("a")`                                 |
| `Path.relative_to()`         | Mendapatkan path relatif terhadap path tertentu.                                            | `Path("/a/b/c").relative_to("/a")`                                |
| `Path.match()`               | Mengecek apakah path cocok dengan pola glob tertentu.                                       | `Path("test.py").match("*.py")`                                   |
| `Path.glob()`                | Mencari file/direktori berdasarkan pola glob.                                               | `Path("data").glob("*.txt")`                                      |
| `Path.rglob()`               | Melakukan pencarian glob secara rekursif ke subdirektori.                                   | `Path("data").rglob("*.py")`                                      |
| `Path.iterdir()`             | Mengiterasi isi sebuah direktori.                                                           | `for p in Path("data").iterdir(): print(p)`                       |
| `Path.exists()`              | Mengecek apakah path ada.                                                                   | `Path("data.txt").exists()`                                       |
| `Path.is_file()`             | Mengecek apakah path menunjuk ke file biasa.                                                | `Path("data.txt").is_file()`                                      |
| `Path.is_dir()`              | Mengecek apakah path menunjuk ke direktori.                                                 | `Path("data").is_dir()`                                           |
| `Path.is_symlink()`          | Mengecek apakah path merupakan symbolic link.                                               | `Path("link").is_symlink()`                                       |
| `Path.is_mount()`            | Mengecek apakah path merupakan mount point.                                                 | `Path("/").is_mount()`                                            |
| `Path.is_socket()`           | Mengecek apakah path menunjuk ke Unix socket.                                               | `Path("socket").is_socket()`                                      |
| `Path.is_fifo()`             | Mengecek apakah path merupakan FIFO/named pipe.                                             | `Path("pipe").is_fifo()`                                          |
| `Path.is_block_device()`     | Mengecek apakah path merupakan block device.                                                | `Path("device").is_block_device()`                                |
| `Path.is_char_device()`      | Mengecek apakah path merupakan character device.                                            | `Path("device").is_char_device()`                                 |
| `Path.stat()`                | Mendapatkan informasi metadata file/direktori.                                              | `Path("data.txt").stat()`                                         |
| `Path.lstat()`               | Mendapatkan metadata path tanpa mengikuti symbolic link.                                    | `Path("link").lstat()`                                            |
| `Path.owner()`               | Mendapatkan nama owner file/direktori.                                                      | `Path("data.txt").owner()`                                        |
| `Path.group()`               | Mendapatkan nama group file/direktori.                                                      | `Path("data.txt").group()`                                        |
| `Path.chmod()`               | Mengubah permission/mode file atau direktori.                                               | `Path("data.txt").chmod(0o644)`                                   |
| `Path.lchmod()`              | Mengubah permission symbolic link tanpa mengikuti link.                                     | `Path("link").lchmod(0o777)`                                      |
| `Path.mkdir()`               | Membuat direktori baru.                                                                     | `Path("data").mkdir()`                                            |
| `Path.mkdir(parents=True)`   | Membuat direktori beserta parent yang belum ada.                                            | `Path("a/b/c").mkdir(parents=True)`                               |
| `Path.mkdir(exist_ok=True)`  | Membuat direktori tanpa error jika direktori sudah ada.                                     | `Path("data").mkdir(exist_ok=True)`                               |
| `Path.rmdir()`               | Menghapus direktori yang kosong.                                                            | `Path("data").rmdir()`                                            |
| `Path.unlink()`              | Menghapus file atau symbolic link.                                                          | `Path("data.txt").unlink()`                                       |
| `Path.rename()`              | Mengganti nama atau memindahkan path.                                                       | `Path("old.txt").rename("new.txt")`                               |
| `Path.replace()`             | Mengganti path tujuan, termasuk menimpa file yang sudah ada.                                | `Path("old.txt").replace("new.txt")`                              |
| `Path.touch()`               | Membuat file kosong atau memperbarui timestamp file.                                        | `Path("data.txt").touch()`                                        |
| `Path.read_text()`           | Membaca isi file sebagai string.                                                            | `Path("data.txt").read_text()`                                    |
| `Path.write_text()`          | Menulis string ke file.                                                                     | `Path("data.txt").write_text("Hello")`                            |
| `Path.read_bytes()`          | Membaca isi file dalam bentuk `bytes`.                                                      | `Path("data.bin").read_bytes()`                                   |
| `Path.write_bytes()`         | Menulis data `bytes` ke file.                                                               | `Path("data.bin").write_bytes(b"Hello")`                          |
| `Path.open()`                | Membuka file seperti fungsi built-in `open()`.                                              | `with Path("data.txt").open("r") as f: print(f.read())`           |
| `Path.samefile()`            | Mengecek apakah dua path menunjuk ke file yang sama.                                        | `Path("a.txt").samefile("b.txt")`                                 |
| `Path.symlink_to()`          | Membuat symbolic link yang menunjuk ke path tertentu.                                       | `Path("link").symlink_to("data.txt")`                             |
| `Path.hardlink_to()`         | Membuat hard link ke file tertentu.                                                         | `Path("copy.txt").hardlink_to("data.txt")`                        |
| `Path.readlink()`            | Mendapatkan target dari symbolic link.                                                      | `Path("link").readlink()`                                         |
| `Path.walk()`                | Melakukan traversal direktori secara top-down/bottom-up dan menghasilkan root, dirs, files. | `for root, dirs, files in Path(".").walk(): print(root, files)`   |
| `PurePath()`                 | Membuat objek path murni tanpa operasi filesystem.                                          | `from pathlib import PurePath; PurePath("a/b.txt")`               |
| `PurePosixPath()`            | Membuat pure path dengan aturan POSIX.                                                      | `from pathlib import PurePosixPath; PurePosixPath("/a/b")`        |
| `PureWindowsPath()`          | Membuat pure path dengan aturan Windows.                                                    | `from pathlib import PureWindowsPath; PureWindowsPath(r"C:\a\b")` |
| `PurePath.parts`             | Mendapatkan komponen-komponen pure path.                                                    | `PurePath("a/b/c").parts`                                         |
| `PurePath.name`              | Mendapatkan nama terakhir dari pure path.                                                   | `PurePath("a/b.txt").name`                                        |
| `PurePath.stem`              | Mendapatkan nama tanpa suffix.                                                              | `PurePath("a/b.txt").stem`                                        |
| `PurePath.suffix`            | Mendapatkan suffix/ekstensi terakhir.                                                       | `PurePath("a/b.txt").suffix`                                      |
| `PurePath.suffixes`          | Mendapatkan seluruh suffix/ekstensi.                                                        | `PurePath("a/b.tar.gz").suffixes`                                 |
| `PurePath.parent`            | Mendapatkan parent pure path.                                                               | `PurePath("a/b/c").parent`                                        |
| `PurePath.parents`           | Mendapatkan seluruh parent path.                                                            | `PurePath("a/b/c").parents`                                       |
| `PurePath.anchor`            | Mendapatkan anchor dari pure path.                                                          | `PurePath("/a/b").anchor`                                         |
| `PurePath.joinpath()`        | Menggabungkan bagian-bagian pure path.                                                      | `PurePath("a").joinpath("b", "c")`                                |
| `PurePath.is_absolute()`     | Mengecek apakah pure path bersifat absolut.                                                 | `PurePath("/a").is_absolute()`                                    |
| `PurePath.is_relative_to()`  | Mengecek apakah pure path relatif terhadap path tertentu.                                   | `PurePath("a/b").is_relative_to("a")`                             |
| `PurePath.relative_to()`     | Mendapatkan pure path relatif terhadap path tertentu.                                       | `PurePath("a/b/c").relative_to("a")`                              |
| `PurePath.match()`           | Mengecek kecocokan pure path dengan pola glob.                                              | `PurePath("test.py").match("*.py")`                               |
| `PurePath.as_posix()`        | Mengubah pure path menjadi format POSIX.                                                    | `PurePath(r"a\b").as_posix()`                                     |
| `PurePath.as_uri()`          | Mengubah pure path absolut menjadi URI.                                                     | `PurePath("/a/b").as_uri()`                                       |
| `Path.from_uri()`            | Membuat `Path` dari URI `file://`.                                                          | `Path.from_uri("file:///tmp/test.txt")`                           |
| `Path.from_fd()`             | Membuat `Path` dari file descriptor.                                                        | `Path.from_fd(fd)`                                                |
| `Path` sebagai `os.PathLike` | Objek `Path` dapat digunakan langsung pada API Python yang menerima path-like object.       | `open(Path("data.txt"))`                                          |
| `os.fspath()`                | Mengambil representasi filesystem path dari objek `Path`.                                   | `os.fspath(Path("data.txt"))`                                     |
