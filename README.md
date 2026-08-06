# Hosting Minecraft Terbaik!

Situs statis peringkat hosting Minecraft, siap di-deploy ke **GitHub Pages**.

## Struktur file

```
.
├── index.html   # Halaman utama (daftar peringkat)
├── login.html   # Halaman "login" (tampilan saja, tanpa autentikasi nyata)
└── README.md
```

## Cara publikasi ke GitHub Pages

1. **Buat repository baru** di GitHub (public), misalnya `hosting-minecraft`.
2. **Upload semua file** di folder ini ke repository tersebut:
   - Bisa lewat web GitHub (tombol "Add file" → "Upload files"), atau
   - Lewat git:
     ```bash
     git init
     git add .
     git commit -m "Initial commit"
     git branch -M main
     git remote add origin https://github.com/USERNAME/hosting-minecraft.git
     git push -u origin main
     ```
3. Buka repository di GitHub → **Settings** → **Pages** (menu kiri).
4. Pada bagian **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main**, folder **/ (root)**
   - Klik **Save**.
5. Tunggu 1–2 menit, lalu situs bisa diakses di:
   ```
   https://USERNAME.github.io/hosting-minecraft/
   ```
   (ganti `USERNAME` dan `hosting-minecraft` sesuai akun/nama repo Anda)

## Catatan

- Situs ini murni **statis** (HTML + CSS + sedikit JS), tidak butuh proses build apa pun — cocok untuk GitHub Pages.
- Tombol **"Keluar (Logout)"** di `index.html` mengarah ke `login.html`. Halaman login ini hanya tampilan; karena GitHub Pages tidak punya server/database, tidak ada verifikasi username/password yang sesungguhnya. Jika nanti butuh login sungguhan, perlu layanan pihak ketiga (mis. Firebase Auth, Auth0) atau backend terpisah.
- Semua link penyedia hosting bersifat eksternal dan dibuka di tab baru (`target="_blank"`), sudah dilengkapi `rel="noopener noreferrer"` untuk keamanan.
