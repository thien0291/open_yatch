# AI Agent System for Yacht Design & Construction

## Overview

This AI-driven system orchestrates the complete design, engineering, and construction process for a custom yacht using the **BMAD (Build-Measure-Assess-Design)** methodology. The system coordinates specialized AI agents to produce comprehensive documentation including Product Requirements Document (PRD), Technical Design Documents (TDD), Bill of Materials (BOM), cost estimates, and build plans.

## BMAD Methodology Implementation

The system follows an iterative BMAD approach:

1. **Build**: Generate complete design packages and documentation
2. **Measure**: Evaluate designs against requirements and constraints
3. **Assess**: Review safety, cost, and buildability tradeoffs
4. **Design**: Refine specifications based on assessment feedback

## Directory Structure

```
ai/
├── agents/                    # Specialized AI agent definitions
│   ├── naval_architect.md           # Hull form and general arrangement
│   ├── composite_structure_engineer.md  # FRP structure and laminate schedules
│   ├── stability_weight_engineer.md     # Weight distribution and stability
│   ├── watertight_flooding_engineer.md   # Compartmentation and flooding safety
│   ├── glazing_engineer.md               # Panoramic glazing design
│   ├── electrical_engineer.md            # AC-first electrical systems
│   ├── propulsion_engineer.md            # Propulsion system interfaces
│   ├── cost_engineer.md                  # Cost estimation and control
│   ├── build_and_qa.md                   # Construction and QA procedures
│   ├── regulatory_consultant.md          # Compliance and certification
│   ├── test_trials_engineer.md           # Testing and sea trials
│   ├── product_manager.md                # Requirements and project management
│   └── orchestrator.md                   # System coordination and integration
├── tasks/
│   └── overall.md               # Complete orchestration workflow
└── README.md                    # This file
```

## Project Objectives

### Single-Run Deliverables
The system aims to produce all critical project documentation in a single coordinated run:

- **Complete Design Package**: Hull form, structural analysis, systems integration
- **Cost Control Framework**: Detailed BoQ with multiple scenarios and risk analysis
- **Build & QA Plan**: Step-by-step construction procedures with quality gates
- **Safety & Compliance**: Comprehensive risk assessment and regulatory compliance
- **Testing Protocol**: Verification test matrix and sea trial procedures

### Key Project Characteristics
- **Vessel Type**: 24m FRP river + nearshore cruiser
- **Construction**: Symmetrical mono-hull with panoramic glazing
- **Power**: AC-first 220V electrical system with donor hybrid/EREV propulsion
- **Safety Focus**: Multi-compartment watertight design with redundancy
- **Cost Optimization**: Local sourcing in Vietnam with safety-first approach

## Agent Roles & Responsibilities

### Core Engineering Agents

#### Naval Architect (`naval_architect.md`)
- Hull form design and optimization
- General arrangement planning
- Hydrostatic calculations and stability targets
- Bulkhead and compartmentation strategy

#### Composite Structure Engineer (`composite_structure_engineer.md`)
- FRP laminate schedules by zone
- Structural grid design (frames and longitudinals)
- Load analysis and reinforcement planning
- Material specifications and build methods

#### Stability & Weight Engineer (`stability_weight_engineer.md`)
- Weight budget and center of gravity management
- Stability analysis and inclining procedures
- Performance targets and safety margins
- Tradeoff analysis for weight vs. functionality

#### Watertight & Flooding Engineer (`watertight_flooding_engineer.md`)
- Compartment zoning and bulkhead placement
- Flooding scenarios and damage stability
- Bilge systems and drainage design
- Penetration and sealing specifications

#### Glazing Engineer (`GlazingOpenings Engineer.md`)
- Panoramic window module design
- Structural integration and reinforcement
- Sealing and bonding specifications
- Replacement and maintenance procedures

#### Electrical Engineer (`Electrical_enginner.md`)
- AC-first 220V distribution system
- Safety protection (RCD/RCBO/earthing)
- Load analysis and power management
- Wet zone and hazardous area classification

#### Propulsion Integration Engineer (`Propulsion Integration Engineer.md`)
- Donor drivetrain interface design
- Cooling and ventilation integration
- Vibration isolation and noise control
- Alignment and mounting specifications

### Support & Control Agents

#### Cost Engineer (`cost Engineer – Hull Shell Only.md`)
- Detailed Bill of Quantities (BoQ)
- Multiple cost scenarios (safe minimum, balanced, premium)
- Risk analysis and contingency planning
- Change control and budget tracking

#### Build & QA Engineer (`build_and_QA.md`)
- Construction sequencing and procedures
- Quality control checkpoints and hold points
- Inspection criteria and acceptance tests
- Failure mode analysis and prevention

