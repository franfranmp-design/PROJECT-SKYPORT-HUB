# PROJECT SKYPORT-HUB: Autonomous Urban eVTOL Vertiport Systems Architecture & Trade Study

An end-to-end Systems Engineering capstone project executing the complete DoD/INCOSE Systems Engineering V-Model for an autonomous urban vertiport terminal. The project encompasses requirements decomposition, Model-Based Systems Engineering (MBSE), hardware-in-the-loop test procedures, stochastic discrete-event simulation trade studies, MIL-STD-882E hazard analyses, and formal configuration management.

---

## Systems Engineering Lifecycle Architecture (Phases 1–5)

### Phase 1: Requirements Engineering & ConOps
- **Concept of Operations (`PROJECT-SKYPORT_Phase1_ConOps.docx`):** Defined the operational mission targeting sub-12-minute ground turnarounds across 6 flightline stages.
- **Requirements Traceability Matrix (`PROJECT-SKYPORT_Phase1_DOORS_RTM.csv`):** Formulated 15 hierarchical requirements in DOORS schema utilizing RFC-2119 ("SHALL") language, allocating ownership to Power, Swapping, Civil, Controls, Safety, and UTM subsystems with defined Verification Methods (I, A, D, T).

### Phase 2: MBSE Architecture & Interface Management
- **Structural Decomposition (`PROJECT-SKYPORT_Phase2_BDD`):** Authored SysML Block Definition Diagrams decomposing system hierarchy and requirement allocations.
- **Logical & Physical Flows (`PROJECT-SKYPORT_Phase2_IBD`):** Modeled 480VAC grid feeds, 1000VDC HVDC buses, 24VDC hardwired safety interlocks, and low-latency RF telemetry links.
- **Interface Control Document (`PROJECT-SKYPORT_Phase2_ICD.csv`):** Defined 8 bidirectional interfaces with electrical, mechanical, protocol, and coolant specifications.

### Phase 3: Verification & Test Engineering
- **Verification Cross-Reference Matrix (`PROJECT-SKYPORT_Phase3_VCRM.csv`):** Mapped all 15 requirements to formal verification milestones (FAT, SIT, Conformance Audits) and acceptance criteria.
- **Master Test Bench Procedures (`PROJECT-SKYPORT_Phase3_TBP.pdf`):** Authored detailed test bench procedures specifying Tektronix 4-channel oscilloscopes, Fluke 87V DMMs, and Spirent network analyzers to verify contactor isolation (<50ms) and EPO response (<20ms).

### Phase 4: Stochastic Simulation, Trade Study & System Safety
- **Discrete-Event Simulation Engine (`PROJECT-SKYPORT_Phase4_Sim.py`):** Developed a Python DES engine (`heapq`, NumPy, Pandas) modeling Poisson arrivals, dynamic State of Charge (SOC), and triangular task durations across a 400-hour stress test.
- **Trade Study Matrix (`PROJECT-SKYPORT_Phase4_TradStd.csv`):** Evaluated Megawatt Fast-Charging vs. Automated Battery Swapping; identified cascading queue collapse under fast-charging (5.2% compliance; 54.8 min max wait) and validated battery swapping (9.4 min mean TAT; 90.8% compliance).
- **MIL-STD-882E Hazard Analysis (`PROJECT-SKYPORT_Phase4_FMEA.csv`):** Synthesized Risk Assessment Codes (RAC) and Risk Priority Numbers (RPN) across 5 critical hazards, achieving a 92.6% mean RPN reduction via hardwired 24VDC interlocks and shunt-trip breakers.

### Phase 5: Configuration Management & Technical Performance
- **Engineering Change Proposal (`PROJECT-SKYPORT_Phase5_ECP_001.csv`):** Formulated ECP-001 through Configuration Control Board (CCB) disposition, documenting technical, financial (+1.6M CapEx), and schedule impacts of pivoting to hybrid battery swapping.
- **Technical Performance Measure Ledger (`PROJECT-SKYPORT_Phase5_TPM_Ledger.csv`):** Tracked 5 key TPMs from SRR through PDR to CDR, verifying a 21.67% turnaround time margin and 99.53% operational availability (Ao).
