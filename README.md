# 🎯 Balloon Shooting Game

### Assembly Language Project — Department of Computer Science

---

## 🧠 Overview

**Balloon Shooting Game** is a real-time arcade-style game developed entirely in **x86 Assembly Language (8086)** for **real-mode DOS**.

The player controls a character positioned on the left side of the screen, moving vertically and shooting arrows at balloons drifting from right to left. Missing **9 balloons results in Game Over**.

This project showcases low-level system programming and direct hardware interaction.

---

## 🚀 Key Concepts Demonstrated

* Direct video memory manipulation (**0B800h**)
* BIOS & DOS interrupt handling
* Real-time game loop implementation
* Register-level collision detection
* Dynamic score tracking with screen updates

---

## 👨‍💻 Team Members

| Name           | Student ID  | Responsibilities                |
| -------------- | ----------- | ------------------------------- |
| Nahah Butt     | 23-UON-0338 | Game Logic, Collision Detection |
| Muhammad Talha | 23-UON-0446 | UI Rendering, Score System      |

---

## 🎮 Controls

| Key          | Action               |
| ------------ | -------------------- |
| ⬆ Up Arrow   | Move player up       |
| ⬇ Down Arrow | Move player down     |
| Spacebar     | Shoot arrow          |
| Enter        | Start / Restart game |

---

## ⚙️ Technical Specifications

| Component    | Details                             |
| ------------ | ----------------------------------- |
| Processor    | Intel 8086 / x86 (16-bit Real Mode) |
| Memory Model | Small Model (.model small)          |
| Assembler    | MASM (Microsoft Macro Assembler)    |
| Platform     | MS-DOS / DOSBox                     |
| Video Memory | 0B800h (CGA Text Mode)              |
| Screen Mode  | 80×25 Text Mode (16 Colors)         |
| Input        | BIOS Interrupt (INT 16h)            |
| Output       | DOS INT 21h & BIOS INT 10h          |

---

## 📂 Project Structure

```
balloon-shooting-game/
│
├── bubleshootinggame.asm        # Main game source code
├── README.md                    # Documentation
└── docs/
    └── Balloon_Shooting_Game_Report.docx
```

---

## 🔄 Game Logic

### Game Loop Flow

1. Check keyboard input via BIOS buffer
2. Handle movement and shooting actions
3. Track missed balloons (Game Over at 9)
4. Detect collisions between arrow & balloon
5. Move balloons left across the screen
6. Move arrows toward the target
7. Render updated positions to video memory
8. Repeat continuously

---

## 💥 Collision Detection

Collision is detected by comparing **16-bit video memory offsets** of the arrow and balloon.

When both positions match:

* A beep sound is triggered
* Score increases
* A new balloon is generated

---

## 📚 References

* Irvine, K. R. *Assembly Language for x86 Processors (7th Edition)*
* Intel 8086 Family User Manual
* Ralf Brown’s Interrupt List
* DOSBox Official Documentation

---

## 📄 License

This project was developed for **academic purposes** as part of the Assembly Language course under the Department of Computer Science.

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!