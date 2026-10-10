# health-ai-assurance-kit

An open toolkit for US healthcare organizations preparing for AI governance certification or accreditation with no dedicated AI risk staff.

It maps the Coalition for Health AI (CHAI) governance framework — four domains, with domain 4 split into five subdomains — to the instruments a health system is answering to: the Joint Commission / CHAI Responsible Use of AI in Healthcare (RUAIH) guidance, URAC Health Care AI Accreditation, NIST AI RMF, ISO/IEC 42001, Texas SB 1188 and HB 149 (TRAIGA), and the proposed HIPAA Security Rule. One control set, one evidence list.

## Who this is for

- Hospital and health-system CISOs, CMIOs, compliance and quality leaders preparing for RUAIH certification or URAC accreditation
- Health-AI vendors answering customer due-diligence questionnaires
- Anyone running an AI governance committee that has policies but no operating system

## What's here

| Folder | What it is | Status |
| --- | --- | --- |
| `crosswalk/` | CHAI domains × instruments, with a per-cell verification record | element level (8 rows); control level in progress |
| `SOURCES.md` | Every instrument cited, with access type and the date it was last checked | current |
| `docs/sources-to-acquire.md` | What still has to be obtained, and what each one unblocks | current |
| `readiness-assessment/` | RUAIH readiness questionnaire and scorer | planned |
| `vendor-assessment/` | Health-AI vendor due-diligence template | planned |
| `policy-templates/` | AI policy, intake form, clinician disclosure script, human-review attestation | planned |
| `evidence-map/` | Which artifact proves each control, owner, cadence | planned |

## What it can do today

The crosswalk is at element level: eight rows, one per CHAI domain or subdomain. That is enough to see which instruments bear on each part of a governance program and to check whether the evidence artifact for each exists. It is not enough to score a program or prepare for a survey. Control-level rows arrive once the CHAI playbook controls are loaded (see `docs/sources-to-acquire.md`).

To use it now: open `crosswalk/crosswalk.csv`, drop the columns for instruments that don't apply to you, and for each row mark whether the evidence artifact exists, exists but is stale, or doesn't exist. The row with the most gaps is the first remediation sprint.

## What it is not yet

- Not control-level. Eight rows, not sixty.
- Not a map to the RUAIH *certification*. The `ruaih_guidance_2025` column is verified against the Sept 2025 guidance (seven elements). The `ruaih_certification` column is empty until the Joint Commission certification standards are obtained; the two documents may not share a structure.
- Not verified end to end. `crosswalk/verification.csv` records, per cell, whether the mapping was checked against primary text, a secondary summary, or not at all. Read it before relying on any cell.
- Not legal or regulatory advice, and not endorsed by Joint Commission, CHAI, URAC, NIST, ISO, FDA, or the State of Texas.

## Verification discipline

A cell moves to `primary` only when checked against the instrument's own text, and the change is logged in `CHANGELOG.md`. Clause numbers and standard names are mapped freely; text from paid standards is never reproduced.

## Citing

See `CITATION.cff`.

## License

MIT. Use it, fork it, improve it. Pull requests welcome, especially from clinicians and compliance officers who find a mapping wrong.
