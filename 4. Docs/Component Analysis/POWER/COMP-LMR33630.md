

**Synchronous Step-Down Voltage Converter

**Author(s):** Gabriel-Alexandru Constantinescu
**Version:** 1.0
**Date:** July 11, 2025
[[LMR33630.pdf]]

---
### Section 1: Executive Summary

* **Component:** LMR33630, Texas Instruments - A 3.8V to 36V, 3A synchronous step-down voltage converter.
* **Intended Application:** Primary 5V step-down regulator for both the ACB and DLT boards.
* **Recommendation:** **Highly Recommended for Flight Hardware.**
* **Summary of Rationale:** The LMR33630 is an ideal choice for the first stage of our onboard power regulation. Its wide input voltage range comfortably accommodates our 2S Li-Ion battery, and its 3A output current capability is sufficient to handle all system loads, including the servo's stall current. Its high switching frequency (up to 2.1 MHz) allows for the use of smaller external components, saving board space.

---

### Section 2: Key Performance Metrics vs. Project Requirements

| Metric                    | Datasheet Value                | Project Requirement (5V Rail)         | Pass/Fail/Notes                                                        |
| :------------------------ | :----------------------------- | :------------------------------------ | :--------------------------------------------------------------------- |
| **Performance**           |                                |                                       |                                                                        |
| Input Voltage Range       | **3.8V to 36V**                | 6.0V to 8.4V                          | **Pass:** Excellent margin.                                            |
| Output Current            | **3A**                         | > 1A                                  | Pass                                                                   |
| Switching Frequency       | **400 kHz, 1.4 MHz, 2.1 MHz**  | 2.1 MHz                               | Pass: We will use the 2.1 MHz version for the smallest component size. |
| Peak Efficiency           | **> 95%**                      | As high as possible                   | Pass: Excellent efficiency for a buck converter.                       |
| **Physical & Electrical** |                                |                                       |                                                                        |
| Operating Temp. Range     | **-40°C to +125°C** (Junction) | -40°C to +85°C                        | Pass                                                                   |
| Quiescent Current         | **25 µA** (Operating)          | < 100 µA                              | Pass: Very low quiescent current is beneficial for battery life.       |
| **Features**              |                                |                                       |                                                                        |
| Enable Pin                | Yes, with precision thresholds | Required for power sequencing         | Pass                                                                   |
| Power Good Flag           | Yes, open-drain output         | Required for system health monitoring | Pass                                                                   |

---

### Section 3: Qualitative Assessment

**3.1. Pros:**
* **High Current, Wide Vin:** The combination of a 3A output and a 36V maximum input makes it extremely robust and versatile for our application.
* **High Efficiency:** Synchronous rectification leads to high efficiency, especially at heavier loads, which minimizes heat generation in the avionics bay.
* **Excellent Integration:** The device integrates the power MOSFETs and the compensation network, simplifying the external circuit design and reducing component count.
* **Small Solution Size:** The high switching frequency and VQFN package option allow for a very compact power supply design.

**3.2. Cons:**
* **Layout Sensitivity:** As with any high-frequency switching converter, performance is highly dependent on a tight PCB layout. The input capacitor loop must be minimized to reduce noise and ringing.

**3.3. Developer Experience & Community Support:**
* I have used this SMPS in every project of mine in the last year.

---
