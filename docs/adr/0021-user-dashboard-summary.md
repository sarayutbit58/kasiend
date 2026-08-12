# ADR 0021: User Dashboard Summary

## Decision
เพิ่ม User Dashboard ด้านบนของหน้า ใต้ Banner Ads เพื่อให้ผู้ใช้เห็นภาพรวมเส้นทาง KasienD โดยไม่ต้องเลื่อนกลับไปดูผลลัพธ์ทีละ Stage

## Dashboard Content
- สถานะเงินสำรองฉุกเฉินและเปอร์เซ็นต์ของเป้า
- เงินออมต่อเดือน
- เป้าเงินเกษียณและช่องว่างที่ยังขาด
- ขั้นถัดไปที่ควรทำ
- Progress ของทั้ง 3 Stage
- ผลดอกเบี้ยทบต้นจะแสดงเมื่อผู้ใช้เริ่มกรอก Stage 2

## Design Boundary
ใช้ข้อมูลจาก input/result ที่มีอยู่ใน browser เท่านั้น อัปเดตแบบ live ไม่เพิ่ม login, backend, tracking หรือ calculator ใหม่ และไม่เปลี่ยนสูตรคำนวณเดิม

## Rationale
เลือก Modern Financial Dashboard ผสม Soft Friendly เพื่อให้ตัวเลขสำคัญเด่น แต่ยังอ่านง่ายสำหรับผู้ใช้ที่ไม่มีพื้นฐานการเงิน
