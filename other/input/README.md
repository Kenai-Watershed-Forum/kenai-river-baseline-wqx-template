Year-specific raw data and supporting assets for a repo created from this
template. In this template repo, only stable (non-year-specific) subfolders are
pre-populated; a real year-repo additionally needs a `{{YEAR}}/` directory with
that year's raw lab/field data (see `templates/pipeline_template.qmd` and
`templates/preliminary_report_template.qmd` Year Configuration/setup chunks for
the exact expected layout, e.g. `{{YEAR}}/spring_{{YEAR}}_wqx_data/`,
`{{YEAR}}/summer_{{YEAR}}_wqx_data/`, `{{YEAR}}/images/`).

- `images/` - stable report images reused every year (watershed/site maps, KWF
  logo). Not year-specific; carried forward as-is from the report repo.
- `wqx_templates/` - WQX/CDX formatting templates and matching tables used by
  `pipeline_template.qmd` Parts B-D. See that directory's own README.
- `{{YEAR}}/images/` (not pre-populated here) - that year's field season cover
  photo for `preliminary_report_template.qmd`; add one `.jpg`/`.jpeg` and point
  the `{{FIELDWORK_IMAGE_FILENAME}}` token at it.
