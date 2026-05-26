# Todo

- [x] Replace fixed graph dimensions with responsive container-derived dimensions.
- [x] Re-render circle packing on browser/container resize.
- [x] Scale circle geometry and SVG text from available graph area for maximum readability.
- [x] Remove the CSV paste input box from the Data tab.
- [x] Update embedded seed data from `testdata(3).csv`.
- [x] Save browser state and load it before embedded seed data.
- [x] Rename `index.html` to `kompetens.html`.
- [x] Create a browser favicon for `kompetens.html`.
- [x] Keep zoom, CSV file import/export, row editing, PNG export, and ordinary cluster `0` behavior intact.
- [x] Verify syntax and browser resize behavior.
- [x] Document review notes and verification results below.

## Review

- Status: complete
- Graph sizing now reads the rendered SVG dimensions and recalculates the circle pack through `ResizeObserver`, so browser size changes update the viewBox, circle positions, and text scale.
- Increased graph height and reduced non-text padding/gaps so the available space is used for larger, more readable labels.
- Removed the CSV paste textarea and Render CSV button from the Data tab; file upload/open/save/download and row editing remain.
- Replaced the embedded seed data with the exact contents of `testdata(3).csv`, yielding 23 rows, 13 clusters, and 21 competences.
- Added browser state persistence: current CSV is saved to `localStorage` and a cookie backup, and saved state loads before embedded seed data.
- Verified JavaScript parsing with `rtk node -e ...`.
- Browser-verified via temporary localhost server and Playwright: no CSV textarea, responsive viewBox updates across viewport sizes, saved browser state overrides seed on reload, clearing browser state falls back to the new seed, and console has no errors.
- Renamed the standalone app file from `index.html` to `kompetens.html` and verified the renamed file parses with the `testdata(3).csv` seed intact.
- Added a self-contained SVG favicon data URL to `kompetens.html` using the Region Norrbotten blue/cyan palette and circle-pack motif.
