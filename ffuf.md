# ffuf

| Command | Deskripsi | Contoh |
|---|---|---|
| `ffuf -h` | Menampilkan bantuan dan daftar opsi ffuf. | `ffuf -h` |
| `-u <URL>` | Menentukan URL target yang mengandung keyword `FUZZ`. | `ffuf -u http://127.0.0.1/FUZZ` |
| `-w <wordlist>` | Menentukan wordlist yang digunakan untuk fuzzing. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt` |
| `-w <file>:<keyword>` | Memuat wordlist dan menghubungkannya dengan keyword tertentu. | `ffuf -w words.txt:FUZZ` |
| `-mc <codes>` | Match berdasarkan HTTP status code. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mc 200,204` |
| `-ms <size>` | Match berdasarkan ukuran response dalam byte. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ms 1234` |
| `-ml <lines>` | Match berdasarkan jumlah baris response. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ml 10` |
| `-mw <words>` | Match berdasarkan jumlah kata dalam response. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mw 20` |
| `-mr <regex>` | Match response berdasarkan regular expression. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mr "Welcome"` |
| `-mt <time>` | Match berdasarkan waktu response dalam milidetik. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mt 100` |
| `-fc <codes>` | Filter response berdasarkan HTTP status code. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fc 404` |
| `-fs <size>` | Filter response berdasarkan ukuran response dalam byte. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fs 1234` |
| `-fl <lines>` | Filter response berdasarkan jumlah baris. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fl 10` |
| `-fw <words>` | Filter response berdasarkan jumlah kata. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fw 20` |
| `-fr <regex>` | Filter response berdasarkan regular expression. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fr "Not Found"` |
| `-ft <time>` | Filter response berdasarkan waktu response dalam milidetik. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ft 100` |
| `-t <threads>` | Menentukan jumlah thread/concurrent requests. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -t 20` |
| `-rate <requests>` | Membatasi jumlah request per detik. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -rate 50` |
| `-p <delay>` | Memberikan delay antar-request; dapat menggunakan rentang delay. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -p 0.1` |
| `-timeout <seconds>` | Menentukan timeout setiap request. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -timeout 10` |
| `-maxtime <seconds>` | Membatasi waktu maksimum keseluruhan proses fuzzing. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -maxtime 300` |
| `-maxtime-job <seconds>` | Membatasi waktu maksimum untuk satu job fuzzing. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -maxtime-job 60` |
| `-s` | Menjalankan ffuf dalam mode silent tanpa progress output. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -s` |
| `-v` | Menampilkan hasil secara verbose. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -v` |
| `-c` | Mengaktifkan output berwarna. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -c` |
| `-ac` | Mengaktifkan auto-calibration untuk membantu menentukan baseline response. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ac` |
| `-acc <string>` | Menentukan keyword/string untuk auto-calibration. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -acc random` |
| `-ach` | Mengaktifkan auto-calibration per host. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ach` |
| `-ack <keyword>` | Menentukan keyword yang digunakan sebagai marker pada auto-calibration. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ack FUZZ` |
| `-acs <size>` | Menentukan ukuran response untuk calibration tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -acs 100` |
| `-accs <codes>` | Menentukan status code untuk calibration tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -accs 200` |
| `-acse <regex>` | Menentukan regex untuk calibration tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -acse "error"` |
| `-acsf <filter>` | Menentukan filter calibration tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -acsf 404` |
| `-ac` | Menentukan baseline response secara otomatis sebelum fuzzing. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ac` |
| `-H <header>` | Menambahkan HTTP header ke request. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -H "X-Test: 1"` |
| `-X <method>` | Menentukan HTTP method yang digunakan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -X POST` |
| `-b <cookies>` | Menentukan cookie HTTP. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -b "session=test"` |
| `-d <data>` | Menentukan HTTP POST data/body. | `ffuf -u http://127.0.0.1/ -w words.txt -X POST -d "name=FUZZ"` |
| `-http2` | Menggunakan HTTP/2 jika didukung oleh target. | `ffuf -u https://127.0.0.1/FUZZ -w words.txt -http2` |
| `-raw` | Tidak melakukan URL encoding terhadap keyword fuzzing. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -raw` |
| `-ignore-body` | Tidak mengambil body response sehingga dapat mengurangi penggunaan bandwidth. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ignore-body` |
| `-r` | Mengikuti HTTP redirect. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -r` |
| `-recursion` | Mengaktifkan recursive fuzzing pada hasil direktori tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -recursion` |
| `-recursion-depth <depth>` | Menentukan kedalaman maksimum recursive fuzzing. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -recursion -recursion-depth 2` |
| `-recursion-strategy <strategy>` | Menentukan strategi recursive scanning yang digunakan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -recursion-strategy greedy` |
| `-e <extensions>` | Menambahkan ekstensi file untuk setiap wordlist entry. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -e .php,.txt` |
| `-enc <encoder>` | Menentukan encoder keyword untuk transformasi payload. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -enc "FUZZ:urlencode"` |
| `-mode <mode>` | Menentukan mode operasi multi-wordlist. | `ffuf -w users.txt:USER -w ids.txt:ID -u http://127.0.0.1/?u=USER&id=ID -mode clusterbomb` |
| `-input-cmd <command>` | Menggunakan output command sebagai input fuzzing. | `ffuf -input-cmd "cat words.txt" -u http://127.0.0.1/FUZZ` |
| `-input-num <number>` | Menentukan jumlah input yang dihasilkan oleh `-input-cmd`. | `ffuf -input-cmd "seq 1 100" -input-num 100 -u http://127.0.0.1/id/FUZZ` |
| `-input-shell <shell>` | Menentukan shell yang digunakan untuk menjalankan input command. | `ffuf -input-shell /bin/bash -input-cmd "cat words.txt" ...` |
| `-request <file>` | Membaca request HTTP mentah dari file. | `ffuf -request request.txt -request-proto http -w words.txt` |
| `-request-proto <protocol>` | Menentukan protocol untuk request yang dibaca dari file. | `ffuf -request request.txt -request-proto https -w words.txt` |
| `-replay-proxy <URL>` | Mengirim ulang request yang menghasilkan match ke proxy yang ditentukan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -replay-proxy http://127.0.0.1:8080` |
| `-x <proxy>` | Menggunakan HTTP atau SOCKS proxy untuk request. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -x http://127.0.0.1:8080` |
| `-proxy <URL>` | Menentukan proxy yang digunakan untuk request pada versi yang mendukung opsi ini. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -proxy http://127.0.0.1:8080` |
| `-sni <hostname>` | Menentukan Server Name Indication untuk koneksi TLS. | `ffuf -u https://127.0.0.1/FUZZ -w words.txt -sni example.test` |
| `-http2` | Memaksa penggunaan HTTP/2. | `ffuf -u https://127.0.0.1/FUZZ -w words.txt -http2` |
| `-unsafe` | Mengizinkan request yang dianggap tidak aman oleh HTTP client. | `ffuf -u https://127.0.0.1/FUZZ -w words.txt -unsafe` |
| `-recursion` | Melakukan fuzzing secara rekursif pada direktori yang ditemukan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -recursion` |
| `-recursion-depth <n>` | Membatasi kedalaman recursive fuzzing. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -recursion -recursion-depth 3` |
| `-e <ext>` | Menguji setiap kata dengan ekstensi tambahan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -e .php` |
| `-D` | Mengaktifkan opsi tertentu terkait path/directory handling pada versi yang mendukungnya. | `ffuf -D ...` |
| `-ic` | Mengabaikan komentar dalam wordlist. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ic` |
| `-input-mode <mode>` | Menentukan mode pembacaan input pada versi yang mendukungnya. | `ffuf -input-mode clusterbomb ...` |
| `-json` | Menghasilkan output dalam format JSON. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -json` |
| `-o <file>` | Menyimpan hasil fuzzing ke file. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -o result.json` |
| `-of <format>` | Menentukan format file output. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of json` |
| `-od <directory>` | Menentukan direktori untuk menyimpan hasil response. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -od output` |
| `-debug-log <file>` | Menyimpan informasi debugging ke file. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -debug-log debug.log` |
| `-noninteractive` | Menonaktifkan kontrol interaktif selama proses berjalan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -noninteractive` |
| `-s` | Menonaktifkan output progress dan banner agar cocok untuk scripting. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -s` |
| `-v` | Menampilkan URL lengkap dan informasi tambahan pada hasil. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -v` |
| `-c` | Menggunakan warna pada output terminal. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -c` |
| `-json` | Mengeluarkan setiap hasil dalam format JSON. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -json` |
| `-of json` | Menyimpan hasil dalam format JSON. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of json -o result.json` |
| `-of ejson` | Menggunakan extended JSON output jika didukung versi ffuf. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of ejson -o result.json` |
| `-of html` | Menyimpan hasil dalam format HTML. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of html -o result.html` |
| `-of md` | Menyimpan hasil dalam format Markdown. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of md -o result.md` |
| `-of csv` | Menyimpan hasil dalam format CSV pada versi yang mendukungnya. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of csv -o result.csv` |
| `-of ecsv` | Menggunakan extended CSV output jika didukung versi ffuf. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of ecsv -o result.csv` |
| `-of all` | Menghasilkan beberapa format output sekaligus pada versi yang mendukungnya. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of all -o results` |
| `-H "Name: Value"` | Menambahkan header HTTP custom. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -H "Authorization: Bearer TOKEN"` |
| `-H "Host: example.test"` | Mengubah Host header untuk virtual host testing pada lingkungan yang diizinkan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -H "Host: example.test"` |
| `-X GET` | Menggunakan HTTP GET. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -X GET` |
| `-X POST` | Menggunakan HTTP POST. | `ffuf -u http://127.0.0.1/ -w words.txt -X POST -d "q=FUZZ"` |
| `-X PUT` | Menggunakan HTTP PUT. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -X PUT` |
| `-X DELETE` | Menggunakan HTTP DELETE. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -X DELETE` |
| `-b "name=value"` | Menambahkan cookie ke HTTP request. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -b "session=test"` |
| `-d "key=FUZZ"` | Mengirim data HTTP body yang mengandung keyword fuzzing. | `ffuf -u http://127.0.0.1/ -w words.txt -X POST -d "id=FUZZ"` |
| `-mode sniper` | Menggunakan satu wordlist dan satu posisi fuzzing secara berurutan. | `ffuf -mode sniper -w words.txt:FUZZ -u http://127.0.0.1/?id=FUZZ` |
| `-mode clusterbomb` | Menguji kombinasi setiap entry dari beberapa wordlist. | `ffuf -mode clusterbomb -w users.txt:USER -w ids.txt:ID -u http://127.0.0.1/?u=USER&id=ID` |
| `-mode pitchfork` | Menggunakan entry dengan posisi yang sama dari beberapa wordlist secara bersamaan. | `ffuf -mode pitchfork -w users.txt:USER -w ids.txt:ID -u http://127.0.0.1/?u=USER&id=ID` |
| `FUZZ` | Keyword default yang digantikan oleh setiap entry wordlist. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt` |
| `FUZZ` pada path | Melakukan fuzzing bagian path/URL. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt` |
| `FUZZ` pada query | Melakukan fuzzing parameter query. | `ffuf -u http://127.0.0.1/?id=FUZZ -w words.txt` |
| `FUZZ` pada header | Melakukan fuzzing nilai header. | `ffuf -u http://127.0.0.1/ -w words.txt -H "X-Test: FUZZ"` |
| `FUZZ` pada body | Melakukan fuzzing data request body. | `ffuf -u http://127.0.0.1/ -w words.txt -X POST -d "name=FUZZ"` |
| `FUZZ` pada Host header | Melakukan virtual-host fuzzing pada environment yang diizinkan. | `ffuf -u http://127.0.0.1/ -w hosts.txt -H "Host: FUZZ"` |
| `-w <file>:<keyword>` | Memberikan nama keyword khusus untuk wordlist sehingga beberapa wordlist dapat digunakan dalam satu request. | `ffuf -w users.txt:USER -w paths.txt:PATH -u http://127.0.0.1/PATH?user=USER` |
| `-request <file>` | Menggunakan request mentah yang diekspor dari proxy/tool HTTP sebagai template fuzzing. | `ffuf -request request.txt -request-proto http -w words.txt` |
| `-request-proto http` | Menentukan HTTP sebagai protokol request template. | `ffuf -request request.txt -request-proto http -w words.txt` |
| `-request-proto https` | Menentukan HTTPS sebagai protokol request template. | `ffuf -request request.txt -request-proto https -w words.txt` |
| `-x http://proxy:port` | Mengirim request melalui HTTP proxy. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -x http://127.0.0.1:8080` |
| `-x socks5://proxy:port` | Mengirim request melalui SOCKS5 proxy. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -x socks5://127.0.0.1:1080` |
| `-replay-proxy <proxy>` | Mengirim ulang request yang menghasilkan match ke proxy untuk inspeksi. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -replay-proxy http://127.0.0.1:8080` |
| `-ignore-body` | Hanya memproses metadata response tanpa mengambil body. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ignore-body` |
| `-r` | Mengikuti redirect HTTP. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -r` |
| `-raw` | Mengirim keyword tanpa URL encoding otomatis. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -raw` |
| `-sni <host>` | Menentukan hostname SNI pada koneksi TLS. | `ffuf -u https://127.0.0.1/FUZZ -w words.txt -sni example.test` |
| `-http2` | Mengaktifkan HTTP/2. | `ffuf -u https://127.0.0.1/FUZZ -w words.txt -http2` |
| `-follow-redirects` | Mengikuti redirect pada versi/configuration yang menyediakan alias ini. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -follow-redirects` |
| `-t 10` | Menjalankan maksimal 10 task secara paralel. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -t 10` |
| `-rate 25` | Membatasi traffic menjadi sekitar 25 request per detik. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -rate 25` |
| `-timeout 5` | Memberikan timeout 5 detik untuk request. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -timeout 5` |
| `-p 0.5` | Memberikan delay sekitar 0,5 detik antar-request. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -p 0.5` |
| `-p 0.1-0.5` | Menggunakan rentang delay acak antar-request jika didukung versi ffuf. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -p 0.1-0.5` |
| `-maxtime 60` | Menghentikan seluruh proses setelah sekitar 60 detik. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -maxtime 60` |
| `-maxtime-job 30` | Menghentikan job tertentu setelah sekitar 30 detik. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -maxtime-job 30` |
| `-fc 404` | Menghilangkan hasil dengan status HTTP 404. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fc 404` |
| `-fc 404,403` | Menghilangkan hasil dengan status HTTP 404 dan 403. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fc 404,403` |
| `-fs 0` | Menghilangkan response dengan ukuran body 0 byte. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fs 0` |
| `-fw 1` | Menghilangkan response yang memiliki satu kata. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fw 1` |
| `-fl 5` | Menghilangkan response yang memiliki lima baris. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fl 5` |
| `-fr "Not Found"` | Menghilangkan response yang cocok dengan regex tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -fr "Not Found"` |
| `-mc all` | Mencocokkan semua status HTTP sebelum filter lain diterapkan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mc all` |
| `-mc 200-299` | Hanya mencocokkan status HTTP dalam rentang 200–299. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mc 200-299` |
| `-mr "admin"` | Hanya mencocokkan response yang memenuhi regex tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mr "admin"` |
| `-ms 1234` | Hanya mencocokkan response dengan ukuran tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ms 1234` |
| `-mw 20` | Hanya mencocokkan response dengan jumlah kata tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mw 20` |
| `-ml 10` | Hanya mencocokkan response dengan jumlah baris tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ml 10` |
| `-mt 100` | Hanya mencocokkan response berdasarkan waktu response tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -mt 100` |
| `-ft 100` | Memfilter response berdasarkan waktu response tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ft 100` |
| `-ac` | Mengaktifkan auto-calibration untuk membantu menentukan filter baseline secara otomatis. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ac` |
| `-acc <value>` | Menambahkan nilai khusus untuk proses auto-calibration. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -acc test` |
| `-ach` | Mengaktifkan auto-calibration secara terpisah untuk host yang berbeda. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ach` |
| `-ack <keyword>` | Mengatur keyword yang digunakan untuk auto-calibration. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ack FUZZ` |
| `-acs <size>` | Menentukan ukuran response calibration tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -acs 1234` |
| `-accs <codes>` | Menentukan status code yang digunakan untuk calibration. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -accs 200` |
| `-acse <regex>` | Menentukan regex yang digunakan untuk calibration. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -acse "error"` |
| `-acsf <filter>` | Menentukan filter calibration tambahan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -acsf 404` |
| `-ic` | Mengabaikan baris komentar dari wordlist. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -ic` |
| `-e .php,.html,.txt` | Menguji wordlist entry dengan beberapa ekstensi file. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -e .php,.html,.txt` |
| `-enc "FUZZ:urlencode"` | Melakukan URL encoding terhadap nilai FUZZ menggunakan encoder yang tersedia. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -enc "FUZZ:urlencode"` |
| `-enc "FUZZ:base64"` | Melakukan encoding Base64 terhadap nilai FUZZ jika encoder tersedia. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -enc "FUZZ:base64"` |
| `-input-cmd "command"` | Menggunakan output command sebagai sumber nilai fuzzing. | `ffuf -input-cmd "cat words.txt" -u http://127.0.0.1/FUZZ` |
| `-input-num <n>` | Menentukan jumlah nilai input yang dihasilkan oleh `-input-cmd`. | `ffuf -input-cmd "seq 1 100" -input-num 100 -u http://127.0.0.1/id/FUZZ` |
| `-input-shell <shell>` | Menentukan shell untuk menjalankan input command. | `ffuf -input-shell /bin/bash -input-cmd "cat words.txt" ...` |
| `-od <directory>` | Menyimpan response body hasil match ke direktori tertentu. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -od responses` |
| `-o <file>` | Menentukan file output hasil fuzzing. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -o result.json` |
| `-of json` | Menentukan output format JSON. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of json -o result.json` |
| `-of html` | Menentukan output format HTML. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of html -o result.html` |
| `-of md` | Menentukan output format Markdown. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of md -o result.md` |
| `-of csv` | Menentukan output format CSV jika didukung versi yang digunakan. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of csv -o result.csv` |
| `-of ejson` | Menentukan extended JSON output. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of ejson -o result.json` |
| `-of ecsv` | Menentukan extended CSV output. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of ecsv -o result.csv` |
| `-of all` | Meminta seluruh format output yang tersedia pada versi ffuf. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -of all -o results` |
| `-debug-log <file>` | Menulis informasi debug ke file. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -debug-log debug.log` |
| `-noninteractive` | Menjalankan ffuf tanpa antarmuka kontrol interaktif. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -noninteractive` |
| `-v` | Menampilkan informasi hasil secara verbose. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -v` |
| `-s` | Menyembunyikan banner dan progress output. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -s` |
| `-c` | Mengaktifkan warna output terminal. | `ffuf -u http://127.0.0.1/FUZZ -w words.txt -c` |
| `-version` | Menampilkan versi ffuf pada versi yang mendukung flag tersebut. | `ffuf -version` |
| `-V` | Menampilkan versi ffuf pada build yang menggunakan opsi ini. | `ffuf -V` |
