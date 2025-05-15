# Ball and Beam

This repository contains our full implementation of a Ball and Beam control system using a 12 V DC motor and a custom-built PVC structure.  
Our main goal is to design, build, and control a real-time system that keeps a ping-pong ball balanced on a beam via sensors and actuators.  

Stay tuned for successive updates on control algorithms, electronics, and computer vision!

---

## 📦 Procurement & Materials

We sourced all parts to build both a test and a final model:

- **PVC sheets**: 4 m of 0.7 cm-thick lightweight PVC (chosen for lightness, aesthetics, and low friction).
- **DC Motor**: 25GA-370, 12 V, 600 RPM + motor mount bracket.
- **Gears**: 57-tooth spur gear + worm shaft (assembled into a custom gearbox).
- **Shafts & Fasteners**: 2 metal shafts + 4 steel bolts (Allen or regular), spring washers.
- **Perforated plates**: 2 × 3×7 cm metal plates for gear support.
- **Sensors**: HC-SR05 ultrasonic, MPU6050 IMU.
- **Potentiometer**: Precision 10 kΩ, 10-turn (blue).
- **Switches**: 2 × micro-switch, 2 × ON/OFF toggle.
- **Brackets & clamps**: 2 × 90° brackets (3-hole per face) + 1 × 90° bracket (1-hole per face) + semi-circular motor clamp.
- **Adhesives**: electrical tape, double-sided tape, duct tape, super glue (one-two-three), hot glue.
- **Electronics**: Arduino Uno, breadboard, jumper wires, 7.4 V Li-ion battery + adapter.
- **Miscellaneous**: transparent plastic sheet, red-marked ping-pong ball (for future vision), straight 11-hole brackets (used for beam articulation), …

---

## 🧱 Mechanical Structure Overview

### PVC Beam
- Stacked 0.7 cm PVC sheets → final beam length = 52 cm (with shaft clearance).

### Custom Gearbox
- 57-tooth spur gear meshed with a worm shaft mounted on the motor.
- Height of motor adjusted using permanent cardboard layer (not a temporary shim).

### Shaft & Support
- Gear shaft held by two 3×7 perforated metal plates; PVC beam mounted directly.
- Two edge stoppers placed along the beam (not at ends) to restrict ball motion to one axis.

### Beam Articulation
- Two 11-hole straight metal brackets (often called "metal strips") connect gear to the beam.
- Spring washers prevent nut loosening and ensure smooth ±15° beam rotation.

---

## 🧪 Test Model & Lessons Learned

**Issues in the test version:**

- **PVC damage**: screws pierced PVC at some mount points  
  → *Final fix*: replaced some joints with strong adhesive instead of mechanical fastening.

- **Unstable base**: initial base lacked rigidity  
  → *Final fix*: used a rectangular solid block for high stability.

- **Limited rotation**: hinge joint limited beam motion  
  → *Final fix*: replaced hinge with free-spinning shaft.

- **Gear misalignment**: motor height mismatched with gear  
  → *Final fix*: fixed with a permanent cardboard layer under motor.

---

## ✅ Final Model

### Precision Alignment
- Used level function of smartphone app (in compass) to align beam and motor shaft accurately.

### Rigid Support
- Added a sturdy rectangular base + in-line stoppers on beam to confine ball motion.

### Optimized Beam Articulation
- Replaced belts with straight 11-hole brackets to articulate beam with ±15° range.
- Spring washers ensure joints stay tight without locking or jamming.

### Custom Gearbox
- Assembled using a 57T spur gear and worm shaft for high torque, low speed.
- Entire gearbox was hand-assembled from separate components.

### Motor Mounting & Vibration Control
- Fixed motor using a semi-circular clamp + cardboard layer for height alignment.
- Used super glue on gear to prevent internal nut from slipping during operation.

---

## ⚙️ Mechanical Challenges & Remedies

| Challenge                                                                          | Remedy                                                                                                     |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Loosening or over-tightening of nuts at the connection of two 11-hole brackets     | Use spring washers under the nuts to maintain proper tension and prevent both loosening and jamming        |
| Motor vibration and gear misalignment                                              | Secure the motor with a semi-circular clamp and a permanent cardboard layer for precise height adjustment  |
| PVC cracking under screw mounting points                                           | Remove problematic screws and replace those joints with high-strength adhesive                             |
| Minor gap between beam and base causing wire-stopper rods to work loose over time | Install a single integrated shaft with holders at both ends to eliminate the gap and secure the wire rods  |

