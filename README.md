# What does running it yourself really cost?

A one-page calculator for the days your team spends running BMC Helix on its own servers, and what that is worth next to SaaS. It follows the shared-responsibility picture: you keep governance, reporting, and administration. BMC Helix runs the platform tasks on SaaS.

**Personal project. Not a BMC Helix tool. My own views. Illustrative estimates only.**

Live: https://suhaylxp-ae.github.io/helix-saas-tco/

Task days, the scaling rule, and the sources are in `effort-defaults.md`.

## Use it in 3 steps

1. Tick the solutions you run on-prem. Service management starts ticked.
2. Read who runs what. Edit any days-a-year number. The i shows that the default is an estimate.
3. Read the days and the staff-time figure. Copy the link or print one page. Add a server count or your own SaaS quote only if you have one.

Open `index.html` in a browser. There is no build step. Chart.js loads from a CDN. If the chart does not load from a local file, run `python3 -m http.server 8080` and open http://127.0.0.1:8080/.

Helix is a trademark of BMC Software.
