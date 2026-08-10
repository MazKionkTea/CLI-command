| Command | Deskripsi | Contoh |
|---|---|---|
| `enum4linux -h` | Menampilkan bantuan dan seluruh opsi yang tersedia pada versi enum4linux yang terpasang. | `enum4linux -h` |
| `enum4linux -a <target>` | Menjalankan seluruh enumerasi sederhana: user, machine, share, group, password policy, RID cycling, OS, NetBIOS, dan printer. | `enum4linux -a 192.168.1.10` |
| `enum4linux <target>` | Menjalankan enumerasi sederhana secara default jika tidak ada opsi lain yang diberikan. | `enum4linux 192.168.1.10` |
| `enum4linux -U <target>` | Mengambil daftar user dari host melalui RPC. | `enum4linux -U 192.168.1.10` |
| `enum4linux -M <target>` | Mengambil daftar machine/account komputer yang dapat ditemukan melalui RPC. | `enum4linux -M 192.168.1.10` |
| `enum4linux -S <target>` | Mengambil daftar SMB share yang tersedia. | `enum4linux -S 192.168.1.10` |
| `enum4linux -P <target>` | Mengambil informasi password policy dari host/domain. | `enum4linux -P 192.168.1.10` |
| `enum4linux -G <target>` | Mengambil daftar group dan informasi membership group. | `enum4linux -G 192.168.1.10` |
| `enum4linux -d <target>` | Mengaktifkan output yang lebih detail; terutama digunakan bersama enumerasi user/share pada enum4linux klasik. | `enum4linux -d -U 192.168.1.10` |
| `enum4linux -u <user> <target>` | Menentukan username yang digunakan untuk autentikasi ke SMB/RPC. | `enum4linux -u testuser 192.168.1.10` |
| `enum4linux -p <password> <target>` | Menentukan password yang digunakan untuk autentikasi. | `enum4linux -u testuser -p testpass 192.168.1.10` |
| `enum4linux -r <target>` | Melakukan enumerasi user menggunakan RID cycling. | `enum4linux -r 192.168.1.10` |
| `enum4linux -R <range> <target>` | Menentukan rentang RID yang akan digunakan untuk RID cycling. | `enum4linux -R 500-1000 192.168.1.10` |
| `enum4linux -K <number> <target>` | Melanjutkan pencarian RID sampai sejumlah RID berturut-turut tidak menghasilkan username. | `enum4linux -K 10 192.168.1.10` |
| `enum4linux -l <target>` | Mengambil informasi domain terbatas melalui LDAP pada domain controller. | `enum4linux -l 192.168.1.10` |
| `enum4linux -s <file> <target>` | Menggunakan wordlist untuk mencoba menebak nama share. | `enum4linux -s shares.txt 192.168.1.10` |
| `enum4linux -k <users> <target>` | Menentukan username yang diketahui untuk membantu proses SID/RID lookup. | `enum4linux -k administrator 192.168.1.10` |
| `enum4linux -k user1,user2 <target>` | Menggunakan beberapa username yang diketahui dalam proses SID lookup. | `enum4linux -k administrator,guest 192.168.1.10` |
| `enum4linux -o <target>` | Mengambil informasi sistem operasi dan versi Samba/Windows yang dapat diperoleh. | `enum4linux -o 192.168.1.10` |
| `enum4linux -i <target>` | Mengambil informasi printer melalui RPC. | `enum4linux -i 192.168.1.10` |
| `enum4linux -w <workgroup> <target>` | Menentukan workgroup/domain secara manual. | `enum4linux -w WORKGROUP 192.168.1.10` |
| `enum4linux -n <target>` | Menjalankan `nmblookup` untuk memperoleh informasi NetBIOS, mirip fungsi `nbtstat`. | `enum4linux -n 192.168.1.10` |
| `enum4linux -v <target>` | Mengaktifkan mode verbose dan menampilkan command eksternal yang dijalankan enum4linux. | `enum4linux -v 192.168.1.10` |
| `enum4linux -a -u <user> -p <password> <target>` | Menjalankan seluruh enumerasi sederhana menggunakan kredensial tertentu. | `enum4linux -a -u testuser -p testpass 192.168.1.10` |
| `enum4linux -U -d <target>` | Mengambil daftar user dengan informasi yang lebih detail. | `enum4linux -U -d 192.168.1.10` |
| `enum4linux -S -d <target>` | Mengambil daftar share dengan informasi yang lebih detail. | `enum4linux -S -d 192.168.1.10` |
| `enum4linux -U -r <target>` | Menggabungkan enumerasi user dengan RID cycling. | `enum4linux -U -r 192.168.1.10` |
| `enum4linux -a -w <workgroup> <target>` | Menjalankan enumerasi lengkap dengan workgroup/domain yang ditentukan secara manual. | `enum4linux -a -w WORKGROUP 192.168.1.10` |
| `enum4linux -a -u <user> -p <password> -w <workgroup> <target>` | Menjalankan enumerasi lengkap menggunakan username, password, dan workgroup tertentu. | `enum4linux -a -u testuser -p testpass -w WORKGROUP 192.168.1.10` |
| `enum4linux -U -u <user> -p <password> <target>` | Mengambil daftar user menggunakan kredensial yang diberikan. | `enum4linux -U -u testuser -p testpass 192.168.1.10` |
| `enum4linux -G -u <user> -p <password> <target>` | Mengambil informasi group menggunakan kredensial yang diberikan. | `enum4linux -G -u testuser -p testpass 192.168.1.10` |
| `enum4linux -S -u <user> -p <password> <target>` | Mengambil daftar share menggunakan kredensial yang diberikan. | `enum4linux -S -u testuser -p testpass 192.168.1.10` |
| `enum4linux -P -u <user> -p <password> <target>` | Mengambil password policy menggunakan kredensial yang diberikan. | `enum4linux -P -u testuser -p testpass 192.168.1.10` |
| `enum4linux -M -u <user> -p <password> <target>` | Mengambil daftar machine menggunakan kredensial yang diberikan. | `enum4linux -M -u testuser -p testpass 192.168.1.10` |
| `enum4linux -o -u <user> -p <password> <target>` | Mengambil informasi OS menggunakan kredensial yang diberikan. | `enum4linux -o -u testuser -p testpass 192.168.1.10` |
| `enum4linux -i -u <user> -p <password> <target>` | Mengambil informasi printer menggunakan kredensial yang diberikan. | `enum4linux -i -u testuser -p testpass 192.168.1.10` |
| `enum4linux -n -w <workgroup> <target>` | Melakukan NetBIOS lookup menggunakan workgroup yang ditentukan. | `enum4linux -n -w WORKGROUP 192.168.1.10` |
| `enum4linux -r -R 500-550 <target>` | Melakukan RID cycling hanya pada rentang RID tertentu. | `enum4linux -r -R 500-550 192.168.1.10` |
| `enum4linux -r -R 1000-1050 <target>` | Melakukan RID cycling pada rentang RID yang lebih tinggi. | `enum4linux -r -R 1000-1050 192.168.1.10` |
| `enum4linux -s <sharelist> <target>` | Mencoba nama share dari file wordlist yang diberikan. | `enum4linux -s /tmp/shares.txt 192.168.1.10` |
| `enum4linux -k administrator <target>` | Menggunakan `administrator` sebagai known user untuk membantu SID lookup. | `enum4linux -k administrator 192.168.1.10` |
| `enum4linux -k administrator,guest,root <target>` | Menggunakan beberapa known user untuk proses SID lookup. | `enum4linux -k administrator,guest,root 192.168.1.10` |
| `enum4linux -a -v <target>` | Menjalankan enumerasi lengkap dengan output verbose. | `enum4linux -a -v 192.168.1.10` |
| `enum4linux -a -d <target>` | Menjalankan enumerasi lengkap dengan informasi detail pada bagian yang mendukungnya. | `enum4linux -a -d 192.168.1.10` |
| `enum4linux -a -r <target>` | Menjalankan enumerasi lengkap sekaligus RID cycling. | `enum4linux -a -r 192.168.1.10` |
| `enum4linux -a -o <target>` | Menjalankan enumerasi lengkap dan meminta informasi OS. | `enum4linux -a -o 192.168.1.10` |
| `enum4linux -a -n <target>` | Menjalankan enumerasi lengkap dan NetBIOS lookup. | `enum4linux -a -n 192.168.1.10` |
| `enum4linux -a -i <target>` | Menjalankan enumerasi lengkap dan informasi printer. | `enum4linux -a -i 192.168.1.10` |
| `enum4linux -a -U -S -G -P <target>` | Menjalankan beberapa pemeriksaan utama secara eksplisit: user, share, group, dan password policy. | `enum4linux -U -S -G -P 192.168.1.10` |
| `enum4linux -U -M -S -P -G <target>` | Menjalankan enumerasi user, machine, share, password policy, dan group secara eksplisit. | `enum4linux -U -M -S -P -G 192.168.1.10` |