---

## 🔧 Assembly Instructions (Detailed)

1. **Cutting PVC Sheets and Drilling Shaft Hole**  
   We cut the PVC sheets to 52 cm in length (matching the beam's width). A hole was drilled for the shaft, 2 cm from one end of the beam.

2. **Gearbox Installation**  
   The 57-tooth spur gear and worm shaft were mounted onto the motor shaft and secured tightly using a set screw.

3. **Beam Alignment and Height Adjustment**  
   Using the leveling tool in a smartphone app, we aligned the beam by adjusting the motor’s position along the beam axis and modifying the beam height. Then we installed the second shaft holder for permanent alignment.

4. **Motor and Bracket Mounting**  
   The motor was mounted on the base bracket, and a cardboard shim was placed underneath to raise its height. This ensured proper meshing between the worm shaft and the spur gear. The gear shaft was fixed onto a perforated metal plate using bolts.

5. **Attaching the 11-Hole Brackets**  
   Two straight 11-hole brackets were attached between the beam and gearbox. Nuts were tightened using spring washers, and ±15° beam rotation was tested.

6. **Sensor Placement**  
   The HC-SR05 ultrasonic sensor and MPU6050 IMU were installed near the beam’s centerline.

7. **Electronics Wiring**  
   Cables were connected to the Arduino Uno, and the motor was powered separately using a 7.4 V Li-ion battery.

*Full wiring diagram and sample code coming soon…*

---

## 🔌 Electrical & Sensor Integration

*Coming soon* – will include:  
- Wiring schematic for ultrasonic, IMU, potentiometer  
- Noise-filtering tips (capacitors, cable routing)  
- Arduino pin mapping and sample sketches  

---

## 💻 Software & Control

*Coming soon* – planned:  
- Project structure under `src/`  
- Simulation scripts (`simulate.py`)  
- PID tuning procedure (Ziegler–Nichols + manual adjust)  
- Data logging and visualization  

---

## 🎥 Image Processing (Optional)

*Coming soon* – ideas:  
- Red-ball detection via OpenCV  
- Color thresholding on the marked ping-pong ball  
- Feedback loop into control algorithm  

---

## 🔘 Switch & Safety Connections

*Coming soon* – planned:  
- Micro-switch end-stops wiring  
- Emergency stop via ON/OFF toggle  

---

## 📋 Bill of Materials (BOM)

| Component                          | Qty     | Notes                                   |
|------------------------------------|---------|-----------------------------------------|
| PVC sheet (0.7 cm)                 | 4 m     | Test + final model                     |
| DC Motor (25GA-370, 600 RPM)       | 1       | Main actuator                           |
| Custom gearbox (57T + worm)        | 1       | Self-built                              |
| Precision potentiometer (10-turn)  | 1       | Blue, for fine tuning                   |
| HC-SR05 ultrasonic sensor          | 1       | Distance measurement                    |
| MPU6050 IMU                        | 1       | Angle measurement                       |
| Shaft holders                      | 2       | For stable beam rotation                |
| Micro-switches                     | 2       | Limit detection                         |
| ON/OFF toggle switches             | 2       | Manual power control                    |
| Perforated plates (3×7 cm)         | 2       | Gear support                            |
| 90° brackets (triple + single)     | 3       | Structural reinforcement                |
| Semi-circular motor clamp          | 1       | Vibration control                       |
| 7.4 V Li-ion battery + adapter     | 1       | Motor power                             |
| Arduino Uno                        | 1       | Main controller                         |
| Breadboard & jumpers               | 1 set   | Prototyping                             |
| Transparent plastic sheet          | 1       | Base support                            |
| Red ping-pong ball                 | 1       | Vision target                           |
| Screws, nuts, spring washers       | Various | Structural fasteners                    |
| Adhesives (various types)          | Various | Tape, super glue, hot glue, etc.        |

---

## 📅 Future Roadmap

1. Implement and optimize **PID** or **LQR** controller  
2. Integrate **sensor feedback loop** and data logging  
3. Develop **wireless** or **automated** control interface  
4. Add **computer vision** for ball tracking  


