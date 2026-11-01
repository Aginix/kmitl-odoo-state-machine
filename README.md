# kmitl-odoo-state-machine

Interactive state machine simulator for the KMITL Odoo 16.0 purchasing flow (stately.ai-style).
Single self-contained `index.html` — open it in a browser, no build needed.

## Menu

| Menu | Model |
|---|---|
| รวม (flow เดียว) | every document as a swimlane in time order, cross-document links, scenario player |
| ภาพรวม | all documents side by side, every event available right now |
| พ.1 | `purchase.request` |
| หนังสือ พ.1 | `sarabun.document` whose origin is the พ.1 |
| พจ.1 | `purchase.request.approval` |
| หนังสือ พจ.1 | `sarabun.document` whose origin is the พจ.1 |
| PO | `purchase.order` |

Firing an event cascades across documents the way the code does (sarabun callbacks,
พจ.1 writing to พ.1, PO creation). Events marked ⚡ are callbacks — clicking one finds
and fires the event that causes it. The Context panel drives the guards (e-GP amount,
contract mode, has_signed, …).

Transitions are mapped by hand from the KMITL addons repo; every event shows the
`file:line` it came from. Update `M` / `CASCADE` in `index.html` when the workflow changes.
