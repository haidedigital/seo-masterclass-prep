# Мастърклас „Техническо SEO в AI ерата" — 90-минутна структура + walk-through на чеклиста + 5 брандирани инструмента

## Context

На 23 април 2026 Адриан Николов изнася 90-минутна лекция (слот 11:45–13:15) на Enterprise Magazine × EURODEA SEO Marketing Masterclass в София. Аудитория: ~15–20 mid-level маркетолози + enterprise stakeholders от eCommerce и SaaS (вкл. IKEA, Lidl регионални представители). Цена на билет: 145 EUR. Адриан говори след Мартин Желязков (GEO философия, 10:00–11:30) и преди Борислав Дончев (E-E-A-T + AI spam), което означава че неговият слот трябва да е **техническият имплементационен пласт** между двете.

Мастъркласът е **промотиран като minване през техническия чеклист** — това е обещанието към аудиторията. Част 2 не може да е separate tool demos; трябва да е walk-through на ключовите точки от съществуващия 60-точков чеклист ([masterclass-prep/masterclass-prep-50-point-checklist.md](masterclass-prep/masterclass-prep-50-point-checklist.md)), където инструментите са **вплетени в точките** като начин за автоматична проверка, а не като отделни презентации.

Решения потвърдени от брифа:
- **Език:** всичко на български (слайдове, скрипт, handout)
- **Live demo:** изцяло на живо (максимален wow factor, risk tolerance приет; backup файлове се подготвят но не се показват)
- **Част 3:** Monitoring stack + workflow (конкретна blueprint архитектура за волатилна среда)
- **Инструменти (5):** Query Fan-Out Simulator, AI Crawler Log Analyzer, 2MB Ceiling + Schema Sanity, Answer Capsule Score (Ski-Ramp), **GSC Prompt Miner (нов, добавен след ревизия)**
- **Част 2:** walk-through на ~20 ключови точки от чеклиста с инструменти вплетени in-flow — не separate tool demos

---

## Нова 90-минутна структура

### ЧАСТ 1 — „Как наистина работят AI системите" (30 мин)

Цел: даваме правилния mental model за retrieval → ranking → citation pipeline на ChatGPT, Claude, Perplexity и Google AI Mode / AI Overviews. Без това, всяка точка от чеклиста в Част 2 звучи произволна. С това — всяка точка става следствие от конкретен pipeline stage.

**1.1 Cold open (3 мин) — „Правилата за видимост се раздвоиха"**
- LinkedIn screenshot + Google Search Central блог пост от 31 март 2026 (2MB HTML лимит, WRS statelessness)
- Ключово твърдение: Google ви казва честно какво може и какво не. AI моделите не — просто не ви цитират.
- Stat hook: „42.6% спад в LLM referral traffic от юли 2025 (Kevin Indig, Growth Memo). И все пак цитираните брандове имат 35% по-висок organic CTR и 91% по-висок paid CTR."
- Обещание: „Ще ви дам 5 безплатни инструмента, чеклиста, мониторинг архитектура и конкретен workflow. Всичко днес. QR кодът ви води до всичко."

**1.2 ChatGPT pipeline (7 мин) — „Класификатор → fan-out → retrieval → re-ranking → citation"**
- 5-стъпковият pipeline с визуална диаграма (използваме `_knowledge/retrieval-infrastructure/retrieval-infrastructure.md` framework)
- Ключови числа: 31% search trigger rate (Nectiv, 8,500 prompts study), fan-out дълбочина 2.17 (GPT-5.3) → 8.5× повече fan-outs при GPT-5.4, средна дължина на fan-out query 5.5 думи
- GPT-5.3 vs GPT-5.4 разликата (Writesonic, Samanyou Garg, March 9 2026): 92% third-party vs 56% brand-website citations. Само **7% overlap** между двете → вашият безплатен и вашият Pro потребител виждат **два различни интернета**.
- Shocking finding: **75% от GPT-5.4 цитиранията НЕ се появяват в Google/Bing organic** за същата заявка (Writesonic). Класирането на №1 в Google не гарантира цитиране.
- Източници: Writesonic, Nectiv Digital (Chris Long), Chris Green (SonicBerry middleware post, chris-green.net).

