# Lock In Timer (PWA)

ไฟล์ในชุดนี้
- index.html            หน้าเว็บทั้งหมด (โค้ดตัวจับเวลา)
- manifest.webmanifest  ข้อมูลบอกเบราว์เซอร์ว่านี่คือ "แอป" (ชื่อ ไอคอน สี โหมดเต็มจอ)
- sw.js                 service worker เก็บไฟล์ไว้ในเครื่อง ใช้ออฟไลน์ได้
- icon-192.png, icon-512.png  ไอคอนแอป

## วิธีอัปขึ้น GitHub Pages (ฟรี)
1. สมัคร/ล็อกอิน github.com
2. กด New repository ตั้งชื่อ lockin-timer เลือก Public แล้ว Create
3. กด "uploading an existing file" ลากไฟล์ทั้ง 5 ไฟล์ (แตก zip ก่อน) ใส่ แล้วกด Commit changes
4. ไปที่ Settings > Pages > Source เลือก "Deploy from a branch" > Branch: main, โฟลเดอร์ /(root) > Save
5. รอประมาณ 1 นาที จะได้ลิงก์ https://ชื่อผู้ใช้.github.io/lockin-timer/

ทางลัด: เข้า app.netlify.com/drop แล้วลากทั้งโฟลเดอร์ใส่ ได้ลิงก์ทันที

## ติดตั้งเป็นแอป
- Android (Chrome): เปิดลิงก์ > เมนู ⋮ > "ติดตั้งแอป" (Install app)
- iPhone (Safari): ปุ่มแชร์ > "เพิ่มลงในหน้าจอโฮม"
- คอม (Chrome/Edge): กดไอคอนติดตั้งทางขวาของแถบที่อยู่

## เมื่อแก้โค้ดภายหลัง
เปลี่ยนเลขใน sw.js บรรทัด const CACHE = 'lockin-v1' เป็น v2, v3, ... ทุกครั้งที่อัปไฟล์ใหม่
ไม่งั้นเครื่องที่เคยเปิดไว้จะยังเห็นของเก่าจากแคช
