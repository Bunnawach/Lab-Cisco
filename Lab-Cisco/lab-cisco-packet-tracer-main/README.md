หมายเหตุ Tutorial นี้จัดทำขึ้นเมื่อปี 2020 และปรับปรุงเมื่อ 2026 

# 🌐 Cisco Packet Tracer Lab Collection

> คอลเลกชันแล็บ Cisco Packet Tracer สำหรับวิชา Data Communication and Computer Network  
> เรียนรู้การตั้งค่าเครือข่ายตั้งแต่พื้นฐานจนถึงขั้นสูง พร้อมคำสั่งและตัวอย่างที่ใช้งานได้จริง

---

## 📖 เกี่ยวกับโปรเจกต์นี้

โปรเจกต์นี้รวบรวมแล็บ Cisco Packet Tracer ที่ครอบคลุมเนื้อหาตั้งแต่พื้นฐานไปจนถึงขั้นสูง เหมาะสำหรับผู้ที่กำลังศึกษาเรื่องเครือข่ายคอมพิวเตอร์และต้องการฝึกปฏิบัติจริง

ในแต่ละ Week คุณจะได้เรียนรู้:
- ✅ การตั้งค่าอุปกรณ์เครือข่าย (Router, Switch, PC)
- ✅ การจัดการ IP Address และ Subnet
- ✅ การสร้างและจัดการ VLAN
- ✅ การตั้งค่า Routing Protocol (RIP)
- ✅ Network Address Translation (NAT)
- ✅ และอีกมากมาย...
---

## 🗂️ โครงสร้างโปรเจกต์

```
lab-cisco-packet-tracer/
│
├── 📁 labs/                    # ไฟล์แล็บทั้งหมด
│   ├── Week01/                 # Introduction to Cisco Packet Tracer
│   ├── Week02/                 # การทดสอบการตั้งค่า
│   ├── Week03/                 # Static IP และ Share IP
│   ├── Week04/                 # แล็บเพิ่มเติม
│   ├── Week06/                 # แล็บพื้นฐาน
│   ├── Week07/                 # VLAN Configuration
│   ├── Week08/                 # แล็บเพิ่มเติม
│   ├── Week09/                 # แล็บพื้นฐาน
│   └── Week10/                 # RIP Routing Protocol
│
├── 📁 docs/                    # เอกสารและคำสั่ง
│   ├── introduction.txt        # คำสั่ง Week 1
│   ├── vlan.txt                # คำสั่ง VLAN
│   └── text.txt                # คำสั่ง RIP
│
├── 📁 images/                  # รูปภาพและ screenshots
│   └── ...
│
└── 📁 examples/                # ไฟล์ตัวอย่างเพิ่มเติม
    └── ...
```

---

## 🎯 เนื้อหาการเรียนรู้

### Week 01: Introduction to Cisco Packet Tracer 🚀
**เริ่มต้นการเดินทางของคุณที่นี่!**

เรียนรู้พื้นฐานการใช้งาน Cisco Packet Tracer ตั้งแต่การเพิ่มอุปกรณ์ การเชื่อมต่อ และการตั้งค่า IP Address พื้นฐาน เหมาะสำหรับผู้เริ่มต้น

#### วัตถุประสงค์
- ทำความคุ้นเคยกับ Cisco Packet Tracer Interface
- เรียนรู้การเพิ่มและเชื่อมต่ออุปกรณ์พื้นฐาน
- เรียนรู้การตั้งค่า IP Address
- เรียนรู้คำสั่งพื้นฐานของ Router
- เรียนรู้การตรวจสอบการเชื่อมต่อ

#### เนื้อหาการเรียนรู้

**1. การใช้งาน Cisco Packet Tracer**
- Interface และ Tools พื้นฐาน
- การเพิ่มอุปกรณ์ (Devices)
- การเชื่อมต่อด้วยสาย (Connections)

**2. การตั้งค่า IP Address**
- การตั้งค่า IP บน PC
- การตั้งค่า IP บน Router Interface
- Subnet Mask และ Default Gateway

