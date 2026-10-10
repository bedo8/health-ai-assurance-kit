# Crosswalk

`crosswalk.csv` maps each CHAI governance element to the instruments a US health system is answering to. One row per CHAI element today; the goal is one row per CHAI control ID once the playbook IDs are loaded.

Columns: `chai_element_id`, `chai_element`, `ruaih_domain`, `urac_health_ai`, `nist_ai_rmf`, `iso_42001`, `texas_sb1188_traiga`, `hipaa_nprm`, `evidence_artifact`, `verified` (yes/no), `notes`.

`verified = no` means the mapping is a first pass and has not been checked against the primary text. Do not rely on an unverified row.

## Open items before v0.1

- [ ] Replace `ruaih_domain` with Joint Commission standard element IDs from the certification manual
- [ ] Add a `chai_control_id` column from the CHAI playbooks and expand rows
- [ ] Confirm Texas Medical Board review standards under SB 1188 are final
- [ ] Verify URAC Health Care AI Accreditation standard names against the URAC standards (first pass is from public summaries)
- [ ] Decide on a separate FDA PCCP/TPLC overlay for manufacturers
