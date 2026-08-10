# metasploit 

| Fitur Metasploit | Deskripsi |
|---|---|
| `Exploits` | Modul untuk memanfaatkan kerentanan (vulnerability) pada target agar memperoleh akses atau mengeksekusi kode. Biasanya dipasangkan dengan payload. |
| `Auxiliary` | Modul yang tidak melakukan eksploitasi. Digunakan untuk tugas seperti scanning, fingerprinting, enumerasi, fuzzing, atau pengecekan layanan. |
| `Payloads` | Kode yang dijalankan pada target setelah exploit berhasil. Contohnya membuka shell, menjalankan perintah, atau membuat koneksi balik (reverse connection). |
| `Post` | Modul yang dijalankan setelah akses ke target diperoleh. Digunakan untuk pengumpulan informasi, pemeriksaan konfigurasi, atau tugas pasca-eksploitasi lainnya. |
| `Encoders` | Modul yang mengubah representasi payload agar sesuai dengan batasan tertentu (misalnya menghindari karakter yang dilarang atau bad characters). Bukan jaminan untuk menghindari deteksi keamanan. |
| `NOPs` | Modul yang menghasilkan rangkaian instruksi No Operation (NOP) untuk membantu penyelarasan eksekusi payload pada beberapa jenis exploit. |
| `Evasion` | Modul yang digunakan untuk menghasilkan atau memodifikasi payload agar lebih sulit dianalisis atau terdeteksi oleh mekanisme keamanan tertentu. Penggunaannya umumnya dibatasi pada lingkungan pengujian yang sah dan berizin. |

| Fitur Metasploit | Deskripsi |
|---|---|
| `Exploits` | Modul untuk memanfaatkan kerentanan (vulnerability) pada target agar memperoleh akses atau mengeksekusi kode. Biasanya dipasangkan dengan payload. |
| `Auxiliary` | Modul yang tidak melakukan eksploitasi. Digunakan untuk tugas seperti scanning, fingerprinting, enumerasi, fuzzing, atau pengecekan layanan. |
| `Payloads` | Kode yang dijalankan pada target setelah exploit berhasil. Contohnya membuka shell, menjalankan perintah, atau membuat koneksi balik (reverse connection). |
| `Post` | Modul yang dijalankan setelah akses ke target diperoleh. Digunakan untuk pengumpulan informasi, pemeriksaan konfigurasi, atau tugas pasca-eksploitasi lainnya. |
| `Encoders` | Modul yang mengubah representasi payload agar sesuai dengan batasan tertentu (misalnya menghindari karakter yang dilarang atau bad characters). Bukan jaminan untuk menghindari deteksi keamanan. |
| `NOPs` | Modul yang menghasilkan rangkaian instruksi No Operation (NOP) untuk membantu penyelarasan eksekusi payload pada beberapa jenis exploit. |
| `Evasion` | Modul yang digunakan untuk menghasilkan atau memodifikasi payload agar lebih sulit dianalisis atau terdeteksi oleh mekanisme keamanan tertentu. Penggunaannya umumnya dibatasi pada lingkungan pengujian yang sah dan berizin. |