**3. คำสั่ง Router พื้นฐาน**
- Privileged Mode และ Configuration Mode
- การตั้งค่า Interface
- การเปิด/ปิด Interface

**4. การตรวจสอบการเชื่อมต่อ**
- คำสั่ง ping
- คำสั่ง show ต่างๆ
- การดูสถานะ Interface

#### แล็บที่แนะนำ

**Lab 1: Basic Network Setup**
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

**Lab 2: Router Configuration Practice**
ฝึกการตั้งค่า Router:
1. เข้าสู่ Privileged Mode: `enable`
2. เข้าสู่ Configuration Mode: `configure terminal`
3. ตั้งค่า Interface: `interface FastEthernet 0/0`
4. ตั้งค่า IP: `ip address 192.168.1.1 255.255.255.0`
5. เปิด Interface: `no shutdown`
6. ตรวจสอบ: `show ip interface brief`

#### คำสั่งที่ควรจำ
```
enable                          # เข้าสู่ privileged mode
configure terminal              # เข้าสู่ configuration mode
interface FastEthernet 0/0      # เลือก interface
ip address [IP] [Subnet]         # ตั้งค่า IP
no shutdown                     # เปิดใช้งาน interface
exit                            # ออกจาก mode ปัจจุบัน
show ip interface brief         # ดูสถานะ interface
ping [IP]                       # ทดสอบการเชื่อมต่อ
```

📂 [ดูรายละเอียดเพิ่มเติม Week 01 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week01/README.md) | 📄 [เอกสารคำสั่ง →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/docs/introduction.txt)

---

### Week 02: การทดสอบการตั้งค่า 🔍
**ตรวจสอบและแก้ไขปัญหาเครือข่าย**

ฝึกทักษะการตรวจสอบการตั้งค่าและการแก้ไขปัญหาเบื้องต้น เรียนรู้การใช้คำสั่ง diagnostic ต่างๆ

#### วัตถุประสงค์
- ทดสอบการตั้งค่าพื้นฐานของอุปกรณ์เครือข่าย
- ฝึกการตรวจสอบการทำงานของ network
- ทำความเข้าใจการตั้งค่า IP และการเชื่อมต่อ

#### เนื้อหาการเรียนรู้

**1. การทดสอบการตั้งค่า**
- การตรวจสอบการตั้งค่า IP Address
- การทดสอบการเชื่อมต่อระหว่างอุปกรณ์
- การใช้คำสั่งตรวจสอบสถานะ

**2. การแก้ไขปัญหาเบื้องต้น**
- การตรวจสอบการเชื่อมต่อสาย
- การตรวจสอบการตั้งค่า Interface
- การใช้คำสั่ง diagnostic

#### ไฟล์แล็บ
- `week2_test_config.pkt` - แล็บทดสอบการตั้งค่าพื้นฐาน

#### ขั้นตอนการทำแล็บ
1. เปิดไฟล์ `week2_test_config.pkt`
2. ตรวจสอบการตั้งค่า IP Address ของอุปกรณ์ทั้งหมด
3. ทดสอบการเชื่อมต่อด้วยคำสั่ง ping
4. ตรวจสอบสถานะ Interface ด้วย `show ip interface brief`
5. ตรวจสอบ routing table ด้วย `show ip route` (ถ้ามี Router)

#### คำสั่งที่ใช้
```
show ip interface brief         # ดูสถานะ interface ทั้งหมด
show running-config             # ดูการตั้งค่าปัจจุบัน
ping [IP Address]               # ทดสอบการเชื่อมต่อ
traceroute [IP Address]         # ติดตามเส้นทางของ packet
show ip route                   # ดู routing table
```

#### การตรวจสอบ
- ✅ ทุกอุปกรณ์สามารถ ping ถึงกันได้
- ✅ Interface ทั้งหมดมีสถานะ UP
- ✅ IP Address ถูกตั้งค่าถูกต้อง
- ✅ Default Gateway ถูกตั้งค่าถูกต้อง

