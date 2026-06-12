# Daily Learning Log - 5 June 2026
**Thursday**

---

## Today's Focus
Deep dive on Warehouse E — อธิบายรายละเอียดระบบที่ไปดูเมื่อวาน

---

## What I Learned

### 1. **22 DWS — ทำงานพร้อมกันทั้งหมด**
- มี 22 สายพานจากรถเข้าเครื่อง DWS 22 เครื่องพร้อมกันเลย
- รองรับปริมาณพัสดุที่เข้ามาจำนวนมากในคราวเดียว

### 2. **Checkpoint ก่อนเข้า DWS**
- มีพนักงานยืนประจำปากสายพาน + ตาชั่ง
- ถ้าหนักเกิน 50 kg หรือรูปทรงแปลก (เช่น เหล็กยาวๆ) → แยกไป **Manual Team** ทันที
- ใช้ทั้งตาชั่งและความชำนาญของพนักงานในการตัดสินใจ
- Manual Team มีทีมแยกต่างหากเลย

### 3. **Inbound รับของ 2 แบบ**
- **ชิ้นๆ** → DWS scan → conveyor แยกเขตอัตโนมัติเลย
- **กระสอบ** → DWS scan กระสอบ → ส่งต่อ Auto Packing

### 4. **Auto Packing — รายละเอียด**
- กระสอบมาจากสาขาย่อยที่รวบรวมของมาส่ง
- กระสอบมี 2 แบบ: แยกปลายทางมาแล้ว / ยังไม่แยก (ระบุใน label)
- พัสดุแต่ละชิ้นข้างในมี label ของตัวเองอยู่แล้ว
- พนักงานยืนแกะกระสอบ แล้วส่งชิ้นๆ เข้า conveyor ใหม่

### 5. **Flip Tray System**
- สายพาน Flip Tray อยู่ข้างๆ พนักงาน Auto Packing เลย
- เจอของกลม/ทรงกระบอกที่กลิ้งได้ → โยนเข้า Flip Tray ทันที
- Flip Tray มีเส้นทางแยก แต่ปลายทางไปรวมกับ conveyor ปกติเหมือนกัน

### 6. **ของเบาเกินไป**
- ของที่เบาเกินจะปลิวบนสายพาน
- พนักงาน Auto Packing รวบใส่กระสอบข้างๆ → พอหนักพอแล้วส่งไป Manual Team

### 7. **Reverse Conveyor — เข้าใจใหม่**
- ไม่ได้ divert ออก แต่พัสดุ **วนอยู่บน conveyor เรื่อยๆ**
- ถ้า DWS อ่าน label ได้ → แยกเขตอัตโนมัติ
- ถ้าอ่านไม่ออก → วนรอ → พนักงานอ่าน label ด้วยตาแล้วปัดลงเขตที่ถูกต้อง

### 8. **Outbound — สายพานซอยจังหวัด**
- สายพานหลักวิ่งตรง แตกซอยออกไปตามจังหวัด
- พนักงานยืนประจำแต่ละซอย ใช้ตาดู label แล้วดึงของเข้าซอยตัวเอง
- ถ้าพลาด → ของวนกลับมาใหม่
- **ทำไมไม่ใช้เครื่อง?** → เคยลองแล้ว แต่ Outbound ของมาทีละหลายชิ้นพร้อมกัน เครื่องไม่ทัน ของตกหล่น SLA ไม่ผ่าน

### 9. **Scan ก่อนขึ้นรถ**
- พนักงาน scan barcode ทุกชิ้นก่อนขึ้นรถ
- เป็นหลักฐานว่าของออกจาก Warehouse SPK แล้ว
- ถ้าของหายหลังจากนี้ → ความรับผิดชอบไม่ใช่ของคลัง SPK

---

## Key Insights

✅ **Automation ≠ เครื่องทุกจุด**
- บางจุดใช้คนเพราะ practical กว่า ไม่ใช่เพราะล้าหลัง
- Outbound ใช้คนเพราะเครื่องรับ volume ไม่ไหว

✅ **ทุก Checkpoint มีหน้าที่ protect ด้วย**
- Scan ก่อนขึ้นรถ = ไม่ใช่แค่ track ของ แต่ protect ความรับผิดชอบของคลัง

✅ **ระบบออกแบบมาเพื่อรับ edge case**
- ของเบา ของกลม ของหนัก ของรูปแปลก มีทางออกหมดทุกกรณี

---

## My Reflections

**สิ่งที่เข้าใจผิดแล้วแก้ได้วันนี้:**
- Reverse conveyor ไม่ได้ divert ออก แต่วนรอ
- Inbound รับทั้งชิ้นๆ และกระสอบ ไม่ใช่แค่ชิ้นๆ

**Questions I have:**
- Manual team ใช้เวลานานกว่า automated ไหม?
- SLA ของ Outbound คืออะไร วัดยังไง? *(รอไฟล์จากเทรนเนอร์)*

---

## Concepts to Understand Better

- [ ] SLA (Service Level Agreement) ของ J&T Express คืออะไร?
- [ ] Capacity จริงๆ ของ 22 DWS slots ต่อชั่วโมง?
- [ ] Manual team process มีขั้นตอนยังไง?

---

## Connection to Management

**Operations Management:**
- การเลือกใช้คนหรือเครื่องต้องดู volume และ context จริงๆ ไม่ใช่แค่ automation = ดีกว่าเสมอ

**Risk Management:**
- Scan ก่อนขึ้นรถ = protect ทุกฝ่าย สร้าง accountability ในระบบ

**Process Design:**
- ทุก edge case มีทางออกชัดเจน ระบบดีคือระบบที่ไม่มีของ "ค้าง" อยู่โดยไม่มีใครดูแล

---

## Tags
`#operations` `#logistics` `#automation` `#warehouse` `#outbound` `#inbound` `#auto-packing` `#SLA` `#j-t-express`

---

## Next Steps

- [ ] ถามเทรนเนอร์: manual team ช้ากว่า automated ไหม?
- [ ] รอไฟล์ SLA จากเทรนเนอร์
- [ ] เริ่มเรียนรู้ Business Understanding และ Team Management
