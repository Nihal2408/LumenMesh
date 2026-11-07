
This project is licensed under the **MIT License** — feel free to modify, print, and adapt it for your own setups!<img width="1671" height="988" alt="Screenshot 2026-11-07 at 11 44 23 AM" src="https://github.com/user-attachments/assets/4dc0f715-7797-46e2-9ceb-576114d7dd75" />
<img width="1671" height="988" alt="Screenshot 2026-11-07 at 11 44 06 AM" src="https://github.com/user-attachments/assets/98b48549-f4c0-4428-b3c7-2e3ae21c775b" />

# LumenMesh · 3D-Printed Ambient Pixel Lamp

A modern, desktop accent lamp featuring parametric surface texturing, custom internal electronics integration, and a sleek two-piece snap-fit assembly. Designed from the ground up in Autodesk Fusion 360 specifically for FDM additive manufacturing.

---

## 🌟 Overview

The **LumenMesh / LED Pixel Lamp** combines functional industrial design with atmospheric lighting. The project consists of two primary 3D-printed sub-assemblies:
1. **The Base Enclosure:** A stable, weighted cylindrical base that conceals power breakout circuitry, internal wire routing channels, and side port access.
2. **The Textured Upper Shade / Diffuser:** A geometrically textured upper diffuser cap engineered with variable wall thicknesses to create dynamic shadows and diffuse ambient light evenly.

---

## 📐 Design & CAD Architecture

Modeled parametrically in **Autodesk Fusion 360**:

* **Base Housing (`Base:1`):**
  * Cylindrical body with smooth base fillets for print bed adhesion and tip-resistance.
  * Offset construction plane cutout on the curved perimeter for power input / control interface.
  * Internal electronics cavity with dedicated pass-through channels to guide wiring into the upper chamber.
* **Top Textured Shade:**
  * Custom exterior relief pattern designed to take advantage of 3D printer toolpaths and layer diffusion.
  * Mating lip engineered with a `0.25 mm` radial tolerance for a clean, fastener-free press/friction fit to the base.
  * Optimized overhang angles to eliminate the need for messy internal supports.

---

## 🖨️ 3D Printing Recommendations

| Parameter | Base Enclosure | Textured Top / Diffuser |
| :--- | :--- | :--- |
| **Material** | PLA / PETG (Matte or Wood-fill) | Translucent / White PLA or PETG |
| **Layer Height** | 0.20 mm | 0.16 mm – 0.20 mm (or Adaptive) |
| **Perimeters / Walls** | 3 – 4 walls | 2 – 3 walls (for optimal diffusion) |
| **Infill** | 15% – 20% (Gyroid) | 0% – 10% (depending on diffusion style) |
| **Supports** | None (print flat side down) | None (print rim down) |
| **Brim** | Optional | Recommended if footprint is narrow |

---

## ⚡ Hardware & Electronics

* **Light Source:** 5V Addressable LED Ring / Strip (WS2812B or SK6812) or warm-white LED puck
* **Power Input:** Type-C USB Breakout Board (5V, 2A–3A)
* **Controller (Optional):** ESP32 / RP2040 / Arduino Nano (for addressable effects) or inline rotary switch
* **Hardware:** Silicone non-slip rubber pads for base underside

---

## 🛠️ Assembly Instructions

1. **Base Assembly:**
   * Insert the USB-C breakout / power interface into the side port opening. Secure with a dab of hot glue or press-fit retention clips.
   * Route the power leads through the vertical wire channel into the upper mounting lip.
2. **Electronics & Lighting:**
   * Solder power and ground lines to the LED core.
   * Secure the LED ring/core onto the central mounting pedestal of the base.
3. **Mating & Final Closure:**
   * Align the textured upper shade with the base locking rim.
   * Press down gently until the friction fit seats flush against the base shoulder.
   * Attach non-slip rubber feet to the underside recess of the base.

---

## 📁 Repository Structure

```text
├── cad/
│   ├── led_pixel_lamp.f3d       # Native Autodesk Fusion 360 archive
│   └── step/
│       ├── base_enclosure.step  # STEP file for the base
│       └── top_shade.step       # STEP file for the textured shade
├── stl/
│   ├── base_enclosure.stl       # Ready-to-slice base file
│   └── top_shade.stl            # Ready-to-slice shade file
├── firmware/                    # (Optional) LED control code for ESP32/Arduino
├── images/                      # CAD renders and physical print photos
└── README.md
```

---

## 📜 License
