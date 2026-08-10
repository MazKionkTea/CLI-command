| Command | Deskripsi | Contoh |
|---|---|---|
| `help` | Menampilkan daftar perintah yang tersedia di dalam sesi `smbclient`. | `smb: \> help` |
| `?` | Alias untuk `help`. | `smb: \> ?` |
| `help <command>` | Menampilkan bantuan untuk perintah tertentu. | `smb: \> help get` |
| `connect <server>` | Menghubungkan ke server/share SMB tertentu. | `smb: \> connect //192.168.1.10/share` |
| `open <share>` | Membuka koneksi ke share tertentu. | `smb: \> open //192.168.1.10/share` |
| `ls` | Menampilkan daftar file dan direktori pada share. | `smb: \> ls` |
| `dir` | Alias untuk `ls`. | `smb: \> dir` |
| `cd <directory>` | Berpindah ke direktori remote. | `smb: \> cd documents` |
| `lcd <directory>` | Berpindah ke direktori lokal. | `smb: \> lcd /tmp` |
| `pwd` | Menampilkan direktori kerja remote saat ini. | `smb: \> pwd` |
| `lpwd` | Menampilkan direktori kerja lokal saat ini. | `smb: \> lpwd` |
| `get <remote>` | Mengunduh satu file dari server SMB. | `smb: \> get report.pdf` |
| `mget <files>` | Mengunduh beberapa file sekaligus. | `smb: \> mget *.pdf` |
| `put <local>` | Mengunggah satu file lokal ke share SMB. | `smb: \> put report.pdf` |
| `mput <files>` | Mengunggah beberapa file sekaligus. | `smb: \> mput *.txt` |
| `reget <remote>` | Melanjutkan download file yang terputus. | `smb: \> reget large.iso` |
| `reput <local>` | Melanjutkan upload file yang terputus. | `smb: \> reput large.iso` |
| `mkdir <directory>` | Membuat direktori baru pada share SMB. | `smb: \> mkdir backup` |
| `md <directory>` | Alias untuk `mkdir`. | `smb: \> md backup` |
| `rmdir <directory>` | Menghapus direktori remote. | `smb: \> rmdir olddata` |
| `rd <directory>` | Alias untuk `rmdir`. | `smb: \> rd olddata` |
| `rm <file>` | Menghapus file pada share SMB. | `smb: \> rm old.txt` |
| `del <file>` | Alias untuk `rm`. | `smb: \> del old.txt` |
| `rename <old> <new>` | Mengubah nama file atau direktori remote. | `smb: \> rename old.txt new.txt` |
| `mv <old> <new>` | Alias/varian untuk operasi rename. | `smb: \> mv old.txt new.txt` |
| `chmod <mode> <file>` | Mengubah mode/permission file jika server mendukungnya. | `smb: \> chmod 644 file.txt` |
| `chown <uid> <file>` | Mengubah owner file jika didukung. | `smb: \> chown 1000 file.txt` |
| `more <file>` | Menampilkan isi file remote secara interaktif. | `smb: \> more readme.txt` |
| `print <file>` | Mencetak file menggunakan layanan printer SMB. | `smb: \> print document.txt` |
| `printmode` | Melihat atau mengubah mode pencetakan. | `smb: \> printmode` |
| `queue` | Menampilkan antrean pekerjaan printer SMB. | `smb: \> queue` |
| `cancel <job>` | Membatalkan pekerjaan print tertentu. | `smb: \> cancel 5` |
| `tarmode` | Mengatur mode transfer berbasis `tar`. | `smb: \> tarmode full` |
| `tar <mode> <file>` | Melakukan operasi backup/restore berbasis tar. | `smb: \> tar c backup.tar` |
| `blocksize <size>` | Mengatur ukuran blok untuk operasi transfer tertentu. | `smb: \> blocksize 4096` |
| `iosize <size>` | Mengatur ukuran I/O untuk transfer. | `smb: \> iosize 65536` |
| `mask <pattern>` | Mengatur pola file untuk operasi `mget`/`mput`. | `smb: \> mask *.txt` |
| `recurse` | Mengaktifkan/menonaktifkan operasi rekursif. | `smb: \> recurse ON` |
| `prompt` | Mengaktifkan/menonaktifkan konfirmasi interaktif. | `smb: \> prompt OFF` |
| `translate` | Mengaktifkan/menonaktifkan translasi karakter. | `smb: \> translate OFF` |
| `lowercase` | Mengaktifkan/menonaktifkan konversi nama file menjadi lowercase. | `smb: \> lowercase ON` |
| `setmode <file> <mode>` | Mengubah atribut/mode file. | `smb: \> setmode file.txt +r` |
| `symlink <target> <link>` | Membuat symbolic link jika didukung server. | `smb: \> symlink target link` |
| `readlink <link>` | Membaca target symbolic link. | `smb: \> readlink link` |
| `hardlink <target> <link>` | Membuat hard link jika didukung server. | `smb: \> hardlink file.txt link.txt` |
| `stat <file>` | Menampilkan informasi/status file remote. | `smb: \> stat file.txt` |
| `allinfo <file>` | Menampilkan informasi metadata file secara lebih lengkap. | `smb: \> allinfo file.txt` |
| `getfacl <file>` | Menampilkan ACL file jika didukung server. | `smb: \> getfacl file.txt` |
| `setfacl <file>` | Mengatur ACL file jika didukung. | `smb: \> setfacl file.txt` |
| `setea <file> <name> <value>` | Mengatur extended attribute file. | `smb: \> setea file.txt user.comment hello` |
| `getea <file> <name>` | Membaca extended attribute file. | `smb: \> getea file.txt user.comment` |
| `showconnect` | Menampilkan informasi koneksi SMB saat ini. | `smb: \> showconnect` |
| `server <name>` | Menentukan server yang digunakan dalam sesi. | `smb: \> server SERVER01` |
| `volume` | Menampilkan informasi volume/share remote. | `smb: \> volume` |
| `logon <username>` | Melakukan autentikasi/logon menggunakan username tertentu. | `smb: \> logon user` |
| `session` | Menampilkan atau mengelola informasi session SMB jika didukung. | `smb: \> session` |
| `dfs` | Menampilkan/menangani informasi DFS jika didukung. | `smb: \> dfs` |
| `posix_encrypt` | Mengatur atau melihat informasi enkripsi POSIX/SMB jika tersedia. | `smb: \> posix_encrypt` |
| `posix_open` | Membuka file menggunakan operasi POSIX SMB. | `smb: \> posix_open file.txt` |
| `posix_mkdir` | Membuat direktori menggunakan operasi POSIX SMB. | `smb: \> posix_mkdir data` |
| `posix_unlink` | Menghapus file menggunakan operasi POSIX SMB. | `smb: \> posix_unlink data.txt` |
| `posix_rmdir` | Menghapus direktori menggunakan operasi POSIX SMB. | `smb: \> posix_rmdir data` |
| `posix_rename` | Mengubah nama file menggunakan operasi POSIX SMB. | `smb: \> posix_rename old new` |
| `posix_whoami` | Menampilkan identitas pengguna POSIX pada server. | `smb: \> posix_whoami` |
| `posix_stat` | Menampilkan informasi POSIX/stat file. | `smb: \> posix_stat file.txt` |
| `posix_chmod` | Mengubah permission POSIX file. | `smb: \> posix_chmod file.txt 0644` |
| `posix_getfacl` | Membaca ACL POSIX. | `smb: \> posix_getfacl file.txt` |
| `posix_setfacl` | Mengatur ACL POSIX. | `smb: \> posix_setfacl file.txt` |
| `echo <text>` | Mengirim request echo melalui koneksi SMB untuk pengujian. | `smb: \> echo hello` |
| `log <file>` | Mengaktifkan atau mengatur logging sesi. | `smb: \> log smb.log` |
| `debug <level>` | Mengatur tingkat debugging `smbclient`. | `smb: \> debug 3` |
| `history` | Menampilkan riwayat perintah jika tersedia. | `smb: \> history` |
| `! <command>` | Menjalankan perintah shell lokal dari dalam `smbclient`. | `smb: \> ! ls -la` |
| `!` | Membuka shell lokal dari dalam sesi `smbclient`. | `smb: \> !` |
| `exit` | Keluar dari `smbclient` dan menutup sesi. | `smb: \> exit` |
| `quit` | Alias untuk `exit`. | `smb: \> quit` |
