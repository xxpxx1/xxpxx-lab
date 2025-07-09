# 🐞 XSS Disamarkan - Writeup

## 🎯 Target
Sistem disamarkan demi etika.

## 🔍 Bug Type
**Reflected XSS** pada parameter input tertentu.

## 🔬 Bukti Konsep
```http
GET /search?query=<script>alert(document.domain)</script>
```

Respon server menyisipkan input tanpa sanitasi → payload dieksekusi di browser korban.

## 🔧 Eksploitasi Lanjutan
- Bisa digunakan untuk mencuri cookie
- Redirection ke URL berbahaya
- Trigger phishing halaman login

## 🔐 Rekomendasi Perbaikan
- Escape semua input HTML
- Validasi parameter `query`

## 📅 Timeline
- Ditemukan: 8 Juli 2025
- Status: Disamarkan
