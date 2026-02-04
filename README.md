# HIDDeck
🎯 What is HIDDeck?  HIDDeck ek hardware-based USB keyboard automation device hai jo SD card se scripts read karta hai aur computer pe automatically keystrokes type karta hai — bilkul real keyboard ki tarah.  Device plug karte hi system ise USB keyboard samajhta hai.

🎯 What is HIDDeck?

HIDDeck ek hardware-based USB keyboard automation device hai jo SD card se scripts read karta hai aur computer pe automatically keystrokes type karta hai — bilkul real keyboard ki tarah.

Device plug karte hi system ise USB keyboard samajhta hai.

🧩 Hardware You’re Using
Component	Role
Arduino Leonardo / CJMCU ATmega32u4	Main controller + USB HID
SD Card Module	Script storage
Micro SD Card (FAT32)	Payload files
LED (Pin 13)	Status indicator
Jumper wires	Script selection
⚙️ How HIDDeck Works

Device USB se power leta hai.

LED ON hoti hai (device active).

SD card initialize hoti hai.

Pins check hote hain to decide which script run karni hai.

Device USB keyboard ban kar commands type karta hai.

Script complete → LED OFF.

🎛️ Script Selection (Important)

HIDDeck me multiple scripts ek hi device me rakh sakte ho.

Pin State	Script Executed
Pin 0 (RX) → GND	script1.txt
Pin 1 (TX) → GND	script2.txt
Pin 2 (SDA) → GND	script3.txt
No pin grounded	script0.txt (default)

👉 Matlab jumper laga ke behavior change kar sakte ho — reprogram ki zarurat nahi.

📁 SD Card Setup

SD card ko FAT32 me format karo

Root directory me files rakho:

script0.txt
script1.txt
script2.txt
script3.txt
