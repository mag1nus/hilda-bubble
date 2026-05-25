# Todo

- [x] Confirm the repository structure and local instructions are in place.
- [x] Create the initial task-tracking scaffold for future work.
- [x] Verify the resulting files and working tree state.
- [x] Create standalone `index.html` with graph and data tabs.
- [x] Implement add and remove row controls for semicolon CSV data.
- [x] Persist edited data to a file using browser file save with a download fallback.
- [x] Verify CSV parsing and row shape.
- [x] Replace graph view with a circlepackeR-style circle packing layout.
- [x] Group graph by `cluster -> competence -> names`.
- [x] Zoom into a cluster when the cluster is clicked.
- [x] Prevent circle overlap inside cluster circles by expanding parent circles as needed.
- [x] Dynamically size competence circles to show all names.
- [x] Restyle the app using Region Norrbotten visual identity cues.
- [x] Add traffic-light coloring to competence circles by name count.
- [x] Render cluster `0` as free competence circles without a parent cluster circle.
- [x] Enable zoom on free cluster `0` competence circles.
- [x] Export current graph view as PNG.
- [x] Preserve SVG colors in exported PNG.
- [x] Size competence circles from measured label content rather than a character-count heuristic.
- [x] Dynamically scale competence text and circles so each circle fills more of its available outer space.

## Review

- Status: initialized
- Notes: This repo currently contains only local RTK instructions and no application code.
- Added `data/testdata.csv` as semicolon-separated starter data for the standalone HTML visualization.
- Added `index.html` with an editable data tab, add/remove row controls, and CSV file save/download persistence.
- Verified `data/testdata.csv` has 21 valid semicolon-separated lines and `index.html` JavaScript parses successfully.
- Replaced the graph with a dependency-free circlepackeR-style packed-circle layout and verified the JavaScript syntax.
- Updated the circlepackeR graph hierarchy to `cluster -> competence -> names`, with names rendered inside competence circles.
- Added cluster click-to-zoom with root/Escape reset and verified the JavaScript syntax.
- Reworked packing to prevent competence-circle overlap inside clusters and verified generated SVG circle geometry.
- Added APA seed rows for Magnus, Hilda, and Test in cluster `1`.
- Sized competence circles from all rendered text lines so all names are shown without `+N names` summaries.
- Restyled the app using Region Norrbotten identity cues: Source Sans Pro, primary blue, bright blue accents, and clearer public-sector UI surfaces.
- Added traffic-light competence coloring: `<2` red, `2` orange, `>2` green.
- Renamed seed-data cluster `Satellit` to `0`.
- Rendered cluster `0` as nine free competence circles with no parent cluster circle or zoom target.
- Enabled click and keyboard zoom on free cluster `0` competence circles.
- Renamed the app title to `Kompetenskarta`.
- Softened the traffic-light competence circle colors.
- Added graph PNG export for the current SVG view.
- Inlined computed SVG styles during PNG export so CSS-driven colors are preserved.
- Replaced the competence-circle radius heuristic with a text-measurement-based layout so circles scale from actual label widths and line counts.
- Added iterative text fitting so competence labels and circle radii scale together instead of staying at fixed font sizes.