📂 [ดูรายละเอียดเพิ่มเติม Week 02 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week02/README.md)

---

### Week 03: Static IP และ Share IP 🌐
**จัดการ IP Address อย่างมืออาชีพ**

เรียนรู้การตั้งค่า Static IP Address และการแชร์ IP Address ด้วย NAT/PAT เพื่อให้เครือข่ายภายในสามารถเข้าถึงอินเทอร์เน็ตได้

#### วัตถุประสงค์
- เรียนรู้การตั้งค่า Static IP Address
- เรียนรู้การแชร์ IP Address (NAT/PAT)
- ทำความเข้าใจความแตกต่างระหว่าง Static IP และ Dynamic IP
- เรียนรู้การตั้งค่า Network Address Translation (NAT)

#### เนื้อหาการเรียนรู้

**1. Static IP Configuration**
- การตั้งค่า IP Address แบบ Static
- การตั้งค่า Subnet Mask และ Default Gateway
- การตั้งค่า DNS Server

**2. IP Sharing (NAT/PAT)**
- Network Address Translation (NAT)
- Port Address Translation (PAT)
- การแชร์ IP Address ระหว่างเครือข่าย

#### ไฟล์แล็บ
- `week03_ex01_StaticIP.pkt` - แล็บการตั้งค่า Static IP
- `week03_ex02_ShareIP.pkt` - แล็บการแชร์ IP Address

#### ขั้นตอนการทำแล็บ

**Lab 1: Static IP Configuration**
1. เปิดไฟล์ `week03_ex01_StaticIP.pkt`
2. ตั้งค่า Static IP Address ให้กับทุกอุปกรณ์
3. ตั้งค่า Default Gateway ให้ถูกต้อง
4. ทดสอบการเชื่อมต่อด้วย ping

**Lab 2: IP Sharing (NAT)**
1. เปิดไฟล์ `week03_ex02_ShareIP.pkt`
2. ตั้งค่า NAT บน Router
3. ตรวจสอบการทำงานของ NAT
4. ทดสอบการเชื่อมต่อจากภายในไปภายนอก

#### คำสั่งที่ใช้

**Static IP Configuration**
```
interface FastEthernet 0/0
ip address [IP] [Subnet Mask]
no shutdown
```

**NAT Configuration**
```
# กำหนด inside interface
interface FastEthernet 0/0
ip nat inside
exit

# กำหนด outside interface
interface Serial 0/0/0
ip nat outside
exit

# สร้าง NAT pool (ถ้าต้องการ)
ip nat pool [pool-name] [start-ip] [end-ip] netmask [subnet]
ip nat inside source list [ACL-number] pool [pool-name]

# หรือใช้ PAT (overload)
ip nat inside source list [ACL-number] interface [interface] overload
```

**การตรวจสอบ NAT**
```
show ip nat translations        # ดู NAT translation table
show ip nat statistics          # ดูสถิติ NAT
debug ip nat                    # debug NAT (ใช้ใน privileged mode)
```

#### การตรวจสอบ
- ✅ ทุกอุปกรณ์มี Static IP Address ที่ถูกต้อง
- ✅ NAT ทำงานถูกต้อง (ถ้ามี)
- ✅ อุปกรณ์ภายในสามารถเชื่อมต่อภายนอกได้
- ✅ การ translate IP Address ทำงานถูกต้อง

📂 [ดูรายละเอียดเพิ่มเติม Week 03 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week03/README.md)

---

### Week 04: แล็บเพิ่มเติม 💡
**ทบทวนและฝึกฝน**

แล็บเพิ่มเติมสำหรับทบทวนความรู้ที่เรียนมาและฝึกทักษะการแก้ไขปัญหาที่ซับซ้อนขึ้น

#### วัตถุประสงค์
- ฝึกทักษะการตั้งค่าเครือข่ายเพิ่มเติม
- ทบทวนความรู้ที่เรียนมา
- เรียนรู้การแก้ไขปัญหาที่ซับซ้อนขึ้น

#### เนื้อหาการเรียนรู้

