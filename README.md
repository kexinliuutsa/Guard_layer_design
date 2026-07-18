## Guard Layer Design

A fatigue-aware and risk-adaptive approval guard for mobile GUI agents.

### Research Question

How can a mobile GUI agent decide when, what, and how to ask a user for approval, so that security improves without overwhelming the user?

### System Overview

The guard is inserted between the GUI agent planner and the action executor.

Screenshot → Planner → Proposed Action → Guard → User Approval → uinput Executor

### Guard Decisions

- Allow
- Ask
- Ask with clarification
- Deny

### Current Scope

The initial prototype runs on a physical Android device using:

- Screenshot-based GUI perception
- LLM-based action planning
- uinput-based action execution
- Offline trajectory replay
- Simulated user approval models

### Repository Structure

- `agent/`: GUI agent planner
- `guard/`: risk assessment and approval policy
- `executor/`: Android uinput action execution
- `recorder/`: trajectory and screenshot logging
- `tasks/`: experimental task definitions
- `simulation/`: simulated user models
- `evaluation/`: metrics and replay evaluation
- `data/`: collected trajectories and annotations

### Status

- [ ] Define initial task set
- [ ] Connect planner and uinput executor
- [ ] Record baseline trajectories
- [ ] Implement guard decisions
- [ ] Implement baseline policies
- [ ] Run offline replay evaluation
