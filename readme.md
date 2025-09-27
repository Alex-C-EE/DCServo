# DCServo

An open-source, high-performance controller for brushed DC and coreless motors.

DCServo is an open-source hardware and firmware project designed to transform common brushed DC and high-performance coreless motors into precise smart actuators. It is built for applications requiring high torque, fast response, and reliable absolute positioning.

## Key Features

- **Control Performance**
  - 32-bit STM32G4 Microcontroller with FPU for high-speed, floating-point control algorithms.
  - Absolute position feedback via a high-resolution, on-axis magnetic encoder.
  - High-frequency PWM and advanced control loops for smooth, precise motion.

- **Hardware**
  - Support for both standard Brushed DC and high-performance Coreless motors.
  - Onboard NTC thermistor input for external motor temperature monitoring.
  - Non-volatile NOR Flash for storing configuration parameters.
  - Multi-layer PCB design for superior thermal performance and noise immunity.

- **Interfaces**
  - **CAN Bus:** Primary command and control interface (DroneCAN target).
  - **Serial:** UART for configuration and debugging.
  - **I/O Expansion:**
    - 1x 6-pin SPI Port (JST-GH/SH)
    - 2x 2-pin General Purpose I/O (JST-GH/SH)

- **Mechanical**
  - Flexible encoder architecture, supporting both direct on-axis and remote off-axis mounting.
  - Compact form factor designed for integration into custom mechanics.

## Project Status

This project is under active development for the V2 hardware and firmware. The previous V1 hardware is considered a functional prototype and is not recommended for new designs. Manufacturing from this repository is not advised until the V2 designs are validated.

## Platform Versions

The V2 platform will be available in two primary configurations. Development is currently focused on the Low Power version.

| Version    | Target Voltage | Target Current | Status                |
|------------|----------------|----------------|-----------------------|
| Low Power  | up to 36V      | ~4A Continuous | In Active Development |
| High Power | TBD            | TBD            | Planned               |

## Documentation

Comprehensive documentation is planned for the V2 release. In the interim, design and firmware source files can be found in the `/hardware` and `/firmware` directories, respectively.

## Contributing

Contributions are welcome. Please open a GitHub Issue to report bugs or suggest features. For code or hardware changes, please submit a Pull Request.

## Community & Contact

Join the discussion and get in touch:

- **Discord:** alex_3d
- **Email:** gconstantinescu03@stud.fiir.upb.ro

## License

- **Hardware:** CERN Open Hardware License v2 (CERN-OHL-S)
- **Software:** MIT License
