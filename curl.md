# curl

| Command | Deskripsi | Contoh |
|---|---|---|
| `curl URL` | Mengambil resource dari URL menggunakan HTTP/HTTPS | `curl https://example.com` |
| `curl -o FILE URL` | Menyimpan output ke file dengan nama tertentu | `curl -o page.html https://example.com` |
| `curl -O URL` | Mengunduh file menggunakan nama file dari URL | `curl -O https://example.com/file.zip` |
| `curl -L URL` | Mengikuti redirect HTTP | `curl -L https://example.com` |
| `curl -I URL` | Mengambil HTTP header saja | `curl -I https://example.com` |
| `curl -i URL` | Menampilkan HTTP header dan response body | `curl -i https://example.com` |
| `curl -v URL` | Menampilkan detail proses koneksi dan request | `curl -v https://example.com` |
| `curl -s URL` | Menjalankan curl tanpa progress meter | `curl -s https://example.com` |
| `curl -S URL` | Menampilkan error meskipun menggunakan silent mode | `curl -sS https://example.com` |
| `curl -f URL` | Menganggap HTTP 4xx/5xx sebagai error | `curl -f https://example.com` |
| `curl -w FORMAT URL` | Menampilkan informasi tambahan setelah request | `curl -w "%{http_code}\n" https://example.com` |
| `curl -X METHOD URL` | Menentukan HTTP method secara manual | `curl -X DELETE https://example.com/users/1` |
| `curl -G URL` | Mengirim data sebagai query parameter GET | `curl -G -d "q=curl" https://example.com/search` |
| `curl -d DATA URL` | Mengirim data menggunakan POST | `curl -d "name=John" https://example.com/users` |
| `curl --data-raw DATA URL` | Mengirim data POST tanpa interpretasi khusus | `curl --data-raw '{"name":"John"}' https://example.com` |
| `curl --data-binary DATA URL` | Mengirim data secara binary/raw | `curl --data-binary @data.json https://example.com` |
| `curl -d @FILE URL` | Mengirim isi file sebagai data POST | `curl -d @data.json https://example.com` |
| `curl --json DATA URL` | Mengirim data JSON dengan header JSON yang sesuai | `curl --json '{"name":"John"}' https://api.example.com/users` |
| `curl -H "Header: Value" URL` | Menambahkan HTTP header | `curl -H "Accept: application/json" https://api.example.com` |
| `curl -A "User-Agent" URL` | Mengubah User-Agent | `curl -A "Mozilla/5.0" https://example.com` |
| `curl -e URL URL` | Menentukan HTTP Referer | `curl -e "https://google.com" https://example.com` |
| `curl -b "name=value" URL` | Mengirim cookie | `curl -b "session=abc123" https://example.com` |
| `curl -c FILE URL` | Menyimpan cookie ke file | `curl -c cookies.txt https://example.com` |
| `curl -b FILE URL` | Membaca cookie dari file | `curl -b cookies.txt https://example.com` |
| `curl -u USER:PASS URL` | Menggunakan HTTP Basic Authentication | `curl -u admin:secret https://example.com` |
| `curl --digest -u USER:PASS URL` | Menggunakan HTTP Digest Authentication | `curl --digest -u admin:secret https://example.com` |
| `curl -F "field=value" URL` | Mengirim form multipart | `curl -F "name=John" https://example.com/upload` |
| `curl -F "file=@FILE" URL` | Mengunggah file melalui multipart form | `curl -F "file=@photo.jpg" https://example.com/upload` |
| `curl -T FILE URL` | Mengunggah file ke URL | `curl -T file.txt https://example.com/file.txt` |
| `curl -X POST URL` | Mengirim HTTP POST | `curl -X POST https://api.example.com/users` |
| `curl -X PUT URL` | Mengirim HTTP PUT | `curl -X PUT https://api.example.com/users/1` |
| `curl -X PATCH URL` | Mengirim HTTP PATCH | `curl -X PATCH https://api.example.com/users/1` |
| `curl -X DELETE URL` | Mengirim HTTP DELETE | `curl -X DELETE https://api.example.com/users/1` |
| `curl -X OPTIONS URL` | Mengirim HTTP OPTIONS | `curl -X OPTIONS https://example.com` |
| `curl -X HEAD URL` | Mengirim HTTP HEAD | `curl -X HEAD https://example.com` |
| `curl -x PROXY URL` | Menggunakan proxy | `curl -x http://proxy:8080 https://example.com` |
| `curl --proxy-user USER:PASS URL` | Autentikasi ke proxy | `curl -x http://proxy:8080 --proxy-user user:pass https://example.com` |
| `curl --noproxy HOST URL` | Melewati proxy untuk host tertentu | `curl --noproxy localhost http://localhost:8080` |
| `curl -k URL` | Melewati verifikasi sertifikat TLS | `curl -k https://internal.example.com` |
| `curl --cacert FILE URL` | Menggunakan CA certificate tertentu | `curl --cacert ca.pem https://example.com` |
| `curl --cert FILE URL` | Menggunakan client certificate | `curl --cert client.pem https://example.com` |
| `curl --key FILE URL` | Menentukan private key client certificate | `curl --cert client.pem --key client.key https://example.com` |
| `curl --tlsv1.2 URL` | Menggunakan TLS 1.2 atau lebih baru | `curl --tlsv1.2 https://example.com` |
| `curl --tls-max VERSION URL` | Membatasi versi TLS maksimum | `curl --tls-max 1.2 https://example.com` |
| `curl --http1.1 URL` | Memaksa penggunaan HTTP/1.1 | `curl --http1.1 https://example.com` |
| `curl --http2 URL` | Menggunakan HTTP/2 | `curl --http2 https://example.com` |
| `curl --http3 URL` | Menggunakan HTTP/3 jika tersedia | `curl --http3 https://example.com` |
| `curl --compressed URL` | Meminta dan menangani response terkompresi | `curl --compressed https://example.com` |
| `curl --limit-rate RATE URL` | Membatasi kecepatan transfer | `curl --limit-rate 1M https://example.com/file.zip` |
| `curl --max-time SECONDS URL` | Membatasi total waktu request | `curl --max-time 10 https://example.com` |
| `curl --connect-timeout SECONDS URL` | Membatasi waktu koneksi | `curl --connect-timeout 5 https://example.com` |
| `curl --retry N URL` | Mengulangi request ketika terjadi kegagalan tertentu | `curl --retry 3 https://example.com` |
| `curl --retry-delay SECONDS URL` | Memberikan jeda antar retry | `curl --retry 3 --retry-delay 2 https://example.com` |
| `curl --retry-all-errors URL` | Mengizinkan retry untuk berbagai error | `curl --retry 3 --retry-all-errors https://example.com` |
| `curl -C - -O URL` | Melanjutkan download yang terputus | `curl -C - -O https://example.com/file.zip` |
| `curl -r RANGE URL` | Mengunduh bagian byte tertentu dari file | `curl -r 0-999 https://example.com/file` |
| `curl --remote-name-all URL` | Mengunduh beberapa URL menggunakan nama file remote | `curl --remote-name-all https://example.com/a.txt https://example.com/b.txt` |
| `curl --parallel URL...` | Menjalankan beberapa transfer secara paralel | `curl --parallel -O https://example.com/a https://example.com/b` |
| `curl --interface IFACE URL` | Menggunakan network interface tertentu | `curl --interface eth0 https://example.com` |
| `curl --ipv4 URL` | Memaksa penggunaan IPv4 | `curl --ipv4 https://example.com` |
| `curl --ipv6 URL` | Memaksa penggunaan IPv6 | `curl --ipv6 https://example.com` |
| `curl --resolve HOST:PORT:IP URL` | Memetakan hostname ke IP tertentu | `curl --resolve example.com:443:192.0.2.10 https://example.com` |
| `curl --connect-to HOST:PORT:HOST:PORT URL` | Mengubah tujuan koneksi tanpa mengubah URL | `curl --connect-to example.com:443:test.example.com:443 https://example.com` |
| `curl --unix-socket SOCKET URL` | Mengakses service melalui Unix socket | `curl --unix-socket /var/run/docker.sock http://localhost/info` |
| `curl --path-as-is URL` | Mempertahankan path URL tanpa normalisasi | `curl --path-as-is https://example.com/a/../b` |
| `curl --get -d PARAM URL` | Menambahkan parameter ke query string | `curl --get -d "page=2" https://example.com/api` |
| `curl --url URL` | Menentukan URL secara eksplisit | `curl --url https://example.com` |
| `curl --proto PROTOCOL URL` | Membatasi protokol yang boleh digunakan | `curl --proto https https://example.com` |
| `curl --proto-redir PROTOCOL URL` | Membatasi protokol ketika redirect | `curl --proto-redir =https -L https://example.com` |
| `curl --max-redirs N URL` | Membatasi jumlah redirect | `curl -L --max-redirs 5 https://example.com` |
| `curl --fail-with-body URL` | Gagal pada HTTP error tetapi tetap mempertahankan response body | `curl --fail-with-body https://example.com/api` |
| `curl --stderr FILE URL` | Mengarahkan pesan error ke file | `curl --stderr error.log https://example.com` |
| `curl --trace FILE URL` | Menyimpan trace komunikasi ke file | `curl --trace trace.log https://example.com` |
| `curl --trace-ascii FILE URL` | Menyimpan trace dalam format ASCII | `curl --trace-ascii trace.log https://example.com` |
| `curl --trace-time URL` | Menambahkan timestamp pada trace | `curl --trace-time --trace-ascii trace.log https://example.com` |
| `curl -D FILE URL` | Menyimpan response header ke file | `curl -D headers.txt https://example.com` |
| `curl -D - URL` | Menampilkan response header di terminal | `curl -D - https://example.com` |
| `curl -o /dev/null URL` | Membuang response body | `curl -o /dev/null https://example.com` |
| `curl --globoff URL` | Menonaktifkan URL globbing | `curl --globoff 'https://example.com/[1-3]'` |
| `curl --config FILE` | Membaca konfigurasi curl dari file | `curl --config curl.conf` |
| `curl -K FILE` | Alias pendek untuk --config | `curl -K curl.conf` |
| `curl --create-dirs -o FILE URL` | Membuat direktori output jika belum ada | `curl --create-dirs -o out/file.txt https://example.com/file.txt` |
| `curl -J -O URL` | Menggunakan nama file dari Content-Disposition | `curl -JO https://example.com/download` |
| `curl -sS -f URL` | Silent, tetapi tetap menampilkan error dan gagal pada HTTP error | `curl -sSf https://example.com` |
| `curl -H "Content-Type: application/json" -d JSON URL` | Mengirim JSON melalui POST | `curl -H "Content-Type: application/json" -d '{"id":1}' https://api.example.com` |
| `curl -H "Accept: application/json" URL` | Meminta response dalam format JSON | `curl -H "Accept: application/json" https://api.example.com/users` |
| `curl -H "Authorization: Bearer TOKEN" URL` | Mengirim Bearer token | `curl -H "Authorization: Bearer TOKEN" https://api.example.com/me` |
| `curl -H "X-API-Key: KEY" URL` | Mengirim API key melalui header | `curl -H "X-API-Key: KEY" https://api.example.com/data` |
| `curl -w "%{http_code}" -o /dev/null URL` | Menampilkan HTTP status code saja | `curl -s -o /dev/null -w "%{http_code}\n" https://example.com` |
| `curl -w "%{time_total}" -o /dev/null URL` | Menampilkan total waktu request | `curl -s -o /dev/null -w "%{time_total}\n" https://example.com` |
| `curl -w "%{url_effective}" URL` | Menampilkan URL akhir setelah redirect | `curl -Ls -o /dev/null -w "%{url_effective}\n" https://example.com` |
| `curl -w "%{size_download}" URL` | Menampilkan jumlah byte yang diunduh | `curl -s -o /dev/null -w "%{size_download}\n" https://example.com` |
| `curl -w "%{content_type}" URL` | Menampilkan Content-Type response | `curl -s -o /dev/null -w "%{content_type}\n" https://example.com` |
| `curl --help` | Menampilkan bantuan penggunaan curl | `curl --help` |
| `curl --help all` | Menampilkan daftar opsi curl yang lebih lengkap | `curl --help all` |
| `curl --version` | Menampilkan versi, protokol, dan fitur curl | `curl --version` |

