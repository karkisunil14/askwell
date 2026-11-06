# Launch check kit

Used in Phase 2 (widget on a plain page), Phase 3 (answers from the PDF) and the launch check.

| File | Use |
|---|---|
| `hollow-pine-guide.pdf` | **Knowledge** → upload. A fictional coffee shop's customer guide, 2 pages. |
| `index.html` | The plain HTML page. Paste the script tag from **Install** at the marked line at the bottom. |
| `askwell-about.txt` | Phase 6, off camera: paste as text into the "Askwell" project behind `LANDING_WIDGET_KEY` |

## Open the page

Serve it. Don't double-click it: from `file://` the page origin is `null`, and the widget panel can't talk to the page.

```bash
cd launch-check
python3 -m http.server 4000
```

Open http://localhost:4000. After you paste or change the script tag, reload.

## Questions to ask

The answers are only in the PDF, so a correct answer proves it came from the upload.

| Ask | Expected answer |
|---|---|
| Can I pause my subscription? | Yes, for up to 12 weeks at a time, from Account → Subscription |
| What if I don't like a coffee? | The Second Bag Promise: tell them within 30 days, they send a different coffee for free, no return needed |
| Do you ship to Canada? | No, only the 50 US states for now |
| Do you sell tea? | The "I don't know" reply (the PDF never mentions tea) |

Landing page chat (`askwell-about.txt`): "What do I get on Pro?" → 5 projects, 2,000 messages a month, custom style, no badge.

## Pink button

**Customize** → button color `#ec4899` → **Save** → reload http://localhost:4000. The shop page is green and cream, so the pink button stands out.
