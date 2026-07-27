# Jemena (jemena)

Jemena is an Australian energy infrastructure owner-operator, headquartered in Melbourne and owned by SGSP (Australia) Assets — 60% State Grid Corporation of China, 40% Singapore Power. It sits on the poles-and-pipes side of the value chain, not the retail side: it runs the Jemena Electricity Network distributing power to north and north-west Melbourne, the Jemena Gas Network distributing gas across New South Wales, the Eastern, Queensland and Northern Gas Pipelines, the Colongra storage facility, and holds 50% of ActewAGL's ACT distribution networks. Its API posture is the inverse of what the Australian Consumer Data Right story would predict. Jemena is NOT a designated CDR energy data holder — the CDR energy designation covers retailers as primary data holders and AEMO as secondary data holder, and the live CDR Register energy brand list contains 84 brands, all of them retailers and none of them a distribution network. There is consequently no Jemena consumer usage or billing API, and the Electricity Outlook customer smart-meter portal no longer resolves in DNS. Jemena also publishes no open market or network data API; its outage map is CloudFront geo-restricted and its Daily Gas Data product is a paid annual email subscription. What Jemena does run is a real, live, standards-conformant machine-to-machine API for grid control: the JEN CSIP-AUS Utility Server, an IEEE 2030.5 / SEP2 implementation of the CSIP-AUS (SA TS 5573) profile, stood up to satisfy the Victorian Government's emergency backstop mandate for remotely curtailable rooftop solar.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/jemena/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/jemena/refs/heads/main/apis.yml)

## Tags

- Energy
- Australia
- Utilities
- Electricity
- Gas
- Grid
- Network Distributor
- DER
- Solar
- Smart Metering
- Demand Response
- IEEE 2030.5

## Timestamps

- **Created:** 2026-07-27
- **Modified:** 2026-07-27

## APIs

### Jemena CSIP-AUS Utility Server (IEEE 2030.5)

Jemena Electricity Networks' CSIP-AUS compliant control server — an IEEE 2030.5 (Smart Energy Profile 2.0) implementation of the Common Smart Inverter Profile Australia (SA TS 5573) — used to discover, monitor and remotely curtail small and medium embedded generation (rooftop solar, batteries, VPP fleets) on the Jemena Victorian distribution network under the Victorian Government's emergency backstop mandate. Access is not self-serve: an OEM or aggregator must submit a Certificate Signing Request and IP addresses to whitelist, receive a Jemena-signed IEEE 2030.5 PKI client certificate, pass connectivity, discovery and functional tests in staging, then be onboarded to production and added to Jemena's CSIP-AUS Approved Listing.

- **Human URL:** [https://www.jemena.com.au/electricity/solar-connections/victoria-emergency-backstop-mechanism/emergency-backstop-mechanism-documents/](https://www.jemena.com.au/electricity/solar-connections/victoria-emergency-backstop-mechanism/emergency-backstop-mechanism-documents/)
- **Base URL:** `https://sep2.aws.jemena.com.au:8443/sep2`

#### Tags

- DER
- Solar
- Grid
- IEEE 2030.5
- CSIP-AUS
- Demand Response
- Smart Inverters

#### Properties

- [Documentation](https://www.jemena.com.au/siteassets/asset-folder/documents/electricity/embedded-generation/jen-oem-technical-guide_handbook_v1.0.1-final.pdf) — JEN OEM technical guide handbook v1.0 (12 June 2025)
- [Documentation](https://www.jemena.com.au/siteassets/asset-folder/documents/electricity/embedded-generation/embedded-generation-emergency-backstop-requirements_public_01-12-2025.pdf) — Embedded Generation Emergency Backstop Requirements (1 December 2025)
- [Documentation](https://www.jemena.com.au/siteassets/asset-folder/documents/electricity/embedded-generation/installer-csip-aus-commissioning-test-procedure_public_22052024.pdf) — Installer CSIP-AUS Commissioning Test Procedure (22 May 2024)
- [Documentation](https://www.jemena.com.au/electricity/solar-connections/victoria-emergency-backstop-mechanism/) — Victoria emergency backstop mechanism
- [Documentation](https://www.jemena.com.au/electricity/solar-and-other-technologies/jemena-approved-list-of-inverters/) — Jemena CSIP-AUS Approved Listing
- [Specification](https://www.csipaus.org/about) — CSIP-AUS (SA TS 5573), the Australian IEEE 2030.5 profile

## Common Properties

- [Website](https://www.jemena.com.au/)
- [Documentation](https://www.jemena.com.au/electricity/solar-connections/victoria-emergency-backstop-mechanism/emergency-backstop-mechanism-documents/)
- [LinkedIn](https://www.linkedin.com/company/jemena)
- [Sign Up](https://myportal.jemena.com.au/)
- [Portal](https://myservices.jemena.com.au/edp/login/auth)
- [Status Page](https://poweroutages.jemena.com.au/)
- [Support](https://www.jemena.com.au/help-support/)
- [Privacy Policy](https://www.jemena.com.au/about-us/privacy-policy/)

## Maintainers

- **Kin Lane** — kin@apievangelist.com
