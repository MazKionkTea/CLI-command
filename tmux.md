#  tmux

| Perintah | Deskripsi | Contoh |
|---|---|---|
| `tmux` | Membuka sesi tmux baru | `tmux` |
| `tmux new -s nama` | Membuat sesi baru dengan nama tertentu | `tmux new -s kerja` |
| `tmux new-session -s nama` | Membuat sesi baru | `tmux new-session -s dev` |
| `tmux ls` | Melihat daftar sesi tmux | `tmux ls` |
| `tmux list-sessions` | Melihat semua sesi | `tmux list-sessions` |
| `tmux attach -t nama` | Masuk kembali ke sesi tertentu | `tmux attach -t kerja` |
| `tmux attach` | Masuk ke sesi terakhir | `tmux attach` |
| `tmux switch-client -t nama` | Berpindah sesi dari dalam tmux | `tmux switch-client -t dev` |
| `tmux has-session -t nama` | Mengecek apakah sesi tersedia | `tmux has-session -t dev` |
| `tmux kill-session -t nama` | Menghapus sesi tertentu | `tmux kill-session -t kerja` |
| `tmux kill-server` | Menghapus semua sesi tmux | `tmux kill-server` |
| `tmux rename-session -t lama baru` | Mengganti nama sesi | `tmux rename-session -t kerja proyek` |
| `tmux detach-client` | Melepaskan client dari sesi | `tmux detach-client -s dev` |

### Shortcut Dasar tmux
| Shortcut | Deskripsi | Contoh |
|---|---|---|
| `Ctrl+b d` | Keluar dari sesi tanpa menghentikan proses (detach) | `Ctrl+b` lalu `d` |
| `Ctrl+b c` | Membuat window baru | `Ctrl+b` lalu `c` |
| `Ctrl+b n` | Pindah ke window berikutnya | `Ctrl+b` lalu `n` |
| `Ctrl+b p` | Pindah ke window sebelumnya | `Ctrl+b` lalu `p` |
| `Ctrl+b 0-9` | Pindah ke window berdasarkan nomor | `Ctrl+b` lalu `1` |
| `Ctrl+b ,` | Mengganti nama window aktif | `Ctrl+b` lalu `,` |
| `Ctrl+b w` | Melihat daftar window | `Ctrl+b` lalu `w` |
| `Ctrl+b &` | Menutup window aktif | `Ctrl+b` lalu `&` |
| `Ctrl+b s` | Melihat dan memilih sesi | `Ctrl+b` lalu `s` |
| `Ctrl+b l` | Kembali ke sesi terakhir | `Ctrl+b` lalu `l` |
| `Ctrl+b $` | Mengganti nama sesi | `Ctrl+b` lalu `$` |

### Window tmux
| Perintah | Deskripsi | Contoh |
|---|---|---|
| `tmux new-window` | Membuat window baru | `tmux new-window` |
| `tmux new-window -n nama` | Membuat window dengan nama | `tmux new-window -n editor` |
| `tmux list-windows` | Melihat daftar window | `tmux list-windows` |
| `tmux rename-window nama` | Mengganti nama window | `tmux rename-window server` |
| `tmux select-window -t nomor` | Memilih window tertentu | `tmux select-window -t 2` |
| `tmux kill-window` | Menghapus window aktif | `tmux kill-window` |
| `Ctrl+b f` | Mencari window berdasarkan nama | `Ctrl+b` lalu `f` |
| `Ctrl+b .` | Memindahkan window ke nomor lain | `Ctrl+b` lalu `.` |

