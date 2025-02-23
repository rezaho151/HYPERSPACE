# HYPERSPACE

# 🚀 Hyperspace AI Node Setup (Linux VPS)
 
Panduan ini menjelaskan cara mengatur node Hyperspace AI di VPS menggunakan CLI.
 
## 🔧 Instalasi
 `curl https://download.hyper.space/api/install | bash   source /root/.bashrc ` 
## ▶️ Menjalankan Node
 `screen -S hyperspace   aios-cli start ` 
Untuk keluar tanpa menghentikan proses: `CTRL+A+D`
 
Untuk kembali ke layar:
 `screen -r hyperspace ` 
## ⚙️ Konfigurasi Node
 
### Download model yang diperlukan
 `aios-cli models add hf:TheBloke/phi-2-GGUF:phi-2.Q4_K_M.gguf ` 
### Import private key
 `nano my.pem  # Tambahkan private key aios-cli hive import-keys ./my.pem   aios-cli hive login   ` 
### Hubungkan node ke Hive
 `aios-cli hive connect   aios-cli hive select-tier 5  # Upgrade ke Tier-3 untuk 2x poin ` 
## 📊 Cek Poin
 `aios-cli hive points ` 
## 🔄 Perintah Berguna
 `aios-cli start --connect  # Shortcut untuk Start, Login, dan Connect   aios-cli version  # Update node   aios-cli kill  # Stop node `
