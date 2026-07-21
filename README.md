# Oracle Capture vs Transcript — Same-Video Demos

What the current production capture (attributes + events) records for a gameplay video, side by side with a full Pass-1 transcript of the **exact same file**. Videos stream directly from prod storage — no local files needed.

## Pages

| Page | What it is |
|---|---|
| [`index.html`](index.html) (= `nexon-capture-demo.html`) | **Presentation page** — MapleStory Idle video `He108OAfILEkavUA1JhVW` (Minnow · KR · 8th session). 40% sticky video + transcript-spine timeline (64 curated moments), prod plotted where it recorded anything: 30 logged · 18 no record · 16 wrong/flattened. Filters, flag-notes, click-to-seek, attributes-from-transcript panel. |
| [`nexon-capture-vs-transcript.html`](nexon-capture-vs-transcript.html) | **Audit page** — same video, strict one-row-per-timestamp table: TIME · prod's event (verbatim) · what's actually on screen. Blank purple cells = prod recorded nothing. Full raw transcript embedded at the bottom. |
| [`blueplanet-capture-vs-transcript.html`](blueplanet-capture-vs-transcript.html) | Blue Planet video `0BNqZE8g0jMLvi6alq14y` — prod's best-case record (37 described events) vs transcript: phantom boss, voluntary ad filed as "interruption", −60s timestamp drift on the whole tail, the Weekly-Card paywall Cancel with zero record. |

| [`case-studies.html`](case-studies.html) | **Show doc** — top 6 case studies + 4 linked-chain examples (upgrade→can't-afford→decline etc.) proving what transcript data makes possible. |

## Data provenance

- `data/compare_maple2_prod_full.json` — the original production record (studio API, verbatim: all 71 events with descriptions + every attribute group).
- `data/compare_bp_prod_record.json` — Blue Planet production record (10k export, verbatim).
- `data/He108_original_transcript.md`, `data/BP_0BNq_original_transcript.md` — Pass-1 transcripts (Gemini, 1 fps) of the same MP4s. Every claim in the pages traces to one of these files.

## Headline findings (Nexon video)

- A **KRW 6,000 real-money product fulfillment** stored as a generic "mailbox claim"
- Offer popups logged as `payment_attempt_initiated` (the event's own description says "Viewed…")
- "x10 weapon summon" events for on-screen bulk summons of **×168 / ×442 / ×245**
- The **2nd Job Advancement (Viper)** — the session's biggest milestone — has no event, and the class attribute records his **companion's** class instead
- A **"Quit the game?" dialog opened and cancelled mid-session** — zero record
- Ad request **denied by frequency cap** → forced ticket spend — zero record
- Combat power ×3.1 growth, all prices, wallet flows, on-screen `PLAYTIME 01:09:19` — no prod field exists for any number

*Internal pilot material — video URLs point to production storage.*
