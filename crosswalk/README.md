# Crosswalk

`crosswalk.csv` maps each CHAI governance domain and subdomain to the instruments a US health system is answering to. One row per CHAI domain today (1, 2, 3, 4.1–4.5); the goal is one row per CHAI baseline control once the playbook PDFs are loaded.

Columns:

| Column | Content |
| --- | --- |
| `chai_id`, `chai_domain` | CHAI's own numbering and names (S1) |
| `ruaih_guidance_2025` | Element number and name from the seven-element Sept 2025 guidance (S2) |
| `ruaih_certification` | Empty until the June 2026 certification standards are obtained (S3) |
| `urac_health_ai` | URAC's seven public evaluation areas (S4); standard-level IDs need the paid standards |
| `nist_ai_rmf` | Function and category IDs (S5) |
| `iso_42001` | Clause and Annex A control references (S6) |
| `texas_sb1188_traiga` | Statutory obligations under SB 1188 (Health & Safety Code ch. 183) and HB 149 (S7, S8) |
| `hipaa_nprm` | Safeguards under the proposed Security Rule (S9) |
| `evidence_artifact` | The author's proposed proof for the row |

Source IDs (S1–S9) are defined in `../SOURCES.md`.

`verification.csv` has one line per cell: `status` is `primary`, `secondary`, `unverified`, or `author`, with the source ID, the date checked, and a note. Do not rely on a cell whose status is not `primary`.

## Open items before v0.1

- [x] RUAIH column mapped to the seven elements of the Sept 2025 guidance (primary)
- [x] CHAI numbering aligned to the four-domain structure
- [x] URAC column uses URAC's published evaluation areas
- [x] Texas column checked against §183.005 statute text
- [ ] Obtain the Joint Commission certification standards and fill `ruaih_certification`
- [ ] Load CHAI playbook baseline controls; expand to one row per control
- [ ] Check NIST column against AI RMF 1.0 subcategory text
- [ ] Purchase ISO/IEC 42001 and check the ISO column
- [ ] Read the HIPAA NPRM text and move the HIPAA column to primary
- [ ] Confirm Texas Medical Board standards referenced in §183.005(a)(3) exist in final form
- [ ] Decide on a separate FDA PCCP/TPLC overlay for manufacturers
