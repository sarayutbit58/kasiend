# Hermes agent เป็นผู้สร้างเว็บ (static HTML/JS ไฟล์เดียว)

แทนที่จะใช้ No-Code platform ภายนอก (Glide/Lovable/Bubble) ให้ Hermes agent เขียนเว็บเป็น static site ไฟล์ HTML เดียว self-contained (CSS+JS ฝังใน) เหตุผล: ผู้สร้างไม่มีพื้นฐานโค้ดและไม่ต้องเขียนเอง, ไม่มีค่ารายเดือน, ไม่มี vendor lock-in, คำนวณทั้งหมดทำฝั่ง client สอดคล้องกับ ADR 0006 (ไม่เก็บข้อมูล) deploy ฟรีผ่าน GitHub Pages หรือ Netlify Drop
