# kenai-river-baseline-wqx-template

Template repository for a single year's Kenai River Baseline Water Quality Monitoring
data pipeline. Mark this repo as a GitHub "template repository" (Settings > Template
repository), then use "Use this template" to create `kenai-river-wqx-{year}` (e.g.
`kenai-river-wqx-2025`) when work begins on a new data year.

Each year-repo created from this template ingests that year's raw lab EDDs, applies
QA/QC, formats and exports WQX/CDX upload files, and renders a preliminary annual
summary report, all from one self-contained repo.

## Layout

- `templates/pipeline_template.qmd` — the annual QA/QC + CDX export pipeline (Parts
  A-D: ingestion, WQX formatting, QA/QC checklist, CDX export). Copy into the new
  repo as `{year}.qmd` and update the Year Configuration block.
- `templates/preliminary_report_template.qmd` — the preliminary annual summary report,
  parameterized by year. Copy into the new repo and update the year/config.
- `functions/` — shared R helper functions used by the pipeline and report (WQX
  formatting, QA/QC flagging, CDX export generation, plotting, threshold tables).
- `reference_data/` — reference data copied fresh into each new year-repo at creation
  time (regulatory thresholds, site metadata, WQX matching tables). Not a shared
  external source; each year-repo's copy is independent after creation.
- `other/input/` — raw lab EDDs and field data for the year (not gitignored; one
  year of lab data is a manageable size to commit).
- `other/output/` — intermediate QA/QC outputs and final WQX/CDX upload files.

## Related repos

- [kenai-river-wqx](https://github.com/Kenai-Watershed-Forum/kenai-river-wqx) — the
  report repo; hosts the integrated multi-year Quarto book, reading published data
  from EPA's Water Quality Portal.
- [kenai-river-wqx-qaqc](https://github.com/Kenai-Watershed-Forum/kenai-river-wqx-qaqc) —
  the predecessor single-repo QA/QC pipeline (2014-2025), retained as read-only
  historical reference once this template-based, per-year-repo architecture is in
  place for all active years.
