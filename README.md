# เครื่องคำนวณภาษีหัก ณ ที่จ่าย 2569 — Greenpro KSP

หน้าเว็บ interactive หน้าเดียวจบ: เครื่องคำนวณภาษีหัก ณ ที่จ่าย + คู่มือฉบับเต็ม (3 วิธีคำนวณ, ตารางอัตรา 2569, การยื่น ภ.ง.ด.3/53)

ไฟล์ `index.html` เป็น standalone ไม่มี dependency ภายนอก (ยกเว้นฟอนต์ Google) เปิดด้วยเบราว์เซอร์ได้ทันที

---

## วิธีเอาขึ้น GitHub + เปิดให้ Manager เข้าเล่น (GitHub Pages)

ทำผ่านเว็บ GitHub ได้เลย ไม่ต้องใช้ command line ใช้เวลา ~2 นาที

### ขั้นตอน

1. เข้า https://github.com แล้ว Login บัญชีของบริษัท
2. กดปุ่ม **+** มุมขวาบน > **New repository**
3. ตั้งชื่อ repo เช่น `wht-calculator` > เลือก **Public** > กด **Create repository**
4. ในหน้า repo ที่ว่าง กดลิงก์ **uploading an existing file** (หรือไปที่ **Add file > Upload files**)
5. ลากไฟล์ `index.html` (และ `README.md` ถ้าต้องการ) เข้าไปวาง > กด **Commit changes**
6. ไปที่แท็บ **Settings** ของ repo > เมนูซ้าย **Pages**
7. ใต้หัวข้อ **Build and deployment > Source** เลือก **Deploy from a branch**
8. เลือก branch **main** + โฟลเดอร์ **/ (root)** > กด **Save**
9. รอประมาณ 1 นาที รีเฟรชหน้า จะได้ลิงก์ live ขึ้นมา

### ลิงก์ที่ Manager ใช้เปิดเล่น

```
https://<ชื่อบัญชี-github>.github.io/wht-calculator/
```

ตัวอย่าง ถ้าบัญชีชื่อ `greenproksp` ลิงก์จะเป็น
`https://greenproksp.github.io/wht-calculator/`

ส่งลิงก์นี้ให้ Manager เปิดในเบราว์เซอร์ได้เลย เล่นได้ทั้งคอมและมือถือ

---

## หมายเหตุก่อนใช้งานจริง

- แก้ลิงก์ปุ่ม **"ปรึกษาฟรี"** ในไฟล์ `index.html` (ค้นหา `greenproksp.com/contact`) ให้เป็น URL หรือ LINE จริงของบริษัท
- ถ้าจะนำขึ้นเว็บหลัก WordPress ดูวิธีฝังในไฟล์ `Interactive-WHT-Page-PLAN.md`
- ตัวเลขทุกสูตรตรวจสอบความถูกต้องแล้ว แต่เนื้อหาเป็นข้อมูลทั่วไป ควรตรวจกับนักบัญชีก่อนนำส่งจริง

© Greenpro KSP
