Shared R functions, carried forward from the live `kenai-river-wqx-qaqc` repo
(`other/misc/qaqc_repo_transition/functions/`, the source of truth) and from the
report repo (`kenai-river-wqx/functions/`):

- `format_wqx.R` - WQX schema formatting (qaqc repo). Sourced by Part B of
  `templates/pipeline_template.qmd`.
- `apply_qaqc_flags.R` - QA/QC flagging logic (qaqc repo). Sourced by Part D.
- `generate_cdx_export.R` - CDX-ready export generation (qaqc repo). Sourced by Part D.
- `static_boxplot_function.R` - parameter boxplots (report repo). Used by the
  preliminary report template.
- `threshold_table.R` - regulatory threshold table rendering (report repo). Used by
  the preliminary report template.
- `render_plots.R` - plot rendering helper (report repo). Used by the preliminary
  report template.
- `table_download.R` - downloadable table helper (report repo). Used by the
  preliminary report template.

These are independent snapshots copied at template-creation time, not symlinks or a
shared package; each year-repo created from this template gets its own copy and any
later bugfixes need to be back-ported manually (duplication/drift accepted since
these change rarely).
