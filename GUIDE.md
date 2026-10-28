# 🎮 คู่มือเว็บไซต์ร้านซื้อขายรหัสเกม Roblox (BLOXANIME STORE)

เว็บไซต์ **BLOXANIME STORE** เป็นเว็บแอปพลิเคชันสำหรับซื้อขายรหัสเกม Roblox และแมพอนิเมะชั้นนำ เช่น **Anime Vanguards, Anime Adventures, Anime Zero, Blox Fruits, King Legacy, Pet Simulator 99** โดยออกแบบในสไตล์ **Dark Cyber & Gaming Aesthetic** รองรับระบบตะกร้าสินค้า, ระบบสั่งซื้อและส่งรหัสอัตโนมัติ (Instant Delivery), ฟอร์มฝากขายรหัส (Consignment), กล่องสุ่ม Lucky Gacha และระบบค้นหา/กรองสินค้า

---

## 🚀 1. วิธีเปิดใช้งานเว็บไซต์ทันที

ไฟล์ทั้งหมดพร้อมใช้งานทันทีในเครื่องของคุณ:
1. ดับเบิลคลิกเปิดไฟล์ [`index.html`](file:///c:/Users/zasgo/Downloads/work%20monday%2013.00/index.html) ผ่าน Google Chrome, Microsoft Edge หรือเบราว์เซอร์ใดก็ได้
2. หรือหากเปิดใน VS Code สามารถคลิกขวาที่ [`index.html`](file:///c:/Users/zasgo/Downloads/work%20monday%2013.00/index.html) แล้วเลือก **Open with Live Server**

---

## 🌟 2. จุดเด่นและฟังก์ชันการทำงานในระบบ

| ฟังก์ชัน | รายละเอียดการทำงาน |
| :--- | :--- |
| **หมวดหมู่แมพ (Map Filters)** | กรองดูเฉพาะ Anime Vanguards, Anime Adventures, Anime Zero, Blox Fruits ฯลฯ ได้ในคลิกเดียว |
| **ระบบค้นหาแบบ Real-time** | พิมพ์ค้นหาชื่อแมพ, สเปก, ยูนิต Secret, หรือคำว่า "ไก่ตัน" ผลลัพธ์จะแสดงทันที |
| **ระบบตะกร้าสินค้า (Cart Drawer)** | กดหยิบใส่ตะกร้า คำนวณราคารวมอัตโนมัติ และสั่งซื้อพร้อมกันได้ |
| **หน้าต่างดูรายละเอียดสเปก (Modal)** | แสดงภาพพรีวิว, สเตตัสในเกม, Trait, ยูนิต, เมลสะอาด และเงื่อนไขการรับประกัน |
| **ระบบจำลองชำระเงินออโต้ (Checkout)** | รองรับทั้ง **QR พร้อมเพย์ (PromptPay)** และ **ซองของขวัญ TrueMoney Wallet** |
| **ระบบจัดส่งรหัสทันที (Instant Delivery)** | เมื่อกดชำระเงิน ระบบจะส่ง **Username & Password** ให้คัดลอกไปล็อกอินได้ทันที |
| **ระบบฝากขายรหัส (Sell Consignment)** | ฟอร์มให้ผู้เล่นคนอื่นนำไอดีมาส่งข้อมูลขอฝากขายกับทางร้าน |
| **กล่องสุ่มลุ้นโชค (Lucky Gacha)** | สุ่มลุ้นรหัส Secret หรือไก่ตัน V4 พร้อมแอนิเมชันและเสียงเอฟเฟกต์ |
| **ระบบเสียงประกอบ (Web Audio API)** | เสียงคลิก, เสียงสำเร็จ, เสียงสุ่มกล่อง สร้างบรรยากาศเกมมิ่งสมจริง |

---

## 🛠️ 3. วิธีการแก้ไขและเพิ่มสินค้าของคุณเอง

คุณสามารถเปิดไฟล์ [`index.html`](file:///c:/Users/zasgo/Downloads/work%20monday%2013.00/index.html) ด้วย Text Editor (เช่น VS Code หรือ Notepad) เพื่อปรับแต่งข้อมูล:

### 3.1 การเพิ่มหรือแก้ไขรหัสสินค้า (Product Catalog)
ค้นหาตัวแปร `const PRODUCTS = [` ในแท็ก `<script>`:
```javascript
{
  id: 13, // เลข ID ห้ามซ้ำกัน
  title: '[Anime Vanguards] รหัส Igris Secret + Trait Monarch',
  map: 'Anime Vanguards', // ชื่อแมพ
  price: 990, // ราคาขายจริง (บาท)
  originalPrice: 1500, // ราคาเต็มก่อนลด (บาท)
  badge: 'HOT SECRET', // ป้ายข้อความบนรูป
  badgeColor: 'bg-purple-600', // สีป้าย เช่น bg-purple-600, bg-cyan-600, bg-emerald-600
  image: 'URL รูปภาพสินค้า', // ลิงก์รูปภาพตัวอย่าง
  stock: 1, // จำนวนสต็อก
  features: [
    'ตัวละครระดับ Secret: Igris (Level Max)',
    'Trait: Monarch ดาเมจ +150%',
    'เพชรคงเหลือ 60,000+ Gems',
    'เมลสะอาด ไม่ผูกเบอร์ ปลอดภัย 100%'
  ],
  desc: 'คำบรรยายเพิ่มเติมเกี่ยวกับไอดีนี้...'
}
```

### 3.2 การเปลี่ยนเลขพร้อมเพย์ (PromptPay QR Code)
ค้นหาแท็ก `id="qrCodeImage"` แล้วเปลี่ยนลิงก์ QR Code ให้เป็นเบอร์พร้อมเพย์ของคุณ:
```html
<img id="qrCodeImage" src="https://promptpay.io/เบอร์โทรหรือเลขบัตรประชาชน/ยอดเงิน" ...>
```
*(หรือนำรูป QR พร้อมเพย์จริงของคุณมาใส่ในแท็ก `src="..."` ได้โดยตรง)*

### 3.3 การเปลี่ยนชื่อร้านและช่องทางติดต่อ
- ค้นหาคำว่า `BLOXANIME` เพื่อเปลี่ยนชื่อร้านเป็นแบรนด์ของคุณ
- ค้นหาแท็กติดต่อในส่วน `<footer>` เพื่อใส่ลิงก์ Facebook Page, Discord หรือ LINE Official Account ของคุณ

---

## 🌐 4. ขั้นตอนการนำเว็บขึ้นออนไลน์ฟรี (Deploy to Web)

หากต้องการให้ลูกค้าทั่วประเทศเปิดดูเว็บของคุณผ่านอินเทอร์เน็ตได้ฟรีตลอด 24 ชม.:

1. **ผ่าน Netlify Drop (ง่ายที่สุด ไม่ต้องเขียนโค้ด)**
   - เข้าเว็บ [app.netlify.com/drop](https://app.netlify.com/drop)
   - ลากโฟลเดอร์นี้ไปปล่อยลงในหน้าเว็บ
   - คุณจะได้รับลิงก์ URL เว็บไซต์ทันที (เช่น `https://my-blox-store.netlify.app`)

2. **ผ่าน GitHub Pages หรือ Vercel**
   - สามารถสร้าง GitHub Repository แล้วเปิดใช้งาน GitHub Pages ในแท็บ Settings ได้ฟรีเช่นกัน