**1. การตั้งค่าเครือข่ายที่ซับซ้อน**
- การเชื่อมต่อหลายเครือข่าย
- การตั้งค่า Router หลายตัว
- การจัดการ Subnet หลายตัว

**2. การแก้ไขปัญหา**
- การวินิจฉัยปัญหาการเชื่อมต่อ
- การตรวจสอบการตั้งค่า
- การแก้ไขข้อผิดพลาด

#### ไฟล์แล็บ
- `LAB_28122021.pkt` - แล็บวันที่ 28 ธันวาคม 2021
- `LAB28112021.pkt` - แล็บวันที่ 28 พฤศจิกายน 2021
- `test.pkt` - แล็บทดสอบ

#### ขั้นตอนการทำแล็บ
1. เปิดไฟล์แล็บที่ต้องการทำ
2. ศึกษาโครงสร้างเครือข่าย
3. ตรวจสอบการตั้งค่าปัจจุบัน
4. ตั้งค่าตามที่กำหนด (ถ้ามี)
5. ทดสอบการเชื่อมต่อ
6. แก้ไขปัญหาที่พบ

#### คำสั่งที่ใช้
```
# การตรวจสอบ
show ip interface brief
show running-config
show ip route
show cdp neighbors

# การตั้งค่า
configure terminal
interface [interface]
ip address [IP] [Subnet]
no shutdown

# การทดสอบ
ping [IP]
traceroute [IP]
```

📂 [ดูรายละเอียดเพิ่มเติม Week 04 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week04/README.md)

---

### Week 06: แล็บพื้นฐาน 📚
**ทบทวนพื้นฐานเครือข่าย**

ทบทวนความรู้พื้นฐานเกี่ยวกับเครือข่าย การตั้งค่าอุปกรณ์ และการทำงานของเครือข่าย

#### วัตถุประสงค์
- ทบทวนความรู้พื้นฐานเกี่ยวกับเครือข่าย
- ฝึกทักษะการตั้งค่าอุปกรณ์เครือข่าย
- ทำความเข้าใจการทำงานของเครือข่ายพื้นฐาน

#### เนื้อหาการเรียนรู้

**1. Network Fundamentals**
- การเชื่อมต่ออุปกรณ์เครือข่าย
- การตั้งค่า IP Address
- การทดสอบการเชื่อมต่อ

**2. Device Configuration**
- การตั้งค่า Router
- การตั้งค่า Switch
- การตั้งค่า End Devices

#### ไฟล์แล็บ
- `W6LAB01.pkt` - แล็บพื้นฐาน Week 6

#### ขั้นตอนการทำแล็บ
1. เปิดไฟล์ `W6LAB01.pkt`
2. ศึกษาโครงสร้างเครือข่าย
3. ตรวจสอบการตั้งค่าปัจจุบัน
4. ตั้งค่าตามที่กำหนด
5. ทดสอบการเชื่อมต่อระหว่างอุปกรณ์
6. ตรวจสอบการทำงานของเครือข่าย

#### คำสั่งที่ใช้
```
# Router Configuration
enable
configure terminal
interface FastEthernet 0/0
ip address [IP] [Subnet Mask]
no shutdown
exit

# การตรวจสอบ
show ip interface brief
show running-config
show ip route

# การทดสอบ
ping [IP Address]
```

📂 [ดูรายละเอียดเพิ่มเติม Week 06 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week06/README.md)

---

### Week 07: VLAN Configuration 🏢
**แยกเครือข่ายแบบลอจิก**

เรียนรู้การสร้างและจัดการ VLAN (Virtual LAN) เพื่อแยกเครือข่ายแบบลอจิกโดยไม่ต้องแยกทางกายภาพ และการเชื่อมต่อระหว่าง VLAN ด้วย Router-on-a-Stick

#### วัตถุประสงค์
- เรียนรู้การสร้างและจัดการ VLAN (Virtual LAN)
- เรียนรู้การตั้งค่า VLAN บน Switch
- เรียนรู้การเชื่อมต่อระหว่าง VLAN (Inter-VLAN Routing)
- ทำความเข้าใจประโยชน์ของ VLAN

