# 🕌 Asmaul Husna API  

[![](https://data.jsdelivr.com/v1/package/gh/wnr-code/asmaul_husna/badge)](https://www.jsdelivr.com/package/gh/wnr-code/asmaul_husna)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Version v1](https://img.shields.io/badge/API-v1-blue)
![Version v2](https://img.shields.io/badge/API-v2-green)

> 99 Nama-nama Allah yang indah dengan terjemahan, makna, faedah, dan referensinya.  
> Disusun oleh **WNR Code** — versi publik API: [`v1.quran.wnr.app`](https://v1.quran.wnr.app)

📘 **Dokumen Lengkap API Publik:** [https://v1.quran.wnr.app/docs](https://v1.quran.wnr.app/docs)

---

## 📖 Tentang Proyek

**Asmaul Husna API** adalah dataset terbuka berisi **99 nama Allah (Asmaul Husna)** dalam bahasa Arab, Latin, Inggris, dan Indonesia — lengkap dengan **makna, faedah, amalan, dan referensi Al-Qur'an**.

Proyek ini tersedia dalam **dua versi data JSON**, disesuaikan untuk kebutuhan ringan maupun lengkap:

| Versi | Deskripsi | Lokasi File (CDN) |
|--------|------------|------------------|
| **v1** | Versi **ringkas**, hanya berisi `id`, `arabic`, `latin`, `en`, dan `idn`. | [v1/asmaul_husna.json](https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/v1/asmaul_husna.json) |
| **v2** | Versi **lengkap**, berisi juga `makna`, `faedah`, `amalan`, dan `referensi` ayat Al-Qur’an. | [v2/asmaul_husna.json](https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/v2/asmaul_husna.json) |

---

## 🧩 Metadata

| Atribut | Nilai |
|----------|--------|
| **Title** | Asmaul Husna |
| **Versi Terbaru** | 2.0.0 |
| **Format** | JSON |
| **Total Items** | 99 |
| **License** | [MIT License](LICENSE) |
| **Language** | Arabic → Indonesian (+ English) |
| **Maintainer** | WNR Code |
| **Source Repo** | [github.com/wnr-code/asmaul_husna](https://github.com/wnr-code/asmaul_husna) |
| **CDN (jsDelivr)** | [jsDelivr Package](https://www.jsdelivr.com/package/gh/wnr-code/asmaul_husna) |
| **Generator** | Gemini & GPT |
| **Created At** | 2025-10-20 |
| **Last Updated** | 2025-10-22 |

---

## 🚀 Endpoint API Publik

Gunakan API ini jika ingin mengakses data Asmaul Husna dengan parameter dan pencarian.

```bash
https://v1.quran.wnr.app/api/asmaulhusna
```

🧭 **Dokumentasi Lengkap:** [https://v1.quran.wnr.app/docs](https://v1.quran.wnr.app/docs)

---

## 📦 Akses File JSON Langsung (CDN)

> Cocok jika kamu hanya butuh dataset mentah tanpa server API.

### 🔹 Versi 1 (Ringkas)
```bash
https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/v1/asmaul_husna.json
```

**Contoh Respons:**
```json
{
  "meta": {
    "version": "1.0.0",
    "total_items": 99
  },
  "asmaul_husna": [
    {
      "id": 1,
      "arabic": "ٱلرَّحْمَـٰنُ",
      "latin": "Ar-Rahmaan",
      "en": "The Most Compassionate",
      "idn": "Yang Maha Pengasih"
    }
  ]
}
```

---

### 🔹 Versi 2 (Lengkap)
```bash
https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/v2/asmaul_husna.json
```

**Contoh Respons:**
```json
{
  "meta": {
    "version": "2.0.0",
    "total_items": 99
  },
  "asmaul_husna": [
    {
      "id": 1,
      "arabic": "ٱلرَّحْمَـٰنُ",
      "latin": "Ar-Rahmaan",
      "en": "The Most Compassionate",
      "idn": "Yang Maha Pengasih",
      "faedah": {
        "makna": "Kasih sayang Allah yang luas mencakup semua makhluk.",
        "amalan": "Berdoa dan berzikir dengan menyebut Ar-Rahmaan.",
        "referensi": [
          "QS. Al-Fatihah: 3",
          "QS. Maryam: 96"
        ]
      }
    }
  ]
}
```

---

## ⚙️ Integrasi Cepat

### 🔸 JavaScript
```js
fetch("https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/v1/asmaul_husna.json")
  .then(res => res.json())
  .then(data => console.log(data.asmaul_husna));
```

### 🔸 Node.js (Axios)
```js
import axios from "axios";

const res = await axios.get("https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/v2/asmaul_husna.json");
console.log(res.data.asmaul_husna[0]);
```

### 🔸 curl
```bash
curl https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/v2/asmaul_husna.json
```

---

## 💡 Contoh di Website

```html
<ul id="asmaul-husna"></ul>

<script>
  fetch("https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/v1/asmaul_husna.json")
    .then(res => res.json())
    .then(data => {
      const list = document.getElementById("asmaul-husna");
      data.asmaul_husna.forEach(item => {
        const li = document.createElement("li");
        li.innerHTML = `<b>${item.arabic}</b> — ${item.idn} (${item.latin})`;
        list.appendChild(li);
      });
    });
</script>
```

---

## 🧾 Lisensi

Proyek ini dirilis di bawah lisensi **[MIT License](LICENSE)**.  
Kamu bebas menggunakan, menyalin, atau memodifikasi selama mencantumkan atribusi ke:

> © 2025 [WNR Code](https://github.com/wnr-code)

---

## 💬 Kontribusi

Kontribusi sangat diterima!  
Kalau kamu menemukan kesalahan atau ingin menambah fitur baru:

1. Fork repositori ini.  
2. Edit file JSON di folder `v1` atau `v2`.  
3. Kirim *Pull Request*.  

---

## ✨ Kredit

* **Data Source:** WNR Code  
* **Generator:** GPT AI  
* **API Host:** [v1.quran.wnr.app](https://v1.quran.wnr.app)  
* **Dokumentasi Publik:** [v1.quran.wnr.app/docs](https://v1.quran.wnr.app/docs)  
* **Kontributor:** Komunitas Pengembang Muslim 🌙  

---

> *"Dan Allah memiliki Asmaul Husna, maka bermohonlah kepada-Nya dengan menyebut Asmaul Husna itu."*  
> **— QS. Al-A’raf: 180**
