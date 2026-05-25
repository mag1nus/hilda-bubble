# Lessons

## Current

- Preserve specific library or style references from the user; do not generalize `ggraph-inspired` to broader `R-inspired` language.
- The graph target is R `circlepackeR` style with hierarchy `cluster -> competence -> names`; names should be written inside competence circles.
- Preserve cluster click-to-zoom when changing graph rendering.
- Competence circles must not overlap inside a cluster; expand cluster and root circles as needed.
- Size competence circles from their full text content so every name is shown, not summarized.
- Color competence circles by name count: `<2` red, `2` orange, `>2` green.
- Cluster `0` is special: render its competence circles free in the root pack without a parent cluster circle, but keep each free circle zoomable.
- Treat the data schema as `competence`, `name`, and `cluster` rows unless the user revises it.
- Store starter data as semicolon-separated CSV, not TSV.
- Use fictional person names in the `name` column for test data, not duplicated competence labels.
- Follow the repo's local instructions first, then keep task tracking lightweight and explicit.