#### เนื้อหาการเรียนรู้

**1. VLAN Basics**
- ความหมายและประโยชน์ของ VLAN
- การแยกเครือข่ายแบบลอจิก
- VLAN ID และ VLAN Name

**2. VLAN Configuration**
- การสร้าง VLAN
- การกำหนด Port ให้กับ VLAN
- การตั้งค่า Trunk Port
- การตั้งค่า Access Port

**3. Inter-VLAN Routing**
- การเชื่อมต่อระหว่าง VLAN ด้วย Router
- Router-on-a-Stick Configuration
- การตั้งค่า Sub-interface

#### ไฟล์แล็บ
- `W7LAB01.pkt` - แล็บ VLAN พื้นฐาน
- `W7LAB02.pkt` - แล็บ VLAN ขั้นสูง
- `W7LAB03.pkt` - แล็บ Inter-VLAN Routing
- `ExtraClass_VLAN.pkt` - แล็บเพิ่มเติม VLAN

#### ขั้นตอนการทำแล็บ

**Lab 1: Basic VLAN Configuration**
1. เปิดไฟล์ `W7LAB01.pkt`
2. สร้าง VLAN ใหม่
3. กำหนด Port ให้กับ VLAN
4. ทดสอบการเชื่อมต่อภายใน VLAN เดียวกัน

**Lab 2: Multiple VLANs**
1. เปิดไฟล์ `W7LAB02.pkt`
2. สร้าง VLAN หลายตัว
3. กำหนด Port ให้กับ VLAN ที่เหมาะสม
4. ทดสอบการแยกเครือข่าย

**Lab 3: Inter-VLAN Routing**
1. เปิดไฟล์ `W7LAB03.pkt`
2. ตั้งค่า Router-on-a-Stick
3. สร้าง Sub-interface สำหรับแต่ละ VLAN
4. ทดสอบการเชื่อมต่อระหว่าง VLAN

#### คำสั่งที่ใช้

**สร้าง VLAN**
```
configure terminal
vlan [VLAN-ID]
name [VLAN-NAME]
exit
```

**กำหนด Port ให้กับ VLAN**
```
configure terminal
interface FastEthernet 0/[port-number]
switchport mode access
switchport access vlan [VLAN-ID]
no shutdown
exit
```

**ตั้งค่า Trunk Port**
```
configure terminal
interface FastEthernet 0/[port-number]
switchport mode trunk
switchport trunk allowed vlan [VLAN-IDs]
no shutdown
exit
```

**Router-on-a-Stick (Inter-VLAN Routing)**
```
configure terminal
interface FastEthernet 0/0.[VLAN-ID]
encapsulation dot1Q [VLAN-ID]
ip address [IP] [Subnet Mask]
no shutdown
exit
```

**การตรวจสอบ VLAN**
```
show vlan                    # ดู VLAN ทั้งหมด
show vlan brief              # ดู VLAN แบบย่อ
show interfaces switchport    # ดูการตั้งค่า switchport
show interfaces trunk        # ดู trunk port
```

#### การตรวจสอบ
- ✅ VLAN ถูกสร้างและตั้งค่าถูกต้อง
- ✅ Port ถูกกำหนดให้กับ VLAN ที่ถูกต้อง
- ✅ อุปกรณ์ใน VLAN เดียวกันสามารถสื่อสารกันได้
- ✅ อุปกรณ์ใน VLAN ต่างกันไม่สามารถสื่อสารกันได้ (ถ้าไม่มี Router)
- ✅ Inter-VLAN Routing ทำงานถูกต้อง (ถ้ามี Router)

📂 [ดูรายละเอียดเพิ่มเติม Week 07 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week07/README.md) | 📄 [คำสั่ง VLAN →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/docs/vlan.txt)

---

### Week 08: แล็บเพิ่มเติม 🎓
**ฝึกฝนขั้นสูง**

