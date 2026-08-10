# docker

| Command | Deskripsi | Contoh |
|---|---|---|
| `docker` | Menjalankan Docker CLI | `docker --help` |
| `docker --help` | Menampilkan bantuan Docker CLI | `docker --help` |
| `docker version` | Menampilkan versi Docker Client dan Server | `docker version` |
| `docker info` | Menampilkan informasi sistem Docker | `docker info` |
| `docker inspect` | Menampilkan informasi detail objek Docker | `docker inspect nginx` |
| `docker login` | Login ke container registry | `docker login` |
| `docker logout` | Logout dari container registry | `docker logout` |
| `docker search` | Mencari image di registry | `docker search nginx` |
| `docker pull` | Mengunduh image dari registry | `docker pull nginx:latest` |
| `docker push` | Mengunggah image ke registry | `docker push username/app:1.0` |
| `docker build` | Membuat image dari Dockerfile | `docker build -t myapp:1.0 .` |
| `docker run` | Membuat dan menjalankan container | `docker run -d --name web nginx` |
| `docker create` | Membuat container tanpa menjalankannya | `docker create --name web nginx` |
| `docker start` | Menjalankan container yang berhenti | `docker start web` |
| `docker stop` | Menghentikan container dengan graceful shutdown | `docker stop web` |
| `docker restart` | Me-restart container | `docker restart web` |
| `docker kill` | Menghentikan container secara paksa | `docker kill web` |
| `docker rm` | Menghapus container | `docker rm web` |
| `docker ps` | Menampilkan container yang sedang berjalan | `docker ps` |
| `docker ps -a` | Menampilkan semua container | `docker ps -a` |
| `docker exec` | Menjalankan command di dalam container | `docker exec -it web sh` |
| `docker logs` | Menampilkan log container | `docker logs web` |
| `docker attach` | Menghubungkan terminal ke proses utama container | `docker attach web` |
| `docker cp` | Menyalin file antara host dan container | `docker cp web:/app/log.txt .` |
| `docker top` | Menampilkan proses dalam container | `docker top web` |
| `docker stats` | Menampilkan penggunaan resource container | `docker stats` |
| `docker port` | Menampilkan mapping port container | `docker port web` |
| `docker rename` | Mengubah nama container | `docker rename web web-prod` |
| `docker pause` | Menjeda proses container | `docker pause web` |
| `docker unpause` | Melanjutkan container yang dijeda | `docker unpause web` |
| `docker wait` | Menunggu container berhenti dan menampilkan exit code | `docker wait web` |
| `docker commit` | Membuat image dari container | `docker commit web myapp:v2` |
| `docker diff` | Menampilkan perubahan filesystem container | `docker diff web` |
| `docker export` | Mengekspor filesystem container ke file tar | `docker export web > web.tar` |
| `docker update` | Mengubah konfigurasi resource container | `docker update --memory 512m web` |
| `docker container` | Management command untuk container | `docker container --help` |
| `docker container ls` | Menampilkan daftar container | `docker container ls -a` |
| `docker container create` | Membuat container | `docker container create nginx` |
| `docker container run` | Membuat dan menjalankan container | `docker container run -d nginx` |
| `docker container start` | Menjalankan container | `docker container start web` |
| `docker container stop` | Menghentikan container | `docker container stop web` |
| `docker container restart` | Me-restart container | `docker container restart web` |
| `docker container kill` | Menghentikan container secara paksa | `docker container kill web` |
| `docker container rm` | Menghapus container | `docker container rm web` |
| `docker container exec` | Menjalankan command dalam container | `docker container exec -it web bash` |
| `docker container logs` | Menampilkan log container | `docker container logs -f web` |
| `docker container inspect` | Menampilkan detail container | `docker container inspect web` |
| `docker container attach` | Attach ke container | `docker container attach web` |
| `docker container cp` | Menyalin file | `docker container cp web:/app/a.txt .` |
| `docker container diff` | Melihat perubahan filesystem | `docker container diff web` |
| `docker container export` | Mengekspor filesystem container | `docker container export web -o web.tar` |
| `docker container pause` | Pause container | `docker container pause web` |
| `docker container unpause` | Unpause container | `docker container unpause web` |
| `docker container port` | Melihat port mapping | `docker container port web` |
| `docker container rename` | Mengubah nama container | `docker container rename web frontend` |
| `docker container stats` | Melihat statistik resource | `docker container stats web` |
| `docker container top` | Melihat proses container | `docker container top web` |
| `docker container update` | Mengubah resource container | `docker container update --cpus 1 web` |
| `docker container wait` | Menunggu container berhenti | `docker container wait web` |
| `docker container prune` | Menghapus stopped container | `docker container prune` |
| `docker image` | Management command untuk image | `docker image --help` |
| `docker images` | Menampilkan daftar image | `docker images` |
| `docker image ls` | Menampilkan daftar image | `docker image ls` |
| `docker image pull` | Mengunduh image | `docker image pull nginx` |
| `docker image push` | Mengunggah image | `docker image push user/app:1.0` |
| `docker image build` | Membuat image dari Dockerfile | `docker image build -t app .` |
| `docker image rm` | Menghapus image | `docker image rm nginx` |
| `docker image inspect` | Melihat detail image | `docker image inspect nginx` |
| `docker image history` | Melihat history layer image | `docker image history nginx` |
| `docker image tag` | Memberikan tag pada image | `docker image tag app user/app:1.0` |
| `docker image save` | Menyimpan image ke file tar | `docker image save nginx -o nginx.tar` |
| `docker image load` | Memuat image dari file tar | `docker image load -i nginx.tar` |
| `docker image import` | Membuat image dari filesystem tar | `docker image import rootfs.tar myimage` |
| `docker image prune` | Menghapus image yang tidak digunakan | `docker image prune` |
| `docker network` | Management command untuk network | `docker network --help` |
| `docker network ls` | Menampilkan network | `docker network ls` |
| `docker network create` | Membuat network | `docker network create app-net` |
| `docker network inspect` | Melihat detail network | `docker network inspect app-net` |
| `docker network connect` | Menghubungkan container ke network | `docker network connect app-net web` |
| `docker network disconnect` | Memutus container dari network | `docker network disconnect app-net web` |
| `docker network rm` | Menghapus network | `docker network rm app-net` |
| `docker network prune` | Menghapus network yang tidak digunakan | `docker network prune` |
| `docker volume` | Management command untuk volume | `docker volume --help` |
| `docker volume ls` | Menampilkan volume | `docker volume ls` |
| `docker volume create` | Membuat volume | `docker volume create db-data` |
| `docker volume inspect` | Melihat detail volume | `docker volume inspect db-data` |
| `docker volume rm` | Menghapus volume | `docker volume rm db-data` |
| `docker volume prune` | Menghapus volume yang tidak digunakan | `docker volume prune` |
| `docker system` | Management command untuk sistem Docker | `docker system --help` |
| `docker system df` | Melihat penggunaan disk Docker | `docker system df` |
| `docker system events` | Melihat event Docker secara realtime | `docker system events` |
| `docker system info` | Menampilkan informasi sistem | `docker system info` |
| `docker system prune` | Membersihkan resource yang tidak digunakan | `docker system prune -a` |
| `docker builder` | Management command untuk builder | `docker builder --help` |
| `docker builder build` | Membuat image menggunakan builder | `docker builder build -t app .` |
| `docker builder prune` | Menghapus build cache | `docker builder prune` |
| `docker buildx` | Build menggunakan BuildKit | `docker buildx --help` |
| `docker buildx build` | Membuat image dengan BuildKit | `docker buildx build -t app .` |
| `docker buildx bake` | Menjalankan build berdasarkan konfigurasi | `docker buildx bake` |
| `docker buildx create` | Membuat builder instance | `docker buildx create --name mybuilder` |
| `docker buildx ls` | Menampilkan builder | `docker buildx ls` |
| `docker buildx inspect` | Melihat detail builder | `docker buildx inspect mybuilder` |
| `docker buildx use` | Memilih builder aktif | `docker buildx use mybuilder` |
| `docker buildx rm` | Menghapus builder | `docker buildx rm mybuilder` |
| `docker buildx stop` | Menghentikan builder | `docker buildx stop mybuilder` |
| `docker buildx prune` | Menghapus BuildKit cache | `docker buildx prune` |
| `docker buildx du` | Melihat penggunaan disk builder | `docker buildx du` |
| `docker buildx version` | Menampilkan versi Buildx | `docker buildx version` |
| `docker buildx imagetools` | Mengelola image manifest di registry | `docker buildx imagetools --help` |
| `docker buildx imagetools inspect` | Melihat manifest image | `docker buildx imagetools inspect nginx` |
| `docker context` | Mengelola Docker context | `docker context --help` |
| `docker context ls` | Menampilkan context | `docker context ls` |
| `docker context show` | Menampilkan context aktif | `docker context show` |
| `docker context use` | Mengganti context aktif | `docker context use production` |
| `docker context create` | Membuat context | `docker context create production --docker host=ssh://user@server` |
| `docker context inspect` | Melihat detail context | `docker context inspect production` |
| `docker context update` | Mengubah context | `docker context update production` |
| `docker context rm` | Menghapus context | `docker context rm production` |
| `docker context export` | Mengekspor context | `docker context export production -o production.dockercontext` |
| `docker context import` | Mengimpor context | `docker context import production production.dockercontext` |
| `docker compose` | Mengelola aplikasi multi-container | `docker compose --help` |
| `docker compose build` | Build service Compose | `docker compose build` |
| `docker compose up` | Membuat dan menjalankan service | `docker compose up -d` |
| `docker compose down` | Menghentikan dan menghapus resource Compose | `docker compose down` |
| `docker compose start` | Menjalankan service yang sudah ada | `docker compose start` |
| `docker compose stop` | Menghentikan service | `docker compose stop` |
| `docker compose restart` | Me-restart service | `docker compose restart web` |
| `docker compose run` | Menjalankan command sekali pada service | `docker compose run --rm web sh` |
| `docker compose exec` | Menjalankan command dalam service container | `docker compose exec web sh` |
| `docker compose logs` | Melihat log service | `docker compose logs -f web` |
| `docker compose ps` | Menampilkan container Compose | `docker compose ps` |
| `docker compose top` | Melihat proses service | `docker compose top` |
| `docker compose stats` | Melihat statistik resource service | `docker compose stats` |
| `docker compose cp` | Menyalin file service | `docker compose cp web:/app/a.txt .` |
| `docker compose rm` | Menghapus stopped service container | `docker compose rm` |
| `docker compose pause` | Pause service | `docker compose pause` |
| `docker compose unpause` | Unpause service | `docker compose unpause` |
| `docker compose config` | Memvalidasi dan menampilkan konfigurasi Compose | `docker compose config` |
| `docker compose convert` | Mengonversi konfigurasi Compose | `docker compose convert` |
| `docker compose commit` | Membuat image dari service container | `docker compose commit web app:snapshot` |
| `docker compose scale` | Mengatur jumlah instance service | `docker compose scale web=3` |
| `docker compose volumes` | Menampilkan volume project | `docker compose volumes` |
| `docker compose wait` | Menunggu service berhenti | `docker compose wait web` |
| `docker compose watch` | Memantau perubahan source | `docker compose watch` |
| `docker compose version` | Menampilkan versi Compose | `docker compose version` |
| `docker compose attach` | Attach ke container service | `docker compose attach web` |
| `docker swarm` | Mengelola Docker Swarm | `docker swarm --help` |
| `docker swarm init` | Membuat Swarm baru | `docker swarm init` |
| `docker swarm join` | Join node ke Swarm | `docker swarm join --token TOKEN IP:2377` |
| `docker swarm join-token` | Menampilkan join token | `docker swarm join-token worker` |
| `docker swarm leave` | Keluar dari Swarm | `docker swarm leave` |
| `docker swarm update` | Mengubah konfigurasi Swarm | `docker swarm update --autolock=true` |
| `docker swarm ca` | Melihat atau rotate root CA | `docker swarm ca` |
| `docker swarm unlock` | Membuka Swarm yang terkunci | `docker swarm unlock` |
| `docker swarm unlock-key` | Mengelola unlock key | `docker swarm unlock-key` |
| `docker node` | Mengelola node Swarm | `docker node --help` |
| `docker node ls` | Menampilkan node Swarm | `docker node ls` |
| `docker node inspect` | Melihat detail node | `docker node inspect node1` |
| `docker node ps` | Melihat task pada node | `docker node ps node1` |
| `docker node promote` | Mengubah worker menjadi manager | `docker node promote node1` |
| `docker node demote` | Mengubah manager menjadi worker | `docker node demote node1` |
| `docker node update` | Mengubah konfigurasi node | `docker node update --availability drain node1` |
| `docker node rm` | Menghapus node | `docker node rm node1` |
| `docker service` | Mengelola service Swarm | `docker service --help` |
| `docker service create` | Membuat service Swarm | `docker service create --name web nginx` |
| `docker service ls` | Menampilkan service | `docker service ls` |
| `docker service ps` | Menampilkan task service | `docker service ps web` |
| `docker service inspect` | Melihat detail service | `docker service inspect web` |
| `docker service logs` | Melihat log service | `docker service logs web` |
| `docker service scale` | Scale service | `docker service scale web=3` |
| `docker service update` | Mengubah konfigurasi service | `docker service update --image nginx:latest web` |
| `docker service rollback` | Rollback service | `docker service rollback web` |
| `docker service rm` | Menghapus service | `docker service rm web` |
| `docker stack` | Mengelola stack Swarm | `docker stack --help` |
| `docker stack deploy` | Deploy stack dari Compose file | `docker stack deploy -c compose.yml app` |
| `docker stack ls` | Menampilkan stack | `docker stack ls` |
| `docker stack ps` | Menampilkan task stack | `docker stack ps app` |
| `docker stack services` | Menampilkan service stack | `docker stack services app` |
| `docker stack config` | Menampilkan konfigurasi stack | `docker stack config -c compose.yml` |
| `docker stack rm` | Menghapus stack | `docker stack rm app` |
| `docker config` | Mengelola Swarm configs | `docker config --help` |
| `docker config create` | Membuat config Swarm | `docker config create nginx.conf nginx.conf` |
| `docker config ls` | Menampilkan config | `docker config ls` |
| `docker config inspect` | Melihat detail config | `docker config inspect nginx.conf` |
| `docker config rm` | Menghapus config | `docker config rm nginx.conf` |
| `docker secret` | Mengelola Swarm secrets | `docker secret --help` |
| `docker secret create` | Membuat secret Swarm | `docker secret create db_password password.txt` |
| `docker secret ls` | Menampilkan secret | `docker secret ls` |
| `docker secret inspect` | Melihat metadata secret | `docker secret inspect db_password` |
| `docker secret rm` | Menghapus secret | `docker secret rm db_password` |
| `docker plugin` | Mengelola Docker plugin | `docker plugin --help` |
| `docker plugin ls` | Menampilkan plugin | `docker plugin ls` |
| `docker plugin install` | Menginstal plugin | `docker plugin install PLUGIN` |
| `docker plugin create` | Membuat plugin | `docker plugin create myplugin ./plugin` |
| `docker plugin enable` | Mengaktifkan plugin | `docker plugin enable myplugin` |
| `docker plugin disable` | Menonaktifkan plugin | `docker plugin disable myplugin` |
| `docker plugin inspect` | Melihat detail plugin | `docker plugin inspect myplugin` |
| `docker plugin set` | Mengubah konfigurasi plugin | `docker plugin set myplugin key=value` |
| `docker plugin upgrade` | Upgrade plugin | `docker plugin upgrade myplugin` |
| `docker plugin push` | Push plugin ke registry | `docker plugin push user/myplugin` |
| `docker plugin rm` | Menghapus plugin | `docker plugin rm myplugin` |
| `docker manifest` | Mengelola image manifest | `docker manifest --help` |
| `docker manifest inspect` | Melihat manifest image | `docker manifest inspect nginx` |
| `docker manifest create` | Membuat manifest list | `docker manifest create user/app:latest user/app:amd64 user/app:arm64` |
| `docker manifest annotate` | Menambahkan informasi platform manifest | `docker manifest annotate user/app:latest user/app:arm64 --arch arm64` |
| `docker manifest push` | Push manifest list | `docker manifest push user/app:latest` |
| `docker manifest rm` | Menghapus manifest lokal | `docker manifest rm user/app:latest` |
| `docker trust` | Mengelola image signing | `docker trust --help` |
| `docker trust inspect` | Melihat signature image | `docker trust inspect user/app` |
| `docker trust sign` | Menandatangani image | `docker trust sign user/app:1.0` |
| `docker trust revoke` | Mencabut signature image | `docker trust revoke user/app:1.0` |
| `docker trust key` | Mengelola signing key | `docker trust key --help` |
| `docker trust key generate` | Membuat signing key | `docker trust key generate alice` |
| `docker trust key load` | Memuat private key | `docker trust key load key.pem` |
| `docker trust signer` | Mengelola signer | `docker trust signer --help` |
| `docker trust signer add` | Menambahkan signer | `docker trust signer add user/app alice` |
| `docker trust signer remove` | Menghapus signer | `docker trust signer remove user/app alice` |
| `docker checkpoint` | Mengelola checkpoint container | `docker checkpoint --help` |
| `docker checkpoint create` | Membuat checkpoint container | `docker checkpoint create web cp1` |
| `docker checkpoint ls` | Menampilkan checkpoint | `docker checkpoint ls web` |
| `docker checkpoint rm` | Menghapus checkpoint | `docker checkpoint rm web cp1` |
| `docker init` | Membuat file starter Docker untuk project | `docker init` |
| `docker debug` | Membuka environment debugging container/image | `docker debug web` |
| `docker desktop` | Mengontrol Docker Desktop melalui CLI | `docker desktop --help` |
| `docker desktop start` | Menjalankan Docker Desktop | `docker desktop start` |
| `docker desktop stop` | Menghentikan Docker Desktop | `docker desktop stop` |
| `docker desktop restart` | Me-restart Docker Desktop | `docker desktop restart` |
| `docker desktop status` | Melihat status Docker Desktop | `docker desktop status` |
| `docker desktop logs` | Melihat log Docker Desktop | `docker desktop logs` |
| `docker desktop diagnose` | Mendiagnosis masalah Docker Desktop | `docker desktop diagnose` |
| `docker desktop version` | Menampilkan versi Docker Desktop | `docker desktop version` |
| `docker desktop update` | Mengelola update Docker Desktop | `docker desktop update` |
| `docker model` | Mengelola Docker Model Runner | `docker model --help` |
| `docker model list` | Menampilkan model | `docker model list` |
| `docker model pull` | Mengunduh model | `docker model pull ai/model` |
| `docker model inspect` | Melihat detail model | `docker model inspect ai/model` |
| `docker model logs` | Melihat log Model Runner | `docker model logs` |
| `docker model run` | Menjalankan model | `docker model run ai/model` |
| `docker model bench` | Benchmark model | `docker model bench ai/model` |
| `docker model df` | Melihat penggunaan disk model | `docker model df` |
| `docker model gateway` | Menjalankan gateway model | `docker model gateway` |
| `docker model launch` | Menjalankan aplikasi model | `docker model launch` |
| `docker model package` | Membuat package model OCI | `docker model package ai/model` |
| `docker model install-runner` | Menginstal Model Runner | `docker model install-runner` |
| `docker scout` | Menganalisis keamanan dan supply chain image | `docker scout --help` |
| `docker scout cves` | Menampilkan CVE image | `docker scout cves nginx:latest` |
| `docker scout sbom` | Menampilkan SBOM image | `docker scout sbom nginx:latest` |
| `docker scout quickview` | Menampilkan ringkasan keamanan image | `docker scout quickview nginx:latest` |
| `docker scout recommendations` | Menampilkan rekomendasi base image | `docker scout recommendations nginx:latest` |
| `docker scout compare` | Membandingkan dua image | `docker scout compare user/app:1.0 --to user/app:2.0` |
| `docker scout push` | Mengirim image ke Docker Scout | `docker scout push user/app:latest` |
| `docker scout enroll` | Mendaftarkan organisasi ke Scout | `docker scout enroll` |
| `docker scout version` | Menampilkan versi Scout | `docker scout version` |
| `docker scout attestation` | Mengelola image attestation | `docker scout attestation --help` |
| `docker scout cache` | Mengelola cache Scout | `docker scout cache --help` |
| `docker scout config` | Mengelola konfigurasi Scout | `docker scout config --help` |
| `docker scout environment` | Mengelola environment Scout | `docker scout environment --help` |
| `docker scout integration` | Mengelola integrasi Scout | `docker scout integration list` |
| `docker scout policy` | Mengevaluasi security policy | `docker scout policy user/app:latest` |
| `docker scout repo` | Mengelola repository Scout | `docker scout repo list` |
| `docker scout stream` | Mengelola Scout stream | `docker scout stream --help` |
| `docker scout vex` | Mengelola VEX attestation | `docker scout vex get user/app:latest` |
| `docker scout watch` | Memantau repository registry | `docker scout watch user/app` |
