# วิธี Deploy บน Netlify (5 นาที ฟรี)

## ขั้นตอนที่ 1 — อัปโหลดไฟล์
1. ไปที่ https://app.netlify.com → Login (หรือสมัครฟรี)
2. กด **"Add new site"** → **"Deploy manually"**
3. ลากโฟลเดอร์ `ff-garment-app` ทั้งโฟลเดอร์วางลงในหน้าเว็บ
4. รอ Deploy เสร็จ (ประมาณ 1 นาที) จะได้ลิงก์เช่น `https://amazing-name-123.netlify.app`

## ขั้นตอนที่ 2 — ใส่ Notion Token (สำคัญมาก!)
Token ต้องใส่ใน Netlify เป็น Environment Variable เพื่อความปลอดภัย
1. ใน Netlify Dashboard → เลือก Site ที่เพิ่ง Deploy
2. ไปที่ **Site configuration** → **Environment variables**
3. กด **"Add a variable"**
4. Key: `NOTION_TOKEN`
5. Value: `YOUR_NOTION_TOKEN_HERE`
6. กด **Save**
7. ไปที่ **Deploys** → กด **"Trigger deploy"** → **"Deploy site"**

## ขั้นตอนที่ 3 — เชื่อม Integration กับ Notion Database
(ถ้ายังไม่ได้ทำ)
1. เปิด Database "รับงานปัก/สกรีน" ใน Notion
2. กด ⋯ มุมขวาบน → **Connections** → เพิ่ม Integration ที่สร้างไว้
3. ทำซ้ำกับ Database "Project"

## ขั้นตอนที่ 4 — ติดตั้งบน Smartphone
**iPhone:** เปิดลิงก์ใน Safari → Share → Add to Home Screen
**Android:** เปิดใน Chrome → ⋮ → Add to Home Screen

---
⚠️ หลังจาก Deploy เสร็จแล้ว แนะนำให้ไป Refresh Token ที่ notion.so/my-integrations
เพราะไฟล์นี้มี Token เก่าอยู่ในเอกสาร แล้วอัปเดต Environment Variable ด้วย Token ใหม่ครับ
