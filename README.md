# Gaze-Assisted Menu Selection

## Project Purpose
This project is a Human–Computer Interaction (HCI) research prototype that explores **gaze-assisted menu selection** using webcam-based eye tracking. The system uses eye gaze only to *highlight* likely menu targets, while final selection is confirmed through a mouse click. This follows the design principle **“eyes point, hands confirm.”**

The goal is to reduce pointing effort during menu interaction without introducing accidental activations or removing user control.

---

## Code Structure Overview

The project is intentionally lightweight and implemented as a **single-page web application**. All logic runs client-side in the browser.


project-root/

│

├── index.html        # Main application file

├── README.md         # Project documentation (this file)


There are no backend services, build tools, or external configuration files.

---

## index.html (Main Application File)

The `index.html` file contains **all components** of the prototype:

### 1. HTML Structure
- Defines the layout of the interface
- Contains menu items that act as gaze-sensitive targets
- Includes overlays for calibration and system feedback

### 2. CSS Styling
- Embedded styles define the visual appearance of the interface
- Highlight effects are used to indicate gaze focus
- Transitions are kept subtle to avoid visual distraction

### 3. JavaScript Logic
The JavaScript code inside `index.html` is responsible for:

- Initializing **WebGazer.js**
- Requesting webcam access
- Handling gaze calibration
- Continuously reading gaze coordinates
- Applying smoothing to reduce jitter
- Determining which menu item is closest to the current gaze
- Visually highlighting the focused item
- Ensuring selection only occurs on mouse click

### 4. Gaze Interaction Model
- Gaze is used **only for pre-selection**
- No actions are triggered automatically by gaze
- Mouse click is always required to confirm selection

This design avoids unintended activation and keeps interaction predictable.

---

## External Libraries

- **WebGazer.js**
  - Used for webcam-based eye tracking
  - Runs entirely in the browser
  - No gaze data or video frames are stored or transmitted

---

## How to Run the Project

1. Open `index.html` in a modern web browser (Chrome or Firefox recommended)
2. Allow webcam access when prompted
3. Complete the on-screen calibration
4. Interact with the menu using gaze + mouse clicks

No installation or server setup is required.

---

## Design and Implementation Notes

- The project is implemented as a **research prototype**, not a production system
- Code is intentionally kept simple and readable
- All processing is local for privacy and transparency
- The structure favors clarity over modularization for ease of review

---

## Author

**G Kushal**  
Stony Brook University  
CSE 518 – Human–Computer Interaction  

---

## License

This project is intended for educational and research purposes.
