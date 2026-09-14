# 🚀 Belajar Git untuk Persiapan PBL (Project Based Learning)

Selamat datang di panduan **Belajar Git**! Panduan ini dirancang khusus agar **pemula (beginner-friendly)** dapat memahami konsep dasar perversi kode (version control) menggunakan Git dan GitHub secara cepat dan mudah.

---

## 📌 Mengapa Belajar Git?

Saat mengerjakan proyek tim (seperti **PBL / Pemrograman Web**), kita sering perlu berbagi kode, menggabungkan fitur baru, atau mengembalikan kode jika ada error. Git membantu kita mencatat setiap riwayat perubahan kode tanpa perlu membuat folder backup manual seperti `project_v1`, `project_v2_final`, dst.

---

## 🧩 3 Perintah Utama yang Wajib Dikuasai

### 1. 📥 `git clone` (Mengunduh Repository)
* **Apa itu?**  
  `git clone` digunakan untuk mendownload/menyalin seluruh isi repository remote (yang ada di GitHub) ke dalam komputer lokal kamu untuk pertama kali.
* **Kapan digunakan?**  
  Saat kamu baru mulai bergabung ke dalam tim PBL atau ingin mengambil sampel proyek dari GitHub ke laptop kamu.
* **Cara Menggunakannya:**
  1. Buka terminal (VS Code / Git Bash / Command Prompt).
  2. Jalankan perintah berikut:
     ```bash
     git clone https://github.com/username/nama-repository.git
     ```
  3. Masuk ke folder repository yang baru di-download:
     ```bash
     cd nama-repository
     ```

---

### 2. 🔄 `git pull` (Mengambil Update Terbaru)
* **Apa itu?**  
  `git pull` digunakan untuk mengambil (fetch) dan menggabungkan (merge) perubahan terbaru dari GitHub ke dalam laptop kamu.
* **Kapan digunakan?**  
  **Selalu jalankan `git pull` sebelum kamu mulai koding** agar kode di laptopmu selalu sinkron dengan kode terbaru dari teman satu timmu.
* **Cara Menggunakannya:**
  ```bash
  git pull origin main
  ```
  *(Catatan: ganti `main` dengan nama branch utama kamu jika berbeda, misalnya `master`).*

---

### 3. 📤 `git push` (Mengirim Perubahan ke GitHub)
* **Apa itu?**  
  `git push` digunakan untuk mengunggah (upload) commit/perubahan yang sudah kamu buat dari komputer lokal ke repository online di GitHub.
* **Kapan digunakan?**  
  Setelah kamu selesai membuat fitur baru, memperbaiki bug, dan sudah melakukan `git add` & `git commit`.

---

## 💡 Alur Kerja Harian (Workflow Git)

Sebelum melakukan `git push`, ada alur standard (3 langkah) yang wajib kamu lalui:

```mermaid
graph LR
    A[Edit Kode] --> B[git add .]
    B --> C[git commit -m "..."]
    C --> D[git push]
```

### Langkah-demi-Langkah:

1. **Cek Status Perubahan**  
   Untuk melihat file apa saja yang baru ditambah atau diubah:
   ```bash
   git status
   ```

2. **Tandai File yang Ingin Disimpan (`git add`)**  
   Gunakan titik (`.`) untuk menandai semua file yang telah diubah:
   ```bash
   git add .
   ```

3. **Simpan Perubahan ke Catatan Git (`git commit`)**  
   Berikan deskripsi pesan commit yang jelas mengenai apa yang kamu kerjakan:
   ```bash
   git commit -m "feat: menambahkan halaman utama index.html"
   ```

4. **Kirim Perubahan ke GitHub (`git push`)**  
   Unggah hasil kerjaan kamu ke GitHub agar bisa dilihat oleh tim:
   ```bash
   git push origin main
   ```

---

## 🛠️ Cheatsheet Perintah Berguna Lainnya

| Perintah | Kegunaan |
| :--- | :--- |
| `git status` | Melihat status file (apakah ada perubahan yang belum di-commit) |
| `git log --oneline` | Melihat riwayat commit secara singkat |
| `git config --list` | Melihat konfigurasi nama dan email Git kamu |

---

## 🎯 Tips Penting untuk Tim PBL
> [!TIP]
> **Kebiasaan Baik Pengguna Git:**
> 1. **Pull Dulu Sebelum Koding**: Selalu jalankan `git pull origin main` setiap hari sebelum mulai ngetik kode baru.
> 2. **Pesan Commit Jelas**: Tulis pesan commit yang mendeskripsikan perubahan dengan singkat dan jelas.
> 3. **Push Secara Berkala**: Jangan menunda push sampai kodingan terlalu banyak agar menghindari *merge conflict* dengan teman tim.