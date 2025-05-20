# Automatic-Door-Control-System
An automation project simulating an automatic door with **manual and automatic modes**, including safety sensors and an emergency stop. Developed using **CODESYS (ST language)** with a full working visualization.
---

## Features
> **Tip** : In CODESYS you can switch between LADDER and FBD !
- Manual mode with Open/Close pushbuttons
- Automatic mode triggered by a presence sensor
- Safety sensor to reopen if passage is detected
- Emergency stop with alarm indication
- Visualized using CODESYS HMI tools



---


## Technologies Used

| Tool            | Purpose                               |
|-----------------|----------------------------------------|
| **CODESYS**     | PLC programming and simulation         |
| **Structured Text** | Main logic implementation        |
| **Ladder Logic**   | Alternative logic implementation    |
| **CODESYS Built-in Visualization** | Visualization of the process (HMI) |

---

## How It Works

The system operates in two main modes:

### Manual Mode
- Activated when `mode_switch = FALSE`
- User manually opens/closes the door using `open_PB` and `close_PB`

### Automatic Mode
- Activated when `mode_switch = TRUE`
- Door opens automatically when `person_sens` is triggered
- After opening, the system waits for `5` seconds before closing
- If `safety_sens` is triggered while closing, the door reopens and restarts the delay
- `stop_PB` overrides all and triggers a safe shutdown with an alarm


---

## What We Learned
> This project was designed to build foundational knowledge in PLC programming and HMI development. Here's what we explored:

- Delay timers and sensor logic
- Manual vs automatic mode handling
- Interlocks to prevent conflicting actions
- Visual HMI design in CODESYS
- Clean project structuring and simulation principles

---

## Author

**Mohamed Fathi Merbouni**  
_Aspiring Automation Engineer_

---

## Contributing
Feedback and improvements are welcome. Fork the repo and submit a pull request!
