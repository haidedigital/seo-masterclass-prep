# Genspark Slide Prompts — Част 3 (Monitoring Stack + Survival Workflow)

> **Deck:** Техническо SEO в AI ерата — Адриан Николов, Haide Digital
> **Event:** Enterprise Magazine × EURODEA SEO Masterclass, София, 23 април 2026
> **Source script:** [script-part3-monitoring-and-workflow.md](script-part3-monitoring-and-workflow.md)
> **Slide count:** 15 (слайдове 58–72, финална част на същия Genspark deck от Part 1 + Part 2)
> **Total runtime:** ~30 минути (pure script, без live browser demos)
> **Language strategy:** EN инструкции към Genspark, БГ slide content в кавички `" "` (не превеждаме).

---

## ВАЖНО — КОНТЕКСТ ЗА GENSPARK (Part 3 — FINAL)

**Тази генерация е Част 3 (финална) от 3-частна презентация.** Добавяш тези 15 слайда към същия Genspark deck, който вече съдържа Part 1 (слайдове 1–26) и Part 2 (слайдове 27–57). **Не започвай нов deck.**

- **Part 1 (DONE)** — слайдове 1–26 — Въведение + как работят AI моделите
- **Part 2 (DONE)** — слайдове 27–57 — Чеклист walk-through + 5 live tool demos
- **Part 3 (ТОЗИ ДОКУМЕНТ, ФИНАЛ)** — слайдове 58–72 — Monitoring stack + survival workflow

**Global Style Brief от Part 1 остава в сила.** Не го paste-вай отново. Master QR element продължава bottom-right на всеки слайд. Slide 71 има enlarged QR (Growth Gap Review CTA).

**След тази генерация deck-ът е ЗАВЪРШЕН: 72 слайда за 90 минути.**

---

## WHAT'S NEW IN PART 3 (визуални patterns)

1. **LAYER CARD pattern (НОВ)** — slides 63–67. Repeatable card за всеки от 5-те monitoring layers. Identical structure: cadence badge → hero number → title → 3 bullets → red-thread tool strip. Consistency е критична — audience трябва да разпознае pattern-а при третия layer.
2. Reuse от Part 1 + Part 2: SECTION DIVIDER, STAT HERO, SPLIT SCREEN, GRID, TRANSITION.
3. **No TOOL ENTRY/EXIT slides in Part 3** — няма live demos. Tools се референцират от red-thread strip на LAYER CARDS.

### LAYER CARD Pattern Specs (за reference при генериране на slides 63–67)

```
Background: Wild Sand #E4EEF0.

Top-left: cadence badge — rounded pill, Haide Orange #FF5B04 background, white text inside,
Poppins Bold 16pt, uppercase. Values: "DAILY", "WEEKLY", "MONTHLY", "ON EVERY DEPLOY".

Hero number: Poppins Black 140pt, Deep Sea Green #075056, left-aligned.
Values: "01", "02", "03", "04", "05".

Layer title: Poppins Bold 48pt, Mirage #16232A, directly below the number.

3-bullet description: Poppins Medium 22pt, Mirage #16232A, stacked vertically with breathing room.
Each bullet has a small grey dot prefix.

Bottom red-thread strip: full-width bar at slide bottom, Wild Sand background with left-aligned text:
arrow icon (→) + "вход: [Tool Name]" in Poppins SemiBold 18pt, Haide Orange #FF5B04.

CRITICAL per-slide anti-crowding: hero number + title + 3 bullets + 1 strip = max 6 elements.
No screenshots, no diagrams, no code snippets on layer cards. Pure information hierarchy.
```

---

# ЧАСТ 3 — MONITORING & SURVIVAL (Слайдове 58–72)

## 3.0 Opening (Слайдове 58–60)

---

## SLIDE 58 — Part 3 Section Divider

**Purpose:** Финален section divider. Breathing moment след Part 2.
**Layout:** SECTION DIVIDER (same pattern as slide 27 Part 2 и slide 1 Part 1).
**Speaker alignment:** script → Слайд 58 (ред 55–61).

### Genspark Prompt