### Panel (Pane) tmux
| Perintah | Deskripsi | Contoh |
|---|---|---|
| `Ctrl+b %` | Membagi panel vertikal | `Ctrl+b` lalu `%` |
| `Ctrl+b "` | Membagi panel horizontal | `Ctrl+b` lalu `"` |
| `tmux split-window -h` | Membagi panel kiri-kanan | `tmux split-window -h` |
| `tmux split-window -v` | Membagi panel atas-bawah | `tmux split-window -v` |
| `Ctrl+b arah` | Berpindah antar panel | `Ctrl+b` lalu `←` |
| `tmux select-pane -L/R/U/D` | Memilih panel berdasarkan arah | `tmux select-pane -L` |
| `tmux list-panes` | Melihat daftar panel | `tmux list-panes` |
| `Ctrl+b x` | Menutup panel aktif | `Ctrl+b` lalu `x` |
| `Ctrl+b z` | Membesarkan panel aktif | `Ctrl+b` lalu `z` |
| `tmux kill-pane` | Menghapus panel aktif | `tmux kill-pane` |
| `tmux resize-pane -L angka` | Memperbesar panel ke kiri | `tmux resize-pane -L 10` |
| `tmux resize-pane -R angka` | Memperbesar panel ke kanan | `tmux resize-pane -R 10` |
| `tmux resize-pane -U angka` | Memperbesar panel ke atas | `tmux resize-pane -U 5` |
| `tmux resize-pane -D angka` | Memperbesar panel ke bawah | `tmux resize-pane -D 5` |
| `tmux swap-pane -D` | Menukar panel ke bawah | `tmux swap-pane -D` |
| `tmux swap-pane -U` | Menukar panel ke atas | `tmux swap-pane -U` |
| `Ctrl+b Space` | Mengganti layout panel | `Ctrl+b` lalu `Space` |
| `Ctrl+b !` | Mengubah panel menjadi window baru | `Ctrl+b` lalu `!` |
| `Ctrl+b {` | Memindahkan panel ke kiri | `Ctrl+b` lalu `{` |
| `Ctrl+b }` | Memindahkan panel ke kanan | `Ctrl+b` lalu `}` |

### Copy Mode dan Buffer
| Perintah | Deskripsi | Contoh |
|---|---|---|
| `Ctrl+b [` | Masuk mode scroll/copy | `Ctrl+b` lalu `[` |
| `Ctrl+b ]` | Paste teks buffer | `Ctrl+b` lalu `]` |
| `tmux capture-pane -p` | Mengambil isi terminal | `tmux capture-pane -p` |
| `tmux save-buffer file.txt` | Menyimpan buffer ke file | `tmux save-buffer output.txt` |
| `tmux load-buffer file.txt` | Memuat buffer dari file | `tmux load-buffer output.txt` |
| `tmux paste-buffer` | Menempelkan buffer | `tmux paste-buffer` |

### Command Mode
| Shortcut | Deskripsi | Contoh |
|---|---|---|
| `Ctrl+b :` | Membuka command mode | `Ctrl+b` lalu `:` |
| `Ctrl+b q` | Menampilkan nomor panel | `Ctrl+b` lalu `q` |
| `Ctrl+b t` | Menampilkan jam | `Ctrl+b` lalu `t` |

### Konfigurasi ~/.tmux.conf
| Konfigurasi | Deskripsi | Contoh |
|---|---|---|
| `set -g mouse on` | Mengaktifkan mouse | `set -g mouse on` |
| `set -g history-limit angka` | Mengatur jumlah history | `set -g history-limit 10000` |
| `set -g base-index 1` | Nomor window mulai dari 1 | `set -g base-index 1` |
| `set -g pane-base-index 1` | Nomor panel mulai dari 1 | `set -g pane-base-index 1` |
| `setw -g mode-keys vi` | Menggunakan mode Vim | `setw -g mode-keys vi` |
| `set -g status off` | Menyembunyikan status bar | `set -g status off` |
| `tmux source-file ~/.tmux.conf` | Memuat ulang konfigurasi | `tmux source-file ~/.tmux.conf` |

### Perintah Keluar
| Perintah | Deskripsi | Contoh |
|---|---|---|
| `exit` | Keluar dari shell/panel aktif | `exit` |
| `Ctrl+d` | Keluar dari shell aktif | `Ctrl+d` |
