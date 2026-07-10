# ESP32-C3 Alarm Clock

A small bedside alarm clock built with an LOLA ESP32-C3, with a TFT display, Wi-Fi time sync, a buzzer, physical buttons, and uses an on-device menu.

When you connect the clock to a 3.3V power source, the clock connects to Wi-Fi and pulls the current time from an NTP server, so it never needs to be set by hand. The screen shows the time, the date, and whether the alarm is currently armed. From there, the buttons control the following: opening the menu, adjusting the alarm time, flipping between display modes (12/24 HRS), and snoozing when the alarm rings.

## Features
- Syncs its clock over Wi-Fi using NTP
- Shows a large, easy-to-read time display on the TFT screen.
- Lets you enable or disable the alarm with one button.
- Has a snooze button for when you're not ready to get up.
- Switches between 12-hour and 24-hour display.
- Uses a simple button-based menu to navigate everything.
- Rings a piezo buzzer when the alarm goes off.
- Fits into a compact enclosure — this was designed to sit on a nightstand, not take one over.

## Hardware
- 1x Lolin C3 Mini ESP32 dev board
- 1x 2.25" TFT display (ST7789)
- 1x 3.3V piezo buzzer
- 1x PCB Breadboard
- 6x push buttons
- Jumper wires

## Software
- Arduino IDE
- Adafruit GFX
- Adafruit ST7789

## Case
A 3d printed case built to house the hardware (the PCB breadboard, ESP32, TFT Display, buzzer and jumper wires).

## Wiring

### TFT display

Display pin | ESP32-C3 pin

- VCC - 3.3V 
- GND - GND
- SCL - GPIO 6
- SDA - GPIO 7
- RES - GPIO 10
- DC - GPIO 8
- CS - GPIO 20
- BL - 3.3V

### Buzzer
- Positive lead - GPIO 21
- Negative lead - GND

### Buttons

Button | GPIO

- UP - 0
- DOWN - 1
- LEFT - 3
- RIGHT - 4
- OK - 5
- SNOOZE - 18

## Controls

- **OK** — open the menu / confirm a selection
- **UP / DOWN** — move through menu items
- **LEFT** — toggle 12-hour / 24-hour mode (outside the menu)
- **RIGHT** — toggle the alarm on or off (outside the menu)
- **SNOOZE** — snooze the alarm while it's ringing
- **UP** — stop the alarm while it's ringing

## Project structure

- `firmware/` — source code for the ESP32
- `cad/` — case and assembly files
- `wiring/` — wiring diagram / schematic
- `images/` — photos and screenshots
- `bom.csv` — bill of materials

## Bill of materials

| Item | Quantity | Notes |
|---|---|---|
| ESP32-C3 dev board | 1 | Lolin C3 Mini |
| TFT display | 1 | 2.25" ST7789 |
| Piezo buzzer | 1 | 3.3V |
| Push buttons | 6 | Momentary switches |
| Jumper wires | 1 set | Male/male, male/female, female/female |
| Case | 1 | 3D printed or custom enclosure |

## Journaling
- `JOURNALING.md`