```
Create a SECTION DIVIDER slide. Full-bleed background: Deep Sea Green #075056.

Centered vertically.

Small eyebrow label, Poppins SemiBold 20pt, Haide Orange #FF5B04, uppercase, centered:
"ЧАСТ 3"

Main headline below, Poppins Bold 110pt, white #FFFFFF, centered:
"Monitoring & Survival"

Subtitle below headline, Poppins Regular 28pt, Wild Sand #E4EEF0, centered:
"Система, която оцелява volatility-то"

Master QR corner element in bottom-right (80x80, white on transparent).

CRITICAL: Same treatment as Part 1 slide 1 and Part 2 slide 27 — pure breathing room. No decoration.
```

---

## SLIDE 59 — Three Questions (Threat List)

**Purpose:** Replay на трите въпроса от slide 57. Visual threat list. Emotional tension builder.
**Layout:** Custom — 3 stacked threat rows on dark background.
**Speaker alignment:** script → Слайд 59 (ред 65–93).

### Genspark Prompt

```
Create a THREAT LIST slide. Background: Mirage #16232A.

Top centered eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"ТРИ СЦЕНАРИЯ · ИДВАТ"

Below eyebrow, 3 threat rows stacked vertically with generous spacing between each. Each row is a rounded rectangle (subtle border, 1px Haide Orange #FF5B04, no fill — transparent on dark background). Inside each row:

Row 1:
Left side — small orange warning icon (⚠ or similar)
Text, Poppins Medium 28pt, white #FFFFFF:
"GPT-5.5 · 50% от казаното днес — outdated за нощ"

Row 2:
Left side — small orange warning icon
Text, Poppins Medium 28pt, white #FFFFFF:
"Core Update · топ страницата ви пада от AIO"

Row 3:
Left side — small orange warning icon
Text, Poppins Medium 28pt, white #FFFFFF:
"Perplexity Sonar · спира да ви цитира без предупреждение"

Below the 3 rows, separated by whitespace, one punchline line, Poppins SemiBold 24pt, Haide Orange, centered:
"Ден 1 или ден 30? Разликата е Signal Architecture."

CRITICAL: 3 rows maximum. Each row has max 1 line of text. The tension builds visually — row 1, 2, 3 — each a different nightmare scenario. Dark background amplifies urgency.
```

---

## SLIDE 60 — Signal Architecture Reveal

**Purpose:** Framework headline момент. Signal Architecture въведен с analogy.
**Layout:** TITLE CARD / FRAMEWORK REVEAL.
**Speaker alignment:** script → Слайд 60 (ред 97–120).

### Genspark Prompt

```
Create a FRAMEWORK REVEAL slide. Background: Deep Sea Green #075056.

Top centered eyebrow, Poppins SemiBold 20pt, Haide Orange #FF5B04, uppercase:
"HAIDE FRAMEWORK"

Main headline below, centered, Poppins Black 96pt, white #FFFFFF:
"Signal Architecture"

Subtitle below, Poppins Medium 36pt, Wild Sand #E4EEF0, centered:
"Архитектура на сигналите"

Below subtitle, generous whitespace, then a quote-style caption, Poppins Italic 24pt, Haide Orange #FF5B04, centered, max 2 lines:
"Контролна зала на електроцентрала —"
"всички сигнали, едно табло, 24/7"

CRITICAL: This is THE framework reveal moment of Part 3. Same visual gravity as Part 1 pipeline reveals. No additional text, no bullets, no diagrams. The name + Bulgarian translation + analogy = the entire slide.
```

---

## 3.1 Dual Budget Principle (Слайд 61)

---

## SLIDE 61 — Dual Budget Principle

**Purpose:** 15–20% observability budget stat hero + SEO vs GEO budget visual.
**Layout:** STAT HERO with supporting visual.
**Speaker alignment:** script → Слайд 61 (ред 126–152).

### Genspark Prompt

```
Create a STAT HERO slide. Background: Mirage #16232A.

Centered vertically, one enormous stat:
- Number in Poppins Black 220pt, Haide Orange #FF5B04:
  "15–20%"
- Caption directly below, Poppins Medium 32pt, white #FFFFFF:
  "observability budget · от вашия SEO/GEO spend"

Below the main stat, separated by generous whitespace (minimum 15% of slide height), a simple horizontal bar comparison:

Bar 1 (wider, Deep Sea Green #075056 fill): label "SEO execution · 80–85%", Poppins SemiBold 20pt, white inside bar
Bar 2 (narrower, Haide Orange #FF5B04 fill): label "GEO observability · 15–20%", Poppins SemiBold 20pt, white inside bar

Below the bars, one small analogy line, Poppins Italic 18pt, Wild Sand #E4EEF0, centered:
"Не плащаш само за колата. Плащаш и за застраховката."

CRITICAL: The 15–20% stat is the hero. The bar comparison is supporting evidence — NOT a chart, just two colored horizontal rectangles with labels. Analogy line is a whisper, not a shout.
```

