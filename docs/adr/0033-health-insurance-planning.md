# ADR 0033: Health & Insurance Planning Tool (education)

## Decision
เพิ่มเครื่องมือ **วางแผนสุขภาพและประกันสุขภาพ** แบบการศึกษา  
ช่วยประมาณ “ภาระที่อาจจ่ายเอง / เงินสดที่ควรมี / งบเบี้ย vs ช่องว่าง”  
**ไม่แนะนำซื้อ–ไม่ซื้อกรมธรรม์รายตัว และไม่เทียบบริษัทประกัน**

## Formula sketch (educational)
- `exposed ≈ shock × rightsFactor + annualOOP`
  - rightsFactor: none 0.70 · gold 0.28 · sso 0.22 · civil 0.18 (สมมติฐานการศึกษา)
- `cashTarget ≈ max(exposed × 0.5, annualOOP × 2)`
- ถ้ามีเบี้ย: `premYear = premium × 12`, `afford = premYear / (income×12)`
- หลังประกันหยาบ: `afterIns = min(shock, deductible) + max(0, shock - coverage)`
- `gap = max(0, afterIns - cash)` (หรือ exposed-cash ถ้าไม่มีประกัน)

## Non-goals
ไม่ underwrite, ไม่คำนวณ prem ตามอายุจริงจากตารางบริษัท, ไม่แทนที่สิทธิรัฐ
