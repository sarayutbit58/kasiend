# ADR 0019: Preset + PMT Linking + Journey Copy

## Decision
ทำแพ็ก UX สั้นตาม Q27=ค: เพิ่ม preset ตัวอย่าง, เชื่อมค่าออมต่อเดือนไป Stage 3, และปรับข้อความให้ 3 Stage อ่านเป็นเส้นทางเดียวกัน โดยไม่เปลี่ยนสูตรและไม่เพิ่ม calculator

## Scope
- Preset: เติมตัวเลขตัวอย่างใน Stage 1 และ Stage 2 ด้วยปุ่มเดียวต่อ Stage; ผู้ใช้แก้ต่อได้
- PMT linking: Stage 2 `ci_monthly` → Stage 3 `ret_planned_pmt`; ถ้าไม่มีค่า ใช้ Stage 1 `ef_monthly`; เติมเฉพาะช่องว่างและมีข้อความแจ้งที่แก้ไขได้
- Copy: ทำคำอธิบายให้ชัดว่า Stage 1 ป้องกันความเสี่ยง → Stage 2 สร้างการเติบโต → Stage 3 ตรวจเป้าหมายเกษียณ
- Q28=ข: หลังทำเสร็จ ผู้ใช้เปิด `index.html` บนมือถือเอง ยังไม่ deploy

## Non-goals
ไม่เพิ่ม calculator #4, ไม่เปลี่ยนสูตร, ไม่ lock stages, ไม่สร้าง backend หรือเก็บข้อมูลเพิ่ม
