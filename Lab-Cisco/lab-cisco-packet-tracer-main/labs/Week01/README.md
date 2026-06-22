# Week 01: Introduction to Cisco Packet Tracer

## วัตถุประสงค์
- ทำความคุ้นเคยกับ Cisco Packet Tracer Interface
- เรียนรู้การเพิ่มและเชื่อมต่ออุปกรณ์พื้นฐาน
- เรียนรู้การตั้งค่า IP Address
- เรียนรู้คำสั่งพื้นฐานของ Router
- เรียนรู้การตรวจสอบการเชื่อมต่อ

## เนื้อหาการเรียนรู้

### 1. การใช้งาน Cisco Packet Tracer
- Interface และ Tools พื้นฐาน
- การเพิ่มอุปกรณ์ (Devices)
- การเชื่อมต่อด้วยสาย (Connections)

### 2. การตั้งค่า IP Address
- การตั้งค่า IP บน PC
- การตั้งค่า IP บน Router Interface
- Subnet Mask และ Default Gateway

### 3. คำสั่ง Router พื้นฐาน
- Privileged Mode และ Configuration Mode
- การตั้งค่า Interface
- การเปิด/ปิด Interface

### 4. การตรวจสอบการเชื่อมต่อ
- คำสั่ง ping
- คำสั่ง show ต่างๆ
- การดูสถานะ Interface

## แล็บที่แนะนำ

### Lab 1: Basic Network Setup
สร้าง network พื้นฐานที่มี:
- 2 PCs
- 1 Switch
- 1 Router

**ขั้นตอน:**
1. เพิ่มอุปกรณ์: 2 PCs, 1 Switch, 1 Router
2. เชื่อมต่อ PCs กับ Switch ด้วยสาย Straight-through
3. เชื่อมต่อ Switch กับ Router ด้วยสาย Straight-through
4. ตั้งค่า IP:
   - PC0: 192.168.1.10/24, Gateway: 192.168.1.1
   - PC1: 192.168.1.20/24, Gateway: 192.168.1.1
   - Router Fa0/0: 192.168.1.1/24
5. เปิด Router Interface: `no shutdown`
6. ทดสอบ ping ระหว่าง PC0 และ PC1

### Lab 2: การตั้งค่าคำสั่งพื้นฐานและเปิด Interface บน Router
1. คลิกที่ตัว **Router0** -> ไปที่แท็บ **CLI** (Command Line Interface)
2. เมื่อระบบถามว่า `Would you like to enter the initial configuration dialog? [yes/no]:` ให้พิมพ์ **`no`** แล้วกด **Enter** (หากไม่ขึ้น ให้กด Enter 1-2 ครั้งจนเจอคำว่า `Router>`)
3. พิมพ์คำสั่งตามลำดับดังต่อไปนี้:

```
Router> enable                                 # เข้าสู่ Privileged Mode
Router# configure terminal                     # เข้าสู่ Global Configuration Mode
Router(config)# interface FastEthernet 0/0     # เลือกพอร์ต Fa0/0 ที่เชื่อมต่อกับ Switch
Router(config-if)# ip address 192.168.1.1 255.255.255.0   # ตั้งค่า IP และ Subnet Mask
Router(config-if)# no shutdown                 # สั่งเปิดใช้งานพอร์ต (สถานะไฟที่สายจะเปลี่ยนจากแดงเป็นเขียว)
Router(config-if)# exit                        # ออกจากโหมดพอร์ต
Router(config)# exit                           # ออกจากโหมดคอนฟิก
```
ตรวจสอบสถานะพอร์ต: พิมพ์คำสั่งตรวจสอบความถูกต้องเพื่อดูว่าพอร์ตเปิดใช้งานจริงหรือไม่
`Router# show ip interface brief`

สังเกตที่บรรทัด FastEthernet0/0 ช่อง Status จะต้องเป็น up และ Protocol จะต้องเป็น up