---

## 3.2 Monitoring Stack Architecture (Слайдове 62–67)

---

## SLIDE 62 — 5-Layer Stack Overview

**Purpose:** Architecture diagram — all 5 layers visible in one slide. Overview before deep-dive.
**Layout:** DIAGRAM (vertical stack of 5 layers).
**Speaker alignment:** script → Слайд 62 (ред 158–176).

### Genspark Prompt

```
Create a DIAGRAM slide — vertical architecture stack. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 40pt, Mirage #16232A:
"Haide Monitoring Stack"

Below headline, draw a VERTICAL STACK of 5 horizontal layers, each a rounded rectangle. Stack from top to bottom. Each layer has:
- Left side: cadence badge (small orange pill with white text, Poppins Bold 14pt)
- Center: layer number (Poppins Bold 24pt, Deep Sea Green) + layer name (Poppins SemiBold 22pt, Mirage)
- Right side: small arrow (→) pointing to a central column labeled "Signal Table" (or just a vertical line connecting all layers to a right-side icon)

The 5 layers (top = fastest cadence, bottom = slowest):

Layer 1: badge "WEEKLY" · "01 · AI Citation Tracking"
Layer 2: badge "DAILY" · "02 · Server Log Ingestion"
Layer 3: badge "WEEKLY" · "03 · Content Freshness + GSC Mining"
Layer 4: badge "ON DEPLOY" · "04 · Schema + 2MB Regression Guard"
Layer 5: badge "MONTHLY" · "05 · Entity Graph Health"

Right side of the stack: a vertical column or icon labeled "Signal Architecture" in Poppins SemiBold 18pt, Haide Orange, with arrows from each layer flowing into it.

CRITICAL: 5 layers maximum. Each layer is ONE horizontal row with 3 elements (badge + name + arrow). Generous vertical spacing between layers. This is an OVERVIEW — not detail. Detail comes in the next 5 slides. Do NOT add descriptions to the layers.
```

---

## SLIDE 63 — Layer 1: AI Citation Tracking

**Purpose:** First layer card deep-dive. Weekly cadence.
**Layout:** LAYER CARD (new pattern — see specs above).
**Speaker alignment:** script → Слайд 63 (ред 182–206).

### Genspark Prompt

```
Create a LAYER CARD slide (new pattern for Part 3). Background: Wild Sand #E4EEF0.

Top-left: cadence badge — rounded pill (Haide Orange #FF5B04 fill, white text), Poppins Bold 16pt, uppercase:
"WEEKLY"

Hero number, left-aligned, Poppins Black 140pt, Deep Sea Green #075056:
"01"

Layer title directly below number, Poppins Bold 48pt, Mirage #16232A:
"AI Citation Tracking"

Below title, 3 bullet lines stacked vertically with generous spacing. Each bullet has a small grey dot (•). Text in Poppins Medium 22pt, Mirage #16232A:

• "Notion template · 20 queries × 5 платформи"
• "3-месечна manual baseline преди SaaS"
• "Неделя сутрин · кафе · 20 минути"

Bottom of slide: full-width strip, Poppins SemiBold 18pt, Haide Orange #FF5B04, left-aligned with arrow:
"→ вход: Haide Prompt Miner"

CRITICAL: This is the first of 5 identical-structure LAYER CARDS. Audience will see this pattern 5 times — consistency is critical. Max 6 elements: badge + number + title + 3 bullets + strip. Nothing else.
```

---

## SLIDE 64 — Layer 2: Server Log Ingestion

**Purpose:** Second layer card. Daily cadence.
**Layout:** LAYER CARD.
**Speaker alignment:** script → Слайд 64 (ред 212–236).

### Genspark Prompt