แล็บเพิ่มเติมสำหรับฝึกทักษะการตั้งค่าเครือข่ายที่ซับซ้อนและการแก้ไขปัญหาขั้นสูง

#### วัตถุประสงค์
- ฝึกทักษะการตั้งค่าเครือข่ายเพิ่มเติม
- ทบทวนความรู้ที่เรียนมา
- เรียนรู้การแก้ไขปัญหาที่ซับซ้อนขึ้น

#### เนื้อหาการเรียนรู้

**1. Advanced Network Configuration**
- การตั้งค่าเครือข่ายที่ซับซ้อน
- การจัดการหลายเครือข่าย
- การแก้ไขปัญหาขั้นสูง

**2. Network Troubleshooting**
- การวินิจฉัยปัญหาการเชื่อมต่อ
- การใช้คำสั่ง diagnostic
- การแก้ไขข้อผิดพลาด

#### ไฟล์แล็บ
- `EXTRA_W8LAB01.pkt` - แล็บเพิ่มเติม Week 8

#### ขั้นตอนการทำแล็บ
1. เปิดไฟล์ `EXTRA_W8LAB01.pkt`
2. ศึกษาโครงสร้างเครือข่าย
3. ตรวจสอบการตั้งค่าปัจจุบัน
4. ตั้งค่าตามที่กำหนด
5. ทดสอบการเชื่อมต่อ
6. แก้ไขปัญหาที่พบ

#### คำสั่งที่ใช้
```
# การตรวจสอบ
show ip interface brief
show running-config
show ip route
show cdp neighbors
show vlan

# การตั้งค่า
configure terminal
interface [interface]
ip address [IP] [Subnet]
no shutdown

# การทดสอบ
ping [IP]
traceroute [IP]
```

📂 [ดูรายละเอียดเพิ่มเติม Week 08 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week08/README.md)

---

### Week 09: แล็บพื้นฐาน 🔧
**ทบทวนและเสริมสร้าง**

ทบทวนความรู้พื้นฐานและเสริมสร้างทักษะการตั้งค่าเครือข่ายและการแก้ไขปัญหา

#### วัตถุประสงค์
- ทบทวนความรู้พื้นฐานเกี่ยวกับเครือข่าย
- ฝึกทักษะการตั้งค่าอุปกรณ์เครือข่าย
- ทำความเข้าใจการทำงานของเครือข่าย

#### เนื้อหาการเรียนรู้

**1. Network Configuration Review**
- การตั้งค่า IP Address
- การตั้งค่า Router
- การตั้งค่า Switch
- การทดสอบการเชื่อมต่อ

**2. Network Troubleshooting**
- การตรวจสอบการตั้งค่า
- การแก้ไขปัญหาเบื้องต้น
- การใช้คำสั่ง diagnostic

#### ไฟล์แล็บ
- `W09LAB1.pkt` - แล็บพื้นฐาน Week 9

#### ขั้นตอนการทำแล็บ
1. เปิดไฟล์ `W09LAB1.pkt`
2. ศึกษาโครงสร้างเครือข่าย
3. ตรวจสอบการตั้งค่าปัจจุบัน
4. ตั้งค่าตามที่กำหนด
5. ทดสอบการเชื่อมต่อระหว่างอุปกรณ์
6. ตรวจสอบการทำงานของเครือข่าย
7. แก้ไขปัญหาที่พบ

#### คำสั่งที่ใช้
```
# Router Configuration
enable
configure terminal
interface FastEthernet 0/0
ip address [IP] [Subnet Mask]
no shutdown
exit

# การตรวจสอบ
show ip interface brief
show running-config
show ip route
show cdp neighbors

# การทดสอบ
ping [IP Address]
traceroute [IP Address]
```

📂 [ดูรายละเอียดเพิ่มเติม Week 09 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week09/README.md)

---

### Week 10: RIP Routing Protocol 🛣️
**เรียนรู้ Dynamic Routing**

เรียนรู้การตั้งค่า RIP (Routing Information Protocol) ซึ่งเป็น Dynamic Routing Protocol ที่ Router ใช้แชร์ routing information กันอัตโนมัติ

