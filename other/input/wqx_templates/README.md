Static WQX schema/lookup files that `functions/format_wqx.R` and
`functions/generate_cdx_export.R` read via `cfg$templates_dir`, carried forward
unmodified from the qaqc repo so those two shared function files don't need to be
edited:

- `wqx_template_matching_table.xlsx` - coordinates, result sample fraction, chemical
  preservative, and sample container lookups (sheets joined by `format_wqx.R`).
- `analytes_list_manual_edit.csv` - analyte-to-abbreviation lookup used to build
  WQX Activity IDs.
- `AWQMS_KWF_Baseline_template.xlsx` - the EPA AWQMS Baseline template defining the
  final WQX column set and order. TEMPLATE: when starting a new data year, copy this
  to `AWQMS_KWF_Baseline_{year}.xlsx` (the filename `cfg$wqx_template_file` expects)
  and verify EPA hasn't revised the template's column structure since the last
  year's submission.

These rarely change, but unlike `reference_data/` (read by this template's own Part A
code via `cfg$reference_dir`), they live here because the unmodified shared functions
expect them under `cfg$templates_dir` = `other/input/wqx_templates/`. Year-specific
working files also land in this directory at pipeline runtime (e.g. the generated
`analytes_list.csv`, `{year}_data_flag_decisions.csv`); those are not pre-populated.
