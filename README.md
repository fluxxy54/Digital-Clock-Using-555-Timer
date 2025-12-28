Status: Hardware Simulation

A complete digital clock system implemented using TTL logic ICs and a 555 Timer IC configured in astable mode. The design covers clock pulse generation, time counting, comparison logic, display driving, and alarm signaling, making it suitable for academic evaluation in Logic Design and Digital Systems courses.

Institution: Benha University – Faculty of Computers & Artificial Intelligence
Course: Logic Design

📸 Hardware Preview

(Insert Proteus / Multisim schematic, timing waveform, or hardware photo here)

🚀 Features

Clock Pulse Generation: NE555 Timer producing ~1 Hz timing signal.

Time Counting: Cascaded decade counters for seconds and minutes.

Digital Comparison Logic: Time comparison using 4-bit magnitude comparators.

Visual Output: BCD-to-7-segment decoding for numeric display.

Control Logic: Flip-flops and logic gates for state control.

Audible Alert: Buzzer output for alarm or event signaling.

Manual Control: DIP switches and push button for user input.

🛠️ Hardware Specifications & Components
🔹 Integrated Circuits (ICs)
Quantity	Component	Function
1×	IC 555 (NE555)	Clock pulse generation (astable mode)
4×	IC 7485	4-bit magnitude comparators (time matching)
6×	IC 7490	Decade counters (seconds & minutes counting)
6×	IC 7447	BCD to 7-segment decoder/driver (common-anode)
1×	IC 7473	Dual JK flip-flop (control logic)
1×	IC 7408	Quad 2-input AND gates
1×	IC 7404	Hex inverter (NOT gates)
🔹 Input / Output Components
Quantity	Component	Purpose
4×	4-Position DIP Switch	Time setting and control inputs
1×	Push Button	Manual reset / mode control
1×	Buzzer	Audible alarm indication
—	7-Segment Displays	Visual time output
🔹 Passive Components
Quantity	Component	Purpose
16×	5 kΩ Resistors	Current limiting / pull-ups
1×	10 kΩ Resistor	Control signal stabilization
1×	10 µF Capacitor	Timing capacitor for 555 Timer
1×	103 Capacitor (0.01 µF)	Noise filtering / decoupling
🔹 Power Supply
Specification	Description
5V DC	Required for all 74xx TTL ICs
🧮 Timing Calculation (555 Timer)

The output frequency of the 555 Timer in astable mode is:

f = 1.44 / ((R1 + 2R2) × C)


Values used:

R1 = 50 kΩ

R2 = 50 kΩ

C = 10 µF

Result:
Clock frequency ≈ 1 Hz, appropriate for real-time second counting.

🧩 System Architecture

The 555 Timer generates continuous clock pulses.

7490 counters increment seconds and minutes.

7485 comparators evaluate time equality for alarm conditions.

7473 flip-flop manages state transitions.

7447 decoders drive the 7-segment displays.

7408 / 7404 logic gates provide combinational control.

Buzzer activates when comparator conditions are met.

(Insert block diagram here)

⚠️ Technical Notes

TTL Logic Constraint: All ICs require a stable 5V supply.

Display Limitation: 7447 supports common-anode displays only.

Accuracy: RC-based oscillators are affected by component tolerances.

Educational Scope: Designed for instructional clarity, not precision clocks.
