# Purple Team Project

A hands-on purple team lab that tests, detects, and hardens a small routed network. The project documents a baseline (unhardened) environment, simulated attack activity, the detections built to catch it, and the hardened configuration that followed.

> **Lab use only.** All activity was performed in an isolated environment that I own and control. Nothing here should be run against systems you don't have explicit permission to test.

## Project Goals

- Build a small multi-router lab network and document its design
- Identify risks and likely attack paths with a threat model
- Run controlled attack simulations (red team) against the baseline
- Write and test detection logic (blue team) for that activity
- Harden the routers and ACLs, then re-test and compare results
- Record findings in an incident report with before/after evidence

## Repository Structure

```
purple-team-proj/
├── README.md
├── docs/
│   ├── architecture.md        # Network design, addressing, and components
│   ├── threat-model.md        # Assets, threats, attack paths, and mitigations
│   └── incident-report.md     # Findings, timeline, impact, and remediation
├── configs/
│   ├── router-r1.txt          # Router R1 configuration (sanitized)
│   ├── router-r2.txt          # Router R2 configuration (sanitized)
│   └── acl-rules.txt          # Access control list rules
├── detection/
│   └── detection-rules.md     # Detection logic and what each rule catches
├── scripts/
│   └── log_analyzer.py        # Parses logs to surface suspicious activity
├── evidence/
│   ├── baseline/              # Screenshots and logs before hardening
│   └── hardened/              # Screenshots and logs after hardening
└── diagrams/
    └── network-topology.png   # Network topology diagram
``
