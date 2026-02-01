# 🚀 [Project Name]

<!-- Ganti badge sesuai dengan teknologi yang digunakan -->
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vue.js&logoColor=4FC08D)

<!-- Tambahkan screenshot atau demo GIF di sini -->
<div align="center">
  <img src="docs/screenshots/demo.gif" alt="Demo" width="800"/>
</div>

## 📝 Overview

[Deskripsi singkat tentang project - 2-3 kalimat yang menjelaskan apa fungsi utama aplikasi ini]

Contoh:
> **EKuasa** adalah sistem pengajuan surat kuasa secara online yang memudahkan proses administrasi. Sistem ini dilengkapi dengan fitur verifikasi admin, notifikasi WhatsApp otomatis, dan generate PDF dengan barcode untuk validasi dokumen.

## ✨ Key Features

- 🔐 **User Authentication** - Sistem login dan registrasi dengan validasi
- 📄 **PDF Generation** - Generate dokumen PDF dengan barcode otomatis
- 📱 **WhatsApp Integration** - Notifikasi otomatis via WhatsApp API
- ✅ **Admin Verification** - Sistem approval untuk validasi surat kuasa
- 🗂️ **Document Management** - Pengelolaan dokumen dengan kategori
- 📊 **Dashboard Analytics** - Statistik dan laporan real-time
- 🔍 **Search & Filter** - Pencarian dan filter data yang powerful
- 📱 **Responsive Design** - Tampilan optimal di semua perangkat

## 🛠️ Tech Stack

### Backend
- **PHP** 8.1+
- **Laravel** 10.x
- **MySQL** 8.0+

### Frontend
- **Vue.js** 3.x
- **Bootstrap** 5.x
- **JavaScript** ES6+

### Libraries & Tools
- **WhatsApp API** - Untuk notifikasi
- **DomPDF** - PDF generation
- **Barcode Generator** - Generate barcode
- **Laravel Sanctum** - API authentication
- **Laravel Excel** - Export data ke Excel

## 📋 Prerequisites

Sebelum menjalankan project ini, pastikan Anda telah menginstall:

- PHP >= 8.1
- Composer
- MySQL >= 8.0
- Node.js >= 16.x
- NPM atau Yarn

## 🚀 Installation

### 1. Clone Repository

```bash
git clone https://github.com/IdhamIKN/project-name.git
cd project-name
```

### 2. Install Dependencies

```bash
# Install PHP dependencies
composer install

# Install Node.js dependencies
npm install
# atau
yarn install
```

### 3. Environment Setup

```bash
# Copy file .env.example
cp .env.example .env

# Generate application key
php artisan key:generate
```

### 4. Database Configuration

Edit file `.env` dan sesuaikan konfigurasi database:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nama_database
DB_USERNAME=root
DB_PASSWORD=
```

### 5. Run Migrations

```bash
# Jalankan migration
php artisan migrate

# Jalankan seeder (optional)
php artisan db:seed
```

### 6. Build Assets

```bash
# Development
npm run dev

# Production
npm run build
```

### 7. Run Application

```bash
# Start Laravel development server
php artisan serve

# Aplikasi akan berjalan di http://localhost:8000
```

## 📸 Screenshots

<div align="center">

### Dashboard
<img src="docs/screenshots/dashboard.png" alt="Dashboard" width="700"/>

### Form Submission
<img src="docs/screenshots/form.png" alt="Form" width="700"/>

### PDF Document
<img src="docs/screenshots/pdf.png" alt="PDF" width="700"/>

</div>

## 🔧 Configuration

### WhatsApp API Setup

1. Dapatkan API Key dari provider WhatsApp API
2. Tambahkan ke file `.env`:

```env
WHATSAPP_API_URL=https://api.whatsapp.com
WHATSAPP_API_KEY=your_api_key_here
WHATSAPP_PHONE_NUMBER=6281234567890
```

### PDF Configuration

Edit `config/dompdf.php` untuk kustomisasi PDF:

```php
'orientation' => 'portrait',
'paper' => 'a4',
'font_dir' => storage_path('fonts/'),
```

## 📖 API Documentation

### Authentication

```http
POST /api/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "password"
}
```

### Create Document

```http
POST /api/documents
Authorization: Bearer {token}
Content-Type: application/json

{
  "title": "Surat Kuasa",
  "content": "...",
  "type": "power_of_attorney"
}
```

### Get All Documents

```http
GET /api/documents
Authorization: Bearer {token}
```

## 🧪 Testing

```bash
# Run all tests
php artisan test

# Run specific test
php artisan test --filter=DocumentTest

# Run with coverage
php artisan test --coverage
```

## 📁 Project Structure

```
project-name/
├── app/
│   ├── Http/
│   │   ├── Controllers/    # Controllers
│   │   └── Middleware/     # Middleware
│   ├── Models/             # Eloquent models
│   └── Services/           # Business logic
├── database/
│   ├── migrations/         # Database migrations
│   └── seeders/            # Database seeders
├── resources/
│   ├── js/                 # Vue.js components
│   ├── css/                # Stylesheets
│   └── views/              # Blade templates
├── routes/
│   ├── web.php            # Web routes
│   └── api.php            # API routes
└── public/                 # Public assets
```

## 🤝 Contributing

Kontribusi sangat diterima! Berikut cara berkontribusi:

1. Fork repository ini
2. Buat branch feature (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

## 📝 Changelog

### v1.0.0 (2024-01-01)
- ✨ Initial release
- ✅ Basic CRUD operations
- ✅ WhatsApp integration
- ✅ PDF generation

### v1.1.0 (2024-02-01)
- ✨ Add barcode feature
- 🐛 Fix authentication bugs
- 📈 Improve performance

## 🐛 Known Issues

- [ ] Issue #1: Description
- [ ] Issue #2: Description

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Idham Kohar Nazarudin**

- LinkedIn: [@idham-kohar](https://linkedin.com/in/idham-kohar)
- GitHub: [@IdhamIKN](https://github.com/IdhamIKN)
- Email: idhamkohar361@gmail.com

## 🙏 Acknowledgments

- [Laravel](https://laravel.com) - The PHP Framework
- [Vue.js](https://vuejs.org) - The Progressive JavaScript Framework
- [Bootstrap](https://getbootstrap.com) - CSS Framework
- Terima kasih kepada semua kontributor!

## 📞 Support

Jika Anda menemukan bug atau memiliki pertanyaan, silakan buat [Issue](https://github.com/IdhamIKN/project-name/issues) atau hubungi saya melalui:

- Email: idhamkohar361@gmail.com
- WhatsApp: [+62 896-1861-9880](https://wa.me/6289618619880)

---

<div align="center">
  Made with ❤️ by Idham Kohar Nazarudin
  
  ⭐ Star this repo if you find it helpful!
</div>