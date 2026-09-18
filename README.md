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
### Non-Functional Requirements (NFRs)
1. **NFR-01 (Fault Tolerance):** The system shall continue operating despite temporary communication interruptions.
2. **NFR-02 (Latency & Processing):** Command processing should normally complete within 5 seconds after a command is received by the rover.
3. **NFR-03 (Scalability - Original):** The system should support communication with multiple rovers simultaneously.
4. **NFR-04 (Communication Constraints):** The system shall handle limited communication bandwidth and multi-minute communication delays without relying on unconfirmed command repetitions.

### Change Request CR-01 — Emergency Safety
* **Original FR-04:** The rover shall enter Safe Mode when a critical battery or thermal condition is detected.
* **Updated FR-04:** The rover shall enter Safe Mode **within 3 seconds** when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

### Change Request CR-02 — Mission Expansion (Scalability)
* **Original NFR-03/04:** The system shall support communication with multiple rovers simultaneously.
* **Updated NFR-04:** The system shall support **at least 20 simultaneously connected rovers** (making the requirement fully measurable).

### Change Request CR-03 — Security Upgrade
* **Original FR-03/NFR:** Only authenticated Mission Control operators shall be permitted to issue rover commands.
* **Updated NFR-02:** The system shall require **authenticated and role-authorized operators** before accepting rover commands.
