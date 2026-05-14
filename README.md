# 📍 Maps Embed Parser

> ถอดค่า **ชื่อสถานที่**, **Latitude**, **Longitude** และ **src URL** จาก Google Maps iframe embed code — ไม่ต้องติดตั้งอะไรทั้งนั้น เปิดเว็บแล้วใช้ได้เลย

---

## 🚀 Demo

🔗 [https://23deepblue.github.io/maps-parser/](https://23deepblue.github.io/maps-parser/)

---

## 🧩 มันทำอะไร

วาง `<iframe>` embed code จาก Google Maps แล้ว utility นี้จะถอดค่าออกมา 4 อย่าง:

| ค่า | ตัวอย่าง |
|---|---|
| **ชื่อสถานที่** | `โรงพยาบาลแม่สอด` |
| **Latitude** | `17.17401074527428` |
| **Longitude** | `99.61539459563596` |
| **src URL** | `https://www.google.com/maps/embed?pb=...` |

---

## 📖 วิธีใช้

**1.** เปิด Google Maps แล้วกด **Share → Embed a map** คัดลอก iframe code มา

```html
<iframe src="https://www.google.com/maps/embed?pb=!1m18!..." width="600" height="450" ...></iframe>
```

**2.** วาง code ลงในช่อง input

**3.** กดปุ่ม **⚡ Parse ได้เลย** (หรือกด `Ctrl + Enter`)

**4.** ค่า ชื่อสถานที่, Latitude, Longitude และ src จะปรากฏ — กดปุ่ม **copy** ข้างแต่ละค่าได้เลย

---

## ⚙️ วิธีทำงาน

ดึงค่าจาก Google Maps URL format ด้วย Regular Expression และ Base64 decoding:

| ค่า | วิธีดึง |
|---|---|
| ชื่อสถานที่ | `!2z{base64}` → decode UTF-8 |
| Longitude | `!2d{value}` |
| Latitude | `!3d{value}` |
| src | `src="..."` attribute |

---

## 🗂 โครงสร้างไฟล์

```
maps-parser/
└── index.html   ← ทุกอย่างอยู่ในไฟล์เดียว (HTML + CSS + JS)
```

---

## 🛠 Tech Stack

- HTML5
- CSS3 (ไม่มี framework)
- Vanilla JavaScript (ไม่มี library)

---

## 📄 License

MIT — ใช้ได้ฟรี แก้ได้ตามใจ
