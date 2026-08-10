# hydra

| Command | Deskripsi | Contoh |
|---|---|---|
| `hydra -h` | Menampilkan bantuan penggunaan Hydra. | `hydra -h` |
| `hydra -U <module>` | Menampilkan bantuan dan opsi khusus module/service. | `hydra -U ssh` |
| `hydra -l <username>` | Menentukan satu username. | `hydra -l testuser ...` |
| `hydra -L <file>` | Membaca daftar username dari file. | `hydra -L users.txt ...` |
| `hydra -p <password>` | Menentukan satu password. | `hydra -p testpass ...` |
| `hydra -P <file>` | Membaca daftar password dari file. | `hydra -P passwords.txt ...` |
| `hydra -C <file>` | Membaca pasangan username/password dari file. | `hydra -C credentials.txt ...` |
| `hydra -e <mode>` | Mengaktifkan password tambahan yang diturunkan dari username/password. `n` = password kosong, `s` = username sebagai password, `r` = password dibalik. | `hydra -l testuser -P passwords.txt -e nsr ...` |
| `hydra -u` | Membalik urutan kombinasi sehingga username diproses terlebih dahulu. | `hydra -L users.txt -P passwords.txt -u ...` |
| `hydra -f` | Berhenti setelah menemukan kredensial valid pada target saat ini. | `hydra -f ...` |
| `hydra -F` | Berhenti setelah menemukan hasil valid pada semua target yang sedang diproses. | `hydra -F ...` |
| `hydra -M <file>` | Membaca daftar target dari file. | `hydra -M targets.txt ...` |
| `hydra -s <port>` | Menentukan port service secara manual. | `hydra -s 2222 ...` |
| `hydra -S` | Menggunakan SSL/TLS untuk koneksi yang didukung module. | `hydra -S ...` |
| `hydra -4` | Memaksa penggunaan IPv4. | `hydra -4 ...` |
| `hydra -6` | Memaksa penggunaan IPv6. | `hydra -6 ...` |
| `hydra -t <tasks>` | Menentukan jumlah task paralel untuk setiap target. | `hydra -t 2 ...` |
| `hydra -T <tasks>` | Menentukan jumlah task paralel secara global. | `hydra -T 4 ...` |
| `hydra -w <seconds>` | Menentukan waktu tunggu koneksi/socket. | `hydra -w 10 ...` |
| `hydra -W <seconds>` | Menentukan waktu tunggu antar-task tertentu. | `hydra -W 5 ...` |
| `hydra -c <seconds>` | Memberikan jeda antar-login untuk module tertentu. | `hydra -c 2 ...` |
| `hydra -x <min:max:charset>` | Membuat kandidat password secara otomatis berdasarkan panjang dan karakter yang ditentukan. | `hydra -x 1:4:a ...` |
| `hydra -y` | Tidak menggunakan karakter khusus ketika membuat kandidat dengan `-x`. | `hydra -x 1:4:a -y ...` |
| `hydra -o <file>` | Menyimpan hasil ke file. | `hydra ... -o result.txt` |
| `hydra -b <format>` | Menentukan format output pada versi yang mendukung opsi tersebut. | `hydra ... -b json` |
| `hydra -v` | Menampilkan informasi proses secara verbose. | `hydra -v ...` |
| `hydra -V` | Menampilkan detail percobaan secara lebih verbose. | `hydra -V ...` |
| `hydra -d` | Mengaktifkan mode debugging. | `hydra -d ...` |
| `hydra -I` | Mengabaikan restore file yang mungkin masih tersedia dan memulai sesi baru. | `hydra -I ...` |
| `hydra -R` | Melanjutkan sesi dari restore file Hydra. | `hydra -R` |
| `hydra -q` | Menekan pesan error tertentu. | `hydra -q ...` |
| `hydra -K` | Mengontrol perilaku melanjutkan atau mempertahankan koneksi/task pada kondisi tertentu. | `hydra -K ...` |
| `hydra -O` | Mengaktifkan kompatibilitas SSL tertentu untuk implementasi/library lama. | `hydra -O ...` |
| `hydra -D <proxy>` | Menggunakan proxy pada konfigurasi yang mendukung fitur tersebut. | `hydra -D 127.0.0.1:8080 ...` |
| `hydra -m <options>` | Memberikan opsi tambahan yang spesifik untuk module/service. | `hydra -m <module-options> ...` |
| `hydra <target> <module>` | Sintaks dasar untuk menjalankan module terhadap satu target. | `hydra 127.0.0.1 ssh` |
| `hydra -M <targets> <module>` | Menjalankan module terhadap beberapa target dari file. | `hydra -M targets.txt ssh` |
| `hydra -l <user> -p <pass> <target> <module>` | Menguji satu pasangan username/password pada service lab. | `hydra -l testuser -p testpass 127.0.0.1 ssh` |
| `hydra -l <user> -P <file> <target> <module>` | Menggunakan satu username dan daftar password. | `hydra -l testuser -P passwords.txt 127.0.0.1 ssh` |
| `hydra -L <file> -p <pass> <target> <module>` | Menggunakan daftar username dan satu password. | `hydra -L users.txt -p testpass 127.0.0.1 ssh` |
| `hydra -L <users> -P <passwords> <target> <module>` | Menggunakan daftar username dan password. | `hydra -L users.txt -P passwords.txt 127.0.0.1 ssh` |
| `hydra -C <file> <target> <module>` | Menggunakan pasangan username/password dari credential file. | `hydra -C credentials.txt 127.0.0.1 ssh` |
| `hydra <target> ftp` | Memilih module FTP. | `hydra 127.0.0.1 ftp ...` |
| `hydra <target> ssh` | Memilih module SSH. | `hydra 127.0.0.1 ssh ...` |
| `hydra <target> telnet` | Memilih module Telnet. | `hydra 127.0.0.1 telnet ...` |
| `hydra <target> smtp` | Memilih module SMTP. | `hydra 127.0.0.1 smtp ...` |
| `hydra <target> pop3` | Memilih module POP3. | `hydra 127.0.0.1 pop3 ...` |
| `hydra <target> imap` | Memilih module IMAP. | `hydra 127.0.0.1 imap ...` |
| `hydra <target> http-get` | Memilih module HTTP GET. | `hydra 127.0.0.1 http-get ...` |
| `hydra <target> http-head` | Memilih module HTTP HEAD. | `hydra 127.0.0.1 http-head ...` |
| `hydra <target> http-post-form` | Memilih module HTTP POST form untuk pengujian autentikasi form. | `hydra 127.0.0.1 http-post-form ...` |
| `hydra <target> http-get-form` | Memilih module HTTP GET form jika tersedia pada build. | `hydra 127.0.0.1 http-get-form ...` |
| `hydra <target> https-get` | Memilih module HTTP GET melalui TLS jika tersedia. | `hydra 127.0.0.1 https-get ...` |
| `hydra <target> https-post-form` | Memilih module HTTPS POST form jika tersedia. | `hydra 127.0.0.1 https-post-form ...` |
| `hydra <target> smb` | Memilih module SMB. | `hydra 127.0.0.1 smb ...` |
| `hydra <target> smb2` | Memilih module SMB2 jika tersedia pada build. | `hydra 127.0.0.1 smb2 ...` |
| `hydra <target> rdp` | Memilih module RDP. | `hydra 127.0.0.1 rdp ...` |
| `hydra <target> vnc` | Memilih module VNC. | `hydra 127.0.0.1 vnc ...` |
| `hydra <target> mysql` | Memilih module MySQL. | `hydra 127.0.0.1 mysql ...` |
| `hydra <target> mssql` | Memilih module Microsoft SQL Server. | `hydra 127.0.0.1 mssql ...` |
| `hydra <target> postgresql` | Memilih module PostgreSQL. | `hydra 127.0.0.1 postgresql ...` |
| `hydra <target> oracle-listener` | Memilih module Oracle Listener jika tersedia. | `hydra 127.0.0.1 oracle-listener ...` |
| `hydra <target> redis` | Memilih module Redis jika tersedia. | `hydra 127.0.0.1 redis ...` |
| `hydra <target> mongodb` | Memilih module MongoDB jika tersedia. | `hydra 127.0.0.1 mongodb ...` |
| `hydra <target> ldap2` | Memilih module LDAPv2 jika tersedia. | `hydra 127.0.0.1 ldap2 ...` |
| `hydra <target> ldap3` | Memilih module LDAPv3 jika tersedia. | `hydra 127.0.0.1 ldap3 ...` |
| `hydra <target> afp` | Memilih module Apple Filing Protocol jika tersedia. | `hydra 127.0.0.1 afp ...` |
| `hydra <target> cisco` | Memilih module autentikasi Cisco tertentu jika tersedia. | `hydra 127.0.0.1 cisco ...` |
| `hydra <target> cisco-enable` | Memilih module Cisco enable authentication jika tersedia. | `hydra 127.0.0.1 cisco-enable ...` |
| `hydra <target> cvs` | Memilih module CVS jika tersedia. | `hydra 127.0.0.1 cvs ...` |
| `hydra <target> svn` | Memilih module Subversion jika tersedia. | `hydra 127.0.0.1 svn ...` |
| `hydra <target> nntp` | Memilih module NNTP. | `hydra 127.0.0.1 nntp ...` |
| `hydra <target> socks5` | Memilih module SOCKS5 jika tersedia. | `hydra 127.0.0.1 socks5 ...` |
| `hydra <target> socks4` | Memilih module SOCKS4 jika tersedia. | `hydra 127.0.0.1 socks4 ...` |
| `hydra <target> xMPP` | Memilih module XMPP jika tersedia pada build. | `hydra 127.0.0.1 xmpp ...` |
| `hydra <target> irc` | Memilih module IRC jika tersedia. | `hydra 127.0.0.1 irc ...` |
| `hydra <target> teamspeak` | Memilih module TeamSpeak jika tersedia. | `hydra 127.0.0.1 teamspeak ...` |
| `hydra <target> sip` | Memilih module SIP jika tersedia. | `hydra 127.0.0.1 sip ...` |
| `hydra <target> snmp` | Memilih module SNMP jika tersedia. | `hydra 127.0.0.1 snmp ...` |
| `hydra <target> rlogin` | Memilih module Rlogin. | `hydra 127.0.0.1 rlogin ...` |
| `hydra <target> rexec` | Memilih module Rexec jika tersedia. | `hydra 127.0.0.1 rexec ...` |
| `hydra <target> rsh` | Memilih module RSH jika tersedia. | `hydra 127.0.0.1 rsh ...` |
| `hydra <target> afp` | Memilih module AFP jika tersedia pada build. | `hydra 127.0.0.1 afp ...` |
| `hydra <target> ncp` | Memilih module NetWare Core Protocol jika tersedia. | `hydra 127.0.0.1 ncp ...` |
| `hydra <target> pcanywhere` | Memilih module PC Anywhere jika tersedia. | `hydra 127.0.0.1 pcanywhere ...` |
| `hydra <target> vmauthd` | Memilih module VMware Authentication Daemon jika tersedia. | `hydra 127.0.0.1 vmauthd ...` |
| `hydra <target> icq` | Memilih module ICQ jika tersedia pada versi lama/build tertentu. | `hydra 127.0.0.1 icq ...` |
| `hydra <target> teamspeak` | Memilih module TeamSpeak. | `hydra 127.0.0.1 teamspeak ...` |
| `hydra <target> oracle` | Memilih module Oracle database jika tersedia. | `hydra 127.0.0.1 oracle ...` |
| `hydra <target> sapr3` | Memilih module SAP R/3 jika tersedia. | `hydra 127.0.0.1 sapr3 ...` |
| `hydra <target> vnc` | Memilih module VNC. | `hydra 127.0.0.1 vnc ...` |
| `hydra <target> xdmcp` | Memilih module XDMCP jika tersedia. | `hydra 127.0.0.1 xdmcp ...` |
| `hydra <target> snmp` | Memilih module SNMP. | `hydra 127.0.0.1 snmp ...` |
| `hydra <target> ldap2` | Memilih module LDAPv2. | `hydra 127.0.0.1 ldap2 ...` |
| `hydra <target> ldap3` | Memilih module LDAPv3. | `hydra 127.0.0.1 ldap3 ...` |
| `hydra <target> afp` | Memilih module Apple Filing Protocol. | `hydra 127.0.0.1 afp ...` |
| `hydra <target> cvs` | Memilih module CVS. | `hydra 127.0.0.1 cvs ...` |
| `hydra <target> svn` | Memilih module SVN. | `hydra 127.0.0.1 svn ...` |
| `hydra <target> ftp` | Menguji autentikasi FTP menggunakan module FTP. | `hydra 127.0.0.1 ftp ...` |
| `hydra <target> ssh` | Menguji autentikasi SSH menggunakan module SSH. | `hydra 127.0.0.1 ssh ...` |
| `hydra <target> smtp` | Menguji autentikasi SMTP menggunakan module SMTP. | `hydra 127.0.0.1 smtp ...` |
| `hydra <target> pop3` | Menguji autentikasi POP3 menggunakan module POP3. | `hydra 127.0.0.1 pop3 ...` |
| `hydra <target> imap` | Menguji autentikasi IMAP menggunakan module IMAP. | `hydra 127.0.0.1 imap ...` |
| `hydra <target> http-get` | Menguji autentikasi HTTP menggunakan GET. | `hydra 127.0.0.1 http-get ...` |
| `hydra <target> http-post-form` | Menguji autentikasi form HTTP POST. | `hydra 127.0.0.1 http-post-form ...` |
| `hydra -U http-post-form` | Menampilkan sintaks dan parameter khusus module `http-post-form`. | `hydra -U http-post-form` |
| `hydra -U ssh` | Menampilkan sintaks dan parameter khusus module SSH. | `hydra -U ssh` |
| `hydra -U ftp` | Menampilkan sintaks dan parameter khusus module FTP. | `hydra -U ftp` |
| `hydra -U smb` | Menampilkan sintaks dan parameter khusus module SMB. | `hydra -U smb` |
| `hydra -U rdp` | Menampilkan sintaks dan parameter khusus module RDP. | `hydra -U rdp` |
| `hydra -U <module>` | Cara umum melihat dokumentasi module tertentu pada instalasi Hydra. | `hydra -U <module>` |
| `hydra -h` | Cara paling umum melihat opsi yang benar-benar didukung oleh versi Hydra yang terpasang. | `hydra -h` |
