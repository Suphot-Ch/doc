# Banana Pi BPI-CM6 vs BPI-M5 vs BPI-M7 — Spec & Price Comparison

**ตรวจสอบเมื่อ:** 2026-08-27 14:19 SEAST  
**แหล่งราคา:** BPI official shop (`bpi-shop.com`) — ราคาแสดงเป็น USD; ยังไม่รวม shipping/tax และอาจเปลี่ยนตาม stock/ตัวเลือกสินค้า

## สรุปเร็ว

| รุ่น | จุดเด่น | RAM / Storage | ราคาอ้างอิงจาก Official Shop |
|---|---|---:|---:|
| **BPI-M5** | SBC ราคาต่ำ, USB 3.0 x4, GbE, HDMI 4K | 4GB LPDDR4 / 16GB eMMC | **US$129** |
| **BPI-CM6** | Compute module RISC-V, industrial temperature, Wi‑Fi 6/BT 5.2 | 4/8/16GB LPDDR4; 8/16/32/128GB eMMC | **US$140 core board**, **US$19 IO**, **US$159 ชุด core+IO** |
| **BPI-M7** | RK3588, NPU 6 TOPS, dual 2.5GbE, 8K, M.2 PCIe | 4/8/32GB; 32/64/128GB eMMC ตามตัวเลือก | **US$255–312** ตาม configuration |

## เปรียบเทียบสเปกหลัก

| รายการ | BPI-CM6 | BPI-M5 | BPI-M7 |
|---|---|---|---|
| SoC / CPU | SpacemiT K1, octa-core 64-bit RISC-V X60; RV64GCVB, RVA22, RVV1.0 | Amlogic S905X3, quad-core Cortex-A55 ~2.0GHz | Rockchip RK3588; 4× Cortex-A76 @2.4GHz + 4× Cortex-A55 @1.8GHz, 8nm |
| AI / NPU | 2.0 TOPS จาก RISC-V core | ไม่ระบุ NPU ในหน้าสเปก | NPU สูงสุด 6 TOPS INT8; รองรับ INT4/INT8/INT16 mixed |
| GPU | IMG BXE-2-32 @819MHz; OpenGL ES 3.2 / OpenCL 3.0 / Vulkan 1.3 | Mali-G31 MP2 @650MHz | ARM Mali-G610 MP4 |
| RAM | 4/8/16GB LPDDR4; default 4GB | 4GB LPDDR4 | 8/16/32GB LPDDR4/LPDDR4x; default 8GB (หน้าร้านมีตัวเลือก 4GB ด้วย) |
| On-board storage | 8/16/32/128GB eMMC; default 16GB | 16GB eMMC; รองรับ MicroSD สูงสุด 256GB และระบุ eMMC สูงสุด 64GB | หน้า docs ระบุ 64/128GB default 64GB; ตาราง hardware ระบุ 32/64/128GB — ต้องยืนยันกับ SKU |
| Network | RTL8211F PHY / RGMII; Wi‑Fi 6 + BT 5.2 onboard | 10/100/1000 Ethernet; Wi‑Fi เป็น expansion/USB dongle | 2× 2.5GbE; Wi‑Fi 6 + BT 5 onboard |
| USB | Core: 1× USB 3.0 + 2× USB 2.0; IO board เพิ่ม USB-A/USB-C | 4× USB 3.0 | 1× USB 3.0, 1× USB-C 3.1 DP/OTG, 1× USB 2.0 |
| Video out | Core: HDMI 1.4 + MIPI DSI; รายละเอียดขึ้นกับ carrier/IO | 1× HDMI 2.1 สูงสุด 4K@60 HDR | HDMI 2.1 สูงสุด 8K@60; MIPI DSI สูงสุด 4K@60; DP 1.4 สูงสุด 8K@30 |
| Camera | Core 3× MIPI CSI; IO board 2× CSI 4-lane | ไม่ระบุในสรุป hardware spec | 2× MIPI CSI แบบ 4-lane สูงสุด 2.5Gbps/lane |
| Expansion | Core 5-lane PCIe 2.1; IO board 2× M.2 M-Key แบบ 2-lane, 26-pin GPIO | 40-pin GPIO; UART/I²C/SPI/PWM | 40-pin Raspberry Pi-compatible; UART/SPI/I²C/I²S/PWM/ADC |
| Power | IO board: 12V DC-in; ต้องดู carrier/IO ที่ใช้ | 5V @3A ผ่าน USB Type-C ตาม docs | USB-C PD 2.0: 9V/2A, 12V/2A, 15V/2A |
| ขนาด | Core 40×55mm; IO board 56×85mm | 85×56mm; 48g | 92×62mm; 46.6g |
| Operating temperature | **-40°C ถึง 85°C** | ไม่ระบุในหน้าหลัก | 0°C ถึง 80°C |
| OS / software | Bianbu, Debian 13 image, Armbian; kernel/u-boot/OpenSBI sources ระบุใน docs | Android 9, Ubuntu 20.04, Debian 10, Armbian และ images อื่น ๆ | Android 12, Debian 11, Buildroot; Armbian/Ubuntu และ images จากผู้ผลิต/ชุมชน |

