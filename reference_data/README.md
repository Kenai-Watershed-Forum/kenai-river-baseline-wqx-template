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
- `parameter_display_reference.csv` - analyte to report display name/parameter
  group/group sort order, used by `preliminary_report_template.qmd` (extracted
  from inline `param_labels`/`param_groups`/`group_order` vectors in
  `2025_preliminary_summary.qmd`).
- `qc_dup_site_display_names.csv` - raw field-duplicate site name (as spelled
  across the SGS, TSS, and YSI data sources) to a consistent display name, used
  by `preliminary_report_template.qmd`'s Field Duplicates table (extracted from
  the inline `dup_site_map` named vector in `2025_preliminary_summary.qmd`).
- `hardness_dependent_metals_formula_params.csv` - ADEC 18 AAC 70 hardness-
  dependent aquatic life chronic criteria formula constants (m_c, b_c, cf_a,
  cf_b) for Cadmium, Chromium, Copper, Lead, and Zinc, used by
  `preliminary_report_template.qmd`'s threshold comparison. These are
  regulatory constants, not year-specific data; distilled from the report
  repo's `other/input/regulatory_limits/formatted_reg_vals/
  calculated_metals_reg_vals.csv` (a 2,883-row historical-results export, not
  copied here directly) down to the 5 distinct formula rows it actually
  encodes.
