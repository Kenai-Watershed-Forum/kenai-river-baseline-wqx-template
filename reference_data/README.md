Shared reference data, snapshotted from the report repo and the qaqc repo at
template-creation time. Each year-repo created from this template gets its own
independent copy (no shared external source; duplication/drift accepted since these
change rarely).

- `master_reg_limits.xlsx` - regulatory threshold tables (from report repo
  `other/input/regulatory_limits/`).
- `baseline_sites.csv` - site metadata, 23 sites (from report repo `other/input/`).
- `sgs_site_names_matching_table.xlsx` - SGS lab sample ID to
  `monitoring_location_id`/`sample_condition` lookup (from qaqc repo).
- `analysis_code_matching_table.xlsx` - SGS analysis code to EPA method ID lookup
  (from qaqc repo).
- `fc_site_matching_table.csv`, `tss_site_matching_table.csv`,
  `ysi_site_matching_table.csv` - raw site name to `monitoring_location_id`/
  `sample_condition` lookups for Fecal Coliform, TSS, and YSI/turbidity data
  sources, each merging spring and summer variants into one table (extracted from
  `2025.qmd` inline `tribble()`s, Phase 2 step 2).
- `ysi_parameter_reference.csv` - YSI raw parameter name to analyte/EPA
  method/units lookup (extracted from 3 separate inline named vectors in
  `2025.qmd`).