## ราคาตาม configuration

### BPI-M7

| Configuration | ราคา |
|---|---:|
| 4GB LPDDR4 + 32GB eMMC | **US$255** |
| 32GB LPDDR4x + 128GB eMMC | **US$257** |
| 8GB LPDDR4x + 64GB eMMC | **US$312** |

### BPI-CM6

| Package | ราคา |
|---|---:|
| CM6 core board | **US$140** |
| CM6 IO board | **US$19** |
| Core board + IO board | **US$159** |

### BPI-M5

| Configuration | ราคา |
|---|---:|
| BPI-M5 product page (4GB LPDDR4 / 16GB eMMC ตาม docs) | **US$129** |

## ข้อสังเกตสำคัญจากการตรวจเอกสาร

1. **M7 มีข้อมูล storage ไม่ตรงกันในหน้าเดียวกัน:** Overview/Key Parameter ระบุ 64/128GB แต่ Hardware Specifications ระบุ 32/64/128GB; ควรยึด SKU จริงก่อนสั่งซื้อ
2. **CM6 เป็น compute module ไม่ใช่ SBC เดี่ยวแบบ M5/M7:** ถ้าต้องการพอร์ตใช้งานจริง ต้องบวก CM6 IO หรือ carrier board ที่เข้ากันได้
3. **M5 เหมาะกับงานทั่วไปและคุ้มราคา:** แต่ Wi‑Fi/BT ไม่ได้ onboard ใน hardware table; ต้องใช้ expansion board หรือ USB
4. **M7 เหมาะกับ AI/video/networking หนัก:** มี NPU 6 TOPS, 8K codec, dual 2.5GbE และ M.2 PCIe
5. **CM6 เหมาะกับ industrial/edge integration:** RISC-V, อุณหภูมิ -40 ถึง 85°C และออกแบบเป็น module พร้อม board-to-board connector

## Sources

- CM6 documentation: https://docs.banana-pi.org/en/BPI-CM6/BananaPi_BPI-CM6
- M5 documentation: https://docs.banana-pi.org/en/BPI-M5/BananaPi_BPI-M5
- M7 documentation: https://docs.banana-pi.org/en/BPI-M7/BananaPi_BPI-M7
- CM6 official shop: https://www.bpi-shop.com/products/banana-pi-bpi-cm6-spacemit-k1-8-core-risc-v.html
- M5 official shop: https://www.bpi-shop.com/products/banana-pi-bpi-m5.html
- M7 official shop: https://www.bpi-shop.com/products/banana-pi-bpi-m7-with-rockchip-rk3588-8-16-32g-ram-64-128g-emmc-wifi6-support.html

> ราคาถูกดึงจาก structured product offers ที่หน้า official shop แสดง ณ เวลาตรวจสอบ ไม่ใช่ใบเสนอราคา และควรตรวจซ้ำก่อนจัดซื้อ
