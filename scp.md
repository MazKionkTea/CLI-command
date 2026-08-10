# scp

| Command | Deskripsi | Contoh |
|---|---|---|
| `scp SOURCE USER@HOST:DEST` | Menyalin file dari komputer lokal ke server remote. | `scp file.txt root@192.168.1.10:/root/` |
| `scp USER@HOST:SOURCE DEST` | Mengunduh file dari server remote ke komputer lokal. | `scp root@192.168.1.10:/root/file.txt ./` |
| `scp USER1@HOST1:SOURCE USER2@HOST2:DEST` | Menyalin file langsung dari satu server remote ke server remote lain. | `scp root@server1:/root/a.txt root@server2:/root/` |
| `scp file1 file2 USER@HOST:DEST` | Mengirim beberapa file sekaligus ke server. | `scp a.txt b.txt root@192.168.1.10:/root/` |
| `scp USER@HOST:/path/* DEST` | Mengunduh beberapa file menggunakan wildcard. | `scp root@192.168.1.10:/root/*.txt ./` |
| `scp -r DIRECTORY USER@HOST:DEST` | Menyalin direktori beserta seluruh isinya secara rekursif. | `scp -r website/ root@192.168.1.10:/var/www/` |
| `scp -r USER@HOST:DIRECTORY DEST` | Mengunduh direktori dari server remote. | `scp -r root@192.168.1.10:/var/www/site ./` |
| `scp -p SOURCE USER@HOST:DEST` | Mempertahankan permission dan timestamp file. | `scp -p file.txt root@192.168.1.10:/root/` |
| `scp -P PORT SOURCE USER@HOST:DEST` | Menggunakan port SSH tertentu. | `scp -P 2222 file.txt root@192.168.1.10:/root/` |
| `scp -i KEY SOURCE USER@HOST:DEST` | Menggunakan private key SSH tertentu. | `scp -i ~/.ssh/id_ed25519 file.txt root@192.168.1.10:/root/` |
| `scp -C SOURCE USER@HOST:DEST` | Mengaktifkan kompresi selama transfer. | `scp -C backup.tar.gz root@192.168.1.10:/backup/` |
| `scp -v SOURCE USER@HOST:DEST` | Menampilkan informasi detail proses koneksi dan transfer untuk debugging. | `scp -v file.txt root@192.168.1.10:/root/` |
| `scp -q SOURCE USER@HOST:DEST` | Mengurangi output/status yang ditampilkan selama transfer. | `scp -q file.txt root@192.168.1.10:/root/` |
| `scp -4 SOURCE USER@HOST:DEST` | Memaksa penggunaan IPv4. | `scp -4 file.txt root@server.example.com:/root/` |
| `scp -6 SOURCE USER@HOST:DEST` | Memaksa penggunaan IPv6. | `scp -6 file.txt root@[2001:db8::10]:/root/` |
| `scp -B SOURCE USER@HOST:DEST` | Menggunakan batch mode dan tidak meminta input interaktif. | `scp -B file.txt root@192.168.1.10:/root/` |
| `scp -l LIMIT SOURCE USER@HOST:DEST` | Membatasi bandwidth transfer dalam Kbit/s. | `scp -l 8000 backup.tar.gz root@192.168.1.10:/backup/` |
| `scp -S PROGRAM SOURCE USER@HOST:DEST` | Menentukan program SSH yang digunakan oleh `scp`. | `scp -S /usr/bin/ssh file.txt root@192.168.1.10:/root/` |
| `scp -F CONFIG SOURCE USER@HOST:DEST` | Menggunakan file konfigurasi SSH tertentu. | `scp -F ~/.ssh/config-prod file.txt root@server:/root/` |
| `scp -o OPTION SOURCE USER@HOST:DEST` | Memberikan opsi konfigurasi SSH secara langsung. | `scp -o ConnectTimeout=10 file.txt root@192.168.1.10:/root/` |
| `scp -O SOURCE USER@HOST:DEST` | Memaksa penggunaan protokol SCP lama. | `scp -O file.txt root@192.168.1.10:/root/` |
| `scp -T SOURCE USER@HOST:DEST` | Menonaktifkan pemeriksaan nama file/target pada sisi remote. | `scp -T file.txt root@192.168.1.10:/root/` |
| `scp -3 USER1@HOST1:SOURCE USER2@HOST2:DEST` | Merutekan transfer antara dua host remote melalui komputer lokal. | `scp -3 root@server1:/a.txt root@server2:/backup/` |
| `scp -c CIPHER SOURCE USER@HOST:DEST` | Memilih cipher SSH yang digunakan untuk enkripsi transfer. | `scp -c aes256-gcm@openssh.com file.txt root@192.168.1.10:/root/` |
| `scp -E LOGFILE SOURCE USER@HOST:DEST` | Menulis pesan diagnostik ke file log pada versi OpenSSH yang mendukung opsi ini. | `scp -E scp.log file.txt root@192.168.1.10:/root/` |
| `scp -o Compression=yes SOURCE USER@HOST:DEST` | Mengaktifkan kompresi melalui konfigurasi SSH. | `scp -o Compression=yes backup.sql root@192.168.1.10:/backup/` |
| `scp -o ConnectTimeout=10 SOURCE USER@HOST:DEST` | Membatasi waktu tunggu koneksi menjadi 10 detik. | `scp -o ConnectTimeout=10 file.txt root@192.168.1.10:/root/` |
| `scp -J USER@JUMP_HOST SOURCE USER@HOST:DEST` | Mengakses server tujuan melalui jump/bastion host. | `scp -J root@10.0.0.5 file.txt root@10.0.0.10:/root/` |
| `scp 'USER@HOST:/path/file name.txt' ./` | Mengunduh file remote yang memiliki spasi pada nama file/path. | `scp 'root@192.168.1.10:/root/my file.txt' ./` |
| `scp ./file.txt USER@HOST:'/path/my file.txt'` | Mengirim file dengan path tujuan yang memiliki spasi. | `scp ./file.txt root@192.168.1.10:'/root/my file.txt'` |
| `scp USER@HOST:/path/file.txt ./newname.txt` | Mengunduh file sekaligus mengganti namanya di lokal. | `scp root@192.168.1.10:/root/file.txt ./backup.txt` |
| `scp ./file.txt USER@HOST:/path/newname.txt` | Mengirim file sekaligus mengganti namanya di server. | `scp ./file.txt root@192.168.1.10:/root/backup.txt` |
| `scp -r -C DIRECTORY USER@HOST:DEST` | Mengirim direktori secara rekursif dengan kompresi. | `scp -r -C website/ root@192.168.1.10:/var/www/` |
| `scp -r -p DIRECTORY USER@HOST:DEST` | Mengirim direktori secara rekursif dan mempertahankan timestamp serta permission. | `scp -r -p website/ root@192.168.1.10:/var/www/` |
| `scp -r -P PORT -i KEY DIRECTORY USER@HOST:DEST` | Mengirim direktori menggunakan port dan private key tertentu. | `scp -r -P 2222 -i ~/.ssh/id_ed25519 website/ root@192.168.1.10:/var/www/` |
| `scp -4 -P PORT -i KEY SOURCE USER@HOST:DEST` | Transfer menggunakan IPv4, port SSH tertentu, dan private key. | `scp -4 -P 2222 -i ~/.ssh/id_ed25519 file.txt root@192.168.1.10:/root/` |
| `scp --help` | Menampilkan bantuan dan opsi `scp` yang tersedia. | `scp --help` |
| `man scp` | Membuka dokumentasi/manual `scp` pada sistem. | `man scp` |
