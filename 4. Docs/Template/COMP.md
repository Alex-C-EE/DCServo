# [Component Name] - [Brief Description]

**Author(s):** [[Your Name]]
**Version:** 1.0
**Date:** YYYY-MM-DD
**Datasheet:** [[Link_to_datasheet.pdf]]
---

### Section 1: Executive Summary
* **Component:** [Full Component Name, Manufacturer]
* **Intended Application:** [e.g., Core MCU for DCServo-LP-V2, Gate Driver for DCServo-HP-V1]
* **Recommendation:** [e.g., Recommended, Proposed for Benchmarking, Not Recommended]
* **Summary of Rationale:** [A brief, one-sentence summary of why this component was chosen or is being considered.]

---

### Section 2: Key Performance Metrics vs. Project Requirements

| Metric | Datasheet Value | Project Requirement | Pass/Fail/Notes |
| :--- | :--- | :--- | :--- |
| **Core & Performance** | | | |
| Core Speed | **170 MHz** | > 100 MHz | Pass |
| Hardware FPU | **Yes** | Required | Pass |
| **Motor Control Peripherals** | | | |
| Advanced Timers | **HRTIM x1** | HRTIM desirable | Pass |
| ADC Resolution/Speed| **12-bit / 4 Msps**| > 1 Msps | Pass |
| **Power & Package** | | | |
| Operating Voltage | **1.71V - 3.6V** | 3.3V nominal | Pass |
| Package | **LQFP-48** | Solderable w/o oven | Pass |

---

### Section 3: Qualitative Assessment

**3.1. Pros:**
* [e.g., Excellent set of peripherals specifically for motor control applications.]
* [e.g., Strong ecosystem support from ST (CubeMX, HAL libraries).]

**3.2. Cons:**
* [e.g., Higher static power consumption than some competitors.]
* [e.g., Certain peripherals share DMA channels, requiring careful planning.]

**3.3. Developer Experience & Community Support:**
* [e.g., Extensive documentation and application notes from ST. Large online community.]

---

### Section 4: Conclusion & Final Recommendation
[Provide a final, clear recommendation and summarize the most important trade-offs.]