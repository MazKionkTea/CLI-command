# grep

| command | deskripsi | contoh |
|----|----|----|
| `grep PATTERN FILE` | Mencari pola teks di dalam file | `grep "error" log.txt` |
| `grep -i PATTERN FILE` | Pencarian tanpa membedakan huruf besar/kecil | `grep -i "error" log.txt` |
| `grep -v PATTERN FILE` | Menampilkan baris yang tidak cocok dengan pola | `grep -v "debug" log.txt` |
| `grep -n PATTERN FILE` | Menampilkan nomor baris yang cocok | `grep -n "error" log.txt` |
| `grep -c PATTERN FILE` | Menghitung jumlah baris yang cocok | `grep -c "error" log.txt` |
| `grep -l PATTERN FILE...` | Menampilkan nama file yang memiliki kecocokan | `grep -l "error" *.log` |
| `grep -L PATTERN FILE...` | Menampilkan file yang tidak memiliki kecocokan | `grep -L "error" *.log` |
| `grep -H PATTERN FILE...` | Selalu menampilkan nama file pada hasil | `grep -H "error" *.log` |
| `grep -h PATTERN FILE...` | Menyembunyikan nama file pada hasil | `grep -h "error" *.log` |
| `grep -o PATTERN FILE` | Hanya menampilkan bagian yang cocok | `grep -o "[0-9]+" file.txt` |
| `grep -w WORD FILE` | Mencari kata secara utuh | `grep -w "root" /etc/passwd` |
| `grep -x PATTERN FILE` | Mencocokkan seluruh isi baris | `grep -x "hello" file.txt` |
| `grep -q PATTERN FILE` | Mode diam, tidak menampilkan output | `grep -q "error" log.txt` |
| `grep -s PATTERN FILE` | Menyembunyikan pesan error | `grep -s "error" file.txt` |
| `grep -r PATTERN DIR` | Mencari secara rekursif di direktori | `grep -r "TODO" ./src` |
| `grep -R PATTERN DIR` | Mencari rekursif dan mengikuti symbolic link | `grep -R "TODO" ./src` |
| `grep -ri PATTERN DIR` | Recursive search tanpa membedakan case | `grep -ri "error" ./logs` |
| `grep -rn PATTERN DIR` | Recursive search dengan nomor baris | `grep -rn "TODO" ./src` |
| `grep -rl PATTERN DIR` | Recursive search dan hanya nama file | `grep -rl "password" .` |
| `grep -e PATTERN FILE` | Menentukan pola pencarian secara eksplisit | `grep -e "error" log.txt` |
| `grep -e PAT1 -e PAT2 FILE` | Mencari beberapa pola sekaligus | `grep -e "error" -e "warning" log.txt` |
| `grep -f PATTERN_FILE FILE` | Mengambil pola dari file | `grep -f patterns.txt data.txt` |
| `grep -E PATTERN FILE` | Menggunakan Extended Regular Expression | `grep -E "error|warning" log.txt` |
| `grep -F STRING FILE` | Mencari string literal tanpa regex | `grep -F "a.b" file.txt` |
| `grep -G PATTERN FILE` | Menggunakan Basic Regular Expression | `grep -G "error" log.txt` |
| `grep -P PATTERN FILE` | Menggunakan Perl Compatible Regular Expression jika didukung | `grep -P "\d{3}" file.txt` |
| `grep --color=auto PATTERN FILE` | Memberi warna pada bagian yang cocok | `grep --color=auto "error" log.txt` |
| `grep --color=always PATTERN FILE` | Selalu menggunakan warna pada hasil | `grep --color=always "error" log.txt` |
| `grep -A N PATTERN FILE` | Menampilkan N baris setelah baris yang cocok | `grep -A 3 "error" log.txt` |
| `grep -B N PATTERN FILE` | Menampilkan N baris sebelum baris yang cocok | `grep -B 3 "error" log.txt` |
| `grep -C N PATTERN FILE` | Menampilkan N baris sebelum dan sesudah | `grep -C 3 "error" log.txt` |
| `grep --include=GLOB PATTERN DIR` | Membatasi pencarian pada file tertentu | `grep -r --include="*.php" "error" .` |
| `grep --exclude=GLOB PATTERN DIR` | Mengecualikan file tertentu | `grep -r --exclude="*.log" "error" .` |
| `grep --exclude-dir=GLOB PATTERN DIR` | Mengecualikan direktori tertentu | `grep -r --exclude-dir=node_modules "TODO" .` |
| `grep -m N PATTERN FILE` | Berhenti setelah menemukan N kecocokan | `grep -m 1 "error" log.txt` |
| `grep -Z PATTERN FILE` | Mengakhiri nama file dengan karakter NUL | `grep -Z -l "error" *.log` |
| `grep -z PATTERN FILE` | Menganggap NUL sebagai pemisah baris | `grep -z "foo" data.txt` |
| `grep -a PATTERN FILE` | Memperlakukan file binary sebagai teks | `grep -a "text" binary.dat` |
| `grep -I PATTERN FILE` | Mengabaikan file binary | `grep -I "error" *` |
| `grep -b PATTERN FILE` | Menampilkan byte offset dari kecocokan | `grep -b "error" log.txt` |
| `grep -T PATTERN FILE` | Menambahkan tab setelah nama file | `grep -T "error" log.txt` |
| `grep -d ACTION PATTERN DIR` | Menentukan perlakuan terhadap direktori | `grep -d recurse "error" .` |
| `grep -D ACTION PATTERN FILE` | Menentukan perlakuan terhadap device/FIFO | `grep -D skip "data" /dev/*` |
| `grep --binary-files=text PATTERN FILE` | Memperlakukan file binary sebagai teks | `grep --binary-files=text "abc" file.bin` |
| `grep --binary-files=without-match PATTERN FILE` | Menganggap file binary tidak memiliki kecocokan | `grep --binary-files=without-match "abc" *` |
| `grep --label=LABEL PATTERN` | Memberikan label pada input dari stdin | `cat log.txt \| grep --label=LOG "error"` |
| `grep --line-buffered PATTERN FILE` | Menggunakan line buffering untuk output | `tail -f app.log \| grep --line-buffered "ERROR"` |
| `grep --null PATTERN FILE` | Menggunakan NUL sebagai pemisah nama file | `grep -lZ "error" *.log` |
| `grep --null-data PATTERN FILE` | Memperlakukan NUL sebagai pemisah baris | `grep -z "foo" data` |
| `grep --only-matching PATTERN FILE` | Hanya menampilkan bagian yang cocok | `grep --only-matching "[0-9]+" file.txt` |
| `grep --quiet PATTERN FILE` | Mode quiet tanpa output | `grep --quiet "error" log.txt` |
| `grep --silent PATTERN FILE` | Alias untuk mode quiet | `grep --silent "error" log.txt` |
| `grep --text PATTERN FILE` | Memperlakukan binary sebagai teks | `grep --text "hello" file.bin` |
| `grep --word-regexp PATTERN FILE` | Mencocokkan kata secara utuh | `grep --word-regexp "root" file.txt` |
| `grep --line-regexp PATTERN FILE` | Mencocokkan seluruh baris | `grep --line-regexp "hello" file.txt` |
| `grep --fixed-strings STRING FILE` | Pencarian string literal | `grep --fixed-strings "a.b" file.txt` |
| `grep --extended-regexp PATTERN FILE` | Mengaktifkan Extended Regex | `grep --extended-regexp "foo|bar" file.txt` |
| `grep --basic-regexp PATTERN FILE` | Menggunakan Basic Regex | `grep --basic-regexp "foo" file.txt` |
| `grep --perl-regexp PATTERN FILE` | Menggunakan Perl Regex jika tersedia | `grep --perl-regexp "\d+" file.txt` |
| `grep --recursive PATTERN DIR` | Bentuk panjang dari `-r` | `grep --recursive "TODO" ./src` |
| `grep --dereference-recursive PATTERN DIR` | Bentuk panjang dari `-R` | `grep --dereference-recursive "TODO" ./src` |
| `grep --ignore-case PATTERN FILE` | Bentuk panjang dari `-i` | `grep --ignore-case "ERROR" log.txt` |
| `grep --invert-match PATTERN FILE` | Bentuk panjang dari `-v` | `grep --invert-match "DEBUG" log.txt` |
| `grep --line-number PATTERN FILE` | Bentuk panjang dari `-n` | `grep --line-number "error" log.txt` |
| `grep --count PATTERN FILE` | Bentuk panjang dari `-c` | `grep --count "error" log.txt` |
| `grep --files-with-matches PATTERN FILE...` | Hanya menampilkan file yang cocok | `grep --files-with-matches "TODO" *.c` |
| `grep --files-without-match PATTERN FILE...` | Hanya menampilkan file yang tidak cocok | `grep --files-without-match "TODO" *.c` |
| `grep --with-filename PATTERN FILE...` | Menampilkan nama file | `grep --with-filename "error" *.log` |
| `grep --no-filename PATTERN FILE...` | Tidak menampilkan nama file | `grep --no-filename "error" *.log` |
| `grep --max-count=N PATTERN FILE` | Membatasi jumlah hasil | `grep --max-count=5 "error" log.txt` |
| `grep --after-context=N PATTERN FILE` | Menampilkan N baris setelah hasil | `grep --after-context=2 "error" log.txt` |
| `grep --before-context=N PATTERN FILE` | Menampilkan N baris sebelum hasil | `grep --before-context=2 "error" log.txt` |
| `grep --context=N PATTERN FILE` | Menampilkan N baris konteks di sekitar hasil | `grep --context=2 "error" log.txt` |
| `grep '^PATTERN' FILE` | Mencari pola di awal baris | `grep '^root' /etc/passwd` |
| `grep 'PATTERN$' FILE` | Mencari pola di akhir baris | `grep 'bash$' /etc/passwd` |
| `grep '^$' FILE` | Mencari baris kosong | `grep '^$' file.txt` |
| `grep '.' FILE` | Mencari baris yang memiliki minimal satu karakter | `grep '.' file.txt` |
| `grep '[0-9]' FILE` | Mencari baris yang mengandung angka | `grep '[0-9]' file.txt` |
| `grep '[a-z]' FILE` | Mencari huruf kecil | `grep '[a-z]' file.txt` |
| `grep '[A-Z]' FILE` | Mencari huruf kapital | `grep '[A-Z]' file.txt` |
| `grep '[[:digit:]]' FILE` | Mencari karakter angka menggunakan POSIX class | `grep '[[:digit:]]' file.txt` |
| `grep '[[:alpha:]]' FILE` | Mencari karakter alfabet | `grep '[[:alpha:]]' file.txt` |
| `grep '[[:alnum:]]' FILE` | Mencari karakter alfanumerik | `grep '[[:alnum:]]' file.txt` |
| `grep '[[:space:]]' FILE` | Mencari whitespace | `grep '[[:space:]]' file.txt` |
| `grep '[[:blank:]]' FILE` | Mencari spasi atau tab | `grep '[[:blank:]]' file.txt` |
| `grep '[[:lower:]]' FILE` | Mencari huruf kecil | `grep '[[:lower:]]' file.txt` |
| `grep '[[:upper:]]' FILE` | Mencari huruf kapital | `grep '[[:upper:]]' file.txt` |
| `grep '[[:punct:]]' FILE` | Mencari tanda baca | `grep '[[:punct:]]' file.txt` |
| `grep 'PAT1\|PAT2' FILE` | OR pada Basic Regex GNU grep | `grep 'error\|warning' log.txt` |
| `grep -E 'PAT1|PAT2' FILE` | OR pada Extended Regex | `grep -E 'error|warning' log.txt` |
| `grep -E 'PAT{N}' FILE` | Mencocokkan pola tepat N kali | `grep -E '[0-9]{4}' file.txt` |
| `grep -E 'PAT{N,M}' FILE` | Mencocokkan pola N sampai M kali | `grep -E '[0-9]{2,4}' file.txt` |
| `grep -E 'PAT+' FILE` | Satu atau lebih kemunculan pola | `grep -E 'go+' file.txt` |
| `grep -E 'PAT?' FILE` | Nol atau satu kemunculan pola | `grep -E 'colou?r' file.txt` |
| `grep -E 'PAT*' FILE` | Nol atau lebih kemunculan pola | `grep -E 'ab*' file.txt` |
| `grep -E '(PAT)' FILE` | Mengelompokkan pola | `grep -E '(error|warning)' log.txt` |
| `grep -E '[^abc]' FILE` | Mencocokkan karakter selain a, b, atau c | `grep -E '[^0-9]' file.txt` |
| `grep -E '\bWORD\b' FILE` | Mencari batas kata | `grep -E '\berror\b' log.txt` |
| `grep PATTERN` | Membaca input dari stdin | `cat log.txt \| grep "error"` |
| `command \| grep PATTERN` | Menyaring output command | `ps aux \| grep nginx` |
| `grep PATTERN file1 file2` | Mencari pada beberapa file | `grep "error" app.log system.log` |
| `grep PATTERN *.txt` | Mencari pada file berdasarkan wildcard | `grep "hello" *.txt` |
| `grep -n PATTERN FILE \| head` | Membatasi hasil menggunakan `head` | `grep -n "error" log.txt \| head` |
| `grep PATTERN FILE \| wc -l` | Menghitung jumlah hasil | `grep "error" log.txt \| wc -l` |
| `grep -v '^#' FILE` | Mengabaikan baris komentar | `grep -v '^#' config.conf` |
| `grep -v '^$' FILE` | Mengabaikan baris kosong | `grep -v '^$' file.txt` |
| `grep -vE '^#\|^$' FILE` | Mengabaikan komentar dan baris kosong | `grep -vE '^#\|^$' config.conf` |
| `grep -iE 'error|fail|warning' FILE` | Mencari beberapa kata tanpa case sensitivity | `grep -iE 'error|fail|warning' app.log` |
| `grep -rn --include='*.py' PATTERN DIR` | Recursive search hanya pada file Python | `grep -rn --include='*.py' 'TODO' .` |
| `grep -rni --exclude-dir=.git PATTERN DIR` | Recursive, case-insensitive, mengecualikan `.git` | `grep -rni --exclude-dir=.git 'password' .` |
| `grep -rnC 2 PATTERN DIR` | Recursive dengan nomor baris dan konteks | `grep -rnC 2 'exception' ./src` |
