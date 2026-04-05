# Genspark Slide Prompts — Част 2 (Чеклист walk-through + 5 Live Tool Demos)

> **Deck:** Техническо SEO в AI ерата — Адриан Николов, Haide Digital
> **Event:** Enterprise Magazine × EURODEA SEO Masterclass, София, 23 април 2026
> **Source script:** [script-part2-checklist-and-tools.md](script-part2-checklist-and-tools.md)
> **Slide count:** 31 (слайдове 27–57, продължение на същия Genspark deck от Part 1)
> **Total runtime:** ~30 минути (23 мин говорене + 7 мин в live browser demos)
> **Language strategy:** EN инструкции към Genspark, БГ slide content в кавички `" "` (не превеждаме).

---

## ВАЖНО — КОНТЕКСТ ЗА GENSPARK (Part 2)

**Тази генерация е Част 2 от 3-частна презентация.** Добавяш тези 31 слайда към същия Genspark deck, който вече съдържа Part 1 (слайдове 1–26). **Не започвай нов deck.** Визуалната консистентност с Part 1 е критична — същите цветове, типография, anti-crowding rules, master QR corner element.

- **Part 1 (DONE)** — слайдове 1–26 — Въведение + как работят AI моделите
- **Part 2 (ТОЗИ ДОКУМЕНТ)** — слайдове 27–57 — Чеклист walk-through + 5 live tool demos
- **Part 3 (СЛЕДВА)** — слайдове 58–~72 — Monitoring stack + survival workflow

**Global Style Brief от Part 1 остава в сила за всички слайдове тук.** Не го paste-вай отново — вече е deck-level instruction. Ако Genspark „забрави" стила на някой слайд, copy-paste-ни го отново в този slide prompt като reminder.

**Master QR element:** продължава в bottom-right corner на всеки слайд (от Part 1 slide 3 нататък). Слайд 28 и слайд 56 имат enlarged QR treatments (описано per slide).

---

## WHAT'S NEW IN PART 2 (визуални patterns, които не съществуват в Part 1)

