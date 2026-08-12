# ADR 0031: Cross-tool data linking hub

## Decision
เพิ่ม `linkCrossTools()` เติมเฉพาะช่องว่าง + ปุ่มนำค่าแบบบังคับระหว่างเครื่องมือ

## Auto (empty only)
- Stage1 expense/saved/monthly → med / freelancer / health ratios
- รายได้จากช่องใดช่องหนึ่ง → PVD / กบข. / SSO / ฟรีแลนซ์ / อัตราส่วน
- อายุ Stage3 → SSO age; ปีถึงเกษียณ → PVD/กบข. years
- เป้า Stage3 → กฎ 4% nest (ถ้าว่าง)

## Buttons (overwrite)
- เป้า Stage3 → กฎ 4%
- PVD+กบข.+บำเหน็จ SSO → กฎ 4% หรือ ret_saved
- ซิงก์ทั้งหมด / กระจายรายได้

## Non-goals
ไม่ล็อก stage, ไม่ทับค่าที่ผู้ใช้พิมพ์ (ยกเว้นปุ่ม), ไม่เรียก API
