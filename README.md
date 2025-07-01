# Automatic Mains Failure (AMF) Control using PLC & HMI – Diesel Generator

This project implements an Automatic Mains Failure (AMF) control system using Delta PLC (ISPSoft) and HMI (DOPSoft). It allows manual control of a diesel generator when mains power fails, ensuring safe and timed switching between power sources. The PLC program uses ladder logic to manage delays, sequencing, and interlocks to avoid overlap between mains and generator supply. The HMI panel provides a straightforward interface with start/stop buttons, real-time status indicators, and visual feedback through green lights for ON status and red lights for OFF status of mains and generator power.

---

## Tools Used

- PLC Software: Delta ISPSoft  
- HMI Software: Delta DOPSoft  
- Programming: Ladder Logic  
- Control Mode: Manual via HMI

---

## Logic Sequence

| Step | Action |
|------|--------|
| 1 | If mains is OFF, turn OFF mains contactor, reset T2, and start T0 (5s delay). |
| 2 | After T0, give start command to DG and start T1 (10s delay). |
| 3 | If mains returns, turn OFF DG contactor, start T2 (2s delay) and T3 (10s delay). |
| 4 | When T2 completes, start mains contactor. |
| 5 | When T3 completes, give stop command to DG. |

---

## HMI Functions

- Manual Start/Stop control for diesel generator  
- Status indication of mains and DG power

---

## Demo Video

[Click here to watch the demo]((https://drive.google.com/file/d/1qJNNb70yEEvOkLCQmNYE3rNRsvSJ8xbo/view)) 
