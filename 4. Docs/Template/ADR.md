# ADR-XXX: [Title of Decision]

**Status:** Proposed / Accepted / Deprecated
**Date:** YYYY-MM-DD

### Context
[Describe the problem, the technical constraints, and the question that needs to be answered. For example: "The controller requires high-frequency control loops and floating-point math for advanced algorithms like MPC. The previous STM32G0 lacks a hardware FPU, leading to performance bottlenecks. Alternatives considered were the STM32F4 series and the STM32G4 series."]

### Decision
[State the final decision clearly and concisely. e.g., "We will upgrade the core microcontroller to the STM32G4 series for the V2 hardware."]

### Consequences
[Detail the results of the decision.]

**Pros:**
* [e.g., Hardware FPU drastically accelerates floating-point calculations, enabling more complex control laws.]
* [e.g., Access to advanced peripherals like HRTIM and richer ADC/DAC features.]

**Cons:**
* [e.g., Increased component cost compared to the STM32G0.]
* [e.g., Higher firmware complexity and larger code footprint.]