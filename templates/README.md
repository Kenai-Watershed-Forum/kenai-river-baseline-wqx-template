- `pipeline_template.qmd` - complete data ingestion, QA/QC evaluation, flagging,
  and CDX export workflow (Parts A-D), generalized from `kenai-river-wqx-qaqc`'s
  `project_year/2025.qmd`. See the per-year-repo architecture migration plan,
  Phase 2, step 2.
- `preliminary_report_template.qmd` - year-parameterized preliminary field
  season summary report, generalized from the report repo's
  `other/documents/preliminary_report_2025/2025_preliminary_summary.qmd`. See
  the migration plan, Phase 2, step 3. `pagebreak-h2.lua` and `references.bib`
  in this same directory are required alongside it (Quarto filter and
  bibliography file; copy all three together into a new year-repo). Search the
  document for `{{` tokens and `TEMPLATE:`/`MANUAL:` comments for everything
  that needs attention each year; several sections (executive summary findings,
  threshold-exceedance narrative, field QC discrepancy notes) are intentionally
  left as placeholders since they describe that year's actual results and
  can't be auto-generated.
- `pagebreak-h2.lua`, `references.bib` - supporting Quarto assets for
  `preliminary_report_template.qmd`, copied unchanged from the 2025 report.