| Command | Deskripsi | Contoh |
|---|---|---|
| `msfconsole` | Membuka Metasploit Framework console | `msfconsole` |
| `msfdb init` | Menginisialisasi database Metasploit | `msfdb init` |
| `msfdb start` | Menjalankan database Metasploit | `msfdb start` |
| `msfdb stop` | Menghentikan database Metasploit | `msfdb stop` |
| `msfdb restart` | Me-restart database Metasploit | `msfdb restart` |
| `msfdb status` | Melihat status database | `msfdb status` |
| `help` | Menampilkan daftar bantuan perintah | `help` |
| `help <command>` | Menampilkan bantuan perintah tertentu | `help search` |
| `?` | Alias untuk bantuan | `?` |
| `version` | Melihat versi Metasploit | `version` |
| `banner` | Menampilkan banner Metasploit | `banner` |
| `exit` | Keluar dari Metasploit console | `exit` |
| `quit` | Keluar dari Metasploit console | `quit` |
| `clear` | Membersihkan tampilan terminal | `clear` |
| `history` | Melihat riwayat perintah | `history` |
| `save` | Menyimpan konfigurasi sesi | `save` |
| `route` | Mengatur routing melalui sesi aktif | `route add 10.0.0.0/24 1` |
| `connect` | Membuat koneksi TCP sederhana | `connect 192.168.1.10 80` |
| `irb` | Membuka Ruby interpreter internal | `irb` |
| `jobs` | Melihat daftar job yang berjalan | `jobs` |
| `jobs -l` | Melihat detail job | `jobs -l` |
| `jobs -k <id>` | Menghentikan job tertentu | `jobs -k 1` |
| `jobs -K` | Menghentikan semua job | `jobs -K` |
| `sessions` | Melihat sesi aktif | `sessions` |
| `sessions -l` | Menampilkan daftar sesi | `sessions -l` |
| `sessions -i <id>` | Masuk ke sesi tertentu | `sessions -i 1` |
| `sessions -k <id>` | Menutup sesi tertentu | `sessions -k 1` |
| `sessions -K` | Menutup semua sesi | `sessions -K` |
| `background` | Memindahkan sesi aktif ke background | `background` |
| `search` | Mencari modul Metasploit | `search type:exploit windows` |
| `use` | Memilih modul | `use exploit/windows/smb/ms17_010_eternalblue` |
| `show` | Menampilkan informasi modul | `show options` |
| `show exploits` | Menampilkan daftar exploit | `show exploits` |
| `show payloads` | Menampilkan daftar payload | `show payloads` |
| `show auxiliary` | Menampilkan modul auxiliary | `show auxiliary` |
| `show encoders` | Menampilkan encoder | `show encoders` |
| `show nops` | Menampilkan generator NOP | `show nops` |
| `show evasion` | Menampilkan modul evasion | `show evasion` |
| `info` | Menampilkan informasi modul | `info exploit/windows/smb/ms17_010_eternalblue` |
| `options` | Melihat opsi modul aktif | `show options` |
| `set` | Mengatur nilai opsi modul | `set RHOSTS 192.168.1.10` |
| `setg` | Mengatur variabel global | `setg RHOSTS 192.168.1.10` |
| `unset` | Menghapus nilai opsi | `unset RHOSTS` |
| `unsetg` | Menghapus variabel global | `unsetg RHOSTS` |
| `get` | Melihat nilai opsi | `get RHOSTS` |
| `getg` | Melihat nilai global | `getg RHOSTS` |
| `check` | Mengecek target tanpa menjalankan modul | `check` |
| `run` | Menjalankan modul aktif | `run` |
| `exploit` | Menjalankan exploit aktif | `exploit` |
| `reload` | Memuat ulang modul | `reload` |
| `reload_all` | Memuat ulang semua modul | `reload_all` |
| `back` | Kembali ke menu utama | `back` |
| `previous` | Kembali ke modul sebelumnya | `previous` |
| `edit` | Membuka modul di editor | `edit` |
| `makerc` | Membuat file resource dari perintah | `makerc commands.rc` |
| `resource` | Menjalankan file resource | `resource script.rc` |
| `spool` | Menyimpan output console ke file | `spool output.txt` |
| `db_status` | Melihat status koneksi database | `db_status` |
| `db_connect` | Menghubungkan database | `db_connect user:pass@localhost/msf` |
| `db_disconnect` | Memutus koneksi database | `db_disconnect` |
| `db_rebuild_cache` | Membuat ulang cache database | `db_rebuild_cache` |
| `hosts` | Melihat daftar host database | `hosts` |
| `services` | Melihat layanan host | `services` |
| `vulns` | Melihat kerentanan yang tersimpan | `vulns` |
| `creds` | Melihat kredensial tersimpan | `creds` |
| `loot` | Melihat data loot | `loot` |
| `notes` | Melihat catatan database | `notes` |
| `workspace` | Mengelola workspace | `workspace` |
| `workspace -a` | Membuat workspace baru | `workspace -a lab` |
| `workspace -d` | Menghapus workspace | `workspace -d lab` |
| `workspace -r` | Mengganti nama workspace | `workspace -r old new` |
| `db_nmap` | Menjalankan Nmap melalui database Metasploit | `db_nmap -sV 192.168.1.10` |
| `db_import` | Mengimpor hasil scan | `db_import scan.xml` |
| `db_export` | Mengekspor database | `db_export -f xml export.xml` |
| `db_autopwn` | Menjalankan autopwn (versi lama) | `db_autopwn` |
| `resource` | Menjalankan script otomatisasi | `resource auto.rc` |
| `load` | Memuat plugin | `load db_tracker` |
| `unload` | Menghapus plugin | `unload db_tracker` |
| `loadpath` | Menambah path modul | `loadpath /opt/modules` |
| `unloadpath` | Menghapus path modul | `unloadpath /opt/modules` |
| `plugins` | Melihat plugin aktif | `plugins` |
| `sessions -u` | Upgrade shell menjadi Meterpreter | `sessions -u 1` |
| `sysinfo` | Melihat informasi sistem Meterpreter | `sysinfo` |
| `getuid` | Melihat user aktif Meterpreter | `getuid` |
| `pwd` | Melihat direktori aktif | `pwd` |
| `ls` | Melihat isi direktori | `ls` |
| `cd` | Berpindah direktori | `cd /tmp` |
| `cat` | Membaca file | `cat file.txt` |
| `download` | Mengambil file dari host | `download file.txt` |
| `upload` | Mengirim file ke host | `upload file.txt` |
| `shell` | Membuka shell sistem | `shell` |
| `execute` | Menjalankan program | `execute -f cmd.exe` |
| `ps` | Melihat proses berjalan | `ps` |
| `kill` | Menghentikan proses | `kill 1234` |
| `getpid` | Melihat PID Meterpreter | `getpid` |
| `migrate` | Memindahkan proses Meterpreter | `migrate 1234` |
| `background` | Menaruh Meterpreter di background | `background` |
| `run` | Menjalankan script Meterpreter | `run post/windows/gather/hashdump` |
| `resource` | Menjalankan script Meterpreter | `resource script.rc` |
| `help` | Bantuan Meterpreter | `help` |
| `hashdump` | Mengambil hash password (modul tertentu) | `hashdump` |
| `getsystem` | Mencoba eskalasi hak akses | `getsystem` |
| `keyscan_start` | Memulai keylogger | `keyscan_start` |
| `keyscan_stop` | Menghentikan keylogger | `keyscan_stop` |
| `keyscan_dump` | Menampilkan hasil keylogger | `keyscan_dump` |
| `screenshot` | Mengambil screenshot layar | `screenshot` |
| `webcam_list` | Melihat perangkat webcam | `webcam_list` |
| `webcam_snap` | Mengambil gambar webcam | `webcam_snap` |
| `record_mic` | Merekam mikrofon | `record_mic -d 10` |
| `enumdesktops` | Melihat desktop aktif | `enumdesktops` |
| `getsystem` | Mendapatkan hak sistem jika memungkinkan | `getsystem` |
| `run post` | Menjalankan modul post exploitation | `run post/windows/gather/enum_logged_on_users` |
| `search <file>` | Mencari file pada sistem target | `search -f password.txt` |
| `clearev` | Membersihkan event log (jika memiliki izin) | `clearev` |
| `reboot` | Restart sistem target | `reboot` |
| `shutdown` | Mematikan sistem target | `shutdown` |

(Daftar mencakup perintah inti Metasploit Console, modul, database, job/session, dan Meterpreter. Perintah modul sangat banyak dan terus berubah sesuai versi Metasploit.)
