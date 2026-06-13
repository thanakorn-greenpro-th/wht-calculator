# วิธี Push ขึ้น GitHub จาก Terminal บน Mac

repo นี้ commit เรียบร้อยแล้ว (branch `master`) เหลือแค่เชื่อม GitHub แล้ว push
เปิด **Terminal** บน Mac แล้วทำตามนี้

---

## ขั้นที่ 0 — เข้าโฟลเดอร์ + ลบ lock ที่ค้างจาก sandbox

```bash
cd ~/Documents/Content/wht-calculator
rm -f .git/*.lock .git/refs/heads/*.lock .git/objects/maintenance.lock
git branch -M main
```

> ที่ต้องลบ `.lock` เพราะระบบไฟล์ที่ Claude ใช้ลบไฟล์พวกนี้ไม่ได้ แต่บน Mac ลบได้ปกติ

---

## ขั้นที่ 1 — สร้าง repo บน GitHub แล้ว push

### ทางเลือก A — มี GitHub CLI (`gh`) ติดตั้งและล็อกอินแล้ว (เร็วสุด จบใน 1 บรรทัด)

```bash
gh repo create wht-calculator --public --source=. --push
```

จากนั้นเปิด GitHub Pages:

```bash
gh api -X POST repos/{owner}/wht-calculator/pages -f "source[branch]=main" -f "source[path]=/"
```

### ทางเลือก B — ไม่มี `gh` (ใช้เว็บสร้าง repo)

1. ไปที่ https://github.com/new สร้าง repo ชื่อ `wht-calculator` แบบ **Public** (อย่าติ๊ก Add README)
2. กลับมาที่ Terminal แล้วรัน (แก้ `<ACCOUNT>` เป็นชื่อบัญชี GitHub ของคุณ):

```bash
git remote add origin https://github.com/<ACCOUNT>/wht-calculator.git
git push -u origin main
```

3. เปิด GitHub Pages: ไปที่ repo > **Settings** > **Pages** > Source: **Deploy from a branch** > เลือก **main** / **/ (root)** > **Save**

---

## ขั้นที่ 2 — ลิงก์ให้ Manager เข้าเล่น

รอ ~1 นาที จะได้ลิงก์:

```
https://<ACCOUNT>.github.io/wht-calculator/
```

ส่งลิงก์นี้ให้ Manager เปิดได้เลย เล่นได้ทั้งคอมและมือถือ

---

## หมายเหตุ

- ก่อนใช้จริง แก้ลิงก์ปุ่ม "ปรึกษาฟรี" ใน `index.html` (ค้นหา `greenproksp.com/contact`) ให้เป็น URL/LINE จริง
- ถ้า push แล้วติด auth: รัน `gh auth login` (ถ้ามี gh) หรือใช้ Personal Access Token แทนรหัสผ่านตอน git ถาม