```
Create a LAYER CARD slide — same pattern as slide 63. Background: Wild Sand #E4EEF0.

Top-left cadence badge:
"DAILY"

Hero number, Poppins Black 140pt, Deep Sea Green:
"02"

Title, Poppins Bold 48pt, Mirage:
"Server Log Ingestion"

3 bullets, Poppins Medium 22pt, Mirage:

• "n8n cron · Nginx / Apache logs"
• "Alerts: нов crawler · изчезнал crawler · 5xx"
• "Free: GoAccess (open-source)"

Bottom strip:
"→ вход: Haide Bot Radar"

CRITICAL: Identical structure to slide 63. Same font sizes, same spacing, same badge style. Only the content and cadence change.
```

---

## SLIDE 65 — Layer 3: Content Freshness + GSC Mining

**Purpose:** Third layer card. Weekly cadence.
**Layout:** LAYER CARD.
**Speaker alignment:** script → Слайд 65 (ред 242–266).

### Genspark Prompt

```
Create a LAYER CARD slide — same pattern as slides 63–64. Background: Wild Sand #E4EEF0.

Top-left cadence badge:
"WEEKLY"

Hero number, Poppins Black 140pt, Deep Sea Green:
"03"

Title, Poppins Bold 48pt, Mirage:
"Content Freshness + GSC Mining"

3 bullets, Poppins Medium 22pt, Mirage:

• "GSC API · regex auto-applied"
• "Нови 7+ word queries всяка седмица"
• "Корелация: Ahrefs drops + AI citation loss = Core Update"

Bottom strip:
"→ вход: Haide Prompt Miner"

CRITICAL: Same pattern. Third repetition — audience now fully recognizes the LAYER CARD structure.
```

---

## SLIDE 66 — Layer 4: CI/CD Schema + 2MB Guard

**Purpose:** Fourth layer card. On every deploy cadence.
**Layout:** LAYER CARD.
**Speaker alignment:** script → Слайд 66 (ред 272–302).

### Genspark Prompt

```
Create a LAYER CARD slide — same pattern as slides 63–65. Background: Wild Sand #E4EEF0.

Top-left cadence badge:
"ON EVERY DEPLOY"

Hero number, Poppins Black 140pt, Deep Sea Green:
"04"

Title, Poppins Bold 48pt, Mirage:
"Schema + 2MB Regression Guard"

3 bullets, Poppins Medium 22pt, Mirage:

• "GitHub Action · Vercel build step"
• "Блокира deploy при >1.5MB или счупена schema"
• "Open-source gist · линк в PDF-а зад QR"

Bottom strip:
"→ вход: Haide Ceiling"

CRITICAL: Same pattern. The "ON EVERY DEPLOY" badge is longer than DAILY/WEEKLY — ensure badge pill expands to fit text naturally without breaking layout.
```

---

## SLIDE 67 — Layer 5: Entity Graph Health

**Purpose:** Fifth and final layer card. Monthly cadence.
**Layout:** LAYER CARD.
**Speaker alignment:** script → Слайд 67 (ред 308–332).

### Genspark Prompt

```
Create a LAYER CARD slide — same pattern as slides 63–66. Background: Wild Sand #E4EEF0.

Top-left cadence badge:
"MONTHLY"

Hero number, Poppins Black 140pt, Deep Sea Green:
"05"

Title, Poppins Bold 48pt, Mirage:
"Entity Graph Health"

3 bullets, Poppins Medium 22pt, Mirage:

• "Cron проверява всички sameAs links"
• "Wikidata · Wikipedia · LinkedIn · GitHub · Crunchbase"
• "Alert при broken link = AI trust erosion"

Bottom strip:
"→ вход: Haide Ceiling + E-E-A-T bodyguard (Част 1)"

CRITICAL: Final layer card. Same pattern. The bottom strip references both a Part 2 tool AND a Part 1 concept — this closes the 90-minute circle.
```

---

## 3.3 Response Workflow (Слайдове 68–69)

---

## SLIDE 68 — 48-Hour Rule

**Purpose:** Core response principle — stat hero moment.
**Layout:** STAT HERO.
**Speaker alignment:** script → Слайд 68 (ред 338–360).

### Genspark Prompt

