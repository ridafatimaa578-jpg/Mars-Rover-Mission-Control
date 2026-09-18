# Mars-Rover-Mission-Control
Operating a rover on Mars comes with unique engineering hurdles, including multi-minute communication delays, limited bandwidth, and harsh environmental conditions. This system bridges the gap between Mission Control and the Martian surface, ensuring secure command execution, real-time telemetry tracking, and automated fail-safes.
## 📋 Task 1: Analysis of Engineering Notes

Based on the initial engineering notes provided by the rover team, the system requirements are divided into Functional and Non-Functional requirements below.

### Functional Requirements (FRs)
1. **FR-01 (Command Execution):** The rover shall receive commands from Mission Control and execute valid commands.
2. **FR-02 (Telemetry Reporting):** The rover shall report its current position, battery level, temperature, and communication status.
3. **FR-03 (Command Authentication):** Only authenticated Mission Control operators shall be allowed to issue commands.
4. **FR-04 (Command Filtering):** The system shall reject invalid or unauthorized commands.
5. **FR-05 (Emergency Safety - Original):** If the rover detects a critical battery or thermal condition, it shall enter Safe Mode.
6. **FR-06 (Execution Status):** Mission Control shall receive command execution status.
7. **FR-07 (Event Logging):** All commands and critical rover events shall be recorded with a timestamp and operator ID.