1. **Tool Entry slide pattern** — hero slide с име на инструмент, URL, 1 изречение, списък на чеклист точките, които покрива. 5 броя (слайдове 32, 40, 46, 48, 50).
2. **Tool Exit slide pattern** — „това видяхте" summary + CTA + screenshot thumbnail. 5 броя (слайдове 33, 41, 47, 49, 51).
3. **Block Section Divider pattern** — малки section dividers между 6-те тематични блока. По-леки от Part 1 section dividers (няма „ЧАСТ X · PIPELINE #Y" eyebrow — тук е „БЛОК X · Y ТОЧКИ").
4. **Checklist Points slide pattern** — 2 или 3 checklist points на слайд, всяка с номер + заглавие + 1 supporting line max. Никога не > 3 points на слайд.
5. **Code snippet slide** — 1 слайд (35) с JSON-LD code example. Monospace font, clean syntax highlighting.

---

## SCREENSHOT CHECKLIST (Part 2 нови)

| ID | Source | Slide |
|---|---|---|
| SS-10 | Chrome DevTools Network tab — Resource vs Transferred columns | 30 |
| SS-11 | Haide Ceiling output — traffic light + fix snippet | 33 |
| SS-12 | schema.org Organization с пълен sameAs граф | 35 |
| SS-13 | Haide Bot Radar dashboard + AI dark matter panel | 41 |
| SS-14 | Haide Ski Ramp side-by-side histogram + scores | 47 |
| SS-15 | Haide Fan-Out Scope node graph (8–12 sub-queries) | 49 |
| SS-16 | Haide Prompt Miner / GSC regex results | 51 |

---

# ЧАСТ 2 — КАК СЕ ИМПЛЕМЕНТИРА (Слайдове 27–57)

## 2.1 Opening (Слайдове 27–28)

---

## SLIDE 27 — Part 2 Section Divider

**Purpose:** Отваряне на Част 2. Кратко dwell (15 сек), breath moment след Part 1 transition.
**Layout:** SECTION DIVIDER (title card).
**Speaker alignment:** script → Слайд 27 (ред 98–108).

### Genspark Prompt

```
Create a SECTION DIVIDER slide. Full-bleed background: Deep Sea Green #075056.

Centered vertically.

Small eyebrow label, Poppins SemiBold 20pt, Haide Orange #FF5B04, uppercase, centered:
"ЧАСТ 2"

Main headline below, Poppins Bold 110pt, white #FFFFFF, centered:
"Имплементация"

Subtitle below headline, Poppins Regular 28pt, Wild Sand #E4EEF0, centered:
"20 точки · 5 инструмента · 30 минути"

Master QR corner element in bottom-right (80x80, white on transparent) — same as every slide from Part 1 slide 3 onwards.

CRITICAL: This is a breathing moment after Part 1 transition. Pure minimalism. No decoration. No images.
```

---

## SLIDE 28 — QR Teaser + Контракт

**Purpose:** Напомняне за QR + контракт за следващите 30 мин (20 точки, 5 инструмента, 6 блока).
**Layout:** SPLIT SCREEN (left: teaser bullets; right: enlarged QR reminder).
**Speaker alignment:** script → Слайд 28 (ред 112–128).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 60/40 vertical split. Background: Wild Sand #E4EEF0.

LEFT (60% width):
Small eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"СЛЕДВАЩИТЕ 30 МИНУТИ"

Below eyebrow, main headline, Poppins Bold 48pt, Mirage #16232A:
"Контрактът е прост"

Below headline, a vertical list of 4 short lines, each with a small orange bullet dot, Poppins Medium 28pt, Mirage #16232A:
"20 от 60 точки заедно"
"5 живи инструмента"
"6 тематични блока"
"Едно волонтьорско demo"

RIGHT (40% width, background Deep Sea Green #075056):
Large QR code centered, roughly 55% of the right section's height. White QR on Deep Sea Green for contrast. Encodes haide.digital/masterclass-2026.

Below the QR, Poppins Medium 22pt, Haide Orange #FF5B04, centered:
"haide.digital/masterclass-2026"

Below that, Poppins Regular 18pt, Wild Sand #E4EEF0, centered:
"60-точков чеклист · PDF · без регистрация"

CRITICAL: Max 4 bullets on the left. No descriptions. Enlarged QR here is the second "scan moment" after Part 1 slide 2. Generous whitespace around all elements.
```

---

## 2.2 Блок 1 — HTML Infrastructure (Слайдове 29–33)

---

## SLIDE 29 — Block 1 Divider

**Purpose:** Секционен divider за Блок 1.
**Layout:** BLOCK SECTION DIVIDER (smaller than Part 1 dividers).
**Speaker alignment:** script → Слайд 29 (ред 136–142).

### Genspark Prompt

```
Create a BLOCK SECTION DIVIDER slide. Background: Mirage #16232A.

Centered vertically, left-aligned.

Eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"БЛОК 1 · 5 ТОЧКИ"

Main headline below, Poppins Bold 84pt, white #FFFFFF:
"HTML Infrastructure"

Subtitle below, Poppins Regular 28pt, Wild Sand #E4EEF0:
"Камионът и мостът"

Master QR corner bottom-right.

CRITICAL: Lighter than Part 1 section dividers. This is a mid-level chapter marker, not a major section break. Max 3 text elements. Lots of empty space.
```

---

## SLIDE 30 — Точки 1 и 2: 2MB HTML лимит

**Purpose:** Двете най-критични HTML точки. Resource vs Transferred screenshot.
**Layout:** SPLIT SCREEN (left: two checklist points; right: DevTools screenshot).
**Speaker alignment:** script → Слайд 30 (ред 146–174).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 55/45 vertical split. Background: Wild Sand #E4EEF0.

Top centered headline spanning full width, Poppins Bold 40pt, Mirage #16232A:
"2 мегабайта. Бетонен мост."

LEFT HALF (55% width):
Two checklist items stacked vertically, with large whitespace between them. Each item:
- Small orange number circle (40px diameter, Haide Orange #FF5B04 background, white number inside, Poppins Bold 22pt)
- Title in Poppins Bold 26pt, Mirage #16232A
- ONE supporting line in Noto Sans Regular 20pt, dark grey

Item 1:
Circle: "1"
Title: "HTML под 2MB некомпресиран"
Support: "Google WRS просто спира да чете над линията"

Item 2:
Circle: "2"
Title: "Критичното съдържание в първите 2MB"
Support: "H1, answer capsule, JSON-LD — всичко преди границата"

RIGHT HALF (45% width):
Screenshot placeholder box with label: [SCREENSHOT: SS-10 — Chrome DevTools Network tab, columns "Resource size" vs "Transferred size" highlighted in orange]

Below the screenshot, small caption Noto Sans Italic 16pt, dark grey:
"Гледайте Resource size, не Transferred"

CRITICAL: Max 2 checklist points on this slide. Do NOT add the 90% / 151KB stat — Adrian says it verbally. Whitespace is the feature.
```

---

## SLIDE 31 — Точки 3, 4, 6: JSON-LD позиция + inline JS

**Purpose:** Три свързани точки за позиция на елементи в HTML.
**Layout:** GRID (3 equal cells).
**Speaker alignment:** script → Слайд 31 (ред 178–198).

### Genspark Prompt

```
Create a GRID slide, 3 equal-width columns. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 40pt, Mirage #16232A:
"Позицията е всичко"

Below headline, 3 equal cells side by side. Each cell contains:
- Large orange number circle (60px, Haide Orange #FF5B04 bg, white number, Poppins Bold 28pt)
- Title in Poppins SemiBold 24pt, Mirage #16232A, 2 lines max
- ONE short supporting line in Noto Sans Regular 18pt, dark grey

Cell 1:
Circle: "3"
Title: "JSON-LD в <head>"
Support: "Не в footer на <body>"

Cell 2:
Circle: "4"
Title: "Meta tags високо"
Support: "Преди tracking + chat widgets"

Cell 3:
Circle: "6"
Title: "JavaScript екстернализиран"
Support: "Без големи inline <script> блокове"

Generous padding inside each cell. Cells clearly separated.

CRITICAL: 3 cells maximum. Max 3 text elements per cell. No paragraphs. The analogy "адресът на гара" stays verbal — not on the slide.
```

---

## SLIDE 32 — Haide Ceiling Entry

**Purpose:** Tool #1 entry slide. Hero moment за първия инструмент.
**Layout:** TOOL ENTRY (new pattern for Part 2).
**Speaker alignment:** script → Слайд 32 (ред 202–222).

### Genspark Prompt

```
Create a TOOL ENTRY slide — a new hero pattern for Part 2. Background: Deep Sea Green #075056.

Centered vertically, left-aligned content.

Small eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"ИНСТРУМЕНТ 1 ОТ 5"

Main tool name, Poppins Black 96pt, white #FFFFFF:
"Haide Ceiling"

URL below tool name, Poppins Medium 28pt, Haide Orange #FF5B04:
"haide.digital/ceiling"

One-line description below URL, Poppins Regular 26pt, Wild Sand #E4EEF0, max one line:
"2MB HTML budget + schema sanity за 8 секунди"

At the bottom of the slide, a small tag strip — Poppins SemiBold 16pt, Haide Orange, uppercase:
"ПОКРИВА ТОЧКИ: 1 · 2 · 3 · 4 · 6 · 11 · 13 · 14"

CRITICAL: This is a hero slide. No screenshots, no additional copy. Just tool name + URL + one line + coverage tag. Adrian switches to browser after 15 seconds of dwell.
```

---

## SLIDE 33 — Haide Ceiling Exit

**Purpose:** Tool #1 exit slide. „Какво видяхте" + CTA + thumbnail.
**Layout:** TOOL EXIT (new pattern).
**Speaker alignment:** script → Слайд 33 (ред 226–236).

### Genspark Prompt

```
Create a TOOL EXIT slide — new pattern for Part 2. Background: Wild Sand #E4EEF0.

Top left, small eyebrow, Poppins SemiBold 16pt, Haide Orange #FF5B04, uppercase:
"HAIDE CEILING · РЕЗЮМЕ"

Main headline below eyebrow, Poppins Bold 44pt, Mirage #16232A:
"Това видяхте"

Below headline, 3 short bullet lines (each with a small orange checkmark icon), Poppins Medium 26pt, Mirage #16232A, stacked with breathing room:
"Resource size проверка"
"Schema валидация"
"Copy-paste fix snippet"

Right side of slide: screenshot placeholder box, roughly 40% of slide width. Label: [SCREENSHOT: SS-11 — Haide Ceiling output — traffic light + fix snippet]

Bottom of slide, one CTA line, Poppins SemiBold 24pt, Deep Sea Green #075056, centered:
"haide.digital/ceiling · без регистрация"

CRITICAL: Max 3 bullets. Screenshot is supporting evidence, not the main focus. The "това видяхте" headline anchors the moment post-demo.
```

---

## 2.3 Блок 2 — Structured Data (Слайдове 34–36)

---

## SLIDE 34 — Block 2 Divider

**Purpose:** Section divider за Блок 2.
**Layout:** BLOCK SECTION DIVIDER.
**Speaker alignment:** script → Слайд 34 (ред 244–250).

### Genspark Prompt

```
Create a BLOCK SECTION DIVIDER slide. Background: Mirage #16232A.

Centered vertically, left-aligned.

Eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"БЛОК 2 · 4 ТОЧКИ"

Main headline, Poppins Bold 84pt, white #FFFFFF:
"Structured Data"

Subtitle, Poppins Regular 28pt, Wild Sand #E4EEF0:
"Личната карта за AI моделите"

Master QR corner bottom-right.

CRITICAL: Same lightweight divider pattern as slide 29. Max 3 text elements.
```

---

## SLIDE 35 — Точки 11, 13: Organization + Article schema

**Purpose:** Двете базови schema-та. Показваме истински code snippet.
**Layout:** SPLIT SCREEN (left: point 11 + Organization code; right: point 13 + Article code).
**Speaker alignment:** script → Слайд 35 (ред 254–274).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical split. Background: Wild Sand #E4EEF0.

Top centered headline spanning full width, Poppins Bold 36pt, Mirage #16232A:
"Лична карта + паспорт"

LEFT HALF:
Small orange number circle (48px) top-left: "11"
Title, Poppins Bold 24pt, Mirage, next to circle:
"Organization · sameAs граф"

Below title, a monospace code snippet box (background Mirage #16232A, rounded corners, padding 20px). Inside the box, JetBrains Mono or similar monospace 14pt, with simple syntax coloring (keys in Haide Orange #FF5B04, string values in Wild Sand #E4EEF0):

{
  "@type": "Organization",
  "name": "Haide Digital",
  "url": "haide.digital",
  "logo": "...",
  "sameAs": [
    "linkedin.com/...",
    "wikipedia.org/...",
    "wikidata.org/...",
    "github.com/...",
    "youtube.com/..."
  ]
}

[SCREENSHOT placeholder: SS-12 — production Organization schema from Haide Digital — optional inline overlay]

RIGHT HALF:
Small orange number circle (48px) top-left: "13"
Title, Poppins Bold 24pt, Mirage, next to circle:
"Article · author + dateModified"

Below title, a monospace code snippet box (same style as left):

{
  "@type": "Article",
  "headline": "...",
  "author": { "@type": "Person", "name": "..." },
  "datePublished": "2026-04-23",
  "dateModified": "2026-04-23"
}

CRITICAL: Two code snippets, both short. Max 10 lines each. Monospace font is small but readable from 3 meters. No extra commentary — the code is the content.
```

---

## SLIDE 36 — Точки 14, 35: Product 2026 + Author schema

**Purpose:** Новите 2026 Product полета + Author Person schema.
**Layout:** SPLIT SCREEN (left: point 14 with 4 orange-highlighted fields; right: point 35).
**Speaker alignment:** script → Слайд 36 (ред 278–298).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical split. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 36pt, Mirage #16232A:
"Product 2026 · Author verified"

LEFT HALF:
Small orange circle: "14"
Title, Poppins Bold 24pt, Mirage:
"Product · 4 нови задължителни полета"

Below title, 4 fields listed vertically, each in Poppins Medium 22pt. The FIELD NAMES are in Haide Orange #FF5B04 (monospace). The descriptions in Mirage #16232A regular:

"hasMerchantReturnPolicy" — return policy
"shippingDetails" — доставка, дни, цена
"priceValidUntil" — валидност на цената
"itemCondition" — ново · използвано · refurbished

Below the list, one short warning line, Poppins SemiBold 18pt, Haide Orange:
"Без тези полета: невидими за ChatGPT Shopping"

RIGHT HALF:
Small orange circle: "35"
Title, Poppins Bold 24pt, Mirage:
"Author · Person schema с sameAs"

Below title, a simple visual list of platforms with small icons or labels, Poppins Medium 22pt, Mirage:
"LinkedIn"
"ORCID (за академични автори)"
"Wikipedia (ако имате запис)"
"Google Scholar"

Below the list, one short line, Poppins Italic 18pt, Deep Sea Green #075056:
"Реален човек. Не 'by admin'."

CRITICAL: Left side orange field names are the visual hook. Do NOT include full JSON-LD code — too much. The 4 field names alone carry the message.
```

---

## 2.4 Блок 3 — AI Crawler Access (Слайдове 37–41)

---

## SLIDE 37 — Block 3 Divider

**Purpose:** Section divider за Блок 3.
**Layout:** BLOCK SECTION DIVIDER.
**Speaker alignment:** script → Слайд 37 (ред 307–313).

### Genspark Prompt

```
Create a BLOCK SECTION DIVIDER slide. Background: Mirage #16232A.

Centered vertically, left-aligned.

Eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"БЛОК 3 · 4 ТОЧКИ"

Main headline, Poppins Bold 84pt, white #FFFFFF:
"AI Crawler Access"

Subtitle, Poppins Regular 28pt, Wild Sand #E4EEF0:
"Списъкът на гости на вратата"

Master QR corner.

CRITICAL: Same lightweight divider pattern. Max 3 elements.
```

---

## SLIDE 38 — 13 AI User-Agents (Точка 19)

**Purpose:** Пълен списък на 13-те AI crawler-а в 2026, групирани по vendor.
**Layout:** GRID (vendor-grouped list, 6-7 vendor blocks).
**Speaker alignment:** script → Слайд 38 (ред 317–337).

### Genspark Prompt

```
Create a GRID slide with vendor-grouped list. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 44pt, Mirage #16232A:
"13 AI crawler-а в 2026"

Small subtitle below headline, Poppins Regular 22pt, dark grey:
"Точка 19 · всички в robots.txt Allow"

Below the headline, a 3-column layout of vendor groups. Each vendor group contains:
- Vendor name, Poppins Bold 22pt, Haide Orange #FF5B04
- Bot names under it, Poppins SemiBold 20pt, Mirage #16232A, monospace (JetBrains Mono), stacked vertically

COLUMN 1:
OpenAI
  GPTBot
  OAI-SearchBot
  ChatGPT-User

Anthropic
  ClaudeBot
  Claude-SearchBot
  Claude-User

COLUMN 2:
Perplexity
  PerplexityBot
  Perplexity-User

Google
  Google-Extended
  Google-Agent

COLUMN 3:
Apple
  Applebot-Extended

Mistral
  MistralAI-User/Index

Common Crawl
  CCBot

Bottom of slide, right-aligned, Poppins Italic 18pt, Deep Sea Green #075056:
"Проверете robots.txt-а си тази вечер"

CRITICAL: 13 bot names total. 7 vendor groups. Monospace font for bot names makes them feel technical and authoritative. Do NOT add descriptions — the names alone are the content.
```

---

## SLIDE 39 — Точки 20, 25, 26: Google-Agent ignores robots.txt

**Purpose:** Най-шокиращият факт в Блок 3 — user-triggered fetchers игнорират robots.txt.
**Layout:** STAT HERO вариант (central warning + 3 small supporting points).
**Speaker alignment:** script → Слайд 39 (ред 341–359).

### Genspark Prompt

```
Create a STAT HERO variant slide. Background: Mirage #16232A.

Top of slide, small eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase, centered:
"ТОЧКА 25 · GOOGLE · 20 МАРТ 2026"

Central hero text, Poppins Black 72pt, white #FFFFFF, centered, max 2 lines:
"Google-Agent игнорира"
"robots.txt"

Below the hero text, a short tag line in Poppins Medium 26pt, Haide Orange #FF5B04, centered:
"Полицейски ордер. Минава и през заключена врата."

Bottom of slide, 3 small supporting points in a horizontal row, Poppins Regular 18pt, Wild Sand #E4EEF0:
"20 · не блокирайте GPTBot · training loss"
"25 · user-triggered = ignore robots"
"26 · логове = ранна предупреждение"

CRITICAL: The shock is the headline. The 3 supporting points are small, grouped, easy to skim. Do NOT expand them into sentences. Adrian carries the narrative verbally.
```

---

## SLIDE 40 — Haide Bot Radar Entry

**Purpose:** Tool #2 entry slide.
**Layout:** TOOL ENTRY (same pattern as slide 32).
**Speaker alignment:** script → Слайд 40 (ред 363–381).

### Genspark Prompt

```
Create a TOOL ENTRY slide — same pattern as slide 32. Background: Deep Sea Green #075056.

Centered vertically, left-aligned content.

Eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"ИНСТРУМЕНТ 2 ОТ 5"

Main tool name, Poppins Black 96pt, white #FFFFFF:
"Haide Bot Radar"

URL, Poppins Medium 28pt, Haide Orange #FF5B04:
"haide.digital/bot-radar"

One-line description, Poppins Regular 26pt, Wild Sand #E4EEF0:
"Качваш server log → виждаш кой от 13-те реално те посещава"

Bottom tag strip, Poppins SemiBold 16pt, Haide Orange, uppercase:
"ПОКРИВА ТОЧКИ: 19 · 20 · 25 · 26"

CRITICAL: Same hero treatment as Haide Ceiling entry slide. Consistency matters — audience will recognize the pattern.
```

---

## SLIDE 41 — Haide Bot Radar Exit

**Purpose:** Tool #2 exit slide. AI Dark Matter списъка е killer feature.
**Layout:** TOOL EXIT (same pattern as slide 33).
**Speaker alignment:** script → Слайд 41 (ред 385–395).

### Genspark Prompt

```
Create a TOOL EXIT slide — same pattern as slide 33. Background: Wild Sand #E4EEF0.

Top left, eyebrow, Poppins SemiBold 16pt, Haide Orange, uppercase:
"HAIDE BOT RADAR · РЕЗЮМЕ"

Main headline, Poppins Bold 44pt, Mirage #16232A:
"AI Dark Matter — видяхте какво никой не вижда"

Below headline, 3 bullet lines with orange checkmarks, Poppins Medium 26pt, Mirage:
"Frequency dashboard (13 bots)"
"AI Dark Matter panel"
"Pages not crawled in 90 days"

Right side: screenshot placeholder, ~40% width. Label: [SCREENSHOT: SS-13 — Haide Bot Radar dashboard + AI Dark Matter list]

Bottom CTA, Poppins SemiBold 24pt, Deep Sea Green #075056, centered:
"haide.digital/bot-radar · Apache + Nginx логове"

CRITICAL: "AI Dark Matter" is the memorable phrase — make it the headline. Max 3 bullets.
```

---

## 2.5 Блок 4 — Content Architecture (CENTRAL) (Слайдове 42–51)

---

## SLIDE 42 — Block 4 Divider (CENTRAL)

**Purpose:** Section divider за най-важния блок. По-силно визуално внимание.
**Layout:** BLOCK SECTION DIVIDER — but emphasized.
**Speaker alignment:** script → Слайд 42 (ред 403–409).

### Genspark Prompt

```
Create an EMPHASIZED BLOCK SECTION DIVIDER slide. Background: Haide Orange #FF5B04 (full bleed — unique in Part 2, marks this as the central block).

Centered vertically, left-aligned.

Eyebrow, Poppins SemiBold 20pt, Mirage #16232A, uppercase:
"БЛОК 4 · 7 ТОЧКИ · 3 ИНСТРУМЕНТА"

Main headline, Poppins Black 96pt, Mirage #16232A:
"Content Architecture"

Subtitle below headline, Poppins Medium 32pt, Mirage #16232A:
"Най-важният блок в чеклиста"

Master QR corner — but use Mirage on the orange background for visibility.

CRITICAL: This is the ONLY orange full-bleed section divider in the entire deck. It marks Block 4 as central. No other slide in Part 2 uses this background. Visually distinctive.
```

---

## SLIDE 43 — Точки 29, 30: answer capsule + entity-first

**Purpose:** Двете core writing rules за AI visibility.
**Layout:** SPLIT SCREEN (left: point 29; right: point 30).
**Speaker alignment:** script → Слайд 43 (ред 413–433).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical split. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 40pt, Mirage #16232A:
"Първите 70 думи решават"

LEFT HALF:
Small orange circle: "29"
Title, Poppins Bold 28pt, Mirage:
"Answer Capsule"

Below title, one supporting line, Poppins Medium 22pt, Mirage:
"Директен отговор в първите 50–70 думи"

Below that, a big stat line in Poppins Black 64pt, Haide Orange #FF5B04:
"72.4%"

Below stat, Poppins Regular 18pt, dark grey:
"от всички цитирания идват от този блок"

RIGHT HALF:
Small orange circle: "30"
Title, Poppins Bold 28pt, Mirage:
"Entity-first"

Below title, one supporting line, Poppins Medium 22pt, Mirage:
"Името на entity-то преди всичко"

Below that, a quoted example in Poppins Italic 22pt, Deep Sea Green #075056 (styled as a quote):
"Haide Digital е organic growth
engineering компания, базирана
в София, България."

CRITICAL: Left side uses a stat to anchor the rule. Right side uses a direct example (in entity-first format). The example IS the rule demonstrated.
```

---

## SLIDE 44 — Точки 31, 32, 33: sources + research + topical authority

**Purpose:** Трите правила за content credibility.
**Layout:** GRID (3 cells).
**Speaker alignment:** script → Слайд 44 (ред 437–453).

### Genspark Prompt

```
Create a GRID slide with 3 equal cells. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 40pt, Mirage #16232A:
"Кредибилност в 3 стъпки"

Below headline, 3 equal-width cells side by side. Each cell:
- Large orange number circle (60px, Haide Orange bg, white number, Poppins Bold 28pt)
- Title, Poppins Bold 26pt, Mirage #16232A
- ONE supporting line, Noto Sans Regular 18pt, dark grey

Cell 1:
Circle: "31"
Title: "Статистика с източник"
Support: "Kevin Indig > неанонимен number"

Cell 2:
Circle: "32"
Title: "Уникално изследване"
Support: "1 benchmark > 50 агрегирани постове"

Cell 3:
Circle: "33"
Title: "Topical Authority"
Support: "Цяла медицинска специалност, не брошурка"

CRITICAL: 3 cells max. Max 3 text elements per cell. Do NOT add Topical Authority Systems trademark line — Adrian carries it verbally.
```

---

## SLIDE 45 — Точки 51, 53: AIO + semantic chunking

**Purpose:** Двете technical writing rules за passage-level retrieval.
**Layout:** SPLIT SCREEN.
**Speaker alignment:** script → Слайд 45 (ред 457–473).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical split. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 40pt, Mirage #16232A:
"Всеки H2 блок стои сам"

LEFT HALF:
Small orange circle: "51"
Title, Poppins Bold 26pt, Mirage:
"AIO source selection"

Below title, Poppins Medium 22pt, Mirage:
"Passage-level front-loading"

Below that, Noto Sans Regular 18pt, dark grey:
"Всеки H2/H3 блок — самостоятелен отговор"

RIGHT HALF:
Small orange circle: "53"
Title, Poppins Bold 26pt, Mirage:
"Semantic chunking за RAG"

Below title, Poppins Medium 22pt, Mirage:
"Торта на хапки за дете"

Below that, a small boxed "don't" example in Mirage #16232A text on light grey background, Noto Sans Regular 18pt:
"❌ 'както споменахме по-горе'"

Below the don't box, a boxed "do" example in Deep Sea Green text on Wild Sand:
"✅ 'както Haide Ceiling показва в раздела за pricing'"

CRITICAL: The don't/do pair is the memorable hook. Max 2 bullet points per half. The torta analogy stays verbal.
```

---

## SLIDE 46 — Haide Ski Ramp Entry

**Purpose:** Tool #3 entry.
**Layout:** TOOL ENTRY.
**Speaker alignment:** script → Слайд 46 (ред 477–497).

### Genspark Prompt

```
Create a TOOL ENTRY slide — same pattern as slides 32 and 40. Background: Deep Sea Green #075056.

Eyebrow, Poppins SemiBold 18pt, Haide Orange, uppercase:
"ИНСТРУМЕНТ 3 ОТ 5"

Main tool name, Poppins Black 96pt, white:
"Haide Ski Ramp"

URL, Poppins Medium 28pt, Haide Orange:
"haide.digital/ski-ramp"

One-line description, Poppins Regular 26pt, Wild Sand:
"Citation-Readiness Score 0–100 за всяка страница"

Bottom tag strip, Poppins SemiBold 16pt, Haide Orange, uppercase:
"ПОКРИВА ТОЧКИ: 29 · 30 · 31 · 32 · 33 · 51 · 53"

CRITICAL: Same hero treatment as previous tool entries. Consistency.
```

---

## SLIDE 47 — Haide Ski Ramp Exit

**Purpose:** Tool #3 exit. Side-by-side histogram is the killer screenshot.
**Layout:** TOOL EXIT (but with larger screenshot — this one is visual).
**Speaker alignment:** script → Слайд 47 (ред 501–511).

### Genspark Prompt

```
Create a TOOL EXIT slide with visual emphasis. Background: Wild Sand #E4EEF0.

Top left, eyebrow, Poppins SemiBold 16pt, Haide Orange, uppercase:
"HAIDE SKI RAMP · РЕЗЮМЕ"

Main headline, Poppins Bold 44pt, Mirage #16232A:
"Две страници. Един скор."

Below headline, LARGE screenshot placeholder spanning most of the slide width. Label: [SCREENSHOT: SS-14 — Haide Ski Ramp side-by-side — two histograms, one cited URL (78/100), one non-cited URL (23/100)]

Below the screenshot, 2 small stat labels side by side, Poppins Bold 32pt:
Left: "78 / 100" in Deep Sea Green #075056 — caption "Cited"
Right: "23 / 100" in grey #888 — caption "Non-cited"

Bottom CTA, Poppins SemiBold 22pt, Haide Orange, centered:
"haide.digital/ski-ramp"

CRITICAL: This exit slide is visually driven by the screenshot — not by bullets. The 78 vs 23 contrast is the hook. Do NOT add bullet list. Screenshot + two numbers = the story.
```

---

## SLIDE 48 — Haide Fan-Out Scope Entry (HEADLINE DEMO)

**Purpose:** Tool #4 entry — highest stakes demo. Voluntary query from audience.
**Layout:** TOOL ENTRY + warning badge.
**Speaker alignment:** script → Слайд 48 (ред 515–533).

### Genspark Prompt

```
Create a TOOL ENTRY slide with live warning badge. Background: Deep Sea Green #075056.

Eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"ИНСТРУМЕНТ 4 ОТ 5 · HEADLINE"

Main tool name, Poppins Black 88pt, white #FFFFFF:
"Haide Fan-Out Scope"

URL, Poppins Medium 28pt, Haide Orange:
"haide.digital/fanout"

One-line description, Poppins Regular 26pt, Wild Sand:
"Рентгенова снимка на това, което AI реално пита"

Large visual badge (rounded rectangle, Haide Orange fill, Mirage text), centered below description, Poppins Black 28pt, uppercase:
"⚡ LIVE · VOLUNTEER QUERY"

Bottom tag strip, Poppins SemiBold 16pt, Haide Orange, uppercase:
"ПОКРИВА ТОЧКИ: 29 · 52 · 55"

CRITICAL: The LIVE VOLUNTEER badge signals to the audience that this one is special. Adrian will use 5-10 second silent pause waiting for a volunteer. Badge must be visually distinctive but NOT crowd the tool name.
```

---

## SLIDE 49 — Haide Fan-Out Scope Exit

**Purpose:** Tool #4 exit. Node graph screenshot is the wow moment.
**Layout:** TOOL EXIT — visual emphasis (screenshot dominates).
**Speaker alignment:** script → Слайд 49 (ред 549–561).

### Genspark Prompt

```
Create a TOOL EXIT slide dominated by a large screenshot. Background: Mirage #16232A.

Top center, eyebrow, Poppins SemiBold 16pt, Haide Orange, uppercase:
"HAIDE FAN-OUT SCOPE · РЕЗЮМЕ"

Main headline below eyebrow, Poppins Bold 48pt, white #FFFFFF, centered:
"8–12 скрити под-заявки от 1 въпрос"

Below headline, LARGE screenshot placeholder — roughly 60% of slide height. Label: [SCREENSHOT: SS-15 — Haide Fan-Out Scope node graph — 1 central query node, 8–12 sub-query nodes connected by arrows]

Below the screenshot, one punchline line, Poppins Bold 28pt, Haide Orange #FF5B04, centered:
"95% от тях: 0 search volume в Ahrefs / Semrush"

Bottom CTA, Poppins Medium 22pt, Wild Sand #E4EEF0, centered:
"haide.digital/fanout"

CRITICAL: Dark background (Mirage) to make the screenshot pop visually. This is the "wow moment" exit — node graph carries it. Do NOT add bullet list. The 95% line is the only text after the screenshot.
```

---

## SLIDE 50 — Haide Prompt Miner Entry

**Purpose:** Tool #5 entry. Reddit credit visible.
**Layout:** TOOL ENTRY + regex badge.
**Speaker alignment:** script → Слайд 50 (ред 565–587).

### Genspark Prompt

```
Create a TOOL ENTRY slide with regex badge. Background: Deep Sea Green #075056.

Eyebrow, Poppins SemiBold 18pt, Haide Orange, uppercase:
"ИНСТРУМЕНТ 5 ОТ 5"

Main tool name, Poppins Black 96pt, white:
"Haide Prompt Miner"

URL, Poppins Medium 28pt, Haide Orange:
"haide.digital/prompt-miner"

One-line description, Poppins Regular 26pt, Wild Sand:
"Извлича реалните LLM-style prompts от вашия GSC"

Large monospace regex badge (rounded rectangle, Wild Sand bg, Mirage text), centered, JetBrains Mono 28pt:
([^" "]*\s){7,}?

Below the regex badge, small credit line, Poppins Italic 16pt, Wild Sand:
"Credit: Ok_Guidance9952 · r/SEO_LLM"

Bottom tag strip, Poppins SemiBold 16pt, Haide Orange, uppercase:
"ПОКРИВА ТОЧКИ: 29 · 30 · 31 · 32 · 33 · 51 · 53"

CRITICAL: The regex badge is visually distinctive and memorable. The Reddit credit is small but present — ethical attribution shown to the audience.
```

---

## SLIDE 51 — Haide Prompt Miner Exit

**Purpose:** Tool #5 exit. Last tool demo before blok 5.
**Layout:** TOOL EXIT.
**Speaker alignment:** script → Слайд 51 (ред 591–601).

### Genspark Prompt

```
Create a TOOL EXIT slide. Background: Wild Sand #E4EEF0.

Top left, eyebrow, Poppins SemiBold 16pt, Haide Orange, uppercase:
"HAIDE PROMPT MINER · РЕЗЮМЕ"

Main headline, Poppins Bold 44pt, Mirage #16232A:
"Content roadmap за 3 месеца · безплатно"

Below headline, 3 short bullet lines with orange checkmarks, Poppins Medium 24pt, Mirage:
"GSC regex · 7+ words"
"Auto-categorization (how/why/compare)"
"50–200 реални въпроса за 5 минути"

Right side: screenshot placeholder, ~40% width. Label: [SCREENSHOT: SS-16 — Haide Prompt Miner / GSC regex output with example queries]

Bottom CTA, Poppins SemiBold 22pt, Deep Sea Green #075056, centered:
"haide.digital/prompt-miner"

CRITICAL: This is the 5th and final tool exit. The pattern is now fully familiar to the audience. Max 3 bullets.
```

---

## 2.6 Блок 5 — Performance Compressed (Слайд 52)

---

## SLIDE 52 — Block 5 Compressed (7 Points, 1 Slide)

**Purpose:** 7 performance точки в един compressed слайд. Quick review, без tool.
**Layout:** COMPRESSED GRID (2 rows × 4 columns, но 7 cells с 1 празна — или 2x4 grid).
**Speaker alignment:** script → Слайд 52 (ред 609–631).

### Genspark Prompt

```
Create a COMPRESSED CHECKLIST slide. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 44pt, Mirage #16232A:
"Блок 5 · 7 точки в 90 секунди"

Small subtitle below, Poppins Regular 20pt, dark grey:
"Performance & Crawlability · класически SEO foundation"

Below headline, a 2x4 grid (8 cells, 1 left intentionally empty for breathing room). Each populated cell:
- Small orange number circle (40px, Poppins Bold 20pt inside)
- Title, Poppins SemiBold 18pt, Mirage
- ONE supporting line, Noto Sans Regular 14pt, dark grey

Cell 1: "37" · "SSR / SSG" · "AI crawlers не изпълняват JS"
Cell 2: "39" · "Core Web Vitals" · "LCP · INP · CLS (не FID)"
Cell 3: "40" · "TTFB < 200ms" · "бавен = crawl-нат по-рядко"
Cell 4: "43" · "Mobile-first rendering" · "primary mobile от юли 2024"
Cell 5: "44" · "Native lazy loading" · "loading='lazy', не custom JS"
Cell 6: "47" · "Self-referencing canonical" · "на всяка indexable страница"
Cell 7: "48" · "3-click depth, 0 orphans" · "AI crawlers не четат sitemap"
Cell 8 (empty — intentional whitespace)

Bottom of slide, centered, Poppins Italic 18pt, Deep Sea Green:
"Нищо ново. Но без него — нищо друго не работи."

CRITICAL: This slide INTENTIONALLY breaks the "max 3 points per slide" rule because it's a rapid-review moment. 7 cells is max. Make text readable from 3 meters — use size carefully. One empty cell is intentional breathing space.
```

---

## 2.7 Блок 6 — AI Citation Layer (Слайдове 53–55)

---

## SLIDE 53 — Block 6 Divider

**Purpose:** Section divider за финалния блок.
**Layout:** BLOCK SECTION DIVIDER.
**Speaker alignment:** script → Слайд 53 (ред 639–645).

### Genspark Prompt

```
Create a BLOCK SECTION DIVIDER slide. Background: Mirage #16232A.

Centered vertically, left-aligned.

Eyebrow, Poppins SemiBold 18pt, Haide Orange, uppercase:
"БЛОК 6 · 4 ТОЧКИ"

Main headline, Poppins Bold 84pt, white:
"AI Citation Layer"

Subtitle, Poppins Regular 28pt, Wild Sand:
"Последният слой преди да ви видят"

Master QR corner.

CRITICAL: Same lightweight divider pattern as slides 29, 34, 37.
```

---

## SLIDE 54 — Точки 52, 55: Knowledge Graph + Multilingual

**Purpose:** Две най-подценените точки за enterprise брандове.
**Layout:** SPLIT SCREEN.
**Speaker alignment:** script → Слайд 54 (ред 649–667).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical split. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 38pt, Mirage #16232A:
"Без Wikidata = AI entity blind"

LEFT HALF:
Small orange circle: "52"
Title, Poppins Bold 26pt, Mirage:
"Knowledge Graph + Wikidata"

Below title, Poppins Medium 22pt, Mirage:
"Parametric knowledge идва от Wikipedia/Wikidata"

Below that, a warning line, Poppins SemiBold 20pt, Haide Orange:
"Нямате запис → AI моделът не знае, че съществувате"

At bottom, action line, Poppins Italic 18pt, Deep Sea Green:
"30 минути работа. За цял живот."

RIGHT HALF:
Small orange circle: "55"
Title, Poppins Bold 26pt, Mirage:
"Мултиезична консистентност"

Below title, Poppins Medium 22pt, Mirage:
"Един entity · два езика"

Below that, a small visual pair showing two language labels connected by a line, Poppins SemiBold 20pt:
"🇧🇬 Адриан Николов  ←sameAs→  🇬🇧 Adrian Nikolov"

At bottom, action line, Poppins Italic 18pt, Deep Sea Green:
"Една Organization · един @id · два URL"

CRITICAL: The BG/EN pair visualization is the memorable hook for point 55. The Wikidata "30 минути работа" is the action trigger for point 52.
```

---

## SLIDE 55 — Точки 56, 58: VideoObject + Monitoring

**Purpose:** Последните две точки от чеклиста.
**Layout:** SPLIT SCREEN.
**Speaker alignment:** script → Слайд 55 (ред 671–691).

### Genspark Prompt

```
Create a SPLIT SCREEN slide, 50/50 vertical split. Background: Wild Sand #E4EEF0.

Top centered headline, Poppins Bold 40pt, Mirage #16232A:
"Видео четимо · Ръчен monitoring"

LEFT HALF:
Small orange circle: "56"
Title, Poppins Bold 26pt, Mirage:
"VideoObject + transcript"

Below title, a short monospace code snippet box (Mirage bg, rounded, padding 16px), JetBrains Mono 14pt, Haide Orange for key names:

{
  "@type": "VideoObject",
  "transcript": "...",
  "uploadDate": "...",
  "contentUrl": "..."
}

Below code, Poppins Regular 18pt, dark grey:
"Transcript в DOM-а, не заключен в player"

RIGHT HALF:
Small orange circle: "58"
Title, Poppins Bold 26pt, Mirage:
"Manual AI citation monitoring"

Below title, a visual checklist of 5 AI models stacked vertically, each with a small icon placeholder and Poppins Medium 20pt, Mirage:
"ChatGPT"
"Perplexity"
"Claude"
"Gemini"
"Google AIO"

Below the list, Poppins Italic 18pt, Deep Sea Green:
"Един съботен час. Всеки месец. Същите 10 въпроса."

Below that, a small warning line, Poppins SemiBold 16pt, Haide Orange:
"Не плащайте за SaaS преди 3 месеца ръчен baseline"

CRITICAL: Left side has a real code snippet (short, readable). Right side has 5 model names in a simple list. The monthly ritual description is the action anchor.
```

---

## 2.8 Заключение на Част 2 (Слайдове 56–57)

---

## SLIDE 56 — "20 от 60" Summary

**Purpose:** Numeric summary of what was covered. QR reminder.
**Layout:** STAT HERO (3 stats) + QR.
**Speaker alignment:** script → Слайд 56 (ред 699–709).

### Genspark Prompt

```
Create a STAT HERO slide with QR sidebar. 70/30 vertical split. Background: Wild Sand #E4EEF0.

LEFT (70% width):
Top centered eyebrow, Poppins SemiBold 18pt, Haide Orange, uppercase:
"РЕЗЮМЕ НА ЧАСТ 2"

Three large stats stacked vertically with large whitespace between, each aligned consistently:

Stat 1:
Number: Poppins Black 140pt, Haide Orange #FF5B04:
"20 / 60"
Caption: Poppins Medium 24pt, Mirage:
"точки от чеклиста"

Stat 2:
Number: Poppins Black 140pt, Deep Sea Green #075056:
"5 / 5"
Caption: Poppins Medium 24pt, Mirage:
"инструмента"

Stat 3:
Number: Poppins Black 140pt, Mirage #16232A:
"6 / 6"
Caption: Poppins Medium 24pt, Mirage:
"тематични блока"

RIGHT (30% width, background Deep Sea Green #075056):
Large QR centered, ~60% of right section height. White QR on Deep Sea Green.
Below QR, Poppins Medium 22pt, Haide Orange, centered:
"haide.digital/masterclass-2026"
Below that, Poppins Regular 16pt, Wild Sand:
"Другите 40 точки + 5 инструмента"

CRITICAL: Three stats stacked, each with a distinct color. The 20/60 is the anchor. Right-side QR is enlarged (like Slide 28) — this is the third scan moment.
```

---

## SLIDE 57 — Transition към Част 3

**Purpose:** Bridge към Часть 3 — monitoring + survival. Teases volatility questions.
**Layout:** TRANSITION (black background, single sentence).
**Speaker alignment:** script → Слайд 57 (ред 713–725).

### Genspark Prompt

```
Create a TRANSITION slide. Full-bleed background: Mirage #16232A (near-black).

Centered vertically.

Small eyebrow, Poppins SemiBold 18pt, Haide Orange #FF5B04, uppercase:
"ЧАСТ 3 · MONITORING & SURVIVAL"

Main sentence below, Poppins Medium 56pt, white #FFFFFF, centered:
"Знаете какво да направите."
"Остава да оцелеете волатилността."

Below that, larger whitespace, then one small teaser line, Poppins Italic 22pt, Wild Sand:
"Signal Architecture — следва."

Master QR corner (white on transparent).

CRITICAL: Maximum simplicity. This is the same transition pattern as Part 1 slide 3 — pure beat of silence. The two-line sentence must breathe. No decorative elements.
```

---

# SPLIT DECISIONS LOG (Part 2)

Няма нови split решения за Part 2 — скриптът вече беше написан с разумни slide boundaries. За разлика от Part 1 (където 3 слайда бяха сплит-нати), тук всеки slide има единствена core idea от начало.

**Slide count break-down:**
- Opening: 2 слайда (27, 28)
- Блок 1 HTML Infrastructure: 5 слайда (29, 30, 31, 32, 33)
- Блок 2 Structured Data: 3 слайда (34, 35, 36)
- Блок 3 AI Crawler Access: 5 слайда (37, 38, 39, 40, 41)
- Блок 4 Content Architecture (CENTRAL): 10 слайда (42, 43, 44, 45, 46, 47, 48, 49, 50, 51)
- Блок 5 Performance (compressed): 1 слайд (52)
- Блок 6 AI Citation Layer: 3 слайда (53, 54, 55)
- Заключение + transition: 2 слайда (56, 57)

**Total: 31 слайда за ~30 мин = средно ~58 сек/слайд.** По-бързо от Part 1 (76 сек/слайд) защото 7 минути се изяждат от live browser demos (7 мин ÷ 5 demos ÷ 2 (entry+exit slides) = demos отнемат време извън слайдовете).

---

# VISUAL PATTERNS REFERENCE (за continuity в Part 3)

Part 2 въвежда 3 нови repeatable patterns, които Part 3 може да използва при нужда:

1. **TOOL ENTRY pattern** (слайдове 32, 40, 46, 48, 50):
   - Background: Deep Sea Green #075056
   - Eyebrow: "ИНСТРУМЕНТ X ОТ 5"
   - Hero name: Poppins Black 96pt white
   - URL: Poppins Medium 28pt Haide Orange
   - 1-line description: Poppins Regular 26pt Wild Sand
   - Bottom tag strip: "ПОКРИВА ТОЧКИ: ..."

2. **TOOL EXIT pattern** (слайдове 33, 41, 47, 49, 51):
   - Background: Wild Sand #E4EEF0 (or Mirage for dramatic exits like 49)
   - Eyebrow: "TOOL NAME · РЕЗЮМЕ"
   - Headline: what they saw
   - 3 bullets OR large screenshot (not both)
   - Right-side screenshot placeholder
   - Bottom CTA with URL

3. **BLOCK SECTION DIVIDER pattern** (слайдове 29, 34, 37, 42, 53):
   - Background: Mirage #16232A (or Haide Orange for central block — slide 42 is unique)
   - Eyebrow: "БЛОК X · Y ТОЧКИ"
   - Headline: Poppins Bold 84pt white
   - Subtitle: one catchy phrase
   - Max 3 text elements

---

# VERIFICATION CHECKLIST ПРЕДИ ГЕНЕРИРАНЕ

- [ ] Global Style Brief от Part 1 е още активен в deck settings (не се paste-ва отново).
- [ ] Тези 31 слайда се добавят към **същия** Genspark deck от Part 1 — не нов deck.
- [ ] Slide numbers 27–57 съответстват на slide numbers в `script-part2-checklist-and-tools.md`.
- [ ] Anti-crowding reminder присъства в КАЖДА prompt.
- [ ] Само 4 цвята (#FF5B04, #075056, #E4EEF0, #16232A). Изключение: слайд 42 (Haide Orange full-bleed — intentional visual marker за central block).
- [ ] 7 screenshot placeholders (SS-10 до SS-16) маркирани правилно.
- [ ] Master QR corner продължава от Part 1 (bottom-right на всеки слайд).
- [ ] Enlarged QR moments: slides 28 + 56 (2 scan reminders в Part 2).
- [ ] Всички 5 tool-а с `Haide` prefix: Ceiling, Bot Radar, Ski Ramp, Fan-Out Scope, Prompt Miner.
- [ ] 5 TOOL ENTRY slides + 5 TOOL EXIT slides = 10 tool slides общо.
- [ ] Code snippets: 2 слайда (35 и 55) — monospace JetBrains Mono, Haide Orange за keys.
- [ ] Slide 42 е единствения оранжев full-bleed divider (marks Block 4 като central).
- [ ] Slide 48 (Fan-Out Scope Entry) има visible LIVE VOLUNTEER badge.
- [ ] Slide 50 (Prompt Miner Entry) има regex badge + Reddit credit.

---

# СЛЕДВАЩИ СТЪПКИ

1. **Отвори същия Genspark deck от Part 1.**
2. **Добави slides 27–57** като нови slides към deck-а — не създавай нов проект.
3. **Слайд по слайд** — copy-paste Genspark Prompt блок, generate, review.
4. **Когато нещо е claustrofobично** — кажи на Genspark "remove X, more whitespace" или split-вай на 2 слайда.
5. **Screenshot capture session** — 7 нови screenshots (SS-10 до SS-16) ТРЯБВА да се направят преди rehearsal.
6. **Когато Part 2 е approved визуално** — minаваме към Part 3 (monitoring stack + survival workflow, ~15 слайда, ~30 мин).

**Очакван финален deck след Part 2:** 57 слайда (Part 1: 26 + Part 2: 31). След Part 3 ще е ~72 слайда за 90 мин = ~1:15 мин/слайд. Professional pace.