### API
| Command | Deskripsi | Contoh |
|---|---|---|
| `curl URL` | GET sederhana | `curl https://api.example.com/users` |
| `curl -G -d "q=value" URL` | GET dengan query parameter | `curl -G -d "q=john" https://api.example.com/users` |
| `curl -H "Accept: application/json" URL` | GET dengan header | `curl -H "Accept: application/json" https://api.example.com/users` |
| `curl --json '{}' URL` | POST JSON | `curl --json '{"name":"John"}' https://api.example.com/users` |
| `curl -X PUT --json '{}' URL` | PUT JSON | `curl -X PUT --json '{"name":"Jane"}' https://api.example.com/users/1` |
| `curl -X PATCH --json '{}' URL` | PATCH JSON | `curl -X PATCH --json '{"name":"Jane"}' https://api.example.com/users/1` |
| `curl -X DELETE URL` | DELETE resource | `curl -X DELETE https://api.example.com/users/1` |
| `curl -H "Authorization: Bearer TOKEN" URL` | API dengan Bearer token | `curl -H "Authorization: Bearer eyJ..." https://api.example.com/me` |
| `curl -u USER:PASS URL` | API dengan Basic Auth | `curl -u admin:password https://api.example.com/me` |
| `curl -F "file=@FILE" URL` | Upload file | `curl -F "file=@report.pdf" https://api.example.com/upload` |
| `curl -o FILE URL` | Download response ke file | `curl -o response.json https://api.example.com/data` |