#### วัตถุประสงค์
- เรียนรู้การตั้งค่า RIP (Routing Information Protocol)
- ทำความเข้าใจการทำงานของ Distance Vector Routing Protocol
- เรียนรู้การแชร์ routing information ระหว่าง Router
- เรียนรู้การตรวจสอบและแก้ไขปัญหา RIP

#### เนื้อหาการเรียนรู้

**1. RIP Basics**
- ความหมายและหลักการทำงานของ RIP
- Distance Vector Routing Protocol
- RIP Version 1 และ Version 2
- Administrative Distance และ Metric

**2. RIP Configuration**
- การเปิดใช้งาน RIP
- การประกาศ Network
- การตั้งค่า RIP Version
- การตรวจสอบ RIP

**3. RIP Troubleshooting**
- การตรวจสอบ RIP Routes
- การแก้ไขปัญหา RIP
- การใช้คำสั่ง debug

#### ไฟล์แล็บ
- `W10LAB01.pkt` - แล็บการตั้งค่า RIP

#### ขั้นตอนการทำแล็บ
1. เปิดไฟล์ `W10LAB01.pkt`
2. ศึกษาโครงสร้างเครือข่ายและ Router ทั้งหมด
3. ตั้งค่า IP Address ให้กับทุก Interface
4. เปิดใช้งาน RIP บน Router ทุกตัว
5. ประกาศ Network ที่เชื่อมต่ออยู่
6. ตรวจสอบ Routing Table
7. ทดสอบการเชื่อมต่อระหว่างเครือข่าย

#### คำสั่งที่ใช้

**การตั้งค่า RIP**
```
configure terminal
router rip
version 2                    # ใช้ RIP version 2 (ถ้าต้องการ)
network [network-address]    # ประกาศ network ที่เชื่อมต่ออยู่
no auto-summary             # ปิดการสรุปอัตโนมัติ (RIP v2)
exit
```

**การตรวจสอบ RIP**
```
show ip route                # ดู routing table
show ip protocols           # ดู routing protocol ที่ใช้งาน
show ip rip database        # ดู RIP database
debug ip rip                # debug RIP (ใช้ใน privileged mode)
```

**การตั้งค่า Interface**
```
configure terminal
interface FastEthernet 0/0
ip address [IP] [Subnet Mask]
no shutdown
exit
```

#### ตัวอย่างการตั้งค่า
```
Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# network 192.168.1.0
Router(config-router)# network 192.168.2.0
Router(config-router)# no auto-summary
Router(config-router)# exit
```

#### การตรวจสอบ
- ✅ RIP ทำงานบน Router ทุกตัว
- ✅ Network ถูกประกาศถูกต้อง
- ✅ Routing Table มี RIP routes
- ✅ อุปกรณ์ในเครือข่ายต่างกันสามารถสื่อสารกันได้
- ✅ Router แชร์ routing information กันได้

#### เปรียบเทียบ RIP กับ Static Routing
- **Static Routing**: ต้องตั้งค่าเองทุกเส้นทาง, ไม่มีการอัปเดตอัตโนมัติ
- **RIP**: เรียนรู้ routes อัตโนมัติ, มีการอัปเดตเป็นระยะ, เหมาะกับเครือข่ายขนาดเล็ก-กลาง

