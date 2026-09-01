---
target: the tasting notes section (site/index.html)
total_score: 22
max_score: 32
na_heuristics: 7,10
p0_count: 0
p1_count: 2
target_identity: "file:/home/user/CapeCask/site/index.html"
target_fingerprint: "sha256:a02941c2bd092f20c92e214b34cbfdafe18dbbd368cb9ac1b077081c53e6be2e"
target_path: /home/user/CapeCask/site/index.html
timestamp: 2026-09-01T15-53-20Z
slug: site-index-html
---
Method: dual-agent (A: design review sub-agent · B: detector/browser-evidence sub-agent)

# Critique — site/index.html (focus: tasting notes section)

## Design Health Score

| # | Heuristic | Score | Key Issue |
|---|-----------|-------|-----------|
| 1 | Visibility of System Status | 3 | Form feedback good; no active-section indicator in sticky nav on a 6,700px page |
| 2 | Match System / Real World | 3 | Authentic category language, but "smooth finish" contradicts the cask-strength positioning; "hazmat" unexplained |
| 3 | User Control and Freedom | 3 | Reduced-motion honored; age gate re-fires each session and lacks focus trap |
| 4 | Consistency and Standards | 2 | Release cards style one bottle as three SKUs; specs restated in four visual systems while flavor gets one |
| 5 | Error Prevention | 3 | Honeypot, validation, disabled-during-submit; generic failure copy |
| 6 | Recognition Rather Than Recall | 2 | Reader must assemble Batch 01 + Cape Gold + 16-Year Reserve into one bottle |
| 7 | Flexibility and Efficiency | n/a | Persuade surface, single linear journey |
| 8 | Aesthetic and Minimalist Design | 3 | Restrained, but proof/oak/pot-still facts stated 3–4x each |
| 9 | Error Recovery | 3 | Failure messages offer human fallback (founder email) |
| 10 | Help and Documentation | n/a | Persuade landing; contact row serves the role |
| **Total** | | **22/32** | **Good (69%)** |

## Design Specificity Verdict

The page frame is genuinely authored for this product (cask-head SVG spec stencil, Table Mountain band, 1672/angels'-share/Colombard-Chenin copy) — but the tasting strip, the sensory heart of a taste product, is the single most category-interchangeable element on the page. "Rich stone fruit · Warm spice · Oak & vanilla · Long, smooth finish" could sit on any brown spirit at any price. Bespoke everywhere except at the sensory core — that inversion is the page's defining design flaw. "Smooth" also contradicts the page's own fire/hazmat positioning.

Deterministic scan (degraded regex mode; parser modules unavailable): 2 advisory findings, both verified — `overused-font` (Fraunces, line 21; mitigated by the three-face system) and `em-dash-overuse` (16 in body copy). No false positives. Absence of further hits is not a clean bill of health given degraded mode; manual contrast verification passed (all token pairs AA or better, tightest 4.70:1).

No user-visible overlay was possible (headless session, no human-attended browser); render evidence captured via scripted Chromium at 1440px and 390px instead.

## Priority Issues

- **[P1] The tasting notes don't earn the flavor story.** One 24-word sentence, smallest featured text in the section, dead last after six spec rows, beside an 84px grapes thumbnail. The Spirit section spends ~85% of its space on how it's made, ~5% on what it's like to drink. Fix: promote tasting to a designed moment (nose/palate/finish structure, liquid-not-agriculture imagery, cask-strength-literate copy). Suggested: full redesign (in progress — see design/tasting-directions.html).
- **[P1] The Release grid reads as three products and buries the 16-year age statement.** Three identical SKU-styled cards for facets of one bottle; hover affordances with no action. Fix: recompose as one bottle profile; lead with the age statement. Suggested command: /impeccable layout + /impeccable clarify.
- **[P2] Tasting-strip layout mechanically breaks at desktop width.** flex-wrap orphans the notes onto a full-width row below the thumbnail (verified in screenshot). Superseded by the P1 redesign.
- **[P2] "Not yet available for sale in the United States" hides in footer fine print.** Surface pre-release status proudly in the signup section — stronger scarcity frame, honest. Suggested command: /impeccable clarify.
- **[P3] Enthusiast jargon (hazmat, barrel picks, heart cut) has no on-ramp for first-timers.** One aside per term keeps the voice while widening the funnel. Suggested command: /impeccable clarify.

## Cognitive Load

4 of 8 checklist failures: chunking (6-row spec list; 12 stacked blocks on mobile), grouping (tasting strip disassociates), visual hierarchy (inverted at section climax), working memory (Release grid merge). No decision point exceeds 4 options — decision architecture is clean.

## Emotional Journey

Strong entry peaks (age gate, hero) and a genuinely good trust-building end (personal email, "nothing more, nothing often"). The valley is exactly where the peak should be: the flavor reveal. The ask arrives without the sensory promise being cashed.

## Persona Red Flags

**Jordan (first-timer):** #spirit lede addresses someone else ("If you chase barrel picks…"); 140+ proof never translated into experience; three-products confusion; availability discovered in fine print.
**Casey (distracted mobile):** 8,653px page, no mobile menu (only "Join the List" survives ≤700px), several-second smooth-scroll flythrough to the form, tasting strip pattern-matches to a footnote at glance speed, age gate re-fires per session.

## Minor Observations

Dead CSS (.tasting-strip .spec-key duplicates .spec-list rule), no og:image, non-interactive cards with hover affordances, .hero-cask naming fossil, .tm-caption at legibility floor, age-gate focus not managed, footer year JS-only, grapes.jpg arbitrary crop.

## Questions to Consider

1. If a visitor remembers one sentence, the design votes four times for "70%+ ABV" and once, quietly, for what it tastes like. Is that the intended vote?
2. Why does the only cask-strength South African brandy describe its flavor in words that fit a $14 supermarket blend?
3. The lede recruits hazmat-chasers; the tasting note offers "smooth" and "on the rocks." Which drinker is the page for?