**1.3 Google AI Mode / AI Overviews pipeline (7 мин)**
- Gemini 3 като default за AI Overviews (януари 2026). 70%+ от searches показват AIO.
- Query fan-out: 9.06 средно per prompt (Nectiv), софтуерни вертикали 11.7, Gemini 3 ъпгрейд до 10.7 (Seer Interactive, Nick Haigler March 2026)
- **95% от fan-out queries имат 0 search volume** → long-tail hyper-specificity. Тук влиза GSC regex trick-а (препратка към Част 2, tool #5).
- E-E-A-T като binary gate: 96% от цитиранията минават прага (ziptie.dev).
- Връзка с organic: 38% от AIO цитирания идват от топ 10 Google, но **80% от AI-cited URLs не са в топ 100**.
- Lily Ray finding: алгоритмични ъпдейти корелират — -26.7% organic, -22.5% AIO, -23.8% AI Mode. Perplexity често divergе positively.

**1.4 Perplexity + Claude pipeline (7 мин)**
- Perplexity: 6-етапен RAG (Sonar models), 8–12 цитирания per response (vs ChatGPT 2–4). Dual-signal freshness (article:modified_time + visible HTML timestamp = +23% visibility, Harbor SEO).
- Claude web search (Brave Search API): inline citations, 3–5 домейна per response. Приоритизира „safety, neutrality, authority, usefulness" — deprioritiza marketing език („best-in-class", „game-changing"). Източници: Infrasity (how-to-rank-in-claude-practices-tips), Trakkr.
- Key insight за enterprise: Claude има 45% от enterprise AI spend (януари 2026), OpenAI надолу от 90% до 68%. Ако таргетирате B2B/enterprise, само-ChatGPT е 60% стратегия. (First Page Sage, April 2026 market share report)

**1.5 Общи паттърни през четирите системи (6 мин) — директна връзка към чеклиста**
- **Answer capsules** — 72.4% от цитираните страници имат 40–60 думи директен отговор, 90%+ link-free. Най-силен единичен предиктор. → Чеклист точка 29, 51.
- **Ski ramp distribution** — 44.2% от цитиранията от първите 30% на съдържанието (Kevin Indig, 3M responses). → Чеклист точка 29, 51.
- **Proper noun density** — оптимално 20.6% (vs 5–8% typical text). → Чеклист точка 30.
- **Flesch-Kincaid grade 16** оптимален. → Чеклист точка 33.
- **Tables** — ChatGPT цитиранията 2.3× по-вероятно имат таблица (Nectiv November 2025, 33% vs 13%).
- **Entity-first writing** („Haide Digital е…" бие „Ние сме…") — Чеклист точка 30.
- Прехвърляне: „Всичко това е в чеклиста, който ще получите сега. Нека минем през най-важните точки — и по пътя ще ви покажа 5 инструмента, които автоматизират проверката."

---

### ЧАСТ 2 — „Walk-through на чеклиста с инструменти за автоматизация" (30 мин)

**Принцип:** Не 60 точки. Избрани **20 най-important** точки, групирани в 6 тематични блока по реда на чеклиста. За всяка точка: (а) защо е важна — връзка с Част 1 pipeline, (б) как се проверява ръчно, (в) Haide инструмент който автоматизира проверката (когато има такъв).

Handout (A4 сгъната до A5, двустранна, с QR към дигитална версия) се раздава **в началото на Част 2**, не в края. Съдържа пълните 60 точки + QR код към `haide.digital/masterclass-2026` с 5-те инструмента.

**2.1 Контракт с аудиторията (1 мин)**
„Раздавам ви чеклиста сега. Няма да четем 60 точки — ще минем през 20 най-важни. Имате пълните 60 в ръцете си за вкъщи. И ще ви дам 5 инструмента, които автоматизират проверката на 85% от чеклиста."

**2.2 Блок 1 — HTML инфраструктура (5 мин, точки 1, 2, 3, 4, 6)**
- **Точка 1 — HTML под 2MB некомпресирано.** Защо: Google WRS тихо отрязва всичко след 2MB. Как се проверява: Chrome DevTools → Network → колона „resource" (НЕ „transferred"). Pitfall: gzip/Brotli не помагат тук.
- **Точка 2 — Критично съдържание в първите 2MB.** Ручан View Source тест.
- **Точка 3 — JSON-LD в `<head>`, не в footer.**
- **Точка 4 — Meta tags, title, canonical високо в `<head>`.**
- **Точка 6 — Екстернализиран JS.** Inline JS bundles са причина №1 за HTML раздуване в модерните SPA.