📂 [ดูรายละเอียดเพิ่มเติม Week 10 →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/labs/Week10/README.md) | 📄 [คำสั่ง RIP →](https://github.com/akkaraponph/lab-cisco-packet-tracer/blob/main/docs/text.txt)

---

## 📚 เอกสารอ้างอิง

ในโฟลเดอร์ `docs/` คุณจะพบเอกสารคำสั่งที่สำคัญ:

- 📄 **introduction.txt** - คำสั่งและขั้นตอนสำหรับ Week 1
- 📄 **vlan.txt** - คำสั่งการตั้งค่า VLAN
- 📄 **text.txt** - คำสั่งการตั้งค่า RIP

---

## 🚀 เริ่มต้นใช้งาน

### ข้อกำหนดเบื้องต้น

- **Cisco Packet Tracer** - ดาวน์โหลดได้จาก [Cisco Networking Academy](https://www.netacad.com/courses/packet-tracer)
- ความรู้พื้นฐานเกี่ยวกับเครือข่ายคอมพิวเตอร์ (แนะนำ)

### ขั้นตอนการใช้งาน

1. **ดาวน์โหลดหรือ Clone โปรเจกต์**
   ```bash
   git clone [repository-url]
   cd lab-cisco-packet-tracer
   ```

2. **เปิดไฟล์แล็บ**
   - เปิด Cisco Packet Tracer
   - เปิดไฟล์ `.pkt` จากโฟลเดอร์ `labs/WeekXX/`

3. **ศึกษาและทำตาม**
   - อ่าน README.md ในแต่ละ Week เพื่อเข้าใจวัตถุประสงค์
   - ทำตามขั้นตอนใน README.md
   - ดูเอกสารใน `docs/` สำหรับคำสั่งที่เกี่ยวข้อง

4. **ทดสอบและตรวจสอบ**
   - ใช้คำสั่ง `ping` เพื่อทดสอบการเชื่อมต่อ
   - ใช้คำสั่ง `show` เพื่อตรวจสอบการตั้งค่า
   - ใช้ Simulation Mode เพื่อดูการทำงานของ packets

---

## 💡 Tips & Tricks

### สำหรับผู้เริ่มต้น
- เริ่มจาก Week 01 เพื่อทำความคุ้นเคยกับ Cisco Packet Tracer
- อ่าน README.md ในแต่ละ Week ก่อนเริ่มทำแล็บ
- ใช้ Help (?) ใน Cisco Packet Tracer เพื่อดูคำสั่งที่ใช้ได้

### สำหรับผู้มีประสบการณ์
- ดูไฟล์ในโฟลเดอร์ `examples/` สำหรับแล็บเพิ่มเติม
- ทดลองแก้ไขและปรับแต่งแล็บเพื่อเรียนรู้เพิ่มเติม
- ใช้ Simulation Mode เพื่อเข้าใจการทำงานของ protocols

### คำสั่งที่ควรจำ
```bash
# การตรวจสอบ
show ip interface brief      # ดูสถานะ interface
show running-config          # ดูการตั้งค่าปัจจุบัน
show ip route                # ดู routing table

# การทดสอบ
ping [IP Address]            # ทดสอบการเชื่อมต่อ
traceroute [IP Address]      # ติดตามเส้นทาง

# การบันทึก
write memory                 # บันทึกการตั้งค่า
```

---

## 📸 Screenshots

ดูรูปภาพและ screenshots จากแล็บต่างๆ ในโฟลเดอร์ `images/`

---

## 🎓 ตัวอย่างเพิ่มเติม

ในโฟลเดอร์ `examples/` คุณจะพบแล็บเพิ่มเติมสำหรับฝึกฝน:
- การเปรียบเทียบ RIP กับ Static Routing
- แล็บ NAT และ DHCP
- และอีกมากมาย...

---

## ⚠️ หมายเหตุสำคัญ

- ไฟล์ทั้งหมดเป็นไฟล์ Cisco Packet Tracer (`.pkt`)
- ใช้ Cisco Packet Tracer เวอร์ชันที่รองรับเพื่อเปิดไฟล์
- เอกสารใน `docs/` เป็นคำสั่งพื้นฐานสำหรับการตั้งค่า
- แนะนำให้บันทึกการตั้งค่าทุกครั้งด้วย `write memory` หรือ `copy running-config startup-config`

---

## 🙏 ขอบคุณ

ขอบคุณที่สนใจโปรเจกต์นี้! คับผ๋ม หวังว่าแล็บเหล่านี้จะช่วยให้คุณเข้าใจการทำงานของเครือข่ายคอมพิวเตอร์มากขึ้น :)

**Happy Learning! 🎉**

---

*อัปเดตล่าสุด: 2026*
