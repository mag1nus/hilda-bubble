# Todo

- [x] Confirm current special handling for cluster `0`.
- [x] Remove free-competence rendering for cluster `0`.
- [x] Pack and render cluster `0` as an ordinary cluster with label, zoom, tooltip, and PNG export support.
- [x] Verify JavaScript parsing and rendered graph counts.
- [x] Document review notes and verification results below.

## Review

- Status: complete
- Removed the special free-competence branch for cluster `0`; all groups now use the same cluster model, render path, tooltip path, and zoom path.
- Removed free-competence CSS, event handlers, state, status text, and PNG export styling.
- Verified JavaScript parsing with `rtk node -e ...`.
- Browser-verified via temporary localhost server and Playwright: seeded graph now renders 5 cluster groups, 0 free-competence groups, 21 competence circles, no console errors, and cluster `0` zoom/reset works through the standard cluster behavior.
