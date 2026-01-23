# Bill of Materials

AlohaMini follows the same architecture and terminology as LeKiwi, consisting of a Client side and a Host side.

- The Client handles computation and control.
- The Host executes commands and returns observations.

This is also commonly referred to as PC side vs. Remote side, and both naming conventions are equivalent.

AlohaMini’s Client hardware includes the mobile base and two follower arms. The arms directly reuse the SO-ARM100 design. Therefore, if you already have two SO-ARM100 arms, you only need to assemble the mobile base. Communication between the mobile base, arms, and Raspberry Pi 5 uses the same bus-servo communication system, and the build guide will explain the wiring in detail.

On AlohaMini, the Host side consists of a PC workstation and leader arms. VR controllers or other devices can also replace the leader arms, and we will release compatible controller kits soon. For beginners, we recommend starting with leader-arm teleoperation.

*Note: Table clamp, screwdriver set, soldering iron, and other common tools can be sourced as needed and are not listed in the tables below.*

## Mobile base 

| Item | Model / Notes | Qty | Unit Cost (US) | Buy (US) | Unit Cost (CN) | Buy (CN) | Unit Cost (IN) | Buy (IN) |
|------|---------------|-----|----------------|----------|----------------|----------|
| Servo motor | Feetech / 12V 1/345 Gear(STS3215-C018)| 4 | $13.89 | [Alibaba](https://www.alibaba.com/product-detail/Feetech-12V-1-345-STS3215-C018_1601637205886.html?spm=a2700.micro_product_manager.0.0.5d083e5fucb6WW) | ¥110 | [taobao](https://item.taobao.com/item.htm?id=996544351583&spm=a213gs.v2success.0.0.73c04831naDrHP) | ₹1,500 | [Robu.in](https://robu.in/) |
| Omni wheel | 4″ (≈100 mm) | 3 | $47 | [Amazon](https://www.amazon.com/Replacement-Plastic-Directional-Accessories-Platform/dp/B0F9W6QX5M/ref=sr_1_1?crid=RUB7HLFVFAW4&dib=eyJ2IjoiMSJ9.OEVluSHnKdSoUssYPqqvc9zDttA_kPqToxcIUPC9mVE.lDKJEFZ-n8SldCgHwC__Ikus8FGKxQcuN14cjtG5WHQ&dib_tag=se&keywords=Omni-Directional+Wheels+4&qid=1762964120&sprefix=omni-directional+wheels+4%2Caps%2C938&sr=8-1) | ¥135 | [pinduoduo](https://mobile.yangkeduo.com/goods.html?ps=kKWPC7xuzw) | ₹210 | [Robu.in](https://robu.in/product/80mm-a-mecanum-wheel-compatible-with-6-7mm-coupling-pack-of-4-yellow/) |
| USB camera | 720p focal length 2.4 mm, 36×36 mm form factor | 3 | — | Amazon | ¥125 | [taobao](https://item.taobao.com/item.htm?id=666278411821) | ₹800 | [Robu.in](https://robu.in/) |
| (optional) Bearing | 12×18×4 mm (ID × OD × W) — wheel axle bearing | 3 | — | Amazon | ¥6 | [tmall](https://detail.tmall.com/item.htm?id=824704356695) | ₹50 | [Robu.in](https://robu.in/) |
| Bearing | 4×13×5 mm (ID × OD × W) — lift axis bearing | 8 | — | Amazon | ¥3 | [taobao](https://item.taobao.com/item.htm?id=565418362178) | ₹40 | [Robu.in](https://robu.in/) |
| M2×12 Phillips screw | For camera mounts (OB_T_Camera_Mount.stl, OB_Top_Camera_Mount) | 12 | — | — | — | — |
| M3×12 hex socket screw | Total 36 pcs (Servo Mount×24 ,Side Panel×12 ) | 36 | — | — | — | — |
| M3×18 hex socket screw | For OB_Chassis_Wheel_Axle_Connector.stl | 12 | — | — | — | — |
| M3×30 hex socket screw | For OB_T_Connector_Right/Left.stl | 8 | — | — | — | — |
| M3 hex nut | For OB_T_Connector_Right/Left.stl | 8 | — | — | — | — |
| M3x5x4 heat-set insert | Total 36 pcs (Servo Mount×24, Side Panel×12) | 36 | — | Amazon | ¥5 | [taobao](https://item.taobao.com/item.htm?id=809241671998) | ₹8 | [Robu.in](https://robu.in/product/heat-set-insert-m3x5x4-brass/) |
| M4×12 hex socket screw | Total 20 pcs (Bearing Cover×12, Z-axis Servo Mount×8) | 20 | — | Amazon | — | — |
| M4x6x5 heat-set insert | For OB_Chassis_Bearing_Cover.stl | 12 | — | Amazon | ¥4 | [taobao](https://item.taobao.com/item.htm?id=809241671998) | ₹10 | [Robu.in](https://robu.in/product/heat-set-insert-m4x6x5-brass/) |
| Adhesive | Epoxy (strongly recommended) / double-sided tape — cable retention & structural bonding | 1 | — | Amazon | ¥12 | [jd](https://item.jd.com/100141557259.html) | ₹200 | [Robu.in](https://robu.in/) |
| Servo extension cable | SCS 3-pin, 90 cm | 2 | — | [Alibaba](https://www.alibaba.com/product-detail/3P-5264-Interface-Bus-Actuator-Connection_1601635790774.html?spm=a2747.product_manager.0.0.5a3e71d2sTo6Ho) | ¥3 | [taobao](https://item.taobao.com/item.htm?id=616460581906) | ₹156 | [Robu.in](https://robu.in/product-category/dc-motors/motors/servo-motors/servo-motor-wire/jr-servo-cable/) |
| Battery | 12 V Li-ion pack with 5521 barrel jack (male & female); one pack for the Raspberry Pi 5, the other for the mobile base and follower arms.| 2 | $43 | [Amazon](https://www.amazon.com/KBT-Rechargeable-Connector-Replacement-Security/dp/B0C242DYT1/ref=sr_1_2_sspa?th=1) | ¥130 | [taobao](https://item.taobao.com/item.htm?id=890828103056) | ₹1,500 | [Robu.in](https://robu.in/) |
| USB Type-C cable | Only for testing the mobile base | 1 | $10 | [Amazon](https://www.amazon.com/Charging-etguuds-Charger-Braided-Compatible/dp/B0B8NWLLW2/?th=1) | ¥20 | [tmall](https://detail.tmall.com/item.htm?id=754024805047) | ₹250 | [Robu.in](https://robu.in/product-category/cables-and-connectors/usb-cables/) |
| Waveshare Bus Servo Controller | Only for testing the mobile base | 1 | $13 | [Amazon](https://www.amazon.com/Waveshare-Integrates-Control-Circuit-Supports/dp/B0CTMM4LWK/) | ¥27 | [tmall](https://detail.tmall.com/item.htm?id=738817173460) | ₹1,200 | [Robu.in](https://robu.in/) |
| 3D-printed parts | PLA/PETG/ABS (files in /hardware/mobile_base/stl) | ~4 kg filament | — | — | — | — |

**3D Printing Parts List:**
- OB_Chassis_Bearing_Cover x3
- OB_Chassis_Servo_Mount x3
- OB_Chassis_Side_Panel x3
- OB_Chassis_Wheel_Axle_Connector x3
- OB_Chassis_Wheel_Guard x3
- OB_Top_Camera_Back_Cover x2
- OB_Chassis_Shaft_Sleeve_12_24 x3
- O_Chassis_Dowel_Pin_12_37 x3
- All other files x1

Note：
All other parts — including the lift mechanism — can be printed on a standard 3D printer. Only the chassis is special, as it requires a build volume of at least 385 × 345 × 64 mm. We recommend choosing a machine with around 400 × 360 × 100 mm or larger. Due to its size, the chassis may need to be outsourced for printing.

### What the Base Can Do

With only the components above, you can assemble the **mobile base** and control:

- movement  
- vertical lift  

Use the following commands to control the base:
```bash
python examples/debug/wheels.py \
   --port /dev/ttyACM0

python examples/debug/axis.py \
   --port /dev/ttyACM0
```

Use W/S/A/D to drive the base, and U/J to raise or lower the lift — all directly from your PC, without installing any single-board computer on the robot.

More details will be provided in the software setup section.

Effect after assembly:

![Assembled AlohaMini mobile base](media/assembled.jpg)
### Standalone Mode (Optional)

If you prefer the base to operate as an **independent host system** (Wi‑Fi, untethered), add:


| Item | Model / Notes | Qty | Unit Cost (US) | Buy (US) | Unit Cost (CN) | Buy (CN) | Unit Cost (IN) | Buy (IN) |
|------|---------------|-----|----------------|----------|----------------|----------|
| Compute board | Raspberry Pi 5 (4GB/8GB) | 1 | $80 | [Adafruit](https://www.adafruit.com/product/5812) | ¥600 | [taobao](https://item.taobao.com/item.htm?id=688878446695) | ₹6,000 | [Robu.in](https://robu.in/product/raspberry-pi-5-8gb-ram/) |
| DC converter | 12V → 5V / 5A buck converter | 1 | $13 | [Amazon](https://www.amazon.com/Klnuoxj-Converter-Interface-Waterproof-Compatible/dp/B0CRVW7N2J?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&smid=A1QRG6NHEUKUZO&gQT=0&th=1) | ¥75 | [taobao](https://item.taobao.com/item.htm?id=800698078303) | ₹400 | [Robu.in](https://robu.in/) |
| Monitor | 7-inch HD IPS HDMI interface + touch + Type C power supply | 1 | — | Amazon | ¥291 | [taobao](https://item.taobao.com/item.htm?id=592070943040) | ₹3,000 | [Amazon.in](https://amazon.in) |


## Follower Arms
| Item | Model / Notes | Qty | Unit Cost (US) | Buy (US) | Unit Cost (CN) | Buy (CN) | Unit Cost (IN) | Buy (IN) |
|------|---------------|-----|----------------|----------|----------------|----------|
| Servo motor | Feetech / 12V 1/345 Gear(STS3215-C018) | 12 | $13.89 | [Alibaba](https://www.alibaba.com/product-detail/Feetech-12V-1-345-STS3215-C018_1601637205886.html?spm=a2700.micro_product_manager.0.0.5d083e5fucb6WW) | ¥110 | [taobao](https://item.taobao.com/item.htm?id=996544351583&spm=a213gs.v2success.0.0.73c04831naDrHP) | ₹1,500 | [Robu.in](https://robu.in/) |
| Waveshare Bus Servo Controller | For connecting to the Raspberry Pi 5 | 2 | $13 | [Amazon](amazon.com/Waveshare-Integrates-Control-Circuit-Supports/dp/B0CTMM4LWK/) | ¥27 | [tmall](https://detail.tmall.com/item.htm?id=738817173460) | ₹1,200 | [Robu.in](https://robu.in/) |
| USB camera | 720p focal length 3.8 mm, 32×32 mm form factor | 2 | — | Amazon | ¥103 | [taobao](https://item.taobao.com/item.htm?id=590682120464) | ₹800 | [Robu.in](https://robu.in/) |
| 1-to-2 DC splitter cable | 30 cm, 5521 connector — for powering the arms | 1 | — | Amazon | ¥5 | [taobao](https://item.taobao.com/item.htm?id=594921965049) | ₹5 | [Robu.in](https://robu.in/product/1-to-2-dc-splitter-cable-30cm-5521-connector/) |
| DC extension cable | 1.5 m, 5521 connector — for powering the arms | 2 | — | Amazon | ¥2.50 | [taobao](https://item.taobao.com/item.htm?id=43628177900) | ₹2.50 | [Robu.in](https://robu.in/product/dc-extension-cable-1-5m-5521-connector/) |
| USB Type-C cable | For connecting to the Raspberry Pi 5 | 2 | $10 | [Amazon](https://www.amazon.com/Charging-etguuds-Charger-Braided-Compatible/dp/B0B8NWLLW2/?th=1) | ¥20 | [tmall](https://detail.tmall.com/item.htm?id=754024805047) | ₹250 | [Robu.in](https://robu.in/product-category/cables-and-connectors/usb-cables/) |
| 3D-printed parts | PLA/PETG/ABS (files in /hardware/arms/stl) | 1 set | — | — | — | — |


**3D Printing Parts List:**
- All "D_*.stl" files: x2
- All "F_*.stl" files: x2

For detailed printing instructions, refer to the [SO-ARM100 project README](https://github.com/TheRobotStudio/SO-ARM100)



## Leader Arms
> **Note:** The official SO-ARM100 design uses three different gear ratios (1/147, 1/191, 1/345) for optimal performance. However, our testing shows that using a single gear ratio (1/147) provides excellent user experience and significantly simplifies assembly. The BOM below reflects this simplified configuration.

| Item | Model / Notes | Qty | Unit Cost (US) | Buy (US) | Unit Cost (CN) | Buy (CN) | Unit Cost (IN) | Buy (IN) |
|------|---------------|-----|----------------|----------|----------------|----------|
| Servo motor | Feetech / 7.4V 1/147 Gear(STS3215-C046) | 12 | $13.89 | [Alibaba](https://www.alibaba.com/product-detail/Feetech-STS3215-Servos-Feetech-7-4V_1601636218844.html?spm=a2700.micro_product_manager.0.0.5d083e5fucb6WW) | ¥99 | [taobao](https://item.taobao.com/item.htm?id=996544351583&spm=a213gs.v2success.0.0.73c04831naDrHP) | ₹1,400 | [Robu.in](https://robu.in/) |
| Waveshare Bus Servo Controller | For connecting to the PC | 2 | $13 | [Amazon](https://www.amazon.com/Waveshare-Integrates-Control-Circuit-Supports/dp/B0CTMM4LWK/) | ¥27 | [tmall](https://detail.tmall.com/item.htm?id=738817173460) | ₹1,200 | [Robu.in](https://robu.in/) |
| Battery | 5V Li-ion pack (5600mAh, DC 5521 connector) | 1 | — | Amazon | ¥30 | [taobao](https://item.taobao.com/item.htm?id=765749120668) | ₹300 | [Robu.in](https://robu.in/) |
| 1-to-2 DC splitter cable | 70 cm — for powering the arms | 1 | — | Amazon | ¥5 | [taobao](https://item.taobao.com/item.htm?id=594921965049) | ₹5 | [Robu.in](https://robu.in/product/1-to-2-dc-splitter-cable-70cm/) |
| USB Type-C cable | For connecting to the PC | 2 | $10 | [Amazon](https://www.amazon.com/Charging-etguuds-Charger-Braided-Compatible/dp/B0B8NWLLW2/?th=1) | ¥20 | [tmall](https://detail.tmall.com/item.htm?id=754024805047) | ₹250 | [Robu.in](https://robu.in/product-category/cables-and-connectors/usb-cables/) |
| 3D-printed parts | PLA/PETG/ABS (files in /hardware/arms/stl) | 1 set | — | — | — | — |

**3D Printing Parts List:**
- All "D_*.stl" files: x2
- All "L_*.stl" files: x2

For detailed printing instructions, refer to the [SO-ARM100 project README](https://github.com/TheRobotStudio/SO-ARM100)