```
Create a STAT HERO slide. Background: Mirage #16232A.

Centered vertically, one enormous stat:
- Number in Poppins Black 280pt, Haide Orange #FF5B04:
  "48h"
- Caption directly below, Poppins Medium 36pt, white #FFFFFF:
  "всяка промяна → първи snapshot в рамките на 48 часа"

Below, separated by generous whitespace, one analogy line, Poppins Italic 24pt, Wild Sand #E4EEF0, centered:
"Златен час в спешната помощ"

Below the analogy, a small contrast pair, Poppins Regular 20pt, centered:
Left text in Deep Sea Green: "Ден 1: бърза корекция"
Separator: " · " in grey
Right text in Haide Orange: "Ден 30: три загубени месеца"

CRITICAL: The "48h" dominates everything. Same visual gravity as the "7%" stat hero on slide 10b (Part 1) and the "−42.6%" on slide 5. Nothing else competes. The day 1 vs day 30 contrast is a whisper at the bottom.
```

---

## SLIDE 69 — Response Workflow Cadence

**Purpose:** 4-column cadence grid — daily, weekly, monthly, quarterly.
**Layout:** GRID (4 equal columns).
**Speaker alignment:** script → Слайд 69 (ред 364–398).

### Genspark Prompt

```
Create a GRID slide with 4 equal-width columns. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 44pt, Mirage #16232A:
"Вашият monitoring ритъм"

Below headline, 4 equal columns side by side. Each column has:
- Top: cadence name in a colored pill badge (Poppins Bold 16pt, white text, uppercase)
- Below badge: time commitment in Poppins Black 48pt, Mirage
- Below time: 1-2 short action lines in Poppins Medium 18pt, Mirage

Column 1:
Badge color: Haide Orange #FF5B04 · text: "DAILY"
Time: "5 мин"
Actions:
"Email триаж"
"Layer 2 alerts"

Column 2:
Badge color: Deep Sea Green #075056 · text: "WEEKLY"
Time: "60 мин"
Actions:
"Layer 1 + Layer 3"
"Неделя · кафе"

Column 3:
Badge color: Mirage #16232A · text: "MONTHLY"
Time: "2 часа"
Actions:
"Layer 5 entity check"
"Месечен pattern review"

Column 4:
Badge color: Haide Orange #FF5B04 · text: "QUARTERLY"
Time: "4 часа"
Actions:
"Playbook refresh"
"Екипен retrospective"

Bottom of slide, centered, Poppins SemiBold 22pt, Deep Sea Green #075056:
"< 20 часа / тримесечие · за цялата AI видимост"

CRITICAL: 4 columns max. Time commitment numbers are the visual anchors (5 мин, 60 мин, 2 часа, 4 часа). Actions are max 2 lines each. The "< 20 часа" bottom line is the key takeaway. Do NOT add more detail — Adrian carries it verbally.
```

---

## 3.4 Information Diet (Слайд 70)

---

## SLIDE 70 — Information Diet

**Purpose:** 7 must-read authors + 3 official sources + what to ignore.
**Layout:** SPLIT SCREEN (left: must-read; right: ignore).
**Speaker alignment:** script → Слайд 70 (ред 404–444).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 60/40 vertical split. Background: Wild Sand #E4EEF0.

Top centered headline spanning full width, Poppins Bold 40pt, Mirage #16232A:
"Information Diet · 2 часа / седмица"

LEFT HALF (60% width) — "Задължителни":
Small eyebrow, Poppins SemiBold 16pt, Deep Sea Green #075056, uppercase:
"ЧЕТЕТЕ"

Below, a compact list of 7 author names, each on its own line, Poppins Medium 20pt, Mirage #16232A:
"Kevin Indig · Growth Memo"
"Chris Long"
"Lily Ray"
"ziptie.dev"
"Seer Interactive"
"iPullRank / Michael King"
"Dan Petrovic"

Below the author list, small separator line, then 3 official sources in Poppins Regular 18pt, Deep Sea Green:
"+ Google Search Central Blog"
"+ OpenAI release notes"
"+ Anthropic / Perplexity changelogs"

Below sources, small tool line, Poppins Italic 16pt, grey:
"Aggregator: Feedly Pro или Inoreader (RSS)"

