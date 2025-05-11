# Ball and Beam

This repository contains our full implementation of a Ball and Beam control system using a 12 V DC motor and a custom-built PVC structure.  
Our main goal is to design, build, and control a real-time system that keeps a ping-pong ball balanced on a beam via sensors and actuators.  

Stay tuned for successive updates on control algorithms, electronics, and computer vision!

---

## 📦 Procurement & Materials

We sourced all parts to build both a **test** and a **final** model:

- **PVC sheets**: 4 m of 0.7 cm-thick lightweight PVC (chosen for lightness, aesthetics, and lower friction vs. perforated metal).  
- **DC Motor**: 25GA-370, 12 V, 600 RPM + motor mount bracket.  
- **Gears**: 57-tooth spur gear + custom-made worm gear (we built our own gearbox).  
- ** shafts & fasteners**: 2 shaft holders + 4 steel bolts (Allen or regular), spring washers.  
- **Perforated plates**: 2 × 3×7 cm metal plates for gear support.  
- **Sensors**: HC-SR05 ultrasonic, MPU6050 IMU.  
- **Potentiometer**: Precision 10 kΩ, 10-turn (blue).  
- **Switches**: 2 × micro-switch, 2 × ON/OFF toggle.  
- **Brackets & clamps**: 2 triple 90° brackets + 1 single 90° bracket + semi-circular motor clamp.  
- **Adhesives**: electrical tape, double-sided tape, duct tape, paper tape, super glue (one-two-three), hot glue.  
- **Electronics**: Arduino Uno, breadboard, jumper wires, 7.4 V Li-ion battery + adapter.  
- **Miscellaneous**: transparent plastic sheet, red-marked ping-pong ball (for future vision), …  

---

## 🧱 Mechanical Structure Overview

1. **PVC Beam**  
   - Stacked 0.7 cm sheets → final beam length = 52 cm (2 cm reserved for shaft pass-through).  
2. **Custom Gearbox**  
   - 57-tooth spur gear meshed with a self-made worm gear on motor shaft.  
   - Temporary cardboard shim under motor for height alignment; later replaced with a second shaft.  
3. **Shaft & Support**  
   - Two 3×7 perforated plates hold the gear shaft.  
   - Edge stoppers on beam ends restrict ball to one linear axis.  
4. **Belt Connection**  
   - Two 11-tooth timing belts link gear to beam carriage, allowing ±15° rotation.  
   - Spring washer between belt-fastening nuts prevents jamming.

---

## 🧪 Test Model & Lessons Learned

**Issues in the test version**:  
- **PVC damage**: over-tightened screws cracked or pierced PVC at belt mounts → _Final fix_: use metal brackets + strong glue.  
- **Unstable base**: single support made structure wobbly → _Final fix_: solid rectangular block base.  
- **Limited rotation**: hinge joint restricted beam angle → _Final fix_: replaced hinge with shaft.  
- **Gear misalignment**: motor too low to engage worm gear → _Final fix_: raised motor by a few mm.  

---

## ✅ Final Model

1. **Precision Alignment**  
   - Used smartphone “compass/level” app to align beam and motor axes exactly.  
2. **Rigid Support**  
   - Added sturdy rectangular base + edge stoppers on both beam sides.  
3. **Optimized Belt & Gear**  
   - Belt anchor positioned to allow ±15° range (±10–12° sufficient for control; ±15° for motor testing).  
   - Spring washer prevents nut loosening and belt jamming.  
4. **Custom-Built Gearbox**  
   - Built from 57T spur gear + self-cut worm screw → increased torque, reduced speed.  
5. **Motor Mounting & Vibration Control**  
   - Semi-circular clamp under motor fixes it downward; tension tuned to avoid blocking shaft.  
   - Super-glued belt to gear when internal nut slipped.  

---

## ⚙️ Mechanical Challenges & Remedies

| Challenge                          | Remedy                                                      |
|------------------------------------|-------------------------------------------------------------|
| Belt slipping inside gear         | Fixed belt with super glue                                  |
| Motor vibration & gear disengagement | Added semi-bracket under motor with controlled tension      |
| PVC cracking at belt mount         | Metal bracket + strong adhesive                             |
| Shaft-base gap causing looseness   | Added second shaft to eliminate gap                         |

---

## 🔧 Assembly Instructions (detailed)

1. **Cut PVC Sheets** to 52 cm × beam width; drill 2 cm hole for shaft.  
2. **Mount Gearbox**: attach 57T gear + worm screw to motor shaft; secure with set-screw.  
3. **Align & Shim**: use cardboard shim, then install second shaft holder for permanent alignment.  
4. **Install Motor & Bracket**: fix motor to base bracket; adjust height to mesh gears smoothly.  
5. **Attach Beam**: slide beam onto shaft; add end-stops.  
6. **Connect Belts**: loop two 11T belts; tighten nuts with spring washer; test ±15° travel.  
7. **Sensor Placement**: position HC-SR05 and MPU6050 near beam centerline.  
8. **Wire Electronics**: route cables to Arduino Uno; power motor via separate 7.4 V supply.  

*Full wiring diagram and code examples coming soon…*

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


