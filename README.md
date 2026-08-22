# Jemena (jemena)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
