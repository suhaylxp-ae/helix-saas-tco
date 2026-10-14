# On-prem vs SaaS: 5-year cost

A one-page calculator that compares five years of running a platform on your own servers with five years of SaaS. It is a cautious example for a conversation. It is not a quote.

**Personal project. Not a BMC Helix tool. My own views. Illustrative estimates only.**

Live: https://suhaylxp-ae.github.io/helix-saas-tco/

## Use it in 3 steps

1. Tick the solutions you run. Check the server count, the team size, and the upgrade fields.
2. Leave the yearly SaaS fee blank to see the fee where the 5-year totals match, or type your own fee.
3. Read the totals, then copy the link or print one page.

Open `index.html` in a browser. There is no build step. Chart.js loads from a CDN. If the chart does not load from a local file, run `python3 -m http.server 8080` and open http://127.0.0.1:8080/.

Helix is a trademark of BMC Software.
