# [Board Name] Specification

**Version:** X.X
**Author:** [[Your Name]]
**Date:** YYYY-MM-DD
**Status:** DRAFT / IN REVIEW / FINAL

### 1. Overview
[e.g., The DCServo-LP-V2 is a compact, high-performance motor controller for brushed DC and coreless motors, designed to operate up to 36V at 4A continuous current.]

### 2. Core Components & Subsystems
* **MCU:** [[COMP-STM32G4A1]]
* **Gate Driver:** [[COMP-DRV8317]]
* **CAN Transceiver:** [[COMP-TCAN1042]]
* **Switching Regulator:** [[COMP-LMR33630]]
* **LDO Regulator:** [[COMP-MCP1727]]

### 3. Functional Requirements
- [ ] Must drive brushed DC and coreless motors up to 36V and 4A.
- [ ] Must provide a CAN bus interface with ESD protection.
- [ ] Must provide an interface for an external NTC thermistor for motor temperature monitoring.
- [ ] Must store configuration parameters in non-volatile memory.
- [ ] Must provide SPI and GPIO for user expansion.

### 4. Design Rationale & Key Decisions
* **Power Architecture:** This board uses the standard two-stage regulation architecture defined in [[ARCH-001]]. This isolates the sensitive 3.3V logic rail from the noisy motor power rail.
* **Gate Driver:** The [[COMP-DRV8317]] was chosen for its integrated power stage and comprehensive protection features (OCP, TSD), which simplifies the layout for the Low Power board.
* **Connectors:** All primary connectors (Power, CAN, IO) are grouped on one side of the PCB to simplify mechanical integration and harness design, per [[ADR-XXX_Connector_Layout]].

### 5. Physical & Connectors
* **Form Factor:** [e.g., Circular, < 30mm diameter]
* **Connectors:**
  - 2x XT30 for Power In/Passthrough
  - 2x JST-GH 3-pin for CAN Bus (In/Out)
  - 1x JST-GH 6-pin for SPI
  - 2x JST-GH 2-pin for GPIO
  - 1x TC2030-CTX Footprint for SWD Programming