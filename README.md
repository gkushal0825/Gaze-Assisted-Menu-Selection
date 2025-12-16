# Gaze-Assisted Menu Selection

A Human–Computer Interaction (HCI) research prototype that explores how webcam-based eye tracking can be used to *assist* menu selection without replacing traditional input. The system follows the principle **“eyes point, hands confirm”**, where gaze is used only for highlighting likely targets and a mouse click is required for final selection.

---

## Project Overview

Menus are a core interaction pattern in modern graphical interfaces, yet they still rely heavily on precise cursor movement. This project investigates whether visual attention—captured using lightweight webcam-based eye tracking—can reduce interaction friction during menu selection.

Instead of activating items directly through gaze, the system uses gaze as a **pre-selection signal**. When a user looks at a menu item, it is visually highlighted. The user then confirms the action with a mouse click. This design avoids accidental activation while still leveraging the speed of eye movements.

The prototype is implemented entirely in the browser using standard web technologies and runs on commodity hardware.

---

## Key Interaction Concept

- **Gaze = attention signal**
- **Mouse click = intentional action**

This separation ensures:
- No accidental activations  
- Clear user control  
- Robust behavior even with imperfect gaze estimates  

---

## Technology Stack

- HTML / CSS / JavaScript  
- WebGazer.js for webcam-based eye tracking  
- Client-side only (no backend, no data storage)  

All gaze processing happens locally in the browser. No video frames or gaze data are saved or transmitted.

---

## Code Structure

project-root/

│

├── index.html # Main application file

├── README.md # Project documentation


For simplicity and portability, all UI logic, styling, and gaze interaction code are contained within a single HTML file.

---

## Core Features

- Webcam-based gaze tracking  
- Gaze calibration overlay  
- Smoothed gaze estimation to reduce jitter  
- Dynamic highlighting of menu items based on gaze proximity  
- Explicit mouse click confirmation for selection  
- Visual feedback to communicate system state  

---

## Design Principles

- **Non-intrusive**: Gaze assists interaction but never overrides user intent  
- **Error-tolerant**: Highlighting is resilient to gaze inaccuracies  
- **Transparent**: Users can see how gaze affects the interface  
- **Accessible**: Runs on everyday hardware with no special setup  

---

## How to Run

1. Open `index.html` in a modern browser (Chrome or Firefox recommended)  
2. Allow webcam access when prompted  
3. Complete the on-screen calibration  
4. Interact with the menu using gaze + mouse clicks  

No installation or server setup is required.

---

## Research Context

This project was developed as part of an HCI course research assignment. It is intended as an **exploratory prototype**, not a production system. The accompanying report discusses:

- Design rationale  
- Relation to Fitts’ Law  
- Hybrid input design  
- Limitations of webcam-based eye tracking  
- Planned user study methodology  

---

## Privacy Considerations

- Webcam access is used only for gaze estimation  
- No gaze data or video is stored  
- All computation is local to the browser  

---

## Author

**Kushal Gubbala**  
Stony Brook University 

---

## License

This project is intended for educational and research purposes.
