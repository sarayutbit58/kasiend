# ADR 0032: UX/UI polish via ui-ux-pro-max guidelines

## Decision
ปรับ UX/UI ของ `index.html` ตาม ui-ux-pro-max (a11y, touch 44px, mobile nav, progressive disclosure, design tokens) โดย**ไม่เปลี่ยนสูตรคำนวณ**

## Changes
- Design tokens + spacing rhythm
- Skip link, main landmark, sticky bottom nav (ภาพรวม/1/2/3/เครื่องมือ)
- จัดกลุ่มเครื่องมือคลังความรู้ใต้หัวข้อชัด
- ปุ่ม/ช่องกรอกสูงขั้นต่ำ 44px, font-size 16px กัน iOS zoom
- Focus ring + reduced-motion
- design-system/kasiend/MASTER.md

## Non-goals
ไม่ย้ายไป React/Tailwind/CDN, ไม่ลบ emoji ที่ผู้ใช้ชอบใน dashboard (คงโทน vibrant)
