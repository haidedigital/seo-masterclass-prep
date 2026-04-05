# Genspark Slide Prompts — Част 1 (Въведение + AI модели)

> **Deck:** Техническо SEO в AI ерата — Адриан Николов, Haide Digital
> **Event:** Enterprise Magazine × EURODEA SEO Masterclass, София, 23 април 2026
> **Source script:** [script-part1-intro-and-ai-models.md](script-part1-intro-and-ai-models.md)
> **Slide count:** 26 (оригинално 23 в скрипта, 3 split-а за anti-crowding — виж [Split decisions log](#split-decisions-log) в края)
> **Total runtime:** ~33 минути
> **Language strategy:** Prompt инструкциите към Genspark са на EN (по-добри резултати при генериране). Цялото slide content (headlines, body, labels) е на **БЪЛГАРСКИ**, подадено в кавички `" "` за да не се превежда.

---

## ВАЖНО — КОНТЕКСТ ЗА GENSPARK

**Тази генерация е САМО Част 1 от 3-частна презентация.** Цялата мастърклас презентация ще бъде 90 минути разделени на три части:

- **Част 1 (ТОВА ДОКУМЕНТ) — Въведение + Как работят AI моделите** · 33 мин · 26 слайда · слайдове 1–26
- **Част 2 (СЛЕДВА) — Walk-through на 60-точков чеклист + 5 live tool demo-та** · ~30 мин · ~25 слайда · слайдове 27–~51
- **Част 3 (СЛЕДВА) — Monitoring stack + workflow за volatile AI среда** · ~30 мин · ~15 слайда · слайдове ~52–~66

**Общо финално deck:** ~66 слайда за 90 мин.

**Важно за continuity:** Global Style Brief, цветове, типография, anti-crowding правила, QR master element, speaker — **всички остават идентични през трите части**. Genspark deck-а трябва да се създава като **един проект**, в който се добавят Part 2 и Part 3 след като Part 1 е approved визуално. Не започвай нов deck за всяка част — добавяй слайдове към същия deck за да запазиш визуалната консистентност.

След като Part 1 приключи и е одобрена, Adrian ще генерира `genspark-prompts-part2.md` и `genspark-prompts-part3.md` по същия формат.

---

## GLOBAL STYLE BRIEF — PASTE THIS ONCE AT TOP OF GENSPARK DECK

```
BRAND: Haide Digital (haide.digital) — an Organic Growth Engineering company.
Tagline: "Get Found. Stay Visible."

CONTEXT: This is Part 1 of a 3-part, 90-minute masterclass presentation. Parts 2 and 3 will be added to this same deck later. Visual consistency across all 3 parts is critical — the style rules below apply to every slide regardless of which part.

VISUAL LANGUAGE — NON-NEGOTIABLE:
- Primary colors ONLY: Haide Orange #FF5B04, Deep Sea Green #075056, Wild Sand #E4EEF0, Mirage #16232A. No other colors.
- Typography: Poppins for all headlines and numbers. Noto Sans for all body text. Bold weights for emphasis.
- Aesthetic: engineering-first, bold, confident. NOT corporate stock-photo style. NOT playful/cartoonish.
- Think: Stripe docs meets Apple keynote meets engineering whitepaper.

CRITICAL ANTI-CROWDING RULE — REPEAT ON EVERY SLIDE:
- MAXIMUM ONE CORE IDEA PER SLIDE. If a slide feels crowded, STOP and tell me — I'll split it.
- Generous whitespace. Minimum 40% of the slide should be empty space.
- Headlines: max 8 words. Body text: max 20 words per slide.
- If there are more than 4 visual elements, it's too many.
- Font sizes: headlines 60-80pt, body 24-32pt, captions 16-20pt. Must be readable from 3 meters away.
- NO dense bullet lists. NO paragraphs. NO walls of text. NO multi-column stats that force the eye to jump.
- When in doubt, REMOVE something.

LANGUAGE RULE:
- All on-slide text is in BULGARIAN (Cyrillic). I will provide it in quotes — do not translate, do not paraphrase.
- All my instructions to you are in English. Only the content inside " " is slide text.

LAYOUT VOCABULARY (choose one per slide):
- TITLE CARD: centered headline, small subtitle, bold background color.
- STAT HERO: one giant number (150pt+), one short caption below.
- SPLIT SCREEN: two halves, one comparison per side.
- DIAGRAM: pipeline or flow, 3-7 nodes max, arrows, generous spacing.
- QUOTE: one short phrase centered, attribution below.
- TRANSITION: black background, single white sentence centered.
- GRID: 2x2 or 3-column for listing items, icon + label + one-line caption.

QR CODE MASTER ELEMENT:
- From slide 3 onwards: small QR code (80x80px) fixed in bottom-right corner of every slide. Caption optional. Use the QR for URL haide.digital/masterclass-2026.
- Slide 2 and slide 26 have special QR treatments (described per slide).
```

---

## HOW TO USE THIS FILE

1. Open Genspark AI Slides.
2. Paste the **GLOBAL STYLE BRIEF** above as your deck-level instructions / system prompt.
3. For each slide below, copy the **Genspark Prompt** block and paste it as the per-slide prompt.
4. Generate, review, iterate. If Genspark overcrowds → tell it "too much on this slide, remove [X], add whitespace". The anti-crowding rule is the most important thing.
5. For mermaid-style pipeline slides (8, 12, 16, 17a, 20), I describe the diagram in plain English below — Genspark will draw it natively. Do NOT paste mermaid source.
6. Speaker alignment line tells you which slide in the script corresponds to which Genspark slide.

---

# ВЪВЕДЕНИЕ (Слайдове 1–3)

---

## SLIDE 1 — Title Card

**Purpose:** Откриване. Кой съм, коя е компанията, каква е темата. 1 слайд, 1:30 говорене.
**Layout:** TITLE CARD.
**Speaker alignment:** script → Слайд 1 (ред 88–106).

### Genspark Prompt

```
Create a TITLE CARD slide. Full-bleed background color: Deep Sea Green #075056.

Centered layout, vertically balanced, huge amounts of whitespace.

Main headline, Poppins Bold, 80pt, white #FFFFFF, centered:
"Техническо SEO в AI ерата"

Subheadline below main headline, Poppins Regular, 32pt, Haide Orange #FF5B04, centered, max one line:
"Как AI моделите избират кого да цитират"

Small metadata block at the bottom of the slide, Noto Sans 20pt, Wild Sand #E4EEF0, centered:
"Адриан Николов  ·  Haide Digital  ·  23 април 2026"

No logos, no images, no decorative elements. Clean, engineering-first, confident.

CRITICAL: This slide must feel spacious and premium. Minimum 50% empty space. No clutter.
```

---

## SLIDE 2 — "Какво ще получите днес" (Contract + QR Reveal)

**Purpose:** Контракт със залата — 4 осезаеми deliverables. Първо появяване на QR (пълен екран дясна половина).
**Layout:** SPLIT SCREEN (left: 4 deliverables as grid; right: large QR code).
**Speaker alignment:** script → Слайд 2 (ред 110–132).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical split.

LEFT HALF (background Wild Sand #E4EEF0):
Small eyebrow label at top, Poppins Bold 18pt, Haide Orange #FF5B04, uppercase:
"КАКВО СИ ОТИВАТЕ С ВКЪЩИ"

Below it, a 2x2 grid of 4 deliverables. Each cell has:
- A simple line icon (Deep Sea Green #075056, 48px)
- A one-line label in Poppins SemiBold 26pt, Mirage #16232A
- NO descriptions, NO paragraphs

The 4 labels (use exactly these words):
1. Icon: document/PDF → "60-точков чеклист · PDF"
2. Icon: wrench/tools → "5 безплатни инструмента"
3. Icon: radar/monitor → "Monitoring blueprint"
4. Icon: calendar → "30-мин Growth Gap Review"

Generous spacing between cells. Each cell must breathe.

RIGHT HALF (background Deep Sea Green #075056):
One large QR code, centered, roughly 60% of the right half's height. White QR on Deep Sea Green background for contrast. QR encodes the URL: haide.digital/masterclass-2026

Below the QR, Poppins Medium 24pt, Haide Orange #FF5B04, centered:
"haide.digital/masterclass-2026"

CRITICAL: This is the ONE slide where the QR is huge. No other text on the right half. Silent dwell moment for the audience to scan.
```

---

## SLIDE 3 — Transition

**Purpose:** Bridge от въведение към Част 1. Психологически „защо първо теория, после чеклист".
**Layout:** TRANSITION (black background, single sentence).
**Speaker alignment:** script → Слайд 3 (ред 136–147).

### Genspark Prompt

```
Create a TRANSITION slide. Full-bleed background: Mirage #16232A (near-black).

One single sentence, centered, Poppins Medium 56pt, white #FFFFFF:
"Преди чеклиста — как наистина работят тези системи."

Nothing else on the slide. No decorative elements. No subtitle. Pure silence.

From this slide onwards, add a small 80x80px QR code in the bottom-right corner (white on transparent), encoding haide.digital/masterclass-2026. This small QR will remain on EVERY slide from here until slide 25.

CRITICAL: Maximum simplicity. The sentence must feel like a beat of silence.
```

---

# ЧАСТ 1 — КАК РАБОТЯТ AI СИСТЕМИТЕ (Слайдове 4–26)

## 1.1 Cold Open (Слайдове 4–6)

---

## SLIDE 4 — "Правилата за видимост се раздвоиха"

**Purpose:** Google призна (31 март 2026): 2MB HTML limit + stateless rendering. AI моделите мълчат. Разрез.
**Layout:** SPLIT SCREEN (left: Google honest; right: AI models silent).
**Speaker alignment:** script → Слайд 4 (ред 156–178).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical split, background Wild Sand #E4EEF0.

Top banner headline spanning the full width, Poppins Bold 48pt, Mirage #16232A, centered:
"Правилата за видимост се раздвоиха"

LEFT HALF — "Google е честен":
- Small eyebrow Poppins SemiBold 18pt, Deep Sea Green #075056, uppercase:
  "GOOGLE · 31 МАРТ 2026"
- Two short lines, Noto Sans Medium 28pt, Mirage #16232A, stacked with space between:
  "2MB HTML лимит"
  "Stateless rendering"
- Small screenshot placeholder box below, labeled: [SCREENSHOT: Google Search Central blog post 31.03.2026 — SS-01]

RIGHT HALF — "AI моделите мълчат":
- Small eyebrow Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
  "CHATGPT · CLAUDE · PERPLEXITY · GEMINI"
- One line, Poppins Bold 32pt, Mirage #16232A:
  "?"
- Below, Noto Sans Regular 22pt, dark grey:
  "Без публикувани правила"

CRITICAL: The contrast between the two halves is the entire message. Do NOT add extra bullet points, charts, or decoration. Whitespace carries the tension.
```

---

## SLIDE 5 — LLM Referral Drop + CTR Paradox

**Purpose:** Парадоксът — LLM трафик надолу 42.6%, но cited брандове имат +35% CTR в Google. AI = доверие, не трафик.
**Layout:** STAT HERO (one huge stat + small counter-stat).
**Speaker alignment:** script → Слайд 5 (ред 180–201).

### Genspark Prompt

```
Create a STAT HERO slide. Background: Mirage #16232A (near-black).

Centered vertically, one enormous stat:
- Number in Poppins Black, 220pt, Haide Orange #FF5B04:
  "−42.6%"
- Caption directly below, Poppins Medium 32pt, Wild Sand #E4EEF0:
  "LLM referral traffic · юли 2025 → днес"
- Source line below caption, Noto Sans Regular 18pt, grey #888:
  "Kevin Indig, Growth Memo"

Then, separated by generous whitespace (at least 20% of slide height gap), a much smaller secondary stat block at the bottom of the slide, Poppins SemiBold 24pt, white #FFFFFF, centered:
"Но цитираните брандове: +35% organic CTR · +91% paid CTR"

[SCREENSHOT placeholder: SS-02 Kevin Indig chart — optional inline small visual on the right side if it fits without crowding]

CRITICAL: The big number is the hero. Everything else is in service of it. Do NOT balance the layout into two halves — the −42.6% must dominate. The +35% line is a whisper, not a shout.
```

---

## SLIDE 6 — Обещание + Teaser (4 AI модела)

**Purpose:** Обещание за следващите 25 мин — pipeline на 4 модела. Тийзър със stats.
**Layout:** GRID (4 quadrants, one per model).
**Speaker alignment:** script → Слайд 6 (ред 205–219).

### Genspark Prompt

```
Create a GRID slide, 2x2 layout, background Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 44pt, Mirage #16232A:
"Следващите 25 минути"

Below the headline, a 2x2 grid of 4 cells. Each cell has:
- A circle or rounded square with the brand logo area (just a simple colored block; do not attempt to fetch real logos)
- Brand name in Poppins Bold 28pt
- ONE stat in Poppins Black 40pt, Haide Orange #FF5B04
- ONE label in Noto Sans Regular 18pt, grey

The 4 cells:
1. "ChatGPT" · "31%" · "trigger rate"
2. "Google AI Mode" · "70%+" · "от всички searches"
3. "Perplexity" · "8–12" · "citations / отговор"
4. "Claude" · "45%" · "enterprise AI spend"

Generous padding inside each cell. Cells separated by clear gaps — not touching.

CRITICAL: 4 cells maximum. Each cell has only 3 text elements. No extra bullets. No descriptions.
```

---

## 1.2 ChatGPT Pipeline (Слайдове 7–11)

---

## SLIDE 7 — ChatGPT Pipeline (Title)

**Purpose:** Секционна бариера — въвеждаме ChatGPT. Кратко dwell.
**Layout:** TITLE CARD (section divider).
**Speaker alignment:** script → Слайд 7 (ред 227–234).

### Genspark Prompt

```
Create a SECTION DIVIDER slide. Background: Deep Sea Green #075056.

Centered vertically.

Small eyebrow label, Poppins SemiBold 20pt, Haide Orange #FF5B04, uppercase, centered:
"ЧАСТ 1 · PIPELINE #1"

Below it, main headline, Poppins Bold 90pt, white #FFFFFF, centered:
"ChatGPT"

Below headline, one subtitle line, Poppins Regular 28pt, Wild Sand #E4EEF0:
"Офис с петима служители"

CRITICAL: Pure minimalism. Section dividers are visual breathing room, not content slides. Keep it bare.
```

---

## SLIDE 8 — ChatGPT 5-Step Pipeline Diagram

**Purpose:** Визуалният pipeline. Потребителят вижда всички 5 стъпки едновременно (или build-reveal в Keynote после).
**Layout:** DIAGRAM (horizontal pipeline, 6 nodes, arrows).
**Speaker alignment:** script → Слайд 8 (ред 237–293).

### Genspark Prompt

```
Create a DIAGRAM slide — horizontal pipeline flow. Background: Wild Sand #E4EEF0.

Small headline at top, Poppins Bold 36pt, Mirage #16232A, centered:
"ChatGPT — 5 стъпки"

Below the headline, draw a HORIZONTAL FLOWCHART with 6 nodes connected by arrows pointing left-to-right. Use rounded rectangles. Generous horizontal spacing between nodes. The flow is:

NODE 1 (Wild Sand bg, dark border): "Заявка"
    → arrow to →
NODE 2 (Haide Orange #FF5B04 bg, white text): "Класификатор"
    → arrow SPLITS into TWO branches:

    UPPER BRANCH (thin arrow, grey): labeled "69%" → leads to a grey muted node: "Parametric · без уеб"

    LOWER BRANCH (bold arrow, orange): labeled "31%" → NODE 3 (Deep Sea Green #075056 bg, white text): "Fan-out · 2.17 → 18.4 под-заявки"
    → arrow to →
NODE 4 (Deep Sea Green bg, white text): "Retrieval · Bing"
    → arrow to →
NODE 5 (Deep Sea Green bg, white text): "Re-ranking"
    → arrow to →
NODE 6 (Haide Orange bg, white text): "Citation · 2–4 източника"

Node text: Poppins SemiBold 20pt. Keep node labels SHORT (max 5 words each). Arrows clearly directional.

CRITICAL: 6 nodes is the maximum. The diagram must be READABLE from the back of the room. If it looks cramped, make the slide landscape and reduce text size of labels, but NEVER reduce padding between nodes. The split into 69% / 31% is the most important visual element — make the 31% arrow visually bolder than the 69% one.
```

---

## SLIDE 9 — ChatGPT Fan-Out Numbers

**Purpose:** 4 ключови числа като memory anchors. Чист grid.
**Layout:** GRID (2x2 stat grid).
**Speaker alignment:** script → Слайд 9 (ред 296–311).

### Genspark Prompt

```
Create a GRID STAT slide, 2x2 layout. Background: Wild Sand #E4EEF0.

Headline at top, Poppins Bold 40pt, Mirage #16232A, centered:
"Четири числа за ChatGPT"

2x2 grid of stat cells. Each cell contains:
- ONE big number in Poppins Black 110pt, Haide Orange #FF5B04, centered
- ONE short label below in Noto Sans Medium 20pt, Mirage #16232A, centered
- NOTHING ELSE

The 4 cells (top-left, top-right, bottom-left, bottom-right):

1. "31%" · "търси в уеб"
2. "2.17 → 18.4" · "fan-out depth"
3. "5.5" · "думи средна дължина"
4. "2–4" · "citations / отговор"

Very generous padding inside cells. Cells clearly separated. Each cell is its own moment.

CRITICAL: 4 stats maximum, one per cell. No sources on this slide (sources were on slide 8 title). No decoration. The numbers do the work.
```

---

## SLIDE 10a — GPT-5.3 vs 5.4 (Split Screen)

**Purpose:** A/B сравнение на стария и новия модел. Visual polarization.
**Layout:** SPLIT SCREEN (50/50, A vs B).
**Speaker alignment:** script → Слайд 10 (ред 314–343), първа половина.
**Split note:** Оригинален слайд 10 е разделен на 10a + 10b за да не се претъпка. 10a = A/B comparison, 10b = killer stat (7% overlap + 75% not in top 100).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, exact 50/50 vertical split.

Top centered headline spanning full width, Poppins Bold 44pt, Mirage #16232A:
"Един въпрос. Два модела. Два различни интернета."

LEFT HALF — background Wild Sand #E4EEF0:
- Eyebrow: Poppins SemiBold 20pt, dark grey, uppercase:
  "ИВАН · БЕЗПЛАТЕН"
- Model label: Poppins Bold 36pt, Mirage:
  "GPT-5.3"
- Big stat: Poppins Black 120pt, Deep Sea Green #075056, centered:
  "92%"
- Caption: Noto Sans Medium 22pt:
  "brand website citations"

RIGHT HALF — background Mirage #16232A:
- Eyebrow: Poppins SemiBold 20pt, Haide Orange, uppercase:
  "МАРИЯ · PRO $20/МЕС"
- Model label: Poppins Bold 36pt, white:
  "GPT-5.4"
- Big stat: Poppins Black 120pt, Haide Orange #FF5B04, centered:
  "56%"
- Caption: Noto Sans Medium 22pt, white:
  "brand · 44% third-party"

CRITICAL: Pure binary comparison. Both halves have IDENTICAL structure so the eye compares instantly. Do NOT add Reddit/YouTube/forum bullets on the right half — Adrian says it verbally. Less is more.
```

---

## SLIDE 10b — The 7% Killer Stat

**Purpose:** Punchline. Седем процента overlap. 75% не са в топ 100.
**Layout:** STAT HERO (two stats, second smaller).
**Speaker alignment:** script → Слайд 10 (ред 337–343), втора половина.
**Split note:** Новодобавен слайд (оригинално беше част от слайд 10).

### Genspark Prompt

```
Create a STAT HERO slide. Background: Mirage #16232A.

Centered vertically, one enormous stat:
- Number in Poppins Black, 280pt, Haide Orange #FF5B04:
  "7%"
- Caption directly below, Poppins Medium 36pt, white #FFFFFF:
  "overlap между GPT-5.3 и GPT-5.4"

Below the main stat, separated by large whitespace (minimum 15% of slide height), a second stat in smaller size:
- Number: Poppins Bold 80pt, Wild Sand #E4EEF0:
  "75%"
- Caption: Poppins Regular 24pt, Wild Sand #E4EEF0:
  "от GPT-5.4 citations НЕ са в Google top 100"

Source line at very bottom, Noto Sans Regular 16pt, grey #777, right-aligned:
"Writesonic · Samanyou Garg · 9 март 2026"

[SCREENSHOT placeholder: SS-07 Writesonic study — optional as small thumbnail in a corner if it doesn't crowd]

CRITICAL: The 7% is the shock moment. It must feel huge and isolated. The 75% is supporting evidence, deliberately smaller. Nothing else on this slide.
```

---

## 1.3 Google AI Mode Pipeline (Слайдове 11–15)

---

## SLIDE 11 — Google AI Mode (Title)

**Purpose:** Секционна бариера — преход към Google AIO.
**Layout:** TITLE CARD (section divider).
**Speaker alignment:** script → Слайд 11 (ред 355–365).

### Genspark Prompt

```
Create a SECTION DIVIDER slide. Background: Deep Sea Green #075056.

Centered vertically.

Eyebrow, Poppins SemiBold 20pt, Haide Orange, uppercase:
"ЧАСТ 1 · PIPELINE #2"

Main headline, Poppins Bold 80pt, white, centered:
"Google AI Mode"

Subtitle, Poppins Regular 28pt, Wild Sand:
"Военен щаб с 10 агенти"

One stat line at bottom, Poppins SemiBold 24pt, Haide Orange:
"70%+ от всички searches · януари 2026"

[SCREENSHOT placeholder: SS-04 Google AIO example — optional small inline screenshot if space permits]

CRITICAL: Section divider, not content slide. Breathing room.
```

---

## SLIDE 12 — Gemini 3 AIO Fan-Out Pipeline Diagram

**Purpose:** Pipeline визуализация за Google AIO.
**Layout:** DIAGRAM (horizontal pipeline, 6 nodes with E-E-A-T gate split).
**Speaker alignment:** script → Слайд 12 (ред 367–444).

### Genspark Prompt

```
Create a DIAGRAM slide — horizontal pipeline. Background: Wild Sand #E4EEF0.

Headline top, Poppins Bold 36pt, Mirage, centered:
"Google AI Mode — Gemini 3 pipeline"

HORIZONTAL FLOWCHART, left-to-right, 6 nodes + a split at the E-E-A-T gate:

NODE 1 (Wild Sand bg): "Заявка"
    →
NODE 2 (Haide Orange bg, white): "Fan-out · 9.06 avg / 10.7 Gemini 3"
    → arrow continues, but add a SMALL annotation bubble above node 2 in red/orange:
    "95% = 0 search volume"
    →
NODE 3 (Deep Sea Green bg, white): "Retrieval · Google index"
    →
NODE 4 (Haide Orange bg, white, rendered as a DIAMOND/decision shape): "E-E-A-T gate · 96% binary"
    → splits into:

    UPPER BRANCH (red, thin): "Fail" → grey muted node: "Филтрирано"
    LOWER BRANCH (green, bold): "Pass" → NODE 5 (Deep Sea Green bg, white): "Citation · 38% от топ 10 · 80% НЕ в топ 100"

Node text Poppins SemiBold 18pt, max 6 words per node.

CRITICAL: 6 nodes + 1 drop-out node = 7 elements maximum. The E-E-A-T gate is the visual climax — make the diamond shape clearly larger and bolder than the other nodes. The 95% annotation above the fan-out must not crowd the arrow; position it with margin.
```

---

## SLIDE 13a — 95% Zero-Volume Queries

**Purpose:** Един практичен извод: 95% от fan-out въпросите нямат search volume → GSC 7+ word regex.
**Layout:** STAT HERO (one stat + practical takeaway).
**Speaker alignment:** script → Слайд 13 (ред 447–457), първа половина.
**Split note:** Оригинален слайд 13 е разделен на 13a + 13b.

### Genspark Prompt

```
Create a STAT HERO slide. Background: Wild Sand #E4EEF0.

Centered.

Massive number, Poppins Black 280pt, Haide Orange #FF5B04:
"95%"

Caption directly below, Poppins Medium 32pt, Mirage:
"от AI fan-out въпросите имат 0 search volume"

Below the caption, separated by generous whitespace, a small practical takeaway box (rounded rectangle, Deep Sea Green #075056 bg, white text), Poppins SemiBold 22pt, centered:
"GSC → Queries → filter 7+ думи · Haide Prompt Miner (Част 2)"

CRITICAL: The 95% is the hero. The takeaway box is a small actionable footnote. No charts, no sources. Nothing else.
```

---

## SLIDE 13b — E-E-A-T Gate (Бодигард чеклист)

**Purpose:** E-E-A-T като binary bouncer. 4-точков чеклист с analogy.
**Layout:** GRID (2x2 checklist) with metaphor header.
**Speaker alignment:** script → Слайд 13 (ред 459–466), втора половина.
**Split note:** Новодобавен слайд.

### Genspark Prompt

```
Create a GRID slide. Background: Mirage #16232A.

Headline top, Poppins Bold 48pt, white, centered:
"E-E-A-T gate = бодигард на входа"

Subtitle, Poppins Regular 24pt, Haide Orange #FF5B04, centered:
"96% binary filter · минаваш или не минаваш"

Below, a 2x2 grid of 4 cells. Each cell is a rounded rectangle with Wild Sand #E4EEF0 background, Mirage text. Each cell has:
- A simple line icon (Deep Sea Green, 40px)
- A one-line label in Poppins SemiBold 26pt

The 4 cells:
1. Icon: person → "Истински автор · не 'admin'"
2. Icon: calendar → "Ясна дата · published + updated"
3. Icon: code brackets → "Organization schema"
4. Icon: link → "Цитирани източници"

Generous padding. Cells separated.

Bottom right corner: tiny source line, Noto Sans 14pt, grey:
"ziptie.dev"

CRITICAL: 4 points, 4 cells, 1 icon + 1 line each. The bouncer metaphor is in the headline, not drawn literally. Do NOT add illustrations of a bouncer.
```

---

## SLIDE 14 — Lily Ray Корелация

**Purpose:** Google Core Updates удрят 3 повърхности едновременно. Сграда с 3 входа.
**Layout:** STAT HERO (3 parallel numbers) + chart placeholder.
**Speaker alignment:** script → Слайд 14 (ред 470–497).

### Genspark Prompt

```
Create a STAT + CHART slide. Background: Wild Sand #E4EEF0.

Headline top, Poppins Bold 44pt, Mirage, centered:
"Един update. Три повърхности."

Below the headline, three numbers arranged HORIZONTALLY in a row, equal spacing, each with the same visual treatment:

COLUMN 1:
- Number: Poppins Black 110pt, Mirage #16232A:
  "−26.7%"
- Label: Noto Sans Medium 22pt, grey:
  "Organic"

COLUMN 2:
- Number: Poppins Black 110pt, Deep Sea Green #075056:
  "−22.5%"
- Label: Noto Sans Medium 22pt, grey:
  "AIO citations"

COLUMN 3:
- Number: Poppins Black 110pt, Haide Orange #FF5B04:
  "−23.8%"
- Label: Noto Sans Medium 22pt, grey:
  "AI Mode"

Below the three columns, separated by whitespace, one italic caption in Poppins Italic 22pt, Mirage, centered:
"Тримата бодигарди получават заповедите си от един щаб."

Source line bottom right, Noto Sans 14pt, grey:
"Lily Ray · Substack · март 2026"

[SCREENSHOT placeholder: SS-08 Lily Ray correlation chart — may be inserted as a small thumbnail above the source line]

CRITICAL: Three numbers, identical structure, same rhythm. The eye reads across and instantly sees "all three drop together". Do NOT add a line chart on the slide — the three numbers ARE the chart.
```

---

## 1.4 Perplexity + Claude (Слайдове 15–20)

---

## SLIDE 15 — Perplexity (Title)

**Purpose:** Секционна бариера.
**Layout:** TITLE CARD (section divider).
**Speaker alignment:** script → Слайд 15 (ред 505–513).

### Genspark Prompt

```
Create a SECTION DIVIDER slide. Background: Deep Sea Green #075056.

Eyebrow: Poppins SemiBold 20pt, Haide Orange, uppercase:
"ЧАСТ 1 · PIPELINE #3"

Main headline: Poppins Bold 80pt, white, centered:
"Perplexity"

Subtitle: Poppins Regular 28pt, Wild Sand:
"Щедрият професор"

Stat: Poppins SemiBold 28pt, Haide Orange:
"8–12 citations · 3× повече от ChatGPT"

[SCREENSHOT placeholder: SS-05 Perplexity answer with visible citations — small inline if possible]

CRITICAL: Divider minimalism.
```

---

## SLIDE 16 — Perplexity 6-Stage Sonar RAG Pipeline

**Purpose:** Pipeline визуализация за Perplexity.
**Layout:** DIAGRAM (horizontal pipeline, 7 nodes).
**Speaker alignment:** script → Слайд 16 (ред 517–574).

### Genspark Prompt

```
Create a DIAGRAM slide — horizontal pipeline. Background: Wild Sand #E4EEF0.

Headline top, Poppins Bold 36pt, Mirage, centered:
"Perplexity — Sonar RAG pipeline"

HORIZONTAL FLOWCHART, 7 nodes, left-to-right:

NODE 1: "Заявка"
    →
NODE 2 (Haide Orange bg, white): "Query expansion · Sonar"
    →
NODE 3 (Deep Sea Green bg, white): "Multi-source retrieval · Google + Bing + own index"
    →
NODE 4 (Deep Sea Green bg, white): "Deduplication"
    →
NODE 5 (Haide Orange bg, white — VISUALLY EMPHASIZED, slightly larger than others): "Freshness scoring · двусигнален"
    →
NODE 6 (Deep Sea Green bg, white): "Re-ranking"
    →
NODE 7 (Haide Orange bg, white): "Citation · 8–12 източника"

Node text Poppins SemiBold 18pt. The freshness scoring node (Node 5) is the key differentiator — make it visually heavier (thicker border, slightly larger, or pulsing glow effect if Genspark supports).

Below the pipeline, ONE small callout annotation pointing to Node 5, in a rounded rectangle:
"+23% visibility при синхронизирани дати · Harbor SEO"

CRITICAL: 7 nodes max. The freshness node stands out visually because Adrian spends the most time on it. Everything else is uniform.
```

---

## SLIDE 17a — Claude Pipeline Diagram

**Purpose:** Claude pipeline с 6 стъпки. Brave Search, safety filter, marketing language punish.
**Layout:** DIAGRAM (horizontal pipeline, 6 nodes).
**Speaker alignment:** script → Слайд 17 (ред 578–645), първа половина.
**Split note:** Оригинален слайд 17 е разделен на 17a (pipeline) + 17b (marketing език A/B).

### Genspark Prompt

```
Create a DIAGRAM slide — horizontal pipeline. Background: Wild Sand #E4EEF0.

Headline top, Poppins Bold 36pt, Mirage, centered:
"Claude — строгият библиотекар"

HORIZONTAL FLOWCHART, 6 nodes:

NODE 1: "Заявка"
    →
NODE 2 (Haide Orange diamond shape, decision): "Web search trigger?"
    → (Yes branch only shown):
NODE 3 (Deep Sea Green bg, white): "Brave Search API"
    →
NODE 4 (Haide Orange bg, white — EMPHASIZED): "Safety + Neutrality filter"
    →
NODE 5 (Haide Orange bg, white — EMPHASIZED): "Deprioritize маркетинг език"
    →
NODE 6 (Deep Sea Green bg, white): "Citation · 3–5 домейна"

Poppins SemiBold 18pt. Nodes 4 and 5 are visually bolder because they are Claude's signature differentiators.

Small callout below Node 3: "45 млн queries/ден"
Small callout below Node 6: "45% enterprise AI spend"

[SCREENSHOT placeholder: SS-06 Claude answer with inline citations — optional small thumbnail in upper right corner if space]

CRITICAL: 6 nodes. The two orange nodes (Safety + Deprioritize marketing) are the "aha" — make them visually heavier than the green ones.
```

---

## SLIDE 17b — Маркетингов език vs Факти (A/B)

**Purpose:** Claude наказва marketing език. A/B сравнение на две изречения.
**Layout:** SPLIT SCREEN (A vs B comparison with verdict).
**Speaker alignment:** script → Слайд 17 (ред 623–642), втора половина.
**Split note:** Новодобавен слайд.

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical.

Top banner headline spanning full width, Poppins Bold 44pt, Mirage:
"Claude наказва маркетинг език"

LEFT HALF — background Wild Sand #E4EEF0, red accent:
- Eyebrow: Poppins SemiBold 18pt, red #C0392B, uppercase:
  "ВАРИАНТ А · ОТХВЪРЛЕН"
- Body text, Noto Sans Italic 24pt, Mirage, with superlatives UNDERLINED or highlighted in red:
  "Our best-in-class, industry-leading platform offers cutting-edge, game-changing performance."
- Verdict at bottom, Poppins Bold 28pt, red #C0392B:
  "✗ реклама"

RIGHT HALF — background Wild Sand #E4EEF0, green accent:
- Eyebrow: Poppins SemiBold 18pt, Deep Sea Green #075056, uppercase:
  "ВАРИАНТ Б · ЦИТИРАН"
- Body text, Noto Sans Regular 24pt, Mirage, with numbers HIGHLIGHTED in orange:
  "Нашата платформа намалява API latency с 47% в benchmarked тестове. Методология в GitHub."
- Verdict at bottom, Poppins Bold 28pt, Deep Sea Green:
  "✓ факт"

Source line at bottom, Noto Sans 14pt, grey, centered:
"Infrasity · Trakkr · януари 2026"

CRITICAL: Identical visual rhythm on both halves. The contrast is in the TONE of the text, not in the layout. Highlight colors do the heavy lifting — red on superlatives in А, orange on numbers in Б.
```

---

## SLIDE 18 — Enterprise Shift: Claude 45%

**Purpose:** Enterprise AI spend — Claude 45%, OpenAI 68% (надолу от 90%). B2B последствие.
**Layout:** STAT HERO (one primary stat + comparison).
**Speaker alignment:** script → Слайд 18 (ред 651–663).

### Genspark Prompt

```
Create a STAT HERO slide. Background: Mirage #16232A.

Centered.

Main stat, Poppins Black 260pt, Haide Orange #FF5B04:
"45%"

Caption directly below, Poppins Medium 32pt, white:
"enterprise AI spend отива към Claude · януари 2026"

Below, separated by whitespace, a small comparison row with two tiny stats side by side:
- Left: Poppins SemiBold 36pt, Wild Sand: "OpenAI 90% → 68%"
- Right: Poppins SemiBold 36pt, Wild Sand: "Others 15%"

Source line bottom, Noto Sans 16pt, grey:
"First Page Sage · април 2026 market share report"

[SCREENSHOT placeholder: SS-09 First Page Sage pie chart — may be a small circular chart in corner, but not required]

CRITICAL: The 45% is the hero. Everything else is whispered context.
```

---

## 1.5 Общи Паттърни (Слайдове 19–26)

---

## SLIDE 19 — Общи Паттърни (Title)

**Purpose:** Секционна бариера — въвеждаме 6-те common patterns.
**Layout:** TITLE CARD (section divider).
**Speaker alignment:** script → Слайд 19 (ред 671–678).

### Genspark Prompt

```
Create a SECTION DIVIDER slide. Background: Deep Sea Green #075056.

Eyebrow: Poppins SemiBold 20pt, Haide Orange, uppercase:
"ЧАСТ 1 · SYNTHESIS"

Main headline: Poppins Bold 80pt, white, centered:
"6 паттърна"

Subtitle: Poppins Regular 28pt, Wild Sand:
"Работят за всички 4 модела · 4× citation probability"

CRITICAL: Divider minimalism.
```

---

## SLIDE 20 — Cross-Model Common Patterns Diagram

**Purpose:** Хероична диаграма — 6 техники около централна страница.
**Layout:** DIAGRAM (hub-and-spoke, central node + 6 surrounding nodes).
**Speaker alignment:** script → Слайд 20 (ред 683–773).

### Genspark Prompt

```
Create a DIAGRAM slide — HUB AND SPOKE layout. Background: Wild Sand #E4EEF0.

Headline top-left corner, small, Poppins Bold 32pt, Mirage:
"6 паттърна → AI Citation"

CENTER OF SLIDE: one large circular or rounded-square node in Haide Orange #FF5B04, white text, Poppins Bold 32pt:
"Вашата страница"

Around the center node, arranged in a HEXAGON pattern (6 nodes, evenly spaced — top, top-right, bottom-right, bottom, bottom-left, top-left), 6 smaller rounded-square nodes, each in Deep Sea Green #075056 background, white text:

1. (top) "Answer Capsule · 40–60 думи"
2. (top-right) "Ski Ramp · първите 30%"
3. (bottom-right) "Proper Nouns · 20.6%"
4. (bottom) "FK Grade 16 · expert"
5. (bottom-left) "Tables · 2.3×"
6. (top-left) "Entity-first · не 'ние'"

Thin arrows from the center node OUT to each surrounding node (or from each surrounding node TO the center — your choice, whichever looks cleaner). Node text Poppins SemiBold 16pt.

CRITICAL: This is a busy slide BY NECESSITY (6 patterns). To prevent crowding:
- Central node must be visibly larger than the 6 surrounding ones (2x size).
- Generous spacing between surrounding nodes — they should NOT touch each other or the edges.
- Short labels only, max 4 words per surrounding node.
- NO extra stats, NO icons, NO decoration. The 6 names + the center are the entire slide.
If this still feels crowded in the first generation, I will split it into 20a (hero overview) and 20b (6 as a list).
```

---

## SLIDE 21 — Answer Capsule + Ski Ramp Stats

**Purpose:** Две числа, които са най-важните практични правила.
**Layout:** SPLIT SCREEN (two stats, one each side).
**Speaker alignment:** script → Слайд 21 (ред 777–795).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical. Background: Wild Sand #E4EEF0.

Headline top, spanning full width, Poppins Bold 40pt, Mirage:
"Двете правила, които пишат бъдещето ви"

LEFT HALF:
- Eyebrow: Poppins SemiBold 18pt, Haide Orange, uppercase:
  "ANSWER CAPSULE"
- Massive number: Poppins Black 180pt, Haide Orange #FF5B04, centered:
  "72.4%"
- Caption: Noto Sans Medium 22pt, Mirage:
  "от цитиранията имат 40–60 думи директен отговор в първите 150 думи"

RIGHT HALF:
- Eyebrow: Poppins SemiBold 18pt, Deep Sea Green, uppercase:
  "SKI RAMP"
- Massive number: Poppins Black 180pt, Deep Sea Green #075056, centered:
  "44.2%"
- Caption: Noto Sans Medium 22pt, Mirage:
  "от цитиранията идват от първите 30% на страницата"

Source line bottom, Noto Sans 14pt, grey, centered:
"iPullRank · Kevin Indig"

CRITICAL: Two stats, identical rhythm, different accent colors. Eye can compare instantly. No extra captions, no formulas.
```

---

## SLIDE 22 — Proper Nouns + FK + Tables

**Purpose:** Другите 3 pattern stats, минимално.
**Layout:** GRID (3 columns).
**Speaker alignment:** script → Слайд 22 (ред 799–815).

### Genspark Prompt

```
Create a 3-COLUMN GRID slide. Background: Mirage #16232A.

Headline top, Poppins Bold 40pt, white, centered:
"Плюс още три паттърна"

3 equal columns below, each with:
- Big number: Poppins Black 100pt, Haide Orange #FF5B04
- Label: Poppins SemiBold 22pt, white
- Tiny caption: Noto Sans Regular 16pt, Wild Sand

COLUMN 1:
- "20.6%"
- "Proper nouns"
- "vs 5–8% normal"

COLUMN 2:
- "16"
- "Flesch-Kincaid Grade"
- "пишете за колега"

COLUMN 3:
- "2.3×"
- "Tables"
- "повече citations"

Below the 3 columns, separated by whitespace, one emphasized line in Poppins Bold 32pt, Haide Orange, centered:
"Всички 6 заедно = 4× citation probability"

Source line bottom, Noto Sans 14pt, grey:
"iPullRank · Nectiv · март 2026"

CRITICAL: 3 columns, identical structure. The 4× takeaway is the punch. Nothing else.
```

---

## SLIDE 23 — Transition към Част 2 (Handout Cue)

**Purpose:** Край на Част 1. Контракт за Част 2. Handout идва.
**Layout:** SPLIT SCREEN (left: handing off; right: enlarged QR).
**Speaker alignment:** script → Слайд 23 (ред 819–835).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 60/40 vertical split. Background: Deep Sea Green #075056.

LEFT (60% width):
- Eyebrow: Poppins SemiBold 20pt, Haide Orange, uppercase:
  "ЧАСТ 2 · ИМПЛЕМЕНТАЦИЯ"
- Main headline: Poppins Bold 64pt, white:
  "Сканирайте QR кода"
- Three short lines, stacked, Poppins Medium 28pt, Wild Sand:
  "60-точков чеклист · PDF"
  "20 ще минем заедно"
  "40 за четене у вас"

RIGHT (40% width):
- Large QR code, centered, roughly 70% of the right section's height. White QR on Deep Sea Green.
- Below QR, Poppins Medium 22pt, Haide Orange:
  "haide.digital/masterclass-2026"
- Below that, Noto Sans Regular 18pt, Wild Sand:
  "Без регистрация"

CRITICAL: This is the second "enlarged QR" moment (after Slide 2). The QR is prominent but not full-screen like Slide 2. Left side has max 4 text elements. No other decoration.
```

---

# SPLIT DECISIONS LOG

| Original slide | Split into | Why |
|---|---|---|
| Slide 10 (GPT-5.3 vs 5.4) | 10a (A/B split screen) + 10b (7% + 75% killer stats) | Оригиналът имаше 4 числа + a/b comparison на един слайд. 7% overlap е punchline и заслужава свой момент. |
| Slide 13 (95% + E-E-A-T) | 13a (95% zero-volume stat) + 13b (E-E-A-T 4-point checklist) | Две различни идеи: едната е "практически extract от GSC", другата е "бодигард checklist". Пренатъпкано заедно. |
| Slide 17 (Claude pipeline + marketing език) | 17a (Claude diagram) + 17b (A/B marketing език) | Pipeline диаграма + дълъг списък от superlatives на един слайд = crowded. A/B сравнението заслужава свой slide за да може публиката да прочете двете изречения. |

**Result:** 23 оригинални слайда → **26 слайда** за генериране в Genspark.

**Slide count бреak-down:**
- Въведение: 3 слайда (1–3)
- Cold open: 3 слайда (4–6)
- ChatGPT: 5 слайда (7, 8, 9, 10a, 10b)
- Google AI Mode: 5 слайда (11, 12, 13a, 13b, 14)
- Perplexity: 2 слайда (15, 16)
- Claude: 3 слайда (17a, 17b, 18)
- Common patterns: 4 слайда (19, 20, 21, 22)
- Transition: 1 слайд (23 — финален)

Total: **26 слайда** за ~33 мин = средно 1:16 мин на слайд. Realistic pace за мастърклас.

---

# VERIFICATION CHECKLIST ПРЕДИ ГЕНЕРИРАНЕ

- [ ] Global style brief copy-pasted в Genspark deck settings.
- [ ] Всяка EN prompt инструкция е ясна за Genspark. Всеки БГ текст е в кавички (не превеждаме).
- [ ] Anti-crowding reminder присъства в КАЖДА prompt (критично — Genspark има тенденция да претъпква).
- [ ] Цветовете са само 4 (#FF5B04, #075056, #E4EEF0, #16232A) — без допълнителни.
- [ ] Screenshot placeholders са маркирани където трябва (SS-01 до SS-09).
- [ ] QR код стратегия: пълен екран на слайд 2, corner master element от слайд 3, увеличен на слайд 23.
- [ ] 5 pipeline диаграми описани без mermaid source (слайдове 8, 12, 16, 17a, 20).
- [ ] Всички 26 слайда имат speaker alignment референция към script файла.

---

# СЛЕДВАЩИ СТЪПКИ

1. **Копирай Global Style Brief в Genspark deck settings.**
2. **Слайд по слайд** — копирай Genspark Prompt блок, генерирай, review.
3. **Когато нещо е claustrofobично** — кажи на Genspark „remove X, more whitespace" или викни мен и го сплитваме на 2 слайда.
4. **Screenshot capture session преди 5 април** — 9 screenshots от checklist-а по-горе (SS-01 до SS-09).
5. **Когато Част 1 е approved визуално** — започваме Част 2 по същия процес (checklist walkthrough + 5 tool demos, ~20 слайда ще стават ~25).
6. **Final:** Част 3 (monitoring stack, ~12 слайда ще стават ~15).

**Очакван финален deck:** ~70 слайда общо за 90 минути = ~1:17 мин/слайд. Professional pace.