**👉 Live demo: Tool #1 — Haide Ceiling (2MB HTML Budget Checker + Schema Sanity)**
- URL: `haide.digital/ceiling`
- Какво прави: въвеждаш URL → crawl-ва raw HTML → (а) uncompressed size vs 2MB cutoff, (б) позиция на meta/title/canonical/JSON-LD спрямо 2MB boundary, (в) schema validness + missing AI-critical properties (Organization sameAs, Product hasMerchantReturnPolicy, Article author+dateModified).
- Output: светофар + конкретен fix snippet за copy-paste.
- Live demo: Адриан иска URL от залата. Ако IKEA/Lidl volunteer — бинго. Иначе pre-selected БГ eCommerce сайт от HTTP Archive.
- Имплементация: reuse `products/haide-seo-crawler` crawl engine + DataForSEO `on_page_content_parsing` + Schema.org validator API. **80% вече съществува.**

**2.3 Блок 2 — Structured Data за AI entity layer (4 мин, точки 11, 13, 14, 35)**
- **Точка 11 — Organization schema с пълен sameAs граф.** Защо: AI моделите решават кого да цитират през parametric knowledge + real-time retrieval. Entity recognition минава през sameAs. Задължителни: Wikipedia, Wikidata, Crunchbase, LinkedIn, GitHub Org, YouTube канал.
- **Точка 13 — Article/BlogPosting с author, dateModified.** AI тежко tежи authorship сигналите при решения за цитиране.
- **Точка 14 — Product schema разширено за 2026.** Базово Product schema вече НЕ стига. ChatGPT Shopping, Gemini Shopping, Perplexity извличат: `hasMerchantReturnPolicy` (MerchantReturnPolicy), `shippingDetails` (OfferShippingDetails), `priceValidUntil`, `itemCondition`. Без тях — невидим.
- **Точка 35 — Author страници с Person schema + sameAs към LinkedIn, ORCID, Wikipedia, Scholar.** E-E-A-T минава през verified author entity.

Tool #1 (Ceiling) вече покрива schema валидация — кратък повторен flash на demo-то.

**2.4 Блок 3 — AI crawler достъп (4 мин, точки 19, 20, 25, 26)**
- **Точка 19 — 13-те user-agents за 2026.** Пълен списък на слайд (от чеклиста): GPTBot, OAI-SearchBot, ChatGPT-User, ClaudeBot, Claude-SearchBot, Claude-User, PerplexityBot, Perplexity-User, Google-Extended, Google-Agent, Applebot-Extended, CCBot, MistralAI-*.
- **Точка 20 — Не блокирайте GPTBot, OAI-SearchBot, ClaudeBot.** Веднъж блокирани → губите дългосрочно място в parametric knowledge.
- **Точка 25 — User-triggered fetchers игнорират robots.txt.** ChatGPT-User, Claude-User, Perplexity-User, Google-Agent — не можете да ги блокирате. Стратегия: оптимизирайте ЗА тях.
- **Точка 26 — Мониторирайте AI crawler трафика в server logs.** Ранна предупредителна система.

**👉 Live demo: Tool #2 — Haide Bot Radar (AI Crawler Log Analyzer)**
- URL: `haide.digital/bot-radar`
- Какво прави: upload server log (Apache/Nginx формат) → парсва и класифицира всички 13 user-agents → честота, покритие, дълбочина, response times + **„AI dark matter" списък** (страници които нито един AI crawler не е посещавал през последните 90 дни).
- Live demo: използваме pre-uploaded anonymized лог от Haide client (~20MB). Upload reveal на живо, но файлът е избран предварително. Обосновка: 20MB upload на сцена с conference Wi-Fi = времево-рисково.
- Имплементация: преизползва `log_analyzer` service от `products/haide-seo-crawler`. **80% готов.**

