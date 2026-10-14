# Public presentation site

This is a standalone static page, not the operational React application.
It contains local HTML/CSS only: no JavaScript, API request, external font or image
dependency. Its content describes the existing catalog, member, loan, return and
report scope. Product copy is Spanish; documentation is English.

Run `docker compose up --build --detach --wait`, then open http://localhost:8081.
The site also opens directly from index.html. It remains readable when the API is
unavailable. The login links point to the separate local HTTPS application;
change that deployment URL when publishing to a real domain.

The layout adapts to desktop and mobile, uses semantic landmarks and keyboard
focus indicators, and honors reduced-motion preferences. Browser evidence is
recorded in evidence/T-23.md after rendering at both sizes. With the sibling app
dependencies installed, run `npx playwright test tests/public-page.spec.js` from
the app repository. This is shared browser test tooling, not a runtime dependency
of the static site.
