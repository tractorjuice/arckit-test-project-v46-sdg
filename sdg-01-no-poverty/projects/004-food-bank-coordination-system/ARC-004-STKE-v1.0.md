# Stakeholder Drivers & Goals Analysis: Food Bank Coordination System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Food Bank Coordination System (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Food Insecurity Programme, Cross-Government (DEFRA lead) |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA, DWP, DHSC, Trussell Trust, IFAN, FareShare, Local Authorities |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Food Bank Coordination System, a cross-government platform linking food banks with referral agencies (Jobcentres, councils, GPs, schools, social workers). The system will coordinate food aid distribution, manage surplus food redistribution (FareShare model), and provide national data on food insecurity for the first time.

### Key Findings

The food bank sector is primarily volunteer-run and charity-led (Trussell Trust network of 1,400+ food banks, Independent Food Aid Network of 1,100+ independent providers, FareShare surplus food redistribution). Government involvement is sensitive — many food bank operators view their existence as evidence of government failure and are cautious about government digital systems. The strongest alignment is around improving referral efficiency and reducing food waste through better surplus redistribution. The most significant tension is between government's desire for national data on food insecurity and food banks' concern that data collection will deter vulnerable people from seeking help.

### Critical Success Factors

- Food banks retain operational independence — the platform must be opt-in and support, not control
- Referral agencies (Jobcentres, councils, GPs) can issue digital vouchers/referrals seamlessly
- Surplus food redistribution from retailers and manufacturers is coordinated to reduce waste and improve food bank supply
- National food insecurity data is collected in a way that protects individual dignity and privacy
- Platform works for volunteer-run organisations with limited digital infrastructure

### Stakeholder Alignment Score

**Overall Alignment**: LOW-MEDIUM

Significant ideological tension between government and food bank sector. Operational alignment is higher — all parties want efficient referrals and less food waste. Data collection is the most contentious area.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DEFRA Minister | Food policy oversight | HIGH | MEDIUM | Keep Satisfied |
| DWP Minister | Benefits and poverty | HIGH | HIGH | Manage Closely |
| DHSC Minister | Public health nutrition | MEDIUM | MEDIUM | Keep Satisfied |
| SRO, Food Insecurity Programme | Programme sponsor | HIGH | HIGH | Manage Closely |
| DWP Jobcentre Plus | Referral agency | MEDIUM | HIGH | Keep Informed |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Trussell Trust | Charity network (1,400+ food banks) | Key partner | HIGH | HIGH |
| IFAN | Independent Food Aid Network (1,100+) | Key partner | HIGH | HIGH |
| FareShare | Surplus food redistribution | Key partner | HIGH | HIGH |
| Local Authority Community Services | Referral and coordination | MEDIUM | HIGH |
| Food bank volunteers and managers | Operational users | LOW | HIGH |
| People experiencing food insecurity | Service users | LOW | HIGH |
| Major retailers (Tesco, Asda, etc.) | Food donors | MEDIUM | MEDIUM |
| Food manufacturers | Food donors | LOW | MEDIUM |
| GPs and NHS services | Referral agencies | MEDIUM | MEDIUM |
| Schools | Referral agencies (holiday hunger) | LOW | HIGH |
| CDDO | Cabinet Office | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * DEFRA Minister   |  * DWP Minister     |
        |  * DHSC Minister    |  * SRO              |
        |  * CDDO             |  * Trussell Trust   |
        |                     |  * IFAN             |
        |                     |  * FareShare        |
 P      |                     |                     |
 O      +---------------------+---------------------+
 W      |                     |                     |
 E      |      MONITOR        |    KEEP INFORMED    |
 R      |                     |                     |
   Low  |  * Food mfrs        |  * People in food   |
        |                     |    insecurity       |
        |                     |  * Volunteers       |
        |                     |  * Local authorities|
        |                     |  * GPs/NHS          |
        |                     |  * Schools          |
        |                     |  * Retailers        |
        |                     |  * Jobcentre Plus   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DWP — Understand Food Insecurity Among Benefit Claimants

