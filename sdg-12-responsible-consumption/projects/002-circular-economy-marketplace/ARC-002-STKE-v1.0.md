# Stakeholder Drivers & Goals Analysis: Circular Economy Marketplace

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Circular Economy Marketplace (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Circular Economy Marketplace Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, WRAP, Environment Agency, SDG 12 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Circular Economy Marketplace, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals.

### Key Findings

The Circular Economy Marketplace faces a classic marketplace challenge: waste producers will only list materials if recyclers and remanufacturers are present to bid, and recyclers will only participate if sufficient material volume is available. DEFRA's strategic ambition to drive materials up the waste hierarchy (reuse before recycling, recycling before energy recovery) creates tension with waste management companies whose business models are built around landfill gate fees and energy-from-waste contracts. WRAP brings critical sector expertise and existing industry relationships but is cautious about a government platform competing with commercial material exchanges. The strongest alignment is around reducing illegal waste dumping (fly-tipping) by making legal disposal and reuse economically attractive and operationally simple.

### Critical Success Factors

- Achieve critical mass of both material suppliers and receivers within 6 months to create a functioning marketplace
- Demonstrate measurable waste hierarchy improvement — materials diverted from landfill and energy-from-waste to reuse and recycling
- Integrate with waste transfer note digitisation (Project 003) for regulatory compliance
- Maintain trust through verified operator credentials (Environment Agency permits, waste carrier licences)
- Deliver material matching algorithms that genuinely prioritise reuse over recycling over disposal

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on reducing waste to landfill and combating fly-tipping. Significant tensions between DEFRA's circular economy ambition and the commercial interests of established waste management operators who may view the marketplace as threatening their existing material brokerage revenues.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Environment | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DEFRA Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Circular Economy Marketplace | Programme Sponsor (DEFRA) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DEFRA CDIO | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| DEFRA Resources and Waste Policy Team | Policy ownership | HIGH | HIGH | Manage Closely — Policy alignment |
| Service Owner | End-to-end service accountability | HIGH | HIGH | Manage Closely — Service reviews |
| DEFRA Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| WRAP | Delivery partner | Material flows expertise | HIGH | HIGH |
| Environment Agency | Regulator | Waste operator licensing | HIGH | HIGH |
| Local Authority Waste Teams | 333 councils | Waste collection and disposal | MEDIUM | HIGH |
| Waste Management Companies | Private sector | Material handling, recycling | MEDIUM | HIGH |
| Manufacturers | Private sector | Material suppliers and receivers | MEDIUM | HIGH |
| Remanufacturers and Repair Networks | Private/charity | Material receivers | LOW | HIGH |
| Charity Reuse Organisations | Charity sector | Furniture/IT reuse | LOW | HIGH |
| Construction and Demolition Sector | Private sector | Major waste producers | MEDIUM | HIGH |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| Chartered Institution of Wastes Management (CIWM) | Professional body | Industry standards | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Secretary of     |
        |  * DEFRA Perm Sec   |    State (DEFRA)    |
        |  * DEFRA Finance    |  * SRO              |
        |  * CDDO             |  * DEFRA CDIO       |
 P      |                     |  * Resources & Waste|
 O      |                     |    Policy Team      |
 W      |                     |  * WRAP             |
 E      |                     |  * Environment Agency|
 R      +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * CIWM             |  * Local Authorities|
        |                     |  * Waste Management |
        |                     |    Companies        |
        |                     |  * Manufacturers    |
        |                     |  * Remanufacturers  |
        |                     |  * Charity Reuse    |
        |                     |  * Construction     |
        |                     |    Sector           |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Resources and Waste Policy Team — Delivering the Resources and Waste Strategy

**Stakeholder**: DEFRA Resources and Waste Policy Team

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Deliver the digital infrastructure needed to implement the Resources and Waste Strategy (2018) and Environment Act 2021 circular economy objectives, demonstrating measurable progress in diverting materials from landfill to reuse and recycling.

**Context & Background**:
The Resources and Waste Strategy committed to doubling resource productivity and eliminating avoidable waste by 2050. The Environment Act 2021 introduces extended producer responsibility (EPR) for packaging, deposit return schemes, and consistent recycling collections. However, no national digital marketplace exists to connect waste producers with organisations that can reuse, repair, or recycle materials. Materials that could be reused are sent to landfill because producers cannot easily find receivers. DEFRA needs a digital platform that makes the waste hierarchy practically operational rather than merely aspirational.

**Driver Intensity**: CRITICAL

**Enablers**:

- A functioning marketplace with critical mass of participants on both sides
- Material matching algorithms that prioritise higher-hierarchy outcomes (reuse > recycling > recovery)
- Integration with waste tracking systems for regulatory compliance
- Measurable waste hierarchy improvement metrics for policy reporting

**Blockers**:

- Failure to achieve marketplace critical mass (chicken-and-egg problem)
- Resistance from established waste management companies protecting brokerage revenues
- Complexity of waste classification making material matching impractical
- Lack of trust between unfamiliar trading partners

---

### SD-2: WRAP — Sector Expertise and Industry Credibility

**Stakeholder**: WRAP (Waste and Resources Action Programme)

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Ensure the Circular Economy Marketplace leverages WRAP's 25 years of material flows expertise, existing industry relationships, and sector knowledge — without duplicating or competing with WRAP's existing programmes and commercial material exchange partnerships.

**Context & Background**:
WRAP is a registered charity funded primarily by DEFRA, the devolved governments, and the EU. It has unparalleled expertise in material flows, circular economy business models, and industry engagement. WRAP already operates voluntary material exchange initiatives and has partnerships with commercial platforms. WRAP is concerned that a government marketplace could undermine its existing programmes and commercial relationships. However, WRAP also recognises that its current reach is limited to engaged organisations and a government platform could scale circular economy practices nationally.

**Driver Intensity**: HIGH

**Enablers**:

- WRAP positioned as the expert advisory body informing marketplace design
- Marketplace complements rather than competes with existing WRAP programmes
- WRAP's material classification and quality standards adopted as marketplace standards
- WRAP's industry networks used for marketplace seeding and adoption

**Blockers**:

- Government marketplace perceived as competing with WRAP's existing partnerships
- WRAP's expertise not adequately consulted in design
- Marketplace design ignores 25 years of WRAP's sector learning

---

### SD-3: Environment Agency — Regulatory Compliance and Operator Verification

**Stakeholder**: Environment Agency

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure the marketplace operates within the waste regulatory framework — all operators hold valid permits and waste carrier licences, waste transfer notes are properly documented, and the platform does not inadvertently facilitate illegal waste activities.

**Context & Background**:
Illegal waste disposal (fly-tipping) costs England approximately GBP 1 billion annually. The Environment Agency is responsible for enforcing waste regulations, including operator permits, waste carrier licences, and duty of care obligations. A marketplace that enables waste transfers without proper regulatory checks could inadvertently facilitate illegal activity. The EA needs the marketplace to integrate with its permit and licence databases, generate compliant waste transfer notes, and provide audit trails that support enforcement action.

**Driver Intensity**: CRITICAL

**Enablers**:

- Integration with EA permit and waste carrier licence databases for operator verification
- Automated waste transfer note generation meeting duty of care requirements
- Audit trail of all material transfers available to EA for enforcement
- Clear escalation process for suspected illegal activity identified through the platform

**Blockers**:

- Marketplace operating without operator verification
- Platform enabling transfers of hazardous waste without appropriate permit checks
- Insufficient audit trail for enforcement investigations
- Data sharing barriers between DEFRA marketplace and EA enforcement systems

---

### SD-4: Local Authority Waste Teams — Reducing Disposal Costs and Fly-Tipping

**Stakeholder**: 333 local authority waste teams in England

**Driver Category**: FINANCIAL / OPERATIONAL

**Driver Statement**: Reduce waste disposal costs (currently GBP 100+ per tonne for landfill tax plus gate fees) by finding reuse and recycling outlets for materials currently sent to landfill or energy-from-waste, while also reducing fly-tipping incidents by providing an accessible alternative for bulky waste producers.

**Context & Background**:
Local authorities in England spend approximately GBP 3.5 billion annually on waste collection and disposal. Landfill tax at GBP 103.70 per tonne (2025/26 rate) makes disposal increasingly expensive. Many councils struggle to find cost-effective recycling outlets, particularly for mixed materials, construction waste, and bulky items. Fly-tipping is a persistent problem — approximately 1 million incidents annually in England — partly driven by the cost and complexity of legal disposal. Councils need a platform that makes it easier and cheaper to divert materials from disposal to reuse and recycling.

**Driver Intensity**: HIGH

**Enablers**:

- Simple listing interface that council waste officers can use without specialist training
- Material matching that finds receivers within economically viable transport distances
- Integration with council waste management systems (may vary by council)
- Demonstrable cost savings versus landfill/EfW gate fees

**Blockers**:

- Platform too complex for overworked council waste teams
- Material matching only finding receivers at impractical distances (transport costs exceed savings)
- Councils required to use the platform mandatorily before they are ready
- Integration requirements with 333 different council systems

---

### SD-5: Waste Management Companies — Commercial Opportunity or Competitive Threat

**Stakeholder**: Waste management companies (Veolia, Biffa, Suez, Viridor, and hundreds of SME operators)

**Driver Category**: FINANCIAL / STRATEGIC / RISK

**Driver Statement**: Understand whether the marketplace represents a commercial opportunity (access to new material streams, reduced sourcing costs) or a competitive threat (disintermediation of existing material brokerage relationships) — and influence its design to protect legitimate business interests while supporting circular economy goals.

**Context & Background**:
The UK waste management sector is a GBP 9 billion industry. Major operators have established material brokerage businesses, recycling facilities, and energy-from-waste contracts. A government marketplace that connects waste producers directly with recyclers and remanufacturers could disintermediate operators who currently act as brokers. However, the marketplace also offers waste management companies access to new material streams and reduced sourcing costs for their recycling operations. The industry's response will be shaped by how the marketplace is positioned — as a complement to existing services or as a government alternative.

**Driver Intensity**: HIGH

**Enablers**:

- Marketplace positioned as additional channel, not replacement for existing services
- Waste management companies can register as both suppliers and receivers
- Commercial terms that do not undercut market rates or distort competition
- Industry consultation on marketplace design and rules

**Blockers**:

- Government marketplace undercutting commercial rates
- Mandatory use requirements that bypass established supply chains
- Platform design that assumes waste management companies are the problem rather than part of the solution

---

## Driver-to-Goal Mapping

### Goal G-1: Functioning Marketplace with 1,000 Active Participants Within 12 Months

**Derived From Drivers**: SD-1, SD-2, SD-4

**Goal Owner**: Service Owner

**Goal Statement**: Achieve 1,000 verified organisations actively listing or receiving materials through the marketplace within 12 months of public launch, with at least 200 local authorities, 300 waste operators, and 500 manufacturers/other organisations.

**Success Metrics**:

- **Primary Metric**: 1,000 verified active participants (listed or bid in last 90 days)
- **Secondary Metrics**:
  - At least 500 material listings per month
  - At least 200 successful material matches per month
  - Material value transacted exceeding GBP 1M per quarter

---

### Goal G-2: 50,000 Tonnes Diverted from Landfill to Higher Waste Hierarchy Outcomes Annually

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: DEFRA Resources and Waste Policy Team

**Goal Statement**: Demonstrate that the marketplace diverts at least 50,000 tonnes of materials annually from landfill or energy-from-waste to reuse, repair, or recycling within 24 months of launch.

**Success Metrics**:

- **Primary Metric**: Annual tonnes diverted (measured by completed transfers categorised by waste hierarchy outcome)
- **Secondary Metrics**:
  - 15% of diverted materials going to reuse/repair (highest hierarchy)
  - 70% going to recycling
  - 15% to energy recovery (lower hierarchy but still diverted from landfill)

---

### Goal G-3: 100% Regulatory Compliance for All Marketplace Transactions

**Derived From Drivers**: SD-3

**Goal Owner**: Environment Agency Liaison

**Goal Statement**: Ensure 100% of marketplace transactions involve verified permitted operators, generate compliant waste transfer notes, and provide audit trails accessible to the Environment Agency.

**Success Metrics**:

- **Primary Metric**: 100% operator verification rate (no transactions with unverified operators)
- **Secondary Metrics**:
  - Digital waste transfer notes generated for all transfers
  - EA enforcement data requests fulfilled within 24 hours
  - Zero instances of hazardous waste transferred without appropriate permits

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DEFRA Policy | SD-1 | Resources and Waste Strategy delivery | G-1 | 1,000 participants | O-1 | National circular economy infrastructure |
| DEFRA Policy | SD-1 | Resources and Waste Strategy delivery | G-2 | 50,000 tonnes diverted | O-1 | National circular economy infrastructure |
| WRAP | SD-2 | Sector expertise integration | G-1 | 1,000 participants | O-1 | National circular economy infrastructure |
| Environment Agency | SD-3 | Regulatory compliance | G-3 | 100% compliance | O-2 | Reduced illegal waste activity |
| Local Authorities | SD-4 | Reduced disposal costs | G-2 | 50,000 tonnes diverted | O-3 | Local authority cost savings |
| Waste Companies | SD-5 | Commercial opportunity | G-1 | 1,000 participants | O-1 | National circular economy infrastructure |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DEFRA (SD-1) wants to prioritise reuse and remanufacturing, but Waste Management Companies (SD-5) derive revenue primarily from recycling and energy recovery. The matching algorithm's hierarchy preferences may route materials away from waste companies' existing facilities.
  - **Resolution Strategy**: Marketplace offers all hierarchy options; matching algorithm presents reuse first but does not prevent recycling. Waste companies can register as reuse partners. Performance metrics track hierarchy improvement without mandating specific outcomes.

- **Conflict 2**: WRAP (SD-2) wants the marketplace to complement existing programmes, but DEFRA (SD-1) may want a comprehensive national platform that effectively replaces fragmented voluntary schemes.
  - **Resolution Strategy**: Position marketplace as national infrastructure that WRAP helps design and seed. WRAP's sector expertise and classification standards embedded in the platform. WRAP retains advisory role and can promote the platform through its industry networks.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Resources and Waste Strategy 2018 | Policy | GOV.UK | Waste hierarchy, circular economy targets | N/A |
| Environment Act 2021 | Legislation | legislation.gov.uk | EPR, waste tracking, enforcement powers | N/A |
| WRAP Circular Economy Reports | Research | wrap.org.uk | Material flows, sector analysis | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Circular Economy Marketplace (Project 002)
**Model**: Claude Opus 4.6
