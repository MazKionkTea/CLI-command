# nmap

| Command | Deskripsi | Contoh |
|---|---|---|
| `nmap TARGET` | Scan dasar terhadap target | `nmap 192.168.1.1` |
| `nmap HOSTNAME` | Scan berdasarkan hostname | `nmap scanme.nmap.org` |
| `nmap IP1 IP2` | Scan beberapa target sekaligus | `nmap 192.168.1.1 192.168.1.2` |
| `nmap 192.168.1.0/24` | Scan seluruh subnet | `nmap 192.168.1.0/24` |
| `nmap 192.168.1.1-254` | Scan rentang alamat IP | `nmap 192.168.1.1-254` |
| `nmap -iL FILE` | Membaca daftar target dari file | `nmap -iL targets.txt` |
| `nmap -iR N` | Memilih target secara acak | `nmap -iR 10` |
| `nmap --exclude HOST` | Mengecualikan host tertentu | `nmap 192.168.1.0/24 --exclude 192.168.1.10` |
| `nmap --excludefile FILE` | Mengecualikan target berdasarkan file | `nmap 192.168.1.0/24 --excludefile exclude.txt` |
| `nmap -sL TARGET` | List Scan tanpa melakukan port scan | `nmap -sL 192.168.1.0/24` |
| `nmap -sn TARGET` | Host discovery tanpa port scan | `nmap -sn 192.168.1.0/24` |
| `nmap -Pn TARGET` | Menganggap semua host aktif dan melewati host discovery | `nmap -Pn 192.168.1.10` |
| `nmap -PS PORT TARGET` | TCP SYN ping ke port tertentu | `nmap -PS80,443 192.168.1.0/24` |
| `nmap -PA PORT TARGET` | TCP ACK ping ke port tertentu | `nmap -PA80,443 192.168.1.0/24` |
| `nmap -PU PORT TARGET` | UDP ping ke port tertentu | `nmap -PU53,161 192.168.1.0/24` |
| `nmap -PE TARGET` | ICMP Echo discovery | `nmap -PE 192.168.1.0/24` |
| `nmap -PP TARGET` | ICMP Timestamp discovery | `nmap -PP 192.168.1.0/24` |
| `nmap -PM TARGET` | ICMP Address Mask discovery | `nmap -PM 192.168.1.0/24` |
| `nmap -PR TARGET` | ARP discovery pada jaringan Ethernet lokal | `nmap -PR 192.168.1.0/24` |
| `nmap -PY PORT TARGET` | SCTP INIT discovery | `nmap -PY5000 192.168.1.0/24` |
| `nmap -PO PROTOCOL TARGET` | IP Protocol Ping | `nmap -PO1,2,6 192.168.1.10` |
| `nmap -n TARGET` | Menonaktifkan reverse DNS resolution | `nmap -n 192.168.1.0/24` |
| `nmap -R TARGET` | Selalu melakukan reverse DNS resolution | `nmap -R 192.168.1.10` |
| `nmap --dns-servers SERVER TARGET` | Menggunakan DNS server tertentu | `nmap --dns-servers 8.8.8.8 example.com` |
| `nmap -sS TARGET` | TCP SYN scan | `nmap -sS 192.168.1.10` |
| `nmap -sT TARGET` | TCP Connect scan | `nmap -sT 192.168.1.10` |
| `nmap -sU TARGET` | UDP scan | `nmap -sU 192.168.1.10` |
| `nmap -sF TARGET` | TCP FIN scan | `nmap -sF 192.168.1.10` |
| `nmap -sN TARGET` | TCP NULL scan | `nmap -sN 192.168.1.10` |
| `nmap -sX TARGET` | TCP Xmas scan | `nmap -sX 192.168.1.10` |
| `nmap -sA TARGET` | TCP ACK scan | `nmap -sA 192.168.1.10` |
| `nmap -sW TARGET` | TCP Window scan | `nmap -sW 192.168.1.10` |
| `nmap -sM TARGET` | TCP Maimon scan | `nmap -sM 192.168.1.10` |
| `nmap -sI ZOMBIE TARGET` | TCP Idle scan menggunakan zombie host | `nmap -sI 192.168.1.20 192.168.1.10` |
| `nmap -sO TARGET` | IP Protocol scan | `nmap -sO 192.168.1.10` |
| `nmap -sY TARGET` | SCTP INIT scan | `nmap -sY 192.168.1.10` |
| `nmap -sZ TARGET` | SCTP COOKIE-ECHO scan | `nmap -sZ 192.168.1.10` |
| `nmap -b FTP_RELAY TARGET` | FTP bounce scan | `nmap -b ftp.example.com 192.168.1.10` |
| `nmap --scanflags FLAGS TARGET` | Menentukan flag TCP secara manual | `nmap --scanflags SYNFIN 192.168.1.10` |
| `nmap -p PORT TARGET` | Scan port tertentu | `nmap -p 80 192.168.1.10` |
| `nmap -p PORT1,PORT2 TARGET` | Scan beberapa port tertentu | `nmap -p 22,80,443 192.168.1.10` |
| `nmap -p 1-1000 TARGET` | Scan rentang port | `nmap -p 1-1000 192.168.1.10` |
| `nmap -p- TARGET` | Scan semua port TCP 1-65535 | `nmap -p- 192.168.1.10` |
| `nmap -p U:PORT TARGET` | Menentukan port UDP | `nmap -p U:53,161 192.168.1.10` |
| `nmap -p T:PORT TARGET` | Menentukan port TCP | `nmap -p T:22,80,443 192.168.1.10` |
| `nmap -p S:PORT TARGET` | Menentukan port SCTP | `nmap -p S:2905 192.168.1.10` |
| `nmap -p T:80,U:53 TARGET` | Scan port TCP dan UDP tertentu | `nmap -p T:80,U:53 192.168.1.10` |
| `nmap --exclude-ports PORTS TARGET` | Mengecualikan port tertentu dari scan | `nmap --exclude-ports 25,110 192.168.1.10` |
| `nmap -F TARGET` | Fast scan terhadap port umum | `nmap -F 192.168.1.10` |
| `nmap --top-ports N TARGET` | Scan N port paling umum | `nmap --top-ports 100 192.168.1.10` |
| `nmap -r TARGET` | Scan port secara berurutan | `nmap -r 192.168.1.10` |
| `nmap --port-ratio RATIO TARGET` | Scan port dengan rasio frekuensi tertentu atau lebih tinggi | `nmap --port-ratio 0.1 192.168.1.10` |
| `nmap -sV TARGET` | Mendeteksi service dan versi | `nmap -sV 192.168.1.10` |
| `nmap --version-intensity LEVEL TARGET` | Mengatur intensitas version detection | `nmap -sV --version-intensity 5 192.168.1.10` |
| `nmap --version-light TARGET` | Menggunakan version detection dengan probe lebih sedikit | `nmap -sV --version-light 192.168.1.10` |
| `nmap --version-all TARGET` | Mencoba seluruh probe version detection | `nmap -sV --version-all 192.168.1.10` |
| `nmap --version-trace TARGET` | Menampilkan detail proses version detection | `nmap -sV --version-trace 192.168.1.10` |
| `nmap -sC TARGET` | Menjalankan default NSE scripts | `nmap -sC 192.168.1.10` |
| `nmap --script SCRIPT TARGET` | Menjalankan NSE script tertentu | `nmap --script http-title 192.168.1.10` |
| `nmap --script SCRIPT1,SCRIPT2 TARGET` | Menjalankan beberapa NSE script | `nmap --script http-title,http-headers 192.168.1.10` |
| `nmap --script CATEGORY TARGET` | Menjalankan kategori NSE tertentu | `nmap --script safe 192.168.1.10` |
| `nmap --script "PATTERN" TARGET` | Menjalankan script berdasarkan pola | `nmap --script "http-*" 192.168.1.10` |
| `nmap --script-args ARG=VALUE TARGET` | Memberikan argumen kepada NSE script | `nmap --script http-title --script-args http.useragent="Mozilla/5.0" 192.168.1.10` |
| `nmap --script-args-file FILE TARGET` | Membaca argumen NSE dari file | `nmap --script http-title --script-args-file args.txt 192.168.1.10` |
| `nmap --script-help SCRIPT` | Menampilkan bantuan NSE script | `nmap --script-help http-title` |
| `nmap --script-trace TARGET` | Menampilkan seluruh komunikasi NSE | `nmap --script http-title --script-trace 192.168.1.10` |
| `nmap --script-updatedb` | Memperbarui database indeks NSE script | `nmap --script-updatedb` |
| `nmap -O TARGET` | Mendeteksi sistem operasi | `nmap -O 192.168.1.10` |
| `nmap --osscan-limit TARGET` | Membatasi OS detection hanya pada target yang cocok | `nmap -O --osscan-limit 192.168.1.0/24` |
| `nmap --osscan-guess TARGET` | Mencoba menebak OS secara lebih agresif | `nmap -O --osscan-guess 192.168.1.10` |
| `nmap --fuzzy TARGET` | Alias untuk OS detection guessing | `nmap -O --fuzzy 192.168.1.10` |
| `nmap --max-os-tries N TARGET` | Mengatur jumlah percobaan OS detection | `nmap -O --max-os-tries 2 192.168.1.10` |
| `nmap -A TARGET` | Mengaktifkan OS detection, version detection, default scripts, dan traceroute | `nmap -A 192.168.1.10` |
| `nmap --traceroute TARGET` | Melakukan traceroute menuju target | `nmap --traceroute 192.168.1.10` |
| `nmap -T0 TARGET` | Timing paranoid, sangat lambat | `nmap -T0 192.168.1.10` |
| `nmap -T1 TARGET` | Timing sneaky, lambat | `nmap -T1 192.168.1.10` |
| `nmap -T2 TARGET` | Timing polite | `nmap -T2 192.168.1.10` |
| `nmap -T3 TARGET` | Timing normal | `nmap -T3 192.168.1.10` |
| `nmap -T4 TARGET` | Timing aggressive | `nmap -T4 192.168.1.10` |
| `nmap -T5 TARGET` | Timing insane, sangat cepat | `nmap -T5 192.168.1.10` |
| `nmap --min-hostgroup SIZE TARGET` | Menentukan ukuran minimum host group | `nmap --min-hostgroup 32 192.168.1.0/24` |
| `nmap --max-hostgroup SIZE TARGET` | Menentukan ukuran maksimum host group | `nmap --max-hostgroup 64 192.168.1.0/24` |
| `nmap --min-parallelism NUM TARGET` | Menentukan minimum probe paralel | `nmap --min-parallelism 10 192.168.1.10` |
| `nmap --max-parallelism NUM TARGET` | Membatasi probe paralel | `nmap --max-parallelism 20 192.168.1.10` |
| `nmap --min-rtt-timeout TIME TARGET` | Menentukan minimum RTT timeout | `nmap --min-rtt-timeout 100ms 192.168.1.10` |
| `nmap --max-rtt-timeout TIME TARGET` | Menentukan maksimum RTT timeout | `nmap --max-rtt-timeout 1s 192.168.1.10` |
| `nmap --initial-rtt-timeout TIME TARGET` | Menentukan initial RTT timeout | `nmap --initial-rtt-timeout 500ms 192.168.1.10` |
| `nmap --max-retries N TARGET` | Membatasi jumlah retransmission probe | `nmap --max-retries 2 192.168.1.10` |
| `nmap --host-timeout TIME TARGET` | Membatasi waktu maksimum per host | `nmap --host-timeout 30s 192.168.1.10` |
| `nmap --scan-delay TIME TARGET` | Memberikan jeda antar probe | `nmap --scan-delay 1s 192.168.1.10` |
| `nmap --max-scan-delay TIME TARGET` | Membatasi maksimum jeda antar probe | `nmap --max-scan-delay 5s 192.168.1.10` |
| `nmap --defeat-rst-ratelimit TARGET` | Mengabaikan pembatasan RST pada kondisi tertentu untuk mempercepat scan | `nmap --defeat-rst-ratelimit 192.168.1.10` |
| `nmap --defeat-icmp-ratelimit TARGET` | Mengurangi dampak ICMP rate limiting pada scan UDP | `nmap -sU --defeat-icmp-ratelimit 192.168.1.10` |
| `nmap -f TARGET` | Memecah paket IP menjadi fragment | `nmap -f 192.168.1.10` |
| `nmap -ff TARGET` | Menggunakan fragmentasi IP yang lebih kecil | `nmap -ff 192.168.1.10` |
| `nmap --mtu SIZE TARGET` | Menentukan ukuran MTU fragmentasi | `nmap --mtu 24 192.168.1.10` |
| `nmap -D DECOY1,DECOY2,ME TARGET` | Menggunakan decoy addresses pada scan | `nmap -D 192.168.1.20,192.168.1.30,ME 192.168.1.10` |
| `nmap -S IP TARGET` | Memalsukan source IP address | `nmap -S 192.168.1.20 192.168.1.10` |
| `nmap -e INTERFACE TARGET` | Menggunakan network interface tertentu | `nmap -e eth0 192.168.1.10` |
| `nmap -g PORT TARGET` | Menggunakan source port tertentu | `nmap -g 53 192.168.1.10` |
| `nmap --source-port PORT TARGET` | Menentukan source port | `nmap --source-port 53 192.168.1.10` |
| `nmap --proxies URL TARGET` | Menggunakan proxy untuk koneksi tertentu | `nmap --proxies http://127.0.0.1:8080 192.168.1.10` |
| `nmap --data-length LENGTH TARGET` | Menambahkan data acak dengan panjang tertentu ke paket | `nmap --data-length 20 192.168.1.10` |
| `nmap --ip-options OPTIONS TARGET` | Menentukan opsi IP header | `nmap --ip-options R 192.168.1.10` |
| `nmap --ttl VALUE TARGET` | Menentukan IP TTL | `nmap --ttl 64 192.168.1.10` |
| `nmap --spoof-mac MAC TARGET` | Menggunakan MAC address tertentu atau vendor tertentu | `nmap --spoof-mac 00:11:22:33:44:55 192.168.1.10` |
| `nmap --badsum TARGET` | Menggunakan checksum IP/TCP/UDP yang salah untuk probe | `nmap --badsum 192.168.1.10` |
| `nmap --send-eth TARGET` | Mengirim paket melalui raw Ethernet | `nmap --send-eth 192.168.1.10` |
| `nmap --send-ip TARGET` | Mengirim paket melalui raw IP | `nmap --send-ip 192.168.1.10` |
| `nmap -6 TARGET` | Mengaktifkan scanning IPv6 | `nmap -6 2001:db8::1` |
| `nmap -4 TARGET` | Memaksa penggunaan IPv4 | `nmap -4 example.com` |
| `nmap --reason TARGET` | Menampilkan alasan port/host mendapatkan status tertentu | `nmap --reason 192.168.1.10` |
| `nmap --open TARGET` | Hanya menampilkan port yang open atau mungkin open | `nmap --open 192.168.1.10` |
| `nmap -v TARGET` | Meningkatkan verbosity output | `nmap -v 192.168.1.10` |
| `nmap -vv TARGET` | Verbosity lebih tinggi | `nmap -vv 192.168.1.10` |
| `nmap -d TARGET` | Mengaktifkan debugging | `nmap -d 192.168.1.10` |
| `nmap -dd TARGET` | Debugging dengan tingkat lebih tinggi | `nmap -dd 192.168.1.10` |
| `nmap --packet-trace TARGET` | Menampilkan paket yang dikirim dan diterima | `nmap --packet-trace 192.168.1.10` |
| `nmap --iflist` | Menampilkan interface dan route jaringan | `nmap --iflist` |
| `nmap -oN FILE TARGET` | Menyimpan output dalam format normal | `nmap -oN scan.txt 192.168.1.10` |
| `nmap -oX FILE TARGET` | Menyimpan output dalam format XML | `nmap -oX scan.xml 192.168.1.10` |
| `nmap -oS FILE TARGET` | Menyimpan output dalam format s|<r>I|p|t | `nmap -oS scan.txt 192.168.1.10` |
| `nmap -oG FILE TARGET` | Menyimpan output dalam format grepable | `nmap -oG scan.gnmap 192.168.1.10` |
| `nmap -oA BASENAME TARGET` | Menyimpan output dalam format normal, XML, dan grepable | `nmap -oA scan 192.168.1.10` |
| `nmap --append-output TARGET` | Menambahkan hasil ke file output yang sudah ada | `nmap -oN scan.txt --append-output 192.168.1.10` |
| `nmap --resume FILE` | Melanjutkan scan dari file output normal | `nmap --resume scan.txt` |
| `nmap --stylesheet PATH FILE.xml` | Menggunakan stylesheet XSL untuk output XML | `nmap -oX scan.xml --stylesheet style.xsl 192.168.1.10` |
| `nmap --webxml TARGET` | Menghasilkan XML yang cocok untuk stylesheet web resmi Nmap | `nmap -oX scan.xml --webxml 192.168.1.10` |
| `nmap --no-stylesheet TARGET` | Menghilangkan referensi stylesheet dari output XML | `nmap -oX scan.xml --no-stylesheet 192.168.1.10` |
| `nmap -oN - TARGET` | Mengirim normal output ke stdout | `nmap -oN - 192.168.1.10` |
| `nmap -oX - TARGET` | Mengirim XML output ke stdout | `nmap -oX - 192.168.1.10` |
| `nmap -oG - TARGET` | Mengirim grepable output ke stdout | `nmap -oG - 192.168.1.10` |
| `nmap --stats-every TIME TARGET` | Menampilkan statistik progres secara berkala | `nmap --stats-every 10s 192.168.1.0/24` |
| `nmap --noninteractive TARGET` | Menonaktifkan interaksi runtime tertentu | `nmap --noninteractive 192.168.1.10` |
| `nmap -d9 TARGET` | Mengaktifkan debugging level tinggi | `nmap -d9 192.168.1.10` |
| `nmap --log-errors TARGET` | Mencatat error ke output | `nmap --log-errors 192.168.1.10` |
| `nmap --append-output TARGET` | Menambahkan hasil ke file output, bukan menimpanya | `nmap -oN scan.txt --append-output 192.168.1.10` |
| `nmap --resume FILENAME` | Melanjutkan scan yang terhenti dari file output | `nmap --resume scan.txt` |
| `nmap -6 -sV TARGET` | Version detection pada IPv6 | `nmap -6 -sV 2001:db8::1` |
| `nmap -sV -p PORT TARGET` | Mendeteksi service/version pada port tertentu | `nmap -sV -p 80,443 192.168.1.10` |
| `nmap -sC -sV TARGET` | Menjalankan default scripts dan version detection | `nmap -sC -sV 192.168.1.10` |
| `nmap -A -T4 TARGET` | Scan agresif dengan timing T4 | `nmap -A -T4 192.168.1.10` |
| `nmap -Pn -p- TARGET` | Scan semua port tanpa host discovery | `nmap -Pn -p- 192.168.1.10` |
| `nmap -sn -PE TARGET` | Host discovery menggunakan ICMP Echo | `nmap -sn -PE 192.168.1.0/24` |
| `nmap -sn -PS80,443 TARGET` | Host discovery menggunakan TCP SYN | `nmap -sn -PS80,443 192.168.1.0/24` |
| `nmap -sn -PR TARGET` | Host discovery menggunakan ARP pada LAN | `nmap -sn -PR 192.168.1.0/24` |
| `nmap -p 22,80,443 --open TARGET` | Hanya menampilkan port tertentu yang terbuka | `nmap -p 22,80,443 --open 192.168.1.10` |
| `nmap -sU -p 53,161 TARGET` | Scan UDP pada port tertentu | `nmap -sU -p 53,161 192.168.1.10` |
| `nmap -sS -sV -O TARGET` | SYN scan dengan service/version dan OS detection | `nmap -sS -sV -O 192.168.1.10` |
| `nmap -A -p- TARGET` | Scan agresif seluruh port TCP | `nmap -A -p- 192.168.1.10` |
| `nmap --top-ports 100 -sV TARGET` | Scan 100 port umum sekaligus version detection | `nmap --top-ports 100 -sV 192.168.1.10` |
| `nmap -iL targets.txt -oA results` | Scan target dari file dan menyimpan tiga format output | `nmap -iL targets.txt -oA results` |
| `nmap -sV --version-light TARGET` | Version detection ringan | `nmap -sV --version-light 192.168.1.10` |
| `nmap -sC TARGET` | Menjalankan kumpulan default NSE scripts | `nmap -sC 192.168.1.10` |
| `nmap --script vuln TARGET` | Menjalankan kategori NSE terkait pemeriksaan vulnerability | `nmap --script vuln 192.168.1.10` |
| `nmap --script safe TARGET` | Menjalankan kategori NSE yang diklasifikasikan safe | `nmap --script safe 192.168.1.10` |
| `nmap --script discovery TARGET` | Menjalankan kategori discovery NSE | `nmap --script discovery 192.168.1.10` |
| `nmap --script version TARGET` | Menjalankan script NSE kategori version | `nmap --script version 192.168.1.10` |
| `nmap --script-help '*'` | Menampilkan bantuan script NSE | `nmap --script-help '*'` |
| `nmap --version` | Menampilkan versi Nmap | `nmap --version` |
| `nmap -V` | Alias untuk menampilkan versi Nmap | `nmap -V` |
| `nmap -h` | Menampilkan bantuan singkat | `nmap -h` |
| `nmap --help` | Menampilkan bantuan penggunaan | `nmap --help` |
| `nmap -h --help` | Menampilkan ringkasan opsi bantuan | `nmap -h` |
| `nmap --iflist` | Menampilkan daftar interface dan route | `nmap --iflist` |
| `nmap --privileged TARGET` | Menganggap user memiliki hak istimewa untuk raw packet operations | `nmap --privileged 192.168.1.10` |
| `nmap --unprivileged TARGET` | Menganggap user tidak memiliki hak raw packet | `nmap --unprivileged 192.168.1.10` |
| `nmap --release-memory TARGET` | Melepaskan memori sebelum keluar | `nmap --release-memory 192.168.1.10` |
| `nmap --datadir DIRECTORY TARGET` | Menentukan direktori data Nmap | `nmap --datadir /usr/share/nmap 192.168.1.10` |
| `nmap --servicedb FILE TARGET` | Menggunakan service database tertentu | `nmap --servicedb services.txt 192.168.1.10` |
| `nmap --versiondb FILE TARGET` | Menggunakan version detection database tertentu | `nmap --versiondb nmap-service-probes 192.168.1.10` |
| `nmap --system-dns TARGET` | Menggunakan DNS resolver sistem | `nmap --system-dns example.com` |
| `nmap --resolve-all TARGET` | Memindai seluruh alamat hasil resolusi hostname | `nmap --resolve-all example.com` |
| `nmap --unique TARGET` | Memindai setiap IP hanya sekali setelah resolusi | `nmap --unique example.com` |
| `nmap --privileged -sS TARGET` | Menjalankan SYN scan dengan asumsi hak istimewa | `nmap --privileged -sS 192.168.1.10` |
| `nmap --unprivileged -sT TARGET` | Memaksa perilaku scan tanpa raw packet privilege | `nmap --unprivileged -sT 192.168.1.10` |
| `nmap --resume FILE` | Melanjutkan scan dari file output sebelumnya | `nmap --resume scan.nmap` |
