
# Wi-Fi Hacking Device with ESP8266

## Overview

This project demonstrates building a Wi-Fi hacking device using the ESP8266 board. The device can execute operations like Wi-Fi jamming, cloning, rogue AP creation, and Evil Twin attacks. Below are detailed steps, components, pin connections, and setup guidelines for the project.

---

## Components Used

| Component                              | Purpose                                      |
| -------------------------------------- | -------------------------------------------- |
| ESP8266 (Type C Board)                 | Mainboard for Wi-Fi hacking tasks            |
| 3 Push Buttons (with Caps)             | User interface control                       |
| Slide Switch                           | Power on/off control                         |
| 0.96" OLED Display                     | Visual interface                             |
| TP4056 Charging Module                 | Charging the Li-Po battery                   |
| DC-DC Step Up Boost Converter (MT3608) | Boosting 3.7V to 5V for powering the ESP8266 |
| Li-Po Battery (3.7V)                   | Power source                                 |
| NeoPixel LED                           | Visual feedback                              |
| External Antenna                       | Enhanced Wi-Fi signal performance            |

---

## Circuit Connections

### ESP8266 Pin Connections:

| Component            | ESP8266 Pin  |
| -------------------- | ------------ |
| OLED GND             | GND          |
| OLED VCC             | 3.3V         |
| OLED SCL             | GPIO 4 (D2)  |
| OLED SDA             | GPIO 5 (D1)  |
| NeoPixel GND         | GND          |
| NeoPixel VCC         | 3.3V         |
| NeoPixel DIN         | GPIO 9 (SD2) |
| Button (Down Signal) | GPIO 14 (D5) |
| Button (Up Signal)   | GPIO 12 (D6) |
| Button (OK Signal)   | GPIO 13 (D7) |

### Power Circuit Connections:

- **TP4056 Charging Module:**

  - `B+` to Li-Po battery positive
  - `B-` to Li-Po battery negative
  - `OUT+` to Boost Converter `IN+`
  - `OUT-` to Boost Converter `IN-`

- **Boost Converter (MT3608):**

  - `OUT+` to ESP8266 VIN
  - `OUT-` to ESP8266 GND

### Additional Connections:

- **Slide Switch:**
  - Connected between the battery and TP4056 module for power control.

### Antenna:

- Soldered directly to the antenna side of the ESP8266 board.

---

## Features

1. **Wi-Fi Jamming:**
   - Disrupts nearby Wi-Fi signals on the 2.4 GHz band.
2. **Rogue Access Point:**
   - Creates a fake Wi-Fi network to capture client data.
3. **Evil Twin Attack:**
   - Mimics legitimate networks to lure users into connecting.
4. **User-Friendly Interface:**
   - Controlled via three large push buttons with caps for navigation.
5. **Compact Design:**
   - Portable and powered by a Li-Po battery with efficient power management.

---

## Project Workflow

1. Assemble the components on a perfboard as per the circuit diagram.
2. Solder all connections carefully to ensure proper conductivity.
3. Install the necessary firmware onto the ESP8266 for Wi-Fi hacking capabilities.
4. Test each function, such as jamming and creating a rogue access point.
5. Mount the assembly in a suitable enclosure for durability and portability.

---

## Diagrams

### Block Diagram:

```
Li-Po Battery --> TP4056 Charging Module --> Boost Converter (MT3608) --> ESP8266
                                                  |
                                    Buttons, OLED, NeoPixel
```

---

## Notes

- Ensure proper insulation between connections to avoid short circuits.
- Use heat shrink tubing where necessary for safety.
- Be mindful of the legal implications of using Wi-Fi hacking devices and ensure ethical use.
