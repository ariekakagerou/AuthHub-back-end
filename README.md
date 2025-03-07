# AuthHub Backend

**AuthHub Backend** adalah API berbasis **Express.js** yang digunakan untuk mengelola profil pengguna secara aman dan efisien. API ini mendukung fitur **autentikasi JWT**, **interaksi dengan Firebase Firestore**, serta pengelolaan profil pengguna.

## 📌 Fitur Utama

✅ **Pengaturan Rute**  
API menyediakan beberapa endpoint utama:
- **GET /profile** → Mendapatkan profil pengguna.
- **POST /profile** → Membuat profil baru.
- **PUT /profile** → Memperbarui profil pengguna.
- **DELETE /profile** → Menghapus profil pengguna.

✅ **Autentikasi Token**  
- Setiap permintaan API harus menyertakan **token JWT** dalam header.
- Jika token tidak ada, API akan mengembalikan **401 Unauthorized**.

✅ **Verifikasi Token**  
- Token diverifikasi menggunakan **kunci rahasia** yang disimpan dalam variabel lingkungan.
- Jika valid, API akan memproses permintaan pengguna.

✅ **Interaksi dengan Firebase Firestore**  
- Data pengguna disimpan di **Firebase Firestore**.
- Setiap profil diidentifikasi berdasarkan **email pengguna**.

✅ **Respons API**  
- API mengembalikan **respons JSON** setelah setiap operasi berhasil.
- Status kode sesuai dengan hasil operasi (200, 201, 400, 401, 500, dll).

## 🚀 Teknologi yang Digunakan
- **Node.js** dengan **Express.js** sebagai framework backend.
- **Firebase Firestore** sebagai database penyimpanan data pengguna.
- **JWT (JSON Web Token)** untuk autentikasi pengguna.
- **dotenv** untuk mengelola variabel lingkungan.

## 🔧 Cara Menjalankan Backend
1. **Clone repository**:
   ```sh
   git clone https://github.com/username/authhub-backend.git
   cd authhub-backend
   ```
2. **Install dependencies**:
   ```sh
   npm install
   ```
3. **Buat file `.env`** dan isi dengan:
   ```env
   PORT=5000
   JWT_SECRET=your_jwt_secret
   FIREBASE_CONFIG=your_firebase_config
   ```
4. **Jalankan server**:
   ```sh
   npm start
   ```
5. **Backend berjalan di `http://localhost:5000`** 🎉

Dengan backend ini, **AuthHub** dapat memberikan pengalaman pengguna yang **mudah, aman, dan efisien** dalam mengelola akun mereka. 🚀