**Stakeholder**: DWP Minister and UC Operations

**Driver Category**: STRATEGIC / POLITICAL

**Driver Statement**: Understand the prevalence and causes of food insecurity among UC claimants to inform policy responses, while improving the referral process from Jobcentres to food banks.

**Context & Background**: DWP faces sustained criticism that benefit levels and the five-week UC wait drive food bank usage. The government needs better data to respond to parliamentary questions and shape policy. Currently, Jobcentre Work Coaches make informal referrals to food banks with paper vouchers. A digital referral system would improve tracking and claimant experience while providing policy-relevant data.

**Driver Intensity**: HIGH

**Enablers**: Digital referral from Jobcentre systems; anonymised aggregate data on referral volumes and reasons; claimant consent-based data sharing; improved referral speed

**Blockers**: Food bank sector resistance to government data collection; perception that data will be used to deny or reduce benefits; media sensitivity around government involvement in food aid

---

### SD-2: Trussell Trust — Protect Dignity, Improve Referral Efficiency

**Stakeholder**: Trussell Trust (1,400+ food banks in the UK)

**Driver Category**: OPERATIONAL / VALUES

**Driver Statement**: Improve the efficiency of the referral and voucher system while protecting the dignity and privacy of people accessing food banks. Any government platform must be opt-in, respect food bank independence, and not create a surveillance mechanism.

**Context & Background**: The Trussell Trust operates the UK's largest food bank network. Their referral model requires a voucher from an approved referral agency (Jobcentre, council, GP, school, social worker). The current paper voucher system is inefficient — vouchers are lost, expired, or issued for locations inconvenient to the person. A digital system could improve referral quality, but the Trussell Trust is deeply concerned about government data collection on their service users. They view food bank usage as evidence of policy failure and resist any framing that normalises food banks as part of the social safety net.

**Driver Intensity**: CRITICAL

**Enablers**: Opt-in platform with food bank governance; digital vouchers that are easier for people in crisis to use; no individual-level data sharing with government without explicit consent; surplus food coordination reducing reliance on public donations

**Blockers**: Mandatory data reporting to government; government branding that implies food banks are an official government service; loss of operational independence; platform requiring significant volunteer training or digital infrastructure

---

### SD-3: FareShare — Efficient Surplus Food Redistribution

**Stakeholder**: FareShare

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Improve the coordination of surplus food redistribution from retailers and manufacturers to food banks and community organisations, reducing food waste while increasing the quality and variety of food available to people in need.

**Context & Background**: FareShare redistributes surplus food from the food industry to approximately 8,500 charities and community organisations. Their model depends on logistics coordination — matching food availability (perishable, with short shelf life) to local demand. A platform that provides real-time demand data from food banks and referral agencies would dramatically improve allocation efficiency and reduce waste.

**Driver Intensity**: HIGH

**Enablers**: Real-time demand data from food banks (what stock is needed, where); logistics coordination for perishable goods; retailer integration for surplus food alerts; cold chain management data

**Blockers**: Poor food bank stock data quality; inconsistent digital infrastructure across food banks; perishable food logistics complexity; retailer reluctance to share surplus data openly

---

### SD-4: People Experiencing Food Insecurity — Accessible, Dignified Support

**Stakeholder**: People experiencing food insecurity

**Driver Category**: CUSTOMER / USER

**Driver Statement**: Access emergency food support quickly, close to home, without stigma or excessive bureaucracy, with referral to longer-term support (benefits, debt advice, mental health services).

**Context & Background**: People accessing food banks are in crisis — they cannot afford to feed themselves or their families. Many are in temporary accommodation, fleeing domestic abuse, experiencing benefit sanctions, or dealing with sudden income loss. They need food urgently (often same-day), close to where they are, and without having to navigate complex processes. Dignity is paramount — the experience of asking for food is already deeply stigmatising for many people.

