# telnet

| Command | Deskripsi | Contoh |
|---|---|---|
| `telnet` | Memulai koneksi Telnet ke host | `telnet 192.168.1.1` |
| `open` | Membuka koneksi ke host dan port tertentu | `open example.com 23` |
| `close` | Menutup koneksi aktif | `close` |
| `quit` | Keluar dari program Telnet | `quit` |
| `exit` | Keluar dari program Telnet | `exit` |
| `status` | Menampilkan status koneksi saat ini | `status` |
| `display` | Menampilkan konfigurasi Telnet saat ini | `display` |
| `mode` | Mengubah mode transfer (line/character) | `mode character` |
| `send` | Mengirim karakter atau sinyal kontrol | `send ao` |
| `set` | Mengubah parameter atau opsi Telnet | `set localecho` |
| `unset` | Menonaktifkan parameter atau opsi | `unset localecho` |
| `toggle` | Mengaktifkan/menonaktifkan opsi tertentu | `toggle crlf` |
| `slc` | Mengatur Special Line Characters | `slc export` |
| `auth` | Mengatur atau melihat autentikasi | `auth status` |
| `encrypt` | Mengatur enkripsi sesi Telnet (jika didukung) | `encrypt enable` |
| `environ` | Mengelola variabel lingkungan | `environ list` |
| `z` | Menangguhkan (suspend) sesi Telnet (Unix) | `z` |
| `?` | Menampilkan bantuan singkat | `?` |
| `help` | Menampilkan daftar bantuan | `help` |
| `help send` | Bantuan untuk subperintah send | `help send` |
| `help set` | Bantuan untuk subperintah set | `help set` |
| `help toggle` | Bantuan untuk subperintah toggle | `help toggle` |
| `send ao` | Mengirim Abort Output | `send ao` |
| `send ayt` | Mengirim Are You There | `send ayt` |
| `send brk` | Mengirim Break | `send brk` |
| `send ec` | Mengirim Erase Character | `send ec` |
| `send el` | Mengirim Erase Line | `send el` |
| `send eof` | Mengirim End of File | `send eof` |
| `send eor` | Mengirim End of Record | `send eor` |
| `send escape` | Mengirim karakter escape | `send escape` |
| `send ga` | Mengirim Go Ahead | `send ga` |
| `send ip` | Mengirim Interrupt Process | `send ip` |
| `send nop` | Mengirim No Operation | `send nop` |
| `send synch` | Mengirim Synch | `send synch` |
| `send susp` | Mengirim Suspend Process | `send susp` |
| `send abort` | Mengirim Abort Process | `send abort` |
| `send do` | Negosiasi opsi (DO) | `send do echo` |
| `send dont` | Negosiasi opsi (DONT) | `send dont echo` |
| `send will` | Negosiasi opsi (WILL) | `send will suppress-go-ahead` |
| `send wont` | Negosiasi opsi (WONT) | `send wont echo` |
| `set escape` | Mengatur karakter escape | `set escape ^]` |
| `set localecho` | Mengaktifkan echo lokal | `set localecho` |
| `unset localecho` | Menonaktifkan echo lokal | `unset localecho` |
| `set crlf` | Mengaktifkan translasi CR/LF | `set crlf` |
| `unset crlf` | Menonaktifkan translasi CR/LF | `unset crlf` |
| `set binary` | Mengaktifkan mode biner | `set binary` |
| `unset binary` | Menonaktifkan mode biner | `unset binary` |
| `toggle autoflush` | Toggle autoflush | `toggle autoflush` |
| `toggle autosynch` | Toggle autosynch | `toggle autosynch` |
| `toggle autologin` | Toggle autologin | `toggle autologin` |
| `toggle skiprc` | Toggle pembacaan file .telnetrc | `toggle skiprc` |
| `toggle localchars` | Toggle pemrosesan karakter lokal | `toggle localchars` |
| `toggle netdata` | Toggle tampilan data jaringan | `toggle netdata` |
| `toggle prettydump` | Toggle format dump data | `toggle prettydump` |
| `toggle options` | Toggle tampilan negosiasi opsi | `toggle options` |
| `toggle debug` | Toggle mode debug | `toggle debug` |
| `toggle termdata` | Toggle tampilan data terminal | `toggle termdata` |
| `toggle inbinary` | Toggle mode input biner | `toggle inbinary` |
| `toggle outbinary` | Toggle mode output biner | `toggle outbinary` |
| `toggle binary` | Toggle mode biner dua arah | `toggle binary` |
| `toggle crmod` | Toggle mode carriage return | `toggle crmod` |
| `toggle echo` | Toggle echo lokal | `toggle echo` |
| `toggle verbose_encrypt` | Toggle informasi enkripsi | `toggle verbose_encrypt` |
| `toggle verbose` | Toggle output verbose | `toggle verbose` |
| `toggle rlogin` | Toggle mode kompatibilitas rlogin | `toggle rlogin` |
| `toggle flowcontrol` | Toggle flow control | `toggle flowcontrol` |
