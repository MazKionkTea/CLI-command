# nikto

| Command | Deskripsi | Contoh |
|---|---|---|
| `-h <host>` | Menentukan target host atau URL yang akan dipindai. | `nikto -h https://example.com` |
| `-host <host>` | Alias untuk `-h`, menentukan target host. | `nikto -host example.com` |
| `-p <port>` | Menentukan port target secara manual. | `nikto -h example.com -p 8080` |
| `-port <port>` | Alias untuk `-p`. | `nikto -h example.com -port 443` |
| `-ssl` | Memaksa penggunaan SSL/TLS. | `nikto -h example.com -ssl` |
| `-nossl` | Menonaktifkan penggunaan SSL/TLS. | `nikto -h example.com -nossl` |
| `-vhost <host>` | Menentukan virtual host yang digunakan saat melakukan request. | `nikto -h 192.168.1.10 -vhost example.com` |
| `-id <user:pass>` | Menentukan kredensial HTTP Basic Authentication. | `nikto -h example.com -id admin:password` |
| `-root <directory>` | Menentukan direktori root/path dasar untuk target. | `nikto -h example.com -root /app` |
| `-Tuning <options>` | Membatasi jenis pengujian yang dilakukan Nikto berdasarkan kategori tuning. | `nikto -h example.com -Tuning 123` |
| `-Cgidirs <directories>` | Menentukan direktori CGI yang akan diperiksa. | `nikto -h example.com -Cgidirs all` |
| `-Plugins <plugins>` | Menentukan plugin Nikto yang akan digunakan. | `nikto -h example.com -Plugins apache_expect_xss` |
| `-list-plugins` | Menampilkan daftar plugin yang tersedia. | `nikto -list-plugins` |
| `-Display <options>` | Mengatur jenis informasi yang ditampilkan selama proses scanning. | `nikto -h example.com -Display V` |
| `-evasion <techniques>` | Menggunakan teknik HTTP IDS evasion tertentu. | `nikto -h example.com -evasion 1` |
| `-mutate <options>` | Mengaktifkan teknik mutation untuk mencoba variasi nama file/direktori. | `nikto -h example.com -mutate 1` |
| `-mutate-options <options>` | Menentukan opsi tambahan untuk mutation yang digunakan. | `nikto -h example.com -mutate 1 -mutate-options 1` |
| `-timeout <seconds>` | Menentukan batas waktu koneksi/request. | `nikto -h example.com -timeout 10` |
| `-Pause <seconds>` | Memberikan jeda antar-request untuk memperlambat scanning. | `nikto -h example.com -Pause 2` |
| `-maxtime <seconds>` | Membatasi waktu maksimum keseluruhan scanning. | `nikto -h example.com -maxtime 300` |
| `-until <time>` | Menjalankan scanning sampai waktu tertentu. | `nikto -h example.com -until 23:00` |
| `-no404` | Menonaktifkan pemeriksaan halaman 404 tertentu. | `nikto -h example.com -no404` |
| `-nointeractive` | Menjalankan Nikto tanpa prompt interaktif. | `nikto -h example.com -nointeractive` |
| `-useragent <string>` | Menentukan User-Agent HTTP yang digunakan saat request. | `nikto -h example.com -useragent "Mozilla/5.0"` |
| `-useproxy <proxy>` | Menggunakan proxy yang ditentukan untuk koneksi. | `nikto -h example.com -useproxy http://127.0.0.1:8080` |
| `-config <file>` | Menggunakan file konfigurasi Nikto tertentu. | `nikto -config nikto.conf` |
| `-dbcheck` | Memeriksa database Nikto untuk menemukan masalah atau inkonsistensi. | `nikto -dbcheck` |
| `-update` | Memperbarui database/plugin Nikto dari sumber yang tersedia. | `nikto -update` |
| `-Version` | Menampilkan versi Nikto. | `nikto -Version` |
| `-Help` | Menampilkan bantuan penggunaan Nikto. | `nikto -Help` |
| `-Format <format>` | Menentukan format output hasil scan. | `nikto -h example.com -Format txt` |
| `-output <file>` | Menyimpan hasil scanning ke file. | `nikto -h example.com -output report.txt` |
| `-o <file>` | Alias untuk `-output`. | `nikto -h example.com -o report.txt` |
| `-Format htm` | Menghasilkan laporan dalam format HTML. | `nikto -h example.com -Format htm -o report.htm` |
| `-Format csv` | Menghasilkan laporan dalam format CSV. | `nikto -h example.com -Format csv -o report.csv` |
| `-Format txt` | Menghasilkan laporan dalam format teks biasa. | `nikto -h example.com -Format txt -o report.txt` |
| `-Format xml` | Menghasilkan laporan dalam format XML. | `nikto -h example.com -Format xml -o report.xml` |
| `-Format nbe` | Menghasilkan output dalam format NBE yang dapat digunakan oleh tool tertentu. | `nikto -h example.com -Format nbe -o report.nbe` |
| `-Format json` | Menghasilkan output dalam format JSON pada versi yang mendukungnya. | `nikto -h example.com -Format json -o report.json` |
| `-Save <file>` | Menyimpan informasi sesi/hasil tertentu untuk digunakan kembali. | `nikto -h example.com -Save scan.session` |
| `-resume <file>` | Melanjutkan scanning dari sesi yang sebelumnya disimpan. | `nikto -resume scan.session` |
| `-host <file>` | Menggunakan daftar host dari file untuk scanning. | `nikto -host hosts.txt` |
| `-h <file>` | Menggunakan file yang berisi daftar target jika format input didukung versi Nikto. | `nikto -h hosts.txt` |
| `-ipv4` | Memaksa penggunaan IPv4. | `nikto -h example.com -ipv4` |
| `-ipv6` | Memaksa penggunaan IPv6. | `nikto -h example.com -ipv6` |
| `-v` | Mengaktifkan output verbose. | `nikto -h example.com -v` |
| `-V` | Menampilkan informasi versi/versi program sesuai implementasi Nikto. | `nikto -V` |
| `-D <level>` | Mengatur level debug/output debugging. | `nikto -h example.com -D 2` |
| `-ask <options>` | Mengatur perilaku Nikto terhadap prompt atau pertanyaan interaktif. | `nikto -h example.com -ask no` |
| `-nointeractive` | Menjalankan scan tanpa interaksi pengguna. | `nikto -h example.com -nointeractive` |
| `-Plugins ALL` | Meminta Nikto menggunakan seluruh plugin yang tersedia sesuai konfigurasi. | `nikto -h example.com -Plugins ALL` |
| `-Tuning 1` | Memfokuskan scan pada kategori file menarik. | `nikto -h example.com -Tuning 1` |
| `-Tuning 2` | Memfokuskan scan pada konfigurasi atau informasi yang berpotensi menarik. | `nikto -h example.com -Tuning 2` |
| `-Tuning 3` | Memfokuskan scan pada disclosure informasi. | `nikto -h example.com -Tuning 3` |
| `-Tuning 4` | Memfokuskan scan pada injection/XSS tertentu sesuai database Nikto. | `nikto -h example.com -Tuning 4` |
| `-Tuning 5` | Memfokuskan scan pada remote file retrieval/source disclosure tertentu. | `nikto -h example.com -Tuning 5` |
| `-Tuning 6` | Memfokuskan scan pada denial-of-service checks tertentu. | `nikto -h example.com -Tuning 6` |
| `-Tuning 7` | Memfokuskan scan pada file upload checks tertentu. | `nikto -h example.com -Tuning 7` |
| `-Tuning 8` | Memfokuskan scan pada command execution checks tertentu. | `nikto -h example.com -Tuning 8` |
| `-Tuning 9` | Memfokuskan scan pada SQL injection checks tertentu. | `nikto -h example.com -Tuning 9` |
| `-Tuning 0` | Memfokuskan scan pada file upload atau konfigurasi tertentu sesuai kategori tuning versi Nikto. | `nikto -h example.com -Tuning 0` |
| `-Tuning a` | Mengaktifkan kategori pemeriksaan tertentu berdasarkan authentication-related checks. | `nikto -h example.com -Tuning a` |
| `-Tuning b` | Mengaktifkan kategori pemeriksaan software identification/version. | `nikto -h example.com -Tuning b` |
| `-Tuning c` | Mengaktifkan kategori pemeriksaan miscellaneous/information disclosure tertentu. | `nikto -h example.com -Tuning c` |
| `-Tuning x` | Mengecualikan kategori tuning tertentu sesuai sintaks versi Nikto. | `nikto -h example.com -Tuning x6` |
| `-evasion 1` | Menggunakan URL encoding tertentu untuk mencoba melewati filter IDS/IPS. | `nikto -h example.com -evasion 1` |
| `-evasion 2` | Menggunakan variasi path separator tertentu untuk request. | `nikto -h example.com -evasion 2` |
| `-evasion 3` | Menggunakan variasi path traversal/encoding tertentu. | `nikto -h example.com -evasion 3` |
| `-evasion 4` | Menggunakan variasi URL encoding tertentu. | `nikto -h example.com -evasion 4` |
| `-evasion 5` | Menggunakan variasi path/URL tertentu untuk IDS evasion. | `nikto -h example.com -evasion 5` |
| `-evasion 6` | Menggunakan variasi HTTP request tertentu untuk IDS evasion. | `nikto -h example.com -evasion 6` |
| `-evasion 7` | Menggunakan variasi request tertentu untuk menguji respons filter. | `nikto -h example.com -evasion 7` |
| `-evasion 8` | Menggunakan variasi URL/request tertentu untuk IDS evasion. | `nikto -h example.com -evasion 8` |
| `-evasion 9` | Menggunakan teknik HTTP request tertentu untuk IDS evasion. | `nikto -h example.com -evasion 9` |
| `-evasion A` | Menggunakan variasi URL encoding tertentu. | `nikto -h example.com -evasion A` |
| `-evasion B` | Menggunakan variasi path separator tertentu. | `nikto -h example.com -evasion B` |
| `-evasion C` | Menggunakan variasi URL encoding/request tertentu. | `nikto -h example.com -evasion C` |
| `-evasion D` | Menggunakan variasi HTTP request tertentu. | `nikto -h example.com -evasion D` |
| `-evasion E` | Menggunakan variasi request tertentu untuk menguji filtering. | `nikto -h example.com -evasion E` |
| `-evasion F` | Menggunakan variasi HTTP request tertentu. | `nikto -h example.com -evasion F` |
| `-mutate 1` | Mencoba nama file berdasarkan kombinasi nama yang ditemukan. | `nikto -h example.com -mutate 1` |
| `-mutate 2` | Mencoba nama direktori berdasarkan variasi tertentu. | `nikto -h example.com -mutate 2` |
| `-mutate 3` | Mencoba variasi username tertentu jika relevan. | `nikto -h example.com -mutate 3` |
| `-mutate 4` | Mencoba variasi nama file/direktori tambahan. | `nikto -h example.com -mutate 4` |
| `-Cgidirs all` | Memeriksa seluruh lokasi CGI yang dikenali oleh Nikto. | `nikto -h example.com -Cgidirs all` |
| `-Cgidirs none` | Tidak melakukan pemeriksaan CGI directory tertentu. | `nikto -h example.com -Cgidirs none` |
| `-Display 1` | Mengatur jenis output yang ditampilkan selama scan. | `nikto -h example.com -Display 1` |
| `-Display 2` | Mengatur jenis output tambahan selama scan. | `nikto -h example.com -Display 2` |
| `-Display 3` | Mengaktifkan tampilan tertentu terkait redirect. | `nikto -h example.com -Display 3` |
| `-Display 4` | Mengaktifkan tampilan tertentu terkait cookies. | `nikto -h example.com -Display 4` |
| `-Display V` | Menampilkan output verbose. | `nikto -h example.com -Display V` |
| `-Display D` | Menampilkan informasi debugging. | `nikto -h example.com -Display D` |
| `-Display E` | Menampilkan error selama proses scan. | `nikto -h example.com -Display E` |
| `-Display P` | Menampilkan progress scanning. | `nikto -h example.com -Display P` |
| `-Display S` | Menampilkan status scanning. | `nikto -h example.com -Display S` |
| `-Format csv` | Format laporan CSV untuk diproses oleh aplikasi lain. | `nikto -h example.com -Format csv -o result.csv` |
| `-Format htm` | Format laporan HTML yang mudah dibuka di browser. | `nikto -h example.com -Format htm -o result.htm` |
| `-Format txt` | Format laporan teks biasa. | `nikto -h example.com -Format txt -o result.txt` |
| `-Format xml` | Format laporan XML. | `nikto -h example.com -Format xml -o result.xml` |
| `-Format nbe` | Format output NBE. | `nikto -h example.com -Format nbe -o result.nbe` |
| `-Format json` | Format laporan JSON pada versi yang mendukungnya. | `nikto -h example.com -Format json -o result.json` |
| `-Plugins <list>` | Menjalankan plugin tertentu secara eksplisit. | `nikto -h example.com -Plugins plugin1,plugin2` |
| `-Plugins @@NONE` | Menonaktifkan plugin tertentu sesuai sintaks versi Nikto. | `nikto -h example.com -Plugins @@NONE` |
| `-useproxy <proxy>` | Mengarahkan koneksi Nikto melalui HTTP proxy. | `nikto -h example.com -useproxy http://127.0.0.1:8080` |
| `-useragent <agent>` | Mengganti HTTP User-Agent bawaan Nikto. | `nikto -h example.com -useragent "Mozilla/5.0"` |
| `-id <id>` | Memberikan username dan password untuk autentikasi HTTP. | `nikto -h example.com -id admin:password` |
| `-vhost <host>` | Menentukan hostname pada HTTP Host header untuk virtual hosting. | `nikto -h 10.0.0.10 -vhost example.com` |
| `-root <path>` | Menentukan path root aplikasi web. | `nikto -h example.com -root /webapp` |
| `-timeout <seconds>` | Menentukan timeout koneksi/request. | `nikto -h example.com -timeout 15` |
| `-Pause <seconds>` | Memberikan jeda antar-request. | `nikto -h example.com -Pause 1` |
| `-maxtime <seconds>` | Membatasi durasi maksimum scanning. | `nikto -h example.com -maxtime 600` |
| `-until <time>` | Menjalankan scan hingga waktu yang ditentukan. | `nikto -h example.com -until 22:00` |
| `-no404` | Menghindari pemeriksaan khusus terhadap respons 404. | `nikto -h example.com -no404` |
| `-nointeractive` | Menonaktifkan mode interaktif. | `nikto -h example.com -nointeractive` |
| `-ipv4` | Memaksa koneksi menggunakan IPv4. | `nikto -h example.com -ipv4` |
| `-ipv6` | Memaksa koneksi menggunakan IPv6. | `nikto -h example.com -ipv6` |
| `-dbcheck` | Memeriksa integritas database Nikto. | `nikto -dbcheck` |
| `-update` | Memperbarui database dan plugin Nikto. | `nikto -update` |
| `-list-plugins` | Menampilkan seluruh plugin yang tersedia. | `nikto -list-plugins` |
| `-config <file>` | Memuat file konfigurasi tertentu. | `nikto -config /etc/nikto.conf` |
| `-Version` | Menampilkan versi Nikto yang terinstal. | `nikto -Version` |
| `-Help` | Menampilkan bantuan dan opsi command-line. | `nikto -Help` |
