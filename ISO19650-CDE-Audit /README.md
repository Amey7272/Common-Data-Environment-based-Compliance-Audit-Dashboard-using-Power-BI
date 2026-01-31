# ISO 19650 Common Data Environment based Compliance Auditing using Power BI

This repository contains artefacts supporting an academic dissertation that investigates the **automation of Common Data Environment (CDE) compliance auditing** using **Power BI**, aligned with **ISO 19650-1 and ISO 19650-2** standards.

The project operationalises ISO 19650 information management rules as **data-driven audit logic**, enabling scalable validation of BIM document compliance across multiple data drops.

---

## Scope of the Study

The project focuses on automated verification of:

- **File Naming Compliance (A.01–A.08)**
  - Structure validation against ISO 19650 naming conventions  
  - Segment-level rule enforcement (Originator, Volume, Level, Type, Role, Number)
- **File Duplication Checks (B.01–B.04)**
  - Detection of filename and revision duplication
  - Identification of resubmission and sequencing errors
- **Metadata Compliance (C.01–C.02)**
  - Status code validation
  - Revision code sequencing and format checks

Audits are performed across **multiple Data Drops (DD1–DD3)** to evaluate compliance maturity over time.

---

## Technical Architecture

### Data Pipeline
- CDE file exports (structured metadata)
- Power Query transformations:
  - Column normalisation
  - Rule tokenisation
  - Lookup joins against ISO rule dictionaries

### Data Model
- Star-schema design
- Fact table: document records
- Dimension tables: originator, data drop, rule category, compliance status

### Rule Engine
- DAX measures encode ISO 19650 logic:
  - Boolean compliance flags
  - Failure reason classification
  - Aggregated compliance metrics
- Composite rule scoring and audit summaries

### Visual Analytics
- KPI cards for compliance rates
- Rule-level breakdowns
- Data Drop trend analysis
- Drill-through diagnostics for non-compliant files

---

## Key Technologies
- **Power BI Desktop**
- **DAX**
- **Power Query (M)**
- **ISO 19650 Information Management Framework**
- **BIM CDE Governance Principles**

---

## Research Contribution

- Demonstrates a **low-code alternative** to proprietary CDE audit tools  
- Bridges the gap between **ISO 19650 policy documentation** and **operational enforcement**
- Provides a **repeatable and scalable audit framework** for BIM document governance
- Supports evidence-based compliance monitoring using visual analytics

---

## Limitations
- Relies on structured CDE exports
- Does not modify or write back to the CDE
- Rule definitions reflect project-specific interpretations of ISO 19650

---

## Disclaimer
This repository supports an **academic research project**. All datasets are anonymised, and no proprietary project information is disclosed.

