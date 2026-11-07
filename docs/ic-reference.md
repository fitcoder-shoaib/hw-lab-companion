# 📌 IC Quick Reference

Every IC used in the trainer-kit experiments (Exp 00 to 08). For full pin diagrams, open the **[Exam Guide → Quick reference → All pin diagrams](https://fitcoder-shoaib.github.io/hw-lab-companion/guides/exam-guide.html#c-pins)**.

> [!WARNING]
> **Not every IC has V<sub>CC</sub> on the last pin.** The 7483, 7476 and 7473 are the usual traps. Check the table before you power up.

| IC | Function | Pins | V<sub>CC</sub> | GND | Used in |
|---|---|:-:|:-:|:-:|---|
| **7400** | Quad 2-input NAND | 14 | 14 | 7 | 00, 01, 02, 05 |
| **7402** | Quad 2-input NOR | 14 | 14 | 7 | 00, 01 |
| **7404** | Hex inverter (NOT) | 14 | 14 | 7 | 00, 01, 02, 05 |
| **7408** | Quad 2-input AND | 14 | 14 | 7 | 00, 01, 02, 07 |
| **7410** | Triple 3-input NAND | 14 | 14 | 7 | 00, 05 |
| **7432** | Quad 2-input OR | 14 | 14 | 7 | 00, 01, 02 |
| **7486** | Quad 2-input XOR | 14 | 14 | 7 | 00, 02, 03 |
| **7483** | 4-bit binary full adder | 16 | ⚠️ **5** | ⚠️ **12** | 03 |
| **74151** | 8 : 1 multiplexer | 16 | 16 | 8 | 04 |
| **74154** | 1 : 16 demultiplexer / 4 : 16 decoder | 24 | 24 | 12 | 04 |
| **7476** | Dual JK master-slave FF with preset & clear | 16 | ⚠️ **5** | ⚠️ **13** | 05, 06, 07, 08 |
| **7473** | Dual JK FF with clear | 14 | ⚠️ **4** | ⚠️ **11** | 05 |
| **7474** | Dual D FF (+ edge) with preset & clear | 14 | 14 | 7 | 05, 08 |

## Rules of thumb for TTL on the trainer kit

- **Logic 1 = +5 V, logic 0 = 0 V.** TTL runs on 4.75 V to 5.25 V.
- **Pin 1** is next to the notch or dot. Pins count **anticlockwise** when viewed from the top.
- **Unused inputs float HIGH** in TTL. Tie them to V<sub>CC</sub> or GND on purpose so they don't cause surprises.
- **Preset and clear are active-low** on 7474 / 7476 / 7473. Keep them HIGH (or open) during normal counting.
- **Test the IC first** in the IC tester. A dead chip wastes more lab time than anything else.

## The basic gates in one line

| Gate | IC | Output is 1 when… | Expression |
|---|---|---|---|
| AND | 7408 | all inputs are 1 | Y = A · B |
| OR | 7432 | any input is 1 | Y = A + B |
| NOT | 7404 | input is 0 | Y = A′ |
| NAND | 7400 | not all inputs are 1 | Y = (A · B)′ |
| NOR | 7402 | all inputs are 0 | Y = (A + B)′ |
| XOR | 7486 | inputs differ | Y = A ⊕ B |

NAND and NOR are **universal**: any circuit can be built from only NANDs or only NORs.

---

[← Back to README](../README.md)