**2.5 Блок 4 — Content architecture за AI citation (8 мин, точки 29, 30, 31, 32, 33, 51, 53) — CENTRAL BLOCK**
Това е най-важният блок от Част 2. Тук са двата най-силни инструмента.

- **Точка 29 — Директен отговор в първите 50–70 думи (ski ramp).** Не 200 думи. Kevin Indig data: 44.2% цитирания от първите 30% на страницата.
- **Точка 30 — Entity-first писане.** „Haide Digital е organic growth engineering компания, базирана в София, България" vs „Ние сме…". AI моделите нужно недвусмислени entity референции.
- **Точка 31 — Статистически твърдения с източници.** Моделът „Според [източник], [твърдение]" се цитира повече.
- **Точка 32 — Уникално изследване, first-party данни.** AI предпочита оригинални източници пред агрегатори.
- **Точка 33 — Изчерпателно топикално покритие.** Клъстер от дълбоко свързано съдържание = authority сигнал.
- **Точка 51 — AIO source selection optimization.** Front-loaded answers, passage-level структуриране.
- **Точка 53 — Semantic chunking за RAG.** Всеки H2/H3 блок трябва да стои сам без предходен контекст. Pronoun references между секции = счупени chunks.

**👉 Live demo: Tool #3 — Haide Ski Ramp (Answer Capsule Score)**
- URL: `haide.digital/ski-ramp`
- Какво прави: URL input → fetch + parse → визуализира (а) плътност на potentially-citeable passages по позиция — histogram „ски рампа", (б) answer capsule detection (има ли 40–60-думен link-free блок в първите 150 думи?), (в) proper noun density %, (г) Flesch-Kincaid grade, (д) table presence. Citation-Readiness Score 0–100 + конкретна препоръка за rewrite.
- Live demo: два URL-а паралелно — цитиран в AI vs не-цитиран. Видим контраст. Audience „aha" момент.
- Имплементация: Python backend с readability + spaCy NER + custom citation-capsule detector. **Най-много нова работа (ново репо: `products/haide-ski-ramp/`).**