RIGHT HALF (40% width, background Mirage #16232A):
Small eyebrow, Poppins SemiBold 16pt, Haide Orange #FF5B04, uppercase:
"ИГНОРИРАЙТЕ"

Below, 4 items stacked vertically, each with a red/orange "✕" prefix, Poppins Medium 20pt, Wild Sand #E4EEF0:
"✕ LinkedIn 'AI thought leaders'"
"✕ SaaS vendor content marketing"
"✕ Anonymous Twitter акаунти"
"✕ Повечето SEO конференции"

CRITICAL: Left side has 7 + 3 + 1 = 11 text lines — this is intentionally denser than other slides. BUT each line is short (max 5 words). The "ignore" side with ✕ marks is visually contrasting (dark bg vs light bg). Do NOT add descriptions to the names — the names are the content.
```

---

## 3.5 CTA + Close (Слайдове 71–72)

---

## SLIDE 71 — Growth Gap Review CTA

**Purpose:** Soft CTA — free 30-min Growth Gap Review for all attendees. Enlarged QR.
**Layout:** SPLIT SCREEN (left: offer details; right: enlarged QR).
**Speaker alignment:** script → Слайд 71 (ред 450–472).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 60/40 vertical split.

LEFT HALF (60% width, background Deep Sea Green #075056):
Small eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"ЗА ВСИЧКИ В ТАЗИ ЗАЛА"

Main headline, Poppins Bold 56pt, white #FFFFFF:
"Growth Gap Review"

Below headline, Poppins Medium 28pt, Wild Sand #E4EEF0:
"30 минути · безплатно"

Below that, 3 short lines with small orange checkmarks, Poppins Medium 22pt, Wild Sand:
"✓ Без sales pitch"
"✓ Pure data walkthrough"
"✓ Трите най-големи AI visibility пролуки"

Below the 3 lines, generous whitespace, then one small line, Poppins Italic 18pt, Wild Sand:
"Сканирайте · изберете час · попълнете 2 полета"

RIGHT HALF (40% width, background Mirage #16232A):
Large QR code centered, roughly 65% of the right section's height. White QR on Mirage for high contrast. Encodes: haide.digital/masterclass-2026

Below QR, Poppins Medium 24pt, Haide Orange #FF5B04, centered:
"haide.digital/masterclass-2026"

Below URL, Poppins Regular 16pt, Wild Sand, centered:
"Календарът е отворен · 4 седмици"

CRITICAL: This is the ONLY sales-adjacent slide in the entire 90-minute deck. It must feel generous, not salesy. The "без sales pitch" and "pure data walkthrough" lines are the trust builders. Enlarged QR is the third major QR moment (after Part 1 slide 2 and Part 2 slide 28/56).
```

---

## SLIDE 72 — Final Line + Thank You

**Purpose:** Closing slide. Финалната линия на целия мастърклас. Emotional moment.
**Layout:** TRANSITION / CLOSING CARD.
**Speaker alignment:** script → Слайд 72 (ред 478–504).

### Genspark Prompt

```
Create a CLOSING CARD slide. Full-bleed background: Mirage #16232A.

Centered vertically.

Main sentence, Poppins Medium 64pt, white #FFFFFF, centered, two lines:
"Get Found. Stay Visible."
"Но този път — everywhere."

The word "everywhere" should be in Haide Orange #FF5B04 for emphasis (the only colored word in the sentence).

Below the main sentence, generous whitespace (minimum 20% of slide height).

Small metadata block at the bottom, Poppins Regular 20pt, Wild Sand #E4EEF0, centered:
"Адриан Николов  ·  Haide Digital  ·  23 април 2026"

Master QR corner in bottom-right (last appearance — audience's final chance to scan).

CRITICAL: This is the LAST slide of a 90-minute masterclass. Maximum emotional weight. The "everywhere" in orange is the ONLY visual accent. Everything else is white on near-black. Same minimalism as the opening title card (slide 1) — the deck ends where it began. Pure. Clean. Confident.
```

---

# SPLIT DECISIONS LOG (Part 3)

Няма split решения за Part 3. 15 слайда е достатъчно за 30-минутен script-heavy сегмент без live demos. Всеки слайд има единствена core idea.

**Note:** Slide 70 (Information Diet) е най-dense слайдът в Part 3 (11 text lines на лявата половина). Ако при генериране се окаже overcrowded, split на 70a (must-read sources) + 70b (what to ignore). Но опитваме първо като един слайд — split screen layout-а разпределя тежестта.

---

# VISUAL PATTERNS FINAL SUMMARY (целия deck)

| Pattern | Part 1 | Part 2 | Part 3 | Total |
|---|---|---|---|---|
| TITLE CARD | 1 (slide 1) | — | — | 1 |
| SECTION DIVIDER | 4 (7, 11, 15, 17a) | 1 (27) | 1 (58) | 6 |
| BLOCK SECTION DIVIDER | — | 5 (29, 34, 37, 42, 53) | — | 5 |
| STAT HERO | 3 (5, 10b, 13a) | 1 (39) | 2 (61, 68) | 6 |
| SPLIT SCREEN | 5 (2, 4, 10a, 17b, 23) | 6 (28, 30, 35, 36, 43, 45, 54, 55) | 3 (70, 71, 54-55 n/a) | ~14 |
| GRID | 3 (6, 9, 22) | 4 (31, 38, 44, 52) | 1 (69) | 8 |
| DIAGRAM | 5 (8, 12, 16, 17a, 20) | — | 1 (62) | 6 |
| TRANSITION | 2 (3, 23) | 1 (57) | 1 (72) | 4 |
| TOOL ENTRY | — | 5 (32, 40, 46, 48, 50) | — | 5 |
| TOOL EXIT | — | 5 (33, 41, 47, 49, 51) | — | 5 |
| LAYER CARD | — | — | 5 (63, 64, 65, 66, 67) | 5 |
| FRAMEWORK REVEAL | — | — | 1 (60) | 1 |
| THREAT LIST | — | — | 1 (59) | 1 |
| CLOSING CARD | — | — | 1 (72) | 1 |

**Total unique patterns: 14.** Визуално разнообразен deck с consistent brand treatment.

---

# FINAL DECK SUMMARY

| Part | Slides | Duration | Core theme |
|---|---|---|---|
| Part 1 | 1–26 (26 slides) | 33 min | How AI models choose who to cite |
| Part 2 | 27–57 (31 slides) | 30 min | Implementation checklist + 5 live tools |
| Part 3 | 58–72 (15 slides) | 30 min | Monitoring stack + survival workflow |
| **TOTAL** | **72 slides** | **~93 min** | Trim to 90 min at rehearsal |

**Average pace: ~1:17 min/slide.** Professional keynote pace. Part 1 slower (1:16), Part 2 faster (0:58 — demos eat time off-slide), Part 3 moderate (2:00 — script-heavy, no demos).

---

# VERIFICATION CHECKLIST ПРЕДИ ГЕНЕРИРАНЕ

- [ ] Global Style Brief от Part 1 е още активен в deck settings.
- [ ] Тези 15 слайда се добавят към **същия** deck (slides 58–72).
- [ ] Anti-crowding reminder присъства в всяка prompt.
- [ ] Само 4 цвята (#FF5B04, #075056, #E4EEF0, #16232A). Единствено изключение: "everywhere" в orange на slide 72.
- [ ] Master QR corner продължава на всеки слайд.
- [ ] Enlarged QR: slide 71 (Growth Gap Review CTA) — third major QR moment.
- [ ] 5 LAYER CARD slides (63–67) имат identical structure.
- [ ] Cadence badges: WEEKLY (63, 65), DAILY (64), ON EVERY DEPLOY (66), MONTHLY (67).
- [ ] Red-thread strips: Prompt Miner (63, 65), Bot Radar (64), Ceiling (66, 67), E-E-A-T bodyguard (67).
- [ ] Signal Architecture reveal (slide 60) has EN name + БГ translation + analogy.
- [ ] Slide 72 final line: "Get Found. Stay Visible. Но този път — everywhere." with "everywhere" in orange.
- [ ] Information Diet (slide 70): 7 authors + 3 official sources + 4 ignore items.
- [ ] Growth Gap Review (slide 71): "без sales pitch", "pure data walkthrough", enlarged QR.

---

# DECK COMPLETE 🎯

**72 слайда · 90 минути · 3 части · готови за генериране в Genspark AI Slides.**

Следващи стъпки:
1. Генерирай slides 58–72 в Genspark (add to existing deck).
2. Visual review на целия 72-slide deck.
3. Screenshot capture session (SS-01 до SS-16) — overdue.
4. Export за rehearsal (10 април 2026 deadline).
5. Video recording + final polish преди 19 април.
