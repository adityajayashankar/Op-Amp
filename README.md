# LOW POWER OP AMP
This repository consists of Circuit Design and simulation results of 2 stage Low Power Op Amp done on 180nm technology using SCL180 on Cadence.<br>
This Op Amp can be used for Low frequency, Good noise rejection and Low power circuits.<br>
# DESIGN PARAMETERS <br>

| SPECIFIC PARAMETERS        | DESIGNED VALUES |
|----------------------------|----------------|
| Technology                 | 180 nm         |
| Bias Voltage               | 1 V            |
| DC Voltage                 | 1.8 V          |
| DC Current                 | 2 µA           |
| Gain Bandwidth             | 1 - 100 Hz     |
| Gain                       | 70 dB          |
| Phase Margin               | 91°            |
| Compensation Capacitance    | 100 pF        |
| Load Capacitance           | 120 pF        |
| Slew Rate                  | 0.67 V/µs      |

# WORKING OF OPAMP
This is a two-stage operational amplifier (opamp) with a differential input pair, a gain stage(common source stage), and a compensation capacitor for stability.

**1. Power Supply :** <br>
- We are using dual power supply ,this means the op amp operates with a 3.6 V supply range.<br>

**2.  Differential Input Stage :** <br>
i. M1 (0.54/0.2)​ and M2 (0.54/0.2) :<br>
- These are NMOS transistors forming the differential input pair.<br>
- They receive differential input signals (Vin+ and Vin−​).<br>
- The current source M8​ provides the tail current, which splits between M1and M2<br>

ii. M3 (2.7/0.5) and M4 (2.7/0.5) :<br>
- These PMOS transistors act as active load current mirrors.<br>
- They ensure proper differential-to-single-ended conversion.<br>

**Gain for this stage  : Av1 ​= gm1​⋅(ro3​∣∣ro1​) = 40 dB or 100 V/V** <br>

**3. Gain Stage :** <br>
i.  M5 (0.81/ 0.18)   ​: Acts as a current source to bias the second stage.<br>
ii. M6 (10.92/ 0.18)  :<br>
- This PMOS transistor provides gain in the second stage.<br>
- It drives the output Vout​ while being loaded by M7​. <br>

 **Gain for this stage : Av2​ = gm6​⋅(ro6​∣∣ro7​) = 30 dB or 30 V/V** <br>

**4. Output Stage :** <br>
- M7 (2.52/ 0.18) : Acts are common source amplifier providing additional gain and drives the load.<br>

**5.  Compensation :** <br>
- CL = 10pF : Load capacitance <br>
- Cc = 3pF  : Miller compensation capacitor, used to ensure stability and avoid oscillations.<br>

**6. Why we use this particular opamp?** <br>
This two-stage CMOS operational amplifier is chosen for its balance between high gain and stable frequency.<br>It is widely used in low-power, low-voltage applications.<br>