**👉 Live demo: Tool #4 — Haide Fan-Out Scope (Query Fan-Out Simulator) — HEADLINE DEMO**
- URL: `haide.digital/fanout`
- Какво прави: въвеждаш query → backend вика OpenAI Responses API (Chris Long / Nectiv методология, March 2026) + Gemini fan-out extraction → визуализира реалните fan-out sub-queries в node граф.
- Live demo script: volunteer от залата дава query за техния бранд/продукт (напр. „най-добрата ERP система за верига магазини"). Адриан показва 8–12 скрити sub-queries, които ChatGPT/Gemini реално пускат. Прозорец към „черната кутия" на AI. **Най-зрелищният момент на мастъркласа.**
- Превключва разговора: „Виждате ли колко от тези sub-queries не знаете че съществуват? Това не са маркетингови предположения — това са реалните търсения. А сега ще ви покажа нещо още по-силно: как да ги намерите от собствените си GSC данни, безплатно."
- Имплементация: ново репо `products/haide-fanout-scope/`, базирано на Chris Long Python script + Seer Interactive fan-out methodology (Nick Haigler, March 2026). FastAPI backend, Next.js frontend с React Flow за node граф визуализация.

**👉 Live demo: Tool #5 — Haide Prompt Miner (GSC Regex Extractor) — НОВО, КРИТИЧНО**
- URL: `haide.digital/prompt-miner`
- Базис: Reddit пост на Ok_Guidance9952, r/SEO_LLM, „Stop guessing what users ask AI. Here is a GSC Regex to find real LLM-style prompts", ~2 месеца преди event-а.
- **Regex-ът:** `([^" "]*\s){7,}?` — филтрира queries с 7+ думи в GSC → Performance → Query → Filter → Custom (Regex).
- Защо работи: потребителите все повече третират Google като LLM. Queries от 7+ думи са „natural language prompts" — най-близкият набор данни до реални chatbot логове, който имате. Не виждате head terms, виждате *проблеми*.
- Примери които изскачат (от Reddit поста): „how to migrate from hubspot to salesforce without data loss", „stripe webhook error signature verification failed", „best alternative to intercom for b2b saas with small team" — вместо generic „CRM software".
- **Какво прави Haide Prompt Miner tool-а:** (а) стъпка-по-стъпка guided UI или Google Sheets / Looker Studio template с pre-filled regex, (б) вариации 5/7/9 думи tabs (7 е sweet spot), (в) auto-categorization — как/защо/сравнение/грешка/миграция buckets, (г) export към content brief template с топ 10 prompt clusters и препоръчани FAQ/HowTo/Comparison schemas за всеки.
- Live demo: Адриан отваря GSC на Haide Digital, прилага regex-а, показва реални 7+ дума queries + кратко live категоризиране. „Това не са теоретични prompts. Това е вашият CRM, превърнат в chatbot лог."
- Покрива чеклист точки: 29 (direct answer), 30 (entity-first), 31 (източници), 32 (уникални данни), 33 (topical authority), 51 (AIO source selection), 52 (Knowledge Graph presence), 53 (semantic chunking).
- Имплементация: **най-лесен от 5-те** — Google Sheets template с pre-filled regex + Looker Studio dashboard template + 1-страничен HTML landing page с copy-paste regex. Нулев backend. Може да е готов за 1 ден работа.
- Credit attribution: източник линк към Reddit поста в tool UI footer + в handout-а (Haide дава credit, не краде идеята).

**2.6 Блок 5 — Performance & crawlability (кратко, 3 мин, точки 37, 39, 40, 43, 44, 47, 48)**
Бърз преглед за complete-ност; няма tool demo в този блок (tools #1 и #2 го покриват).
- **Точка 37 — SSR/SSG.** AI crawlers НЕ изпълняват JavaScript.
- **Точка 39 — Core Web Vitals (LCP, INP, CLS).** Бързи сайтове се crawl-ват по-често.
- **Точка 43 — Mobile-first verified.** Googlebot е primarily mobile от юли 2024.
- **Точка 48 — 3-click depth, нула orphan страници.** Orphans разчитат на sitemap за откриване, но AI crawlers рядко ползват sitemaps.

**2.7 Блок 6 — AI Citation Layer (Категория 7, 4 мин, точки 52, 55, 56, 58)**
- **Точка 52 — Brand entity в Knowledge Graph и Wikidata.** Wikidata запис с пълни properties. Без това — класиране №1 не гарантира цитиране.
- **Точка 55 — Мултиезична entity консистентност (критично за БГ пазара).** Organization schema с един и същ @id в BG и EN версиите. „Адриан Николов"/„Adrian Nikolov" свързани през Person sameAs.
- **Точка 56 — VideoObject + crawlable transcript.** Заключени transcripts = невидими за AI.
- **Точка 58 — AI citation monitoring (директно питане).** Ежемесечен ръчен тест. Не плащайте за „AI visibility" SaaS преди 3 месеца ръчен baseline.

**2.8 Заключение на Част 2 (1 мин)**
„Минахме 20 от 60-те точки. Останалите 40 са в handout-а. Петте инструмента автоматизират 85% от проверката. Всичко безплатно, без регистрация. QR кодът на гърба на handout-а води до `haide.digital/masterclass-2026`. Защо правим това безплатно? Защото Organic Growth Engineering не работи ако не разберете проблема първо. Сега да поговорим как да построите система, която оцелява волатилността."

---

### ЧАСТ 3 — „Monitoring stack + workflow за волатилна среда" (30 мин)

Цел: Част 1 дава mental model. Част 2 дава чеклист + инструменти за днес. Част 3 дава **архитектура, която оцелява volatility**. Тактиките се менят седмично — системата трябва да е стабилна.

Водеща теза: „Не можеш да оптимизираш за модел, който се update-ва всеки месец. Но можеш да построиш система, която те алармира когато правилата се променят — и ти дава данни да реагираш за 48 часа."

**3.1 Принципът на двойния бюджет (3 мин)**
- „SEO budget" vs „GEO observability budget" — два отделни line items в маркетинг бюджета на 2026.
- За enterprise: GEO observability = 15–20% от SEO бюджета.
- За SMB: започвате с безплатни инструменти + 2 часа седмично ръчен мониторинг (3 месеца преди SaaS).

**3.2 Monitoring Stack архитектура (12 мин) — конкретна blueprint**
Пет лаера, показани като диаграма на един слайд + експанзия на всеки:

**Лаер 1 — AI Citation Tracking (седмичен):**
- Ръчен (безплатно): Notion template с 20 brand/product queries × 5 платформи (ChatGPT, Claude, Perplexity, Gemini, Google AIO). Screenshots + logging. 3 месеца минимум baseline.
- Автоматизиран (paid, с резерва): Profound, SERanking AI Visibility, Otterly, Peec AI — все още ранни, не плащайте преди ръчен baseline.
- **Връзка с Tool #5 (Prompt Miner):** GSC regex queries стават вашите тестови queries за AI platforms — ясно, defensible tracking set.

**Лаер 2 — Server Log Ingestion (ежедневен):**
- n8n workflow → cron → парсва Nginx/Apache → ELK / BigQuery / ClickHouse
- Alerts: нов AI crawler появил се, съществуващ спрял, error rate >5%, 4xx/5xx на страници които crawlers посещават
- Безплатна алтернатива: GoAccess (open source) + weekly email report
- **Връзка с Tool #2 (Bot Radar):** weekly upload и сравнение за нови crawler user-agents

**Лаер 3 — Content Freshness + GSC Prompt Mining (седмичен):**
- GSC API export (автоматизиран) → прилага GSC regex от Tool #5 автоматично
- Детектира нови 7+ word queries седмично → flag като content opportunities
- Correlation check: кои 7+ word queries вече ранжират vs кои не → content gaps
- Ahrefs/Semrush API за позиции dropping без обяснение
- Корелация с Layer 1 AI citation loss → вероятно algorithmic update

**Лаер 4 — Schema + 2MB Regression Guard (CI/CD):**
- GitHub Action / Vercel build step → Schema.org validator API + HTML size check
- Block deploy ако > 1.5MB или schema break
- Haide публикува тази GitHub Action като open source gist (handout mention + QR)

**Лаер 5 — Entity Graph Health (месечен):**
- Cron job проверява sameAs на Organization + Person schema
- Wikidata / Wikipedia / Crunchbase / LinkedIn / GitHub 200 OK
- Алерт при счупен entity граф → AI доверието се срива тихо

Слайд: едностраничен архитектурен диаграм с 5-те лаера + кои от Haide tools влизат в кои лаер.

**3.3 Workflow за реакция при промени (7 мин)**
- **48-часово правило:** всяка голяма AI промяна (модел update, Google Core Update, нов crawler) → в 48ч имаш първоначална data snapshot
- **7-дневен review cycle:** всеки понеделник екипът гледа 5-те лаера, идентифицира 1–2 action items
- **30-дневен audit:** пълен преглед на чеклиста спрямо нови developments
- **Quarterly playbook refresh:** content strategy rewrite базиран на Kevin Indig, Chris Long, Seer Interactive, iPullRank публикации
- Live show: Notion template + GitHub repo с sample n8n workflow JSON.

**3.4 Information diet за SEO leads в 2026 (5 мин)**
Задължително следене (безплатно):
- Kevin Indig Growth Memo (weekly), Chris Long Nectiv Digital, Lily Ray Substack, ziptie.dev, Seer Interactive insights, iPullRank, Dan Petrovic Dejan.ai, Search Engine Land, Google Search Central Blog, OpenAI/Anthropic/Perplexity официални docs
- RSS агрегатор: Feedly Pro или Inoreader (безплатен)
- Twitter/X list: ~15 practitioners (Chris Long, Kevin Indig, Aleyda Solis, Lily Ray, Dan Petrovic, Andrea Volpini, Jes Scholz, Mike King iPullRank, Samanyou Garg Writesonic…)

Какво да игнорирате: „AI SEO" thought leaders без original research, LinkedIn hot takes без data, agency blog posts които рециклират същите 5 stats.

**3.5 Call to action + close (3 мин)**
- „Инструментите са ваши. Чеклистът е ваш. Мониторинг архитектурата е ваша. Какво остава? Имплементацията."
- Soft offer: безплатен 30-мин Growth Gap Review за всички в залата (QR код → calendar). Без product pitch — чист data walkthrough.
- Balkan eCommerce Summit реф: „Намерете ни на щанд 97 следващата седмица."
- Последно изречение: **„Get Found. Stay Visible. Но този път — навсякъде."**

---

## Критични файлове и активи

### Съществуващи (reference only)
- [events/enterprise-masterclass-2026/masterclass-prep/masterclass-prep-50-point-checklist.md](events/enterprise-masterclass-2026/masterclass-prep/masterclass-prep-50-point-checklist.md) — съществуващ 60-точков чеклист, базата за Част 2 walk-through
- [_knowledge/skills/GEO_SGO.md](_knowledge/skills/GEO_SGO.md) — Haide GEO стратегически framework
- [_knowledge/retrieval-infrastructure/retrieval-infrastructure.md](_knowledge/retrieval-infrastructure/retrieval-infrastructure.md) — RAG pipeline framework (Част 1 визуален explainer)
- [products/haide-seo-crawler/docs/playbooks/03_GEO_Audit_Methodology.md](products/haide-seo-crawler/docs/playbooks/03_GEO_Audit_Methodology.md) — база за Част 3 monitoring blueprint
- [_knowledge/company-info/adrian-profile.md](_knowledge/company-info/adrian-profile.md) — voice & style reference

### За създаване (нови файлове/репа)

**Slide deck и speaker notes:**
- `masterclass-prep/slides/outline.md` — slide-by-slide outline (~55 слайда за 90 мин)
- `masterclass-prep/slides/speaker-notes.md` — пълен БГ скрипт за всеки слайд
- Финален формат: Keynote или PowerPoint, експортиран към PDF за partner distribution

**Handout:**
- `masterclass-prep/handout/handout-a4-folded.md` — двустранен A4→A5
- `masterclass-prep/handout/handout-print-ready.pdf` — за печат (15–20 копия + резерв)
- QR код към `haide.digital/masterclass-2026` landing page

**Haide инструменти (5):**
1. `products/haide-fanout-scope/` — ново репо; OpenAI Responses API + Gemini fan-out extractor; FastAPI + Next.js + React Flow
2. `products/haide-seo-crawler/tools/ceiling-checker/` — нов tool в existing crawler; reuse engine + schema validator
3. `products/haide-seo-crawler/tools/bot-logs-radar/` — нов tool; reuse `log_analyzer` service
4. `products/haide-ski-ramp/` — ново репо; Python (readability + spaCy NER) + React frontend; citation-capsule detector
5. `products/haide-prompt-miner/` — ново репо, **най-лесно**; Google Sheets template + Looker Studio dashboard + 1-страничен HTML landing с copy-paste regex `([^" "]*\s){7,}?` + guided steps; credit линк към Reddit източника

**Monitoring blueprint (Част 3 giveaway):**
- `products/haide-monitoring-stack/` — публичен GitHub repo: n8n workflow JSON, GitHub Action template, Notion template link, GoAccess конфиг
- README в БГ + EN

**Landing page:**
- `website/app/masterclass-2026/page.tsx` — нова страница на `haide.digital/masterclass-2026`: 5-те инструменти като cards, пълен 60-точков чеклист (embedded), slides PDF download, monitoring stack GitHub link, Growth Gap Review CTA

---

## Реиспользване на съществуващи Haide активи

Съгласно workspace audit:
- **`products/haide-seo-crawler/`** — production-ready FastAPI + Next.js система с: async crawl engine, JS SEO detection (raw HTML vs rendered DOM), schema detection, log analyzer с bot detection, GEO readiness scoring (Claude-powered), semantic clustering (sentence-transformers + FAISS), white-label report generation.
  - Tool #2 (Ceiling) и Tool #3 (Bot Radar): 80% reuse.
  - Tool #4 (Fan-Out Scope) и Tool #5 (Ski Ramp): използват crawler API pattern + нова logic.
  - Tool #5 (Prompt Miner): не изисква crawler, най-simple (Sheets/Looker).
- **`_knowledge/retrieval-infrastructure/`** → визуална диаграма за Част 1
- **`website/`** design system → консистентен UI за 5-те tool landing pages

---

## Верификация (end-to-end)

**Преди 10 април 2026 (rehearsal + video record deadline):**

1. **Slide deck review:** end-to-end четене на 55 слайда, cross-check всяко stat с URL + дата. Всички claims от Част 1 да имат източник footnote. **Oracle review pass задължителен.**

2. **Инструменти smoke tests:**
   - **Tool #1 (Ceiling):** test с 3 URL (малък ~50KB, голям eCommerce ~800KB, умишлено счупен с inline JSON >2MB). Expected: светофар + fix snippet.
   - **Tool #2 (Bot Radar):** upload sample Nginx log (anonymized Haide client, ~20MB). Expected: dashboard с 13 user-agents + „AI dark matter" списък.
   - **Tool #3 (Ski Ramp):** 3 test URL (добър answer capsule, без, listicle). Expected: histogram + score + rewrite препоръка.
   - **Tool #4 (Fan-Out Scope):** query „най-добра ERP за верига магазини". Expected: 8–12 sub-queries, node graph render < 3s, no API errors.
   - **Tool #5 (Prompt Miner):** Haide Digital GSC account → prилагане на regex → expected: видими 7+ word queries, guided steps работят end-to-end.

3. **Live demo rehearsal:** минимум 2 пълни run-through, хронометър. Част 2 демоси с реален Wi-Fi (не офис) — симулация на conference conditions.

4. **Backup pack (не за показване, а exit ramp):**
   - Screencasts на всички 5 tool demos в 4K
   - Screenshot fallback pack (PDF)
   - Pre-filled test queries и pre-cached API responses
   - Второ устройство с инструментите вече отворени

5. **Handout print proof:** финал на A4 → сгъната до A5 → четимост на 30см разстояние, QR кодове тествани с 3 различни телефона.

**На 23 април 2026 (event day):**

6. **Wi-Fi backup:** 5G hotspot от Адриан + втори от Евгени (два различни оператора). Pre-flight тест.

7. **Pre-flight инструменти:** всички 5 tools отворени в browser tabs, първо API извикване направено 30 мин преди (warm cache), tab titles проверени.

8. **Handouts + печатен checklist:** 25 копия (15–20 attendees + 5 резерв), раздадени в началото на Част 2 (не края).

**Post-event (30-дневен KPI review):**
- ≥ 50% от участниците посещават поне 1 от 5-те tools
- ≥ 30% използват tool повече от 1 път
- ≥ 10% резервират Growth Gap Review call
- ≥ 5 enterprise leads (IKEA/Lidl/подобен калибър) в pipeline
- Video recording views ≥ 500 в първите 30 дни (partner + Haide YouTube)
- Mentions / backlinks в български SEO общност ≥ 10

---

## Source attribution policy

Всеки tool в UI footer има: (а) Haide Digital brand lockup, (б) atribution към оригиналния research източник.

- **Tool #4 (Fan-Out Scope):** credit към Chris Long / Nectiv Digital (fan-out extraction methodology) + Seer Interactive (Gemini fan-out study).
- **Tool #5 (Prompt Miner):** credit към Ok_Guidance9952 / r/SEO_LLM Reddit пост (оригинален regex pattern) + ALM Corp и Search Engine Land за практическата методология.
- **Tool #3 (Ski Ramp):** credit към Kevin Indig / Growth Memo (ski ramp distribution) + iPullRank / Search Engine Land (answer capsule predictor).

Philosophy: Haide стои върху раменете на изследователите, не се представя като автор. Това е part of brand.
