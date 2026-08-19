**Summary of Boeing 737 MAX / MCAS Software Failure Forensics Report**

This case study analyzes the software, architectural, and organizational factors behind the Boeing 737 MAX MCAS (Maneuvering Characteristics Augmentation System) crashes—Lion Air Flight 610 and Ethiopian Airlines Flight 302—which resulted in 346 fatalities and a global fleet grounding.

* **Core Technical Failure:** MCAS was designed to automatically adjust stabilizer trim to prevent stalls caused by larger, relocated engines. However, it relied on a single Angle of Attack (AoA) sensor without data validation or cross-checking, creating a single point of failure (SPOF). Erroneous sensor data repeatedly triggered uncommanded nose-down trim commands that overpowered crew inputs.


* **SDLC & Design Flaws:** Engineers increased MCAS trim authority from 0.6° to 2.5° during development without updating safety assessments, adding bounds, or building loop termination criteria. Testing failed to account for extreme physical pilot workload, such as "aerodynamic lock" on the manual trim wheel.


* **Ethics & Organizational Failures:** Corporate pressure to avoid costly simulator retraining for pilots led Boeing to omit MCAS from pilot manuals and training materials. Executives prioritized launch schedules and cost targets over safety culture, while lead engineers failed to escalate architectural risks.


* **Prevention Plan:** Remedies require mandatory dual-sensor voting logic, hard limits on software trim authority, yoke force override priority, transparent documentation, and realistic human-in-the-loop stress testing.
