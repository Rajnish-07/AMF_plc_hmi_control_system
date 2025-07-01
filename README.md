# 🔧 Automatic Mains Failure (AMF) Control using PLC & HMI – Diesel Generator

This project demonstrates an AMF system using **Delta ISPSoft (PLC)** and **DOPSoft (HMI)** for manual control of a diesel generator during mains failure. Ladder logic manages safe load transfer with defined time delays, and the HMI allows manual start/stop and status display.

---

## ⚙️ Tools Used

- **PLC Software**: Delta ISPSoft  
- **HMI Software**: Delta DOPSoft  
- **Programming**: Ladder Logic  
- **Control Mode**: Manual via HMI

---

## 🔁 Logic Sequence

| Step | Action |
|------|--------|
| 1 | If mains is OFF, turn OFF mains contactor, reset T2, start T0 (5s delay). |
| 2 | After T0, give start command to DG and start T1 (10s delay). |
| 3 | If mains returns, turn OFF DG contactor, start T2 (2s) and T3 (10s). |
| 4 | When T2 completes, start mains contactor. |
| 5 | When T3 completes, give stop command to DG. |

🖼️ Logic Overview:  
![Control Steps](./Screenshot%202025-07-01%20113357.png)

---

## 🖥️ HMI Functions

- Manual Start/Stop buttons for DG  
- Mains and DG status indicators

---

## 📁 Repository Contents

- `amf_ladder_logic.pdf` – Ladder diagram  
- `hmi_screenshots/` – Screens from DOPSoft  
- `Screenshot.png` – Control logic overview  
- `README.md` – Project description  
- `demo_video_link.txt` – Video link (if available)

---

## 📽️ Demo Video

📹 [Click here to watch the demo](https://your-demo-video-link.com)  