**Driver Intensity**: CRITICAL

**Enablers**: Simple digital or SMS-based voucher system; food bank location finder with real-time availability; referral to wider support (benefits, housing, debt advice); dietary and cultural food needs flagged; mobile-friendly with minimal data entry

**Blockers**: Digital exclusion (no smartphone, no data); complex registration processes; food banks far from where people live; inappropriate food (not meeting dietary or cultural needs); fear of data being used against them

---

### SD-5: Local Authorities — Coordinate Local Food Aid and Community Support

**Stakeholder**: Local Authority Community Services

**Driver Category**: OPERATIONAL

**Driver Statement**: Coordinate local food aid provision with wider community support services (housing, benefits, social care) to provide holistic support to vulnerable households rather than emergency food in isolation.

**Context & Background**: Many local authorities have developed Household Support Fund distribution mechanisms and coordinate local food aid partnerships. They want a platform that connects food bank referrals with broader support — "not just food" — ensuring that someone referred to a food bank is also connected to benefits advice, housing support, and mental health services.

**Driver Intensity**: MEDIUM

**Enablers**: Integration with local authority case management; referral pathway to wider support services; Household Support Fund distribution tracking; local food aid partnership coordination

**Blockers**: Fragmented local authority systems; inconsistent Household Support Fund criteria; food bank reluctance to share data with councils; privacy concerns from service users

---

## Driver-to-Goal Mapping

### Goal G-1: Digital Referral Coverage

**Derived From Drivers**: SD-1, SD-2, SD-4

**Goal Owner**: SRO

**Goal Statement**: Enable digital referrals to food banks from at least 80% of Jobcentres, 50% of council services, and 30% of GP practices by March 2029.

**Baseline**: Near-zero digital referrals (paper voucher system)

**Target**: 80% Jobcentre digital referral, 50% council, 30% GP

---

### Goal G-2: Surplus Food Redistribution Increase

**Derived From Drivers**: SD-3

**Goal Owner**: FareShare

**Goal Statement**: Increase surplus food redistributed through the platform by 25% by March 2028, measured in tonnes per year.

**Baseline**: FareShare currently redistributes approximately 30,000 tonnes/year

**Target**: 37,500 tonnes/year through improved coordination

---

### Goal G-3: National Food Insecurity Data

**Derived From Drivers**: SD-1, SD-5

**Goal Owner**: DEFRA

**Goal Statement**: Publish quarterly national food insecurity data (aggregate, anonymised) by March 2028, enabling evidence-based policy responses.

**Baseline**: No consistent national data (Trussell Trust publishes its own network data annually)

**Target**: Quarterly national data covering 70% of food aid provision

---

## Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DWP (SD-1) wants food insecurity data linked to benefit status; Trussell Trust (SD-2) opposes individual-level data sharing with government. Resolution: Aggregate anonymised data only shared with government. Individual-level data stays with food banks. Explicit consent required for any linkage. Independent data governance board.

- **Conflict 2**: Government wants to present the platform as a positive policy intervention; Trussell Trust (SD-2) views food banks as evidence of policy failure and resists government normalisation. Resolution: Platform branded as a coordination tool for the food aid sector, not a government food service. Trussell Trust involved in branding and communications.

**Synergies**:

- FareShare (SD-3) and food bank operators (SD-2) both benefit from better surplus food logistics
- Local authorities (SD-5) and all referral agencies benefit from digital referral replacing paper vouchers

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Household Support Fund guidance | Policy | DWP | Local authority distribution criteria | N/A |
| Trussell Trust State of Hunger reports | Research | Trussell Trust | Food insecurity drivers and trends | N/A |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 1 Programme | Governing principles | projects/000-global/ |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Food Bank Coordination System
**Model**: Claude Opus 4.6
