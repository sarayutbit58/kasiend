# ADR 0034: Multi-step tour subpages (hash views)

## Decision
เปลี่ยนจากหน้าเดียวยาว เป็น **ทัวร์ทีละหน้า** ด้วย hash routing ใน `index.html` ไฟล์เดียว (static / GitHub Pages)

## Routes
- `#home` เริ่มต้น + เลือกกลุ่ม + dashboard
- `#stage1` `#stage2` `#stage3` ทีละขั้น + ปุ่มไปต่อ/ย้อน
- `#summary` สรุปแผน + แนะนำขั้นถัดไป
- `#tools` เครื่องมือเสริม

## Why not separate .html files
เครื่องคำนวณและ data linking อยู่ใน JS ชุดเดียว — แยกไฟล์จะซ้ำโค้ดและพัง sync  
sessionStorage ยังใช้ได้; hash รู้สึกเป็น subpage บนมือถือ

## UX
- ผู้ใช้งงว่าเริ่มไหน → home บอกชัด + CTA ขั้น 1
- ลด cognitive load ทีละจอ
- bottom nav + tour top chips

## Non-goals
ไม่ backend, ไม่ React SPA build step
