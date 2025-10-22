

````markdown
# 🕌 Asmaul Husna API  
[![](https://data.jsdelivr.com/v1/package/gh/wnr-code/asmaul_husna/badge)](https://www.jsdelivr.com/package/gh/wnr-code/asmaul_husna)

> 99 Nama-nama Allah yang indah dengan terjemahan, makna, faedah, dan referensinya.  
> Disusun oleh **WNR Code** — versi publik API: [`v1.quran.wnr.app`](https://v1.quran.wnr.app)

---

## 📖 Tentang Proyek

**Asmaul Husna API** adalah dataset terbuka berisi **99 nama Allah (Asmaul Husna)** dalam bahasa Arab, Latin, Inggris, dan Indonesia — lengkap dengan **makna, faedah, amalan, dan referensi Al-Qur'an**.

Proyek ini dibuat agar dapat diakses oleh publik — baik untuk keperluan:
- Aplikasi Islami 📱  
- Website pembelajaran 🕋  
- Bot Telegram / Discord 🤖  
- Riset bahasa Arab atau tafsir Al-Qur’an 📚  

---

## 🧩 Metadata

| Atribut | Nilai |
|----------|--------|
| **Title** | Asmaul Husna |
| **Version** | 1.0.0 |
| **Format** | JSON |
| **License** | MIT |
| **Total Items** | 99 |
| **Language** | Arabic → Indonesian (+ English) |
| **Maintainer** | WNR Code |
| **Source Repo** | [github.com/wnr-code/asmaul_husna](https://github.com/wnr-code/asmaul_husna) |
| **Data Origin (CDN)** | [jsDelivr](https://www.jsdelivr.com/package/gh/wnr-code/asmaul_husna) |
| **Generator** | Gemini AI |
| **Created At** | 2025-10-20 |
| **Last Updated** | 2025-10-22 |

---

## 🚀 Penggunaan API Publik

### 🔹 Endpoint Utama
```bash
https://v1.quran.wnr.app/api/asmaulhusna
````

### 🔹 Mendapatkan Semua Nama

```bash
GET https://v1.quran.wnr.app/api/asmaulhusna
```

**Contoh Respons:**

```json
{
  "meta": {
    "title": "Asmaul Husna",
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

### 🔹 Mendapatkan Nama Berdasarkan ID

```bash
GET https://v1.quran.wnr.app/api/asmaulhusna/1
```

**Contoh Respons:**

```json
{
  "id": 1,
  "arabic": "ٱلرَّحْمَـٰنُ",
  "latin": "Ar-Rahmaan",
  "en": "The Most Compassionate",
  "idn": "Yang Maha Pengasih",
  "faedah": {
    "makna": "Kasih sayang Allah yang luas...",
    "amalan": "Berdoa dan berzikir...",
    "referensi": [
      "QS. Al-Fatihah: 3",
      "QS. Maryam: 96"
    ]
  }
}
```

---

### 🔹 Pencarian Berdasarkan Nama (Latin / Arab / IDN)

```bash
GET https://v1.quran.wnr.app/api/asmaulhusna/search?q=rahman
```

**Contoh Hasil:**

```json
{
  "result": [
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

## 📦 File JSON Langsung (CDN)

> Jika hanya butuh dataset mentah (tanpa endpoint API), bisa langsung akses via jsDelivr:

📂 **File:**
[https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/asmaul_husna.json](https://cdn.jsdelivr.net/gh/wnr-code/asmaul_husna@main/asmaul_husna.json)

---

## ⚙️ Integrasi Cepat

### 🔸 Menggunakan `fetch` (JavaScript)

```js
fetch("https://v1.quran.wnr.app/api/asmaulhusna")
  .then(res => res.json())
  .then(data => console.log(data.asmaul_husna));
```

### 🔸 Menggunakan `axios` (Node.js)

```js
import axios from "axios";

const res = await axios.get("https://v1.quran.wnr.app/api/asmaulhusna/5");
console.log(res.data);
```

### 🔸 Menggunakan `curl` (Terminal)

```bash
curl https://v1.quran.wnr.app/api/asmaulhusna/10
```

---

## 💡 Contoh Penggunaan di Website

```html
<ul id="asmaul-husna"></ul>

<script>
  fetch("https://v1.quran.wnr.app/api/asmaulhusna")
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

Proyek ini dirilis di bawah lisensi **MIT** — kamu bebas menggunakan, menyalin, atau memodifikasi selama mencantumkan atribusi ke:

> © 2025 [WNR Code](https://github.com/wnr-code)

---

## 💬 Kontribusi

Kontribusi sangat diterima!
Kalau kamu menemukan kesalahan atau ingin menambah fitur baru:

1. Fork repositori ini.
2. Edit file JSON atau tambahkan endpoint.
3. Kirim *Pull Request*.

---

## ✨ Kredit

* **Data Source:** WNR Code
* **Generator:** Gemini AI
* **API Host:** [v1.quran.wnr.app](https://v1.quran.wnr.app)
* **Kontributor:** Komunitas Pengembang Muslim 🌙

---

> *"Dan Allah memiliki Asmaul Husna, maka bermohonlah kepada-Nya dengan menyebut Asmaul Husna itu."*
> **— QS. Al-A’raf: 180**

