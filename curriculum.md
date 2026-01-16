# Electronics Learning Curriculum

Self-paced learning path from fundamentals to practical circuit design.

**Primary reference:** Practical Electronics for Inventors (PEFI)

---

## Phase 1: DC Fundamentals

### 1.1 Ohm's Law and Power
- Voltage, current, resistance relationships
- V = IR in all its forms
- Power calculations: P = IV = I²R = V²/R
- **PEFI:** Chapter 2

**Practice:**
- Calculate current through various resistor/voltage combinations
- Measure with multimeter, compare to calculations
- Calculate power dissipation, verify resistor ratings

### 1.2 Kirchhoff's Laws
- Kirchhoff's Voltage Law (KVL): voltages around a loop sum to zero
- Kirchhoff's Current Law (KCL): currents into a node sum to zero
- Analyzing series and parallel circuits
- **PEFI:** Chapter 2

**Practice:**
- Solve resistor networks on paper
- Build and verify with measurements

### 1.3 Voltage Dividers
- The voltage divider formula: Vout = Vin × (R2 / (R1 + R2))
- Loading effects - why voltage dividers sag under load
- Practical applications: level shifting, sensor interfaces
- **PEFI:** Chapter 2

**Practice:**
- Design dividers for specific ratios
- Measure unloaded vs loaded output
- Interface a sensor to ESP32 ADC

### 1.4 Resistor Networks
- Series and parallel combinations
- Thevenin and Norton equivalents (simplifying complex circuits)
- Current limiting resistors (LEDs, base resistors)
- Pull-up and pull-down resistors
- **PEFI:** Chapter 2

**Practice:**
- Simplify complex networks, verify with measurement
- Calculate and build LED circuits with proper current limiting

---

## Phase 2: Reactive Components

### 2.1 Capacitors
- Capacitance, charge storage: Q = CV
- Capacitor behavior: blocks DC, passes AC
- Types and applications (ceramic, electrolytic, film)
- **PEFI:** Chapter 3

**Practice:**
- Measure capacitor charging with multimeter
- Compare different capacitor types

### 2.2 RC Circuits
- Time constant: τ = RC
- Charging/discharging curves
- RC as low-pass and high-pass filters
- Cutoff frequency: f = 1/(2πRC)
- **PEFI:** Chapter 3

**Practice:**
- Build RC filter, calculate cutoff frequency
- Verify with oscilloscope if available
- Use as simple debounce circuit

### 2.3 Decoupling and Bypass Capacitors
- Why every IC needs decoupling caps
- Placement matters: close to power pins
- Value selection (100nF ceramic + bulk electrolytic)
- **PEFI:** Chapter 3

**Practice:**
- Examine ESP32 devkit schematic, identify decoupling
- Observe noise on power rail with/without decoupling (oscilloscope)

### 2.4 Inductors
- Inductance, energy storage in magnetic field
- Inductor behavior: opposes change in current
- RL time constant
- LC resonance basics
- **PEFI:** Chapter 3

**Practice:**
- Measure inductor behavior with step input
- Build simple LC tank, observe resonance

---

## Phase 3: Semiconductors

### 3.1 Diodes
- PN junction, forward voltage drop
- Rectification (half-wave, full-wave, bridge)
- Protection diodes (reverse polarity, flyback)
- Zener diodes for voltage regulation
- **PEFI:** Chapter 4

**Practice:**
- Build rectifier, measure ripple
- Add protection diode to inductive load (relay, motor)
- Build simple Zener regulator

### 3.2 BJT Transistors - Switching
- NPN and PNP basics
- Saturation mode for switching
- Base resistor calculation: Ib = Ic/hfe (with margin)
- **PEFI:** Chapter 4

**Practice:**
- Switch LED with transistor
- Switch relay or motor from ESP32 GPIO
- Calculate and verify base current

### 3.3 BJT Transistors - Amplification
- Active region operation
- DC biasing: voltage divider bias
- Small signal analysis basics
- **PEFI:** Chapter 4

**Practice:**
- Build voltage divider biased amplifier
- Measure DC operating point
- Observe amplification with signal generator + oscilloscope

### 3.4 MOSFETs
- N-channel and P-channel
- Gate threshold voltage
- MOSFETs for switching (logic level vs standard)
- Gate drive considerations
- **PEFI:** Chapter 4

**Practice:**
- Switch high-current load from ESP32 with logic-level MOSFET
- Compare to BJT switching
- Level shifting for non-logic-level MOSFETs

---

## Phase 4: Building Blocks

### 4.1 Op-Amps - Basics
- Ideal op-amp rules (virtual short, no input current)
- Comparator configuration
- Non-inverting amplifier: Gain = 1 + (Rf/Rin)
- Inverting amplifier: Gain = -Rf/Rin
- **PEFI:** Chapter 8

**Practice:**
- Build comparator (light sensor threshold detector)
- Build non-inverting amplifier, measure gain

### 4.2 Op-Amps - Applications
- Voltage follower (buffer)
- Summing amplifier
- Difference amplifier
- Active filters
- **PEFI:** Chapter 8

**Practice:**
- Buffer a high-impedance sensor for ESP32 ADC
- Build active low-pass filter, compare to passive RC

### 4.3 Linear Voltage Regulators
- How regulators work (feedback control)
- Dropout voltage, power dissipation
- 78xx series, LDO regulators
- Input/output capacitor requirements
- **PEFI:** Chapter 11

**Practice:**
- Build 5V and 3.3V regulated supplies
- Calculate heatsink requirements
- Measure line and load regulation

### 4.4 Switching Power Supplies - Introduction
- Why switching: efficiency
- Buck, boost, buck-boost topologies (conceptual)
- Using integrated switching regulator modules
- **PEFI:** Chapter 11

**Practice:**
- Examine a DC-DC converter module schematic
- Build adjustable supply using module
- Compare efficiency to linear regulator

---

## Progress Tracking

Use the `diary/` folder to document each session:
- Date and topic covered
- Key concepts learned
- Calculations performed
- Circuits built and measurements taken
- Questions or confusion to resolve

Use the `projects/` folder for practical builds that combine multiple concepts.

Use the `notes/` folder for topic summaries in your own words.
