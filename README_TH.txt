HAIR DAILY — งาน Landing Page ขายยาสระผม

สิ่งที่มีในชุดนี้
- Landing page หน้าแรก
- สินค้า 4 SKU / 2 สูตร
- products.json เป็นแหล่งข้อมูลสินค้า
- images/ แยกจากไฟล์ HTML/JS
- order.html รับชื่อ เบอร์โทร ที่อยู่ รายการสินค้า และยอดรวม
- ส่งข้อมูลไป Google Apps Script endpoint เดิม
- admin.html ดึงออเดอร์จาก Google Sheet ที่ publish เป็น CSV
- หน้า admin มีปุ่ม หยิบสินค้า / แพ็กแล้ว / จ่าหน้า
- ปุ่มจ่าหน้าจะเปิดใบจ่าหน้าพัสดุและสั่งพิมพ์

ไฟล์ที่ต้องเอาขึ้น GitHub
index.html
product.html
order.html
admin.html
thankyou.html
script.js
style.css
products.json
images/

สำคัญ
1. ใน products.json ชื่อไฟล์รูปเป็นตัวพิมพ์เล็กทั้งหมด
2. ถ้าจะใช้รูป Gemini ของตัวเอง ให้แทนที่ไฟล์ใน images/ โดยใช้ชื่อเดิม หรือแก้ image ใน products.json ให้ตรงกับชื่อไฟล์จริง
3. โค้ดใช้ Google Apps Script และ Google Sheet endpoint เดิมที่อยู่ใน script.js
4. ถ้าอาจารย์ให้ใช้ Google Sheet ใหม่ ต้องเปลี่ยน ORDER_ENDPOINT และ ORDERS_CSV_URL ใน script.js
5. หลังอัป GitHub แล้วตั้ง Vercel ให้ root เป็นโฟลเดอร์นี้ และ deploy

การสาธิตงาน
หน้าเว็บ -> เลือกสินค้า -> สั่งซื้อ -> ข้อมูลเข้า Google Sheet -> เปิด /admin.html -> ตรวจออเดอร์ -> กดหยิบสินค้า -> แพ็กแล้ว -> จ่าหน้า -> Print
