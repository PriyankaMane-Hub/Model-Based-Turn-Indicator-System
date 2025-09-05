# 🚘 Turn Light Indicator System for Automotive Applications

## 🔧 Model-Based Design & MIL Testing in Simulink

---

## 📌 Project Overview

This project involves the development of a Turn Light Indicator System using a Model-Based Design approach in MATLAB/Simulink. It simulates real-world vehicle behavior by interpreting the states of turn signal and hazard switch inputs and generating corresponding outputs for vehicle indicator lamps. System requirements were defined to reflect real automotive scenarios and implemented using a bus-based architecture for clean and modular signal management. The model was validated through Model-in-the-Loop (MIL) simulations to ensure compliance with timing specifications such as a 50% duty cycle blink for 2 seconds.

---

## ⚙️ What I Built

### ✅ Turn Light Logic System
Simulink model replicating turn indicator behavior:
- **Left Turn Indicator**
- **Right Turn Indicator**
- **Hazard Mode (both sides flash)**

> Developed using logical blocks, timing control, and switch input simulation.

### ✅ MIL Simulation & Validation
Executed MIL testing with comprehensive test scenarios:
- Normal operation (left/right)
- Hazard activation
- Override scenarios
- Simultaneous switch inputs

> Verified correct logic and timing with simulation results and signal logs.

---

## 📈 Key Outcomes

- 🧪 **Requirements-Driven Development**  
  Full traceability from Excel specs to model logic

- ⚙️ **Accurate Indicator Behavior**  
  All valid switch input combinations responded correctly

- 🕒 **Timing Correctness**  
  Indicator lamps toggled at the intended frequency and duration

- ✅ **Verified Safety Logic**  
  No conflicting states under simultaneous or invalid input conditions

---

## 🧠 Tech Stack

| Tool        | Purpose                                  |
|-------------|------------------------------------------|
| MATLAB & Simulink | Model development and simulation     |
| Excel       | Requirement and test case documentation |
| Bus Signals | Structured I/O using `TurnLights_Bus.mat` |

---

## 🔍 How It Works

### 🛠️ Input Signals
- `LH_TL_SW` – Left Turn Switch  
- `RH_TL_SW` – Right Turn Switch  
- `HZ_SW` – Hazard Switch  

### 💡 Output Signals
- `FR_LH_Signal`, `RA_LH_Signal` – Front & Rear Left Lamps  
- `FR_RH_Signal`, `RA_RH_Signal` – Front & Rear Right Lamps  

### 🔄 Indicator Logic Summary
| Input Combination | Output Behavior |
|-------------------|------------------|
| RH_TL_SW ON       | Right lamps blink (50% duty, 2s) |
| LH_TL_SW ON       | Left lamps blink (50% duty, 2s) |
| HZ_SW ON          | All lamps blink (50% duty, 2s) |
| RH_TL_SW + HZ_SW  | All lamps blink (hazard priority) |
| LH_TL_SW + HZ_SW  | All lamps blink (hazard priority) |
| LH_TL_SW + RH_TL_SW | All lamps OFF, error code set |
| All switches ON   | All lamps OFF, error code set |

---

## 📘 What I Learned

This project helped me strengthen my skills in:

- Translating structured requirements into executable Simulink logic
- Designing modular and reusable bus-based interfaces
- Implementing and debugging logical control flows
- Using Model-in-the-Loop (MIL) simulation to verify time-based behaviors
- Creating MIL test reports to document simulation results and trace verification
- Handling edge-case scenarios in safety-critical automotive applications


## 🚘Turn Indicator Simulink Model 

<img width="1677" height="482" alt="Turn_Indicator_Model" src="https://github.com/user-attachments/assets/d501bb55-111f-4a7f-bd06-e77b2849791b" />
