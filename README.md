# health-ai-assurance-kit

An open toolkit for US healthcare organizations that have been told to "get RUAIH-ready" and have no dedicated AI risk staff.

It maps the Coalition for Health AI (CHAI) eight governance elements to the Joint Commission Responsible Use of AI in Healthcare (RUAIH) certification domains, URAC Health Care AI Accreditation, NIST AI RMF, ISO/IEC 42001, Texas SB 1188 / HB 149 (TRAIGA), and the proposed HIPAA Security Rule — so a health system sees one control set and one evidence list instead of six.

## Who this is for

- Hospital and health-system CISOs, CMIOs, compliance and quality leaders preparing for RUAIH
- Health-AI vendors answering customer due-diligence questionnaires
- Anyone running an AI governance committee that has policies but no operating system

## What's here

| Folder | What it is | Status |
| --- | --- | --- |
| `crosswalk/` | CHAI elements × frameworks control mapping (CSV + markdown) | skeleton, first-pass mappings, unverified |
| `readiness-assessment/` | RUAIH readiness questionnaire and scorer | planned |
| `vendor-assessment/` | Health-AI vendor due-diligence template | planned |
| `policy-templates/` | AI policy, intake form, clinician disclosure script, human-review attestation | planned |
| `evidence-map/` | Which artifact proves each control, owner, cadence | planned |

## How to run a self-assessment in a day

1. Open `crosswalk/crosswalk.csv` and delete the columns for instruments that don't apply to you (most deployers can drop the FDA overlay).
2. For each row, mark whether the evidence artifact in the last column exists, exists but is stale, or doesn't exist.
3. Roll the results up by RUAIH domain. The domain with the most "doesn't exist" entries is your first remediation sprint.

## Status and caveats

Every mapping in the crosswalk is a first pass from the published frameworks and must be verified against the primary text before you rely on it. This is not legal or regulatory advice. Nothing here is endorsed by Joint Commission, CHAI, NIST, ISO, FDA, or the State of Texas.

## Changelog

See `CHANGELOG.md`. Rows in the crosswalk flip to `verified = yes` only when checked against the primary text, and that change is logged.

## Citing

See `CITATION.cff`.

## License

MIT. Use it, fork it, improve it. Pull requests welcome, especially from clinicians and compliance officers who find a mapping wrong.
