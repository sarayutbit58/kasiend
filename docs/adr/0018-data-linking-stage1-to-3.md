# ADR 0018: Data Linking Stage 1 → Stage 3 (เบา)

## Decision
เพิ่ม pre-fill จาก Stage 1 (เงินสำรองฉุกเฉิน) ไป Stage 3 (เป้าเงินเกษียณ) แบบเบา — ใช้ sessionStorage ไม่มี lock stages ไม่มี stepper wizard — ตาม Q18=ข

## What's Linked
- Stage 1 `ef_expense` → Stage 3 `ret_expense` (pre-fill ถ้าช่องยังว่าง)
- Stage 1 `ef_saved` → Stage 3 `ret_saved` (pre-fill ถ้าช่องยังว่าง)
- แสดง `link-note` 💡 บอกผู้ใช้ว่าค่านี้ดึงมาจากขั้น ① + แก้ไขได้ตลอด

## What's NOT
- ไม่ลิงก์ไป Stage 2 (ดอกเบี้ยทบต้น — inputs ต่างกัน)
- ไม่ล็อก Stage 2–3 — ผู้ใช้สามารถข้ามไป Stage 3 ได้เลย
- ไม่ stepper wizard / popup
- sessionStorage = per-tab (ไม่ข้ามแท็บ — ข้อจำกัดที่รับได้สำหรับ v1.4)

## Edge Cases Handled
- ไม่มีค่าใน sessionStorage → link-note ซ่อน, ไม่ pre-fill, ไม่ crash
- Stage 3 มีค่าเดิมอยู่แล้ว → ไม่ overwrite (`!ret_expense.value` guard)
- ผู้ใช้ลบค่าใน Stage 1 → storageSet เก็บ 0 → ไม่ pre-fill

## Justification
ผู้ใช้เลือก ข — ต้องการความเชื่อมโยงเบาๆ ก่อน deploy; เพิ่มความซับซ้อนเมื่อมี feedback จากผู้ใช้จริง
