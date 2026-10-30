# kmitl-odoo-state-machine

Interactive state machine simulators for KMITL Odoo 16.0 models (stately.ai-style).
Each page is a single self-contained HTML file — open it in a browser, no build needed.

| Model | Page |
|---|---|
| `purchase.request` (พ.1) | [purchase_request.html](purchase_request.html) |

Transitions are mapped by hand from the `purchase_request_*` modules in the KMITL
addons repo; every event shows the `file:line` it came from. Update the page when
the workflow changes.
