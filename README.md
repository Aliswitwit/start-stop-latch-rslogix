# Start/Stop Latching Motor – RSLogix 500

This PLC project demonstrates a basic Start/Stop motor circuit using ladder logic and a software latch. The motor stays energized after the Start button is released and turns OFF only when the Stop button is pressed.

## 🧠 How it works:
- `I:1/0`: Start Button (Normally Open)
- `I:1/1`: Stop Button (Normally Closed)
- `B3:0/0`: Internal latch bit
- `O:2/0`: Motor output

## 🔧 Ladder Logic:

### 📸 Start Button Pressed
> The Start button (`I:1/0`) has been pressed, initiating the motor control logic. The rung conditions are true, and the internal memory bit `B3:0/0` is energized via the latch logic.

### 📸 Latch Maintained
> The Start button has been released, but the seal-in path keeps the internal memory bit `B3:0/0` latched. This maintains power to the motor (`O:2/0`).

### 📸 Stop Button Pressed
> The Stop button (`I:1/1`) has been pressed, breaking the rung and resetting the latch. The internal bit `B3:0/0` is now de-energized, and the motor (`O:2/0`) is OFF.

