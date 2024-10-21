# auto-deploy-unichain

Hi, saya membuat ini dengan segala yang saya bisa, maka dari itu jangan di-rename ya!  
**auto-deploy-unichain_sepolia**  
Khusus pengguna Termux, bisa scroll sampai bawah jika terjadi gagal saat instalasi dan run.

Selamat datang di repositori Bactiar291! 🎉

## Tentang Proyek Ini
Proyek ini dibuat oleh Bactiar291 untuk tujuan **[memudahkan pengguna]**.  
Proyek ini bertujuan untuk memudahkan pengguna yang menggunakan **[layanan ini]**.

Jika Anda meng-clone atau fork repositori ini, pastikan untuk membaca instruksi di bawah ini untuk memulai.

## Cara Menggunakan
1. Clone repositori ini ke mesin lokal Anda:
    ```bash
    git clone https://github.com/bactiar291/auto-deploy-unichain.git
    ```

2. Salin perintah di bawah ini untuk masuk ke folder:
    ```bash
    cd auto-deploy-unichain
    ```

3. Untuk meng-install dependencies secara manual (jika diperlukan), jalankan perintah berikut:
    ```bash
    pip install -r requirements.txt
    ```

4. Jangan lupa untuk mengganti variabel di file `.env`:
    ```bash
    nano .env
    ```
    Isi **Alamat Address** dan **Private Key** seperti ini:

    ```
    INFURA_URL=INI JANGAN DIUBAH! SUDAH SESUAI DENGAN RPL UNI SEPOLNYA
    SENDER_ADDRESS=PASTE_ALAMAT_ADDRESS_KAMU_DISINI
    PRIVATE_KEY=PASTE_PRIVATE_KEY_KAMU_DISINI
    ```

6. Untuk menjalankan dependencies:
    ```bash
    python3 unichain_sepolia.py
    ```

## Khusus Pengguna Termux
Jika Anda gagal menjalankan cara di atas di Termux, ikuti langkah berikut ini:

1. Masuk ke mode proot distro Ubuntu:
    ```bash
    pkg install proot
    pkg install openssh
    pkg install git
    curl -L -o proot_5.1.107-52_aarch64.deb https://github.com/SukunDev/termux-proot/raw/main/proot_5.1.107-52_aarch64.deb
    dpkg -i proot_5.1.107-52_aarch64.deb
    pkg install -y proot-distro
    proot-distro install ubuntu
    proot-distro login ubuntu
    ```

2. Masuk ke mode venv:
    ```bash
    apt update && apt upgrade
    apt install python3-pip
    pip install --upgrade pip==24.2
    apt install python3-venv
    python3 -m venv myenv
    source myenv/bin/activate
    pip install --upgrade pip setuptools
    ```

    (Jika ada pilihan zona, pilih angka 5 yaitu Asia dan 35 untuk waktu area Jakarta, selanjutnya klik Y dan enter untuk melanjutkan.)

3. Jika sudah masuk, langsung clone repositori dari GitHub di atas dan ikuti langkah-langkah sebelumnya.

## Kontribusi
Kontribusi sangat dihargai! Jika Anda memiliki ide, saran, atau menemukan bug, jangan ragu untuk membuat issue atau pull request.

## Lisensi
Proyek ini menggunakan lisensi **[MIT]**. Silakan baca file LICENSE untuk informasi lebih lanjut.

## Dibuat oleh Bactiar291
Terima kasih telah berkunjung ke repositori saya! 🚀