#### Regulatory Consultant (`Regulation Survey Consultant.md`)
- Classification society requirements
- Local regulatory compliance (Vietnam)
- Safety standards and certification paths
- Documentation and survey procedures

#### Test & Sea Trials Engineer (`testAndSea Trials Engineer.md`)
- Verification test matrix development
- Sea trial protocols and checklists
- Performance validation procedures
- Acceptance criteria and evidence requirements

#### Product Manager (`product_manager.md`)
- Requirements management and prioritization
- Stakeholder coordination and communication
- Scope control and change management
- Success criteria definition and tracking

### System Orchestrator (`orchestrator.md`)
- Overall project coordination and integration
- Conflict resolution between subsystems
- Gate-based progress management
- Decision logging and risk register maintenance

## Orchestration Workflow

The system operates through **6 sequential gates** as defined in `tasks/overall.md`:

### Gate 0: Kickoff & PRD Skeleton
- PRD framework establishment
- Requirements baseline creation
- Document indexing and ID system setup

### Gate 1: Concept Design
- Hull form and general arrangement
- Watertight zoning strategy
- Glazing concept development

### Gate 2: Preliminary Engineering
- Structural design and laminate schedules
- Weight and stability baseline
- Initial calculations and analysis

### Gate 3: Hull Shell Costing
- Detailed BoQ development
- Cost scenario analysis
- Budget control framework

### Gate 4: Electrical Architecture
- AC-first system design
- Safety and protection systems
- Integration planning

### Gate 5: Build Plan & QA
- Construction sequencing
- Quality gates and checkpoints
- Risk mitigation procedures

### Gate 6: Compliance & Testing
- Regulatory compliance verification
- Test plan development
- Final documentation package

## Output Documentation Structure

The system generates a comprehensive documentation package:

### Product Requirements Document (`prd.md`)
- Executive summary and project vision
- Detailed requirements by subsystem
- Cost control and budget management
- Project phasing and milestones
- QA and acceptance criteria

### Technical Design Documents (`technical_design.md`)
- System architecture overview
- Hull form and structural design
- Glazing and openings specifications
- Electrical system design
- Propulsion integration details
- Build procedures and QA plans

### Supporting Files
- Requirements traceability matrix
- Bill of Materials (BOM) and Bill of Quantities (BoQ)
- Weight budget and stability calculations
- Test plans and compliance checklists
- Decision log and risk register

## Progress Tracking & Updates

All progress and TODO items are automatically tracked and updated in the `prd.md` file through the orchestration system. The system maintains:

- **Requirements Traceability**: Links between PRD requirements, TDD specifications, and test cases
- **Decision Log**: Architectural decisions with rationale and tradeoffs (ADR-### format)
- **Risk Register**: Identified risks with mitigation strategies (RISK-### format)
- **Change Control**: Formal process for specification changes with impact analysis

## Safety-First Philosophy

The system enforces strict safety priorities:

1. **No Safety Tradeoffs**: Safety requirements cannot be compromised for cost
2. **Redundancy Design**: Multiple layers of protection for critical systems
3. **Conservative Assumptions**: Default to safer design choices when uncertain
4. **Explicit Risk Acceptance**: All safety-related decisions require formal documentation

## Cost Control Framework

Three-tiered cost management approach:

1. **Safe Minimum**: Basic functional requirements with essential safety margins
2. **Balanced**: Optimized cost-performance ratio for target use case
3. **Safer Premium**: Enhanced safety and performance features

All cost estimates include confidence ratings and risk analysis for volatile components (resin, labor, exchange rates).

## Integration & Conflict Resolution

The orchestrator manages subsystem integration through:

- **Interface Definition**: Clear specifications for subsystem boundaries
- **Conflict Detection**: Automated identification of design conflicts
- **Tradeoff Analysis**: Quantified impact assessment for competing requirements
- **Decision Documentation**: Formal ADR process for resolution choices

## Local Build Considerations

Design optimized for Vietnam construction:

- **Material Availability**: Locally sourced FRP materials and components
- **Labor Skills**: Construction methods suitable for local workforce
- **Equipment Access**: Tooling and facilities available in target region
- **Regulatory Compliance**: Vietnamese maritime and safety requirements

## Success Metrics

Project completion measured by:

- **Deliverable Completeness**: All required documentation packages delivered
- **Requirements Coverage**: 100% of MUST requirements with acceptance criteria
- **Cost Control**: Budget maintained within established ceilings
- **Safety Compliance**: All safety requirements verified and tested
- **Build Readiness**: Complete construction package with QA procedures

---

*This AI agent system transforms yacht design from traditional fragmented processes into an integrated, safety-first, cost-controlled development methodology suitable for custom boat construction.*
