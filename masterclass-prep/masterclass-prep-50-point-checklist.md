# Подготовка за мастърклас — Техническо SEO в AI ерата
## 23 април 2026 | Enterprise Magazine × EURODEA
### Работен документ — Структура на лекцията + 60-точков GEO чеклист

---

## НАРАТИВНА ОС: ИСТОРИЯТА, КОЯТО РАЗКАЗВАТЕ

На 31 март 2026 Google публикува най-прозрачното си обяснение за crawling инфраструктурата досега. Това е вашият входен клин.

**Основната теза на лекцията:**
> Правилата за видимост онлайн се раздвоиха. Google вижда сайта ви по един начин. AI моделите го виждат по съвсем друг. И сега — за първи път — самият Google признава, че собствената му инфраструктура има твърди технически граници, за които повечето собственици на сайтове не подозират. Ако не инженирате за ДВЕТЕ системи едновременно, губите видимост.

**Тристепенна структура:**

### АКТ 1: „Как всъщност ви вижда Google" (15 мин)
Отворете със свежия блог пост. Днешната дата. Първоизточник. Никой в залата не го е чел.

**Ключови откровения за представяне:**

1. **Googlebot не е програма.** Това е един клиент на вътрешна SaaS crawling платформа. Google Shopping, Google News, AdSense — всички използват същата инфраструктура с различни конфигурации. Това преобръща всичко: когато „оптимизирате за Googlebot", всъщност оптимизирате за един tenant на споделена система.

2. **Лимитът от 2MB е реален.** Инфраструктурният default е 15MB, но Google Search го сваля до 2MB за HTML. Всичко след първите 2MB некомпресиран HTML просто не съществува за индексиращия pipeline на Google. Няма предупреждение в Search Console. Тихо отрязване.

3. **Web Rendering Service е напълно stateless.** Изчиства local storage и session данни между всеки request. Ако съдържанието ви зависи от бисквитки или login state, за да се рендира — Google не може да го види. Точка.

4. **Всеки ресурс се изтегля поотделно.** CSS, JS, изображения — всеки получава собствен 2MB лимит. Вашият 3MB JavaScript bundle? Отрязан. Долната половина от кода ви никога не се изпълнява в рендера на Google.

5. **Редът на кода определя какво вижда Google.** Meta tags, title, canonicals, structured data — те трябва да са КОЛКОТО се може ПО-ВИСОКО в документа. Ако седят под 2MB cutoff-а, Google не знае, че съществуват.

**КУТИЯ: Други важни Google развития от Q1 2026 (споменете ги кратко)**
- **Март 2026 Core Update** (стартирал 27 март, още rolling): „Information Gain" сигналът получи реални зъби. Страници, които добавят НОВА информация, отчитат ~22% visibility gain срещу rehashed контента. Page-level authority замества domain protection — силни домейни вече не предпазват слабите страници.
- **Gemini 3 като default за AI Overviews** (януари 2026): follow-up въпросите сега скачат директно в AI Mode. Още по-малко кликове към publishers. Още по-важно е да ви цитират, не само да ви класират.
- **Февруари 2026 Discover Core Update**: първата по рода си Discover-only ъпдейт, фаворизира локално релевантно съдържание.

**Съвет за презентация:** Покажете реалния URL на блог поста на екрана. Нека хората го снимат. Кредибилност чрез актуалност.

---

### АКТ 2: „Как ви виждат AI моделите — и какво е различно" (10 мин)
Мост от Google към AI пейзажа. Тук блести вашата GEO експертиза.

**Ключови контрасти:**

| Параметър | Googlebot | AI Crawlers (GPTBot, ClaudeBot и др.) |
|---|---|---|
| Рендира JavaScript | Да (чрез WRS) | Не — консумират само pre-rendered HTML, няма headless browser |
| Спазва robots.txt | Да | Зависи — training crawlers спазват, user-triggered fetchers игнорират |
| Session/cookies | Stateless (изчиства между заявки) | Stateless |
| Поведение при размер на файл | 2MB, след това отрязва | Недокументирани лимити, но raw HTML е критичен |
| Какво индексира | HTML + рендериран DOM | Raw HTML + structured data |
| Structured data | Използва за rich results | Използва за entity разбиране + решения за цитиране |
| Честота на recrawl | Алгоритмична (crawl budget) | По-рядка, по-непредвидима |

**Новост: Google-Agent** (документирано 20 март 2026)
- Нов user-triggered fetcher за AI продукти като Project Mariner
- **Игнорира robots.txt** — защото действа като proxy за реален човешки request
- Това означава: дори да блокирате AI crawlers, когато реален човек помоли Google AI да извлече съдържанието ви, блокът се заобикаля
- Същият модел при **ChatGPT-User, Claude-User и Perplexity-User** — трите също игнорират robots.txt, когато потребител изрично поиска fetch
- Изводът: блокирането на AI crawlers е все по-безсмислено; стратегията трябва да е оптимизация ЗА тях, не блокиране

**Поантата на Акт 2:**
> Ако оптимизирате само за Google — пропускате ChatGPT, Perplexity, Claude, Gemini и всичко, което идва след тях. Ако оптимизирате само за AI — пропускате 90% от сегашния трафик. Трябва да инженирате за двете системи едновременно.

---

### АКТ 3: „60-те точки — и как да ги приложите" (25 мин)
Това е същината. Раздайте чеклиста. Разходете се през категориите на живо, но им дайте пълния документ за вкъщи.

---

## 60-ТОЧКОВИЯТ GEO ТЕХНИЧЕСКИ ЧЕКЛИСТ

### Легенда:
- 🤖 = Може да се автоматизира с AI инструменти
- 🔧 = Може да се автоматизира с традиционни SEO инструменти
- 👁️ = Изисква ръчна проверка
- ⚡ = Бърза победа (под 30 минути)
- 🏗️ = Инфраструктурна промяна (нужен е разработчик)

---

### КАТЕГОРИЯ 1: HTML И СТРУКТУРА НА ДОКУМЕНТА (Точки 1–10)

**1. HTML файлът под 2MB (некомпресиран)**
🔧⚡ | Проверка с: Chrome DevTools → Network → колона „resource" (не „transferred")
- 2MB важи за НЕКОМПРЕСИРАНИ данни — gzip/Brotli не помагат тук
- 90% от страниците са под 151KB — ако сте над 500KB, одитирайте сериозно

**2. Критичното съдържание в първите 2MB от HTML source**
👁️ | Ръчна проверка: View Source → вашето основно съдържание, заглавия, structured data близо до върха ли са?
- Ако meta tags, JSON-LD или основното съдържание седят под тежки inline скриптове, Google може никога да не ги обработи

**3. JSON-LD structured data в `<head>`, не във footer на `<body>`**
🤖⚡ | Google изрично поддържа JSON-LD в `<head>` — преместете го там
- Това гарантира, че structured data е сред първите обработени байтове

**4. Meta tags, title, canonical tags ВИСОКО в `<head>`**
🔧⚡ | Трябва да са в първите няколко KB от документа
- Някои CMS теми и плъгини инжектират tracking скриптове преди meta tags — поправете това

**5. Екстернализирайте CSS — без големи inline `<style>` блокове**
🏗️ | Преместете CSS във външни файлове (всеки под 2MB)
- Външните ресурси се fetch-ват отделно със собствен 2MB лимит
- Inline CSS наду­ва HTML-а и изяжда 2MB бюджета

**6. Екстернализирайте JavaScript — без големи inline `<script>` блокове**
🏗️ | Преместете JS във външни файлове (всеки под 2MB)
- Inline JS е причина №1 за HTML раздуване на модерните сайтове
- SPA-та с inline bundle-и са най-рисковата категория

**7. Няма рендиране зависещо от session/cookies**
👁️ | Тест: променя ли се съдържанието на страницата, когато изчистите всички бисквитки?
- WRS на Google е напълно stateless — изчиства всичко между заявки
- Персонализирани content gates, „continue reading" модали, cookie-wall съдържание = невидими за Google

**8. Чиста HTML йерархия: H1 → H2 → H3 семантичен поток**
🤖⚡ | AI crawlers особено разчитат на heading йерархия, за да разбират структурата
- И Googlebot, и AI моделите използват headings като основен сигнал за топикално сегментиране

**9. Декларация на езика в `<html lang="">` таг**
🔧⚡ | Критично за AI модели, за да обработват и цитират мултиезично съдържание коректно
- AI моделите го ползват, за да определят езика за цитиране и релевантност

**10. Минимална DOM дълбочина — избягвайте дълбоко вложени елементи**
🔧 | Дълбокото влагане увеличава HTML размера и забавя рендирането
- Плоските, семантични структури се парсват по-бързо и от WRS на Google, и от AI crawlers

---

### КАТЕГОРИЯ 2: STRUCTURED DATA И SCHEMA (Точки 11–18)

**11. Organization schema на началната страница**
🤖⚡ | Дефинира вашата entity за Knowledge Graph и AI модели
- Name, URL, logo, sameAs (социални профили), foundingDate, description
- AI моделите го ползват за изграждане на entity разбиране

**12. WebSite schema със SearchAction**
🔧⚡ | Сигнализира структурата на сайта и вътрешната search възможност
- Помага на Google и AI моделите да разбират сайта ви като навигируема entity

**13. Article/BlogPosting schema на контент страниците**
🤖⚡ | Author, datePublished, dateModified, headline, description
- AI моделите силно тежат authorship сигналите при решения за цитиране

**14. Product schema — разширено за AI shopping асистенти**
🤖 | Базово: name, description, offers, aggregateRating, brand
- **Разширения за 2026:** `hasMerchantReturnPolicy` (MerchantReturnPolicy), `shippingDetails` (OfferShippingDetails), `priceValidUntil`, `itemCondition`
- ChatGPT Shopping, Gemini Shopping и Perplexity извличат точно тези полета. Базово Product schema вече не е достатъчно.
- Източник: schema.org/Product + Google Merchant Center 2026 guidance

**15. FAQ schema където наистина има смисъл**
🤖⚡ | Форматът директен въпрос-отговор е точно това, което AI моделите търсят
- Не го спамете — използвайте го, където наистина имате FAQ
- AI моделите извличат Q&A двойки за директно цитиране

**16. HowTo schema за процесно/туториално съдържание**
🤖 | Структурираните стъпки се мапват директно към начина, по който AI моделите представят процедурни отговори

**17. BreadcrumbList schema**
🔧⚡ | Помага на Google и AI моделите да разбират йерархията на сайта
- Контекстуализира къде седи съдържанието в информационната ви архитектура

**18. Speakable schema (където е приложимо)**
🤖 | Маркира секции, оптимизирани за гласово/аудио възпроизвеждане
- Все по-релевантно, докато AI асистентите четат съдържание на глас

---

### КАТЕГОРИЯ 3: AI CRAWLER ДОСТЪП И КОНФИГУРАЦИЯ (Точки 19–28)

**19. Разрешете основните AI training crawlers в robots.txt**
⚡ | Пълният документиран 2026 списък — разрешете следните user-agents:
- **GPTBot** (OpenAI, training данни за ChatGPT)
- **OAI-SearchBot** (OpenAI, search резултати в ChatGPT)
- **ChatGPT-User** (OpenAI, user-triggered fetches — игнорира robots.txt)
- **ClaudeBot** (Anthropic, training)
- **Claude-SearchBot** (Anthropic, search)
- **Claude-User** (Anthropic, user-triggered — игнорира robots.txt)
- **PerplexityBot** (Perplexity, training)
- **Perplexity-User** (Perplexity, user-triggered — игнорира robots.txt)
- **Google-Extended** (Google, Gemini/Vertex AI training)
- **Google-Agent** (Google, Project Mariner — игнорира robots.txt)
- **Applebot-Extended** (Apple Intelligence training, отделен от класическия Applebot)
- **MistralAI-User, MistralAI-Index** (Mistral)
- **CCBot** (Common Crawl — захранва training corpora за много LLM-и)

Източници: developers.openai.com/api/docs/bots, docs.anthropic.com, docs.perplexity.ai/docs/resources/perplexity-crawlers, support.apple.com, docs.mistral.ai/robots, commoncrawl.org

**20. Не блокирайте GPTBot, OAI-SearchBot и ClaudeBot**
⚡ | Блокирането им изключва вашия бранд от training корпусите на ChatGPT и Claude
- Веднъж блокирани, губите дългосрочно място в parametric knowledge на моделите

**21. Не блокирайте PerplexityBot**
⚡ | Perplexity е retrieval-first — всеки отговор сочи източници. Блокирането = нулеви цитирания оттам.

**22. Не блокирайте Google-Extended**
⚡ | Контролира дали съдържанието ви се ползва за Gemini и AI Overviews
- Блокирането намалява видимостта ви във всички AI продукти на Google

**23. Не блокирайте Applebot-Extended**
⚡ | НОВО за 2026: контролира включване в training корпуса за Apple Intelligence и Siri
- Apple Intelligence се разширява в iOS 18+ и macOS — този crawler ще става все по-важен

**24. Не блокирайте CCBot (Common Crawl)**
⚡ | Common Crawl захранва training данните на повечето open-source модели и много commercial
- Февруари 2026 crawl: 2.1 милиарда страници. Блокирането = изчезване от open AI екосистемата.

**25. Осъзнайте поведението на user-triggered fetchers**
👁️ | Google-Agent, ChatGPT-User, Claude-User и Perplexity-User ИГНОРИРАТ robots.txt
- Не можете да ги блокирате — те действат като proxy за реални потребителски заявки
- Стратегия: оптимизирайте за тях, вместо да се опитвате да ги ограничите

**26. Мониторирайте AI crawler трафика в server logs**
🔧 | Настройте log анализ за GPTBot, ClaudeBot, PerplexityBot, Googlebot, Applebot-Extended
- Следете кои AI crawlers посещават, колко често, кои страници вземат
- Тези данни са вашата ранна предупредителна система за промени в AI видимостта

**27. Проверете честотата и дълбочината на AI crawl**
🔧 | Сравнете crawl моделите: достигат ли AI bots до дълбокото ви съдържание?
- Ако само вземат началната страница и топ страниците, дълбокото ви съдържание е невидимо за AI отговорите

**28. Бъдещи стандарти: IETF AI Preferences + llms.txt (с резерва)**
👁️ | Следете за enterprise audit/compliance дискусии
- **IETF AI Preferences** (draft-ietf-aipref-attach-04, активен до май 2026): нов Content-Usage HTTP header като стандартизиран заместител на ad-hoc robots.txt директиви. Enterprise compliance комитетите ще питат за това.
- **llms.txt**: СПОМЕНЕТЕ, но с ясна резерва — SE Ranking изследване 2026 показва, че само 1 от топ 50 AI-цитирани домейни го използва. Anthropic го иска за Mintlify документация. За enterprise = ниска ROI извън dev/API docs сайтове. Не го продавайте като must-have.

---

### КАТЕГОРИЯ 4: КОНТЕНТ АРХИТЕКТУРА ЗА AI ЦИТИРАНЕ (Точки 29–36)

**29. Директен отговор в първите 50–70 думи от съдържанието**
🤖👁️ | AI моделите извличат най-ясния, най-кратък отговор близо до върха
- **Данни от изследвания:** 44.2% от ChatGPT цитиранията идват от първите 30% на страницата (Kevin Indig / iPullRank, 2026). 86% от Google AI Overviews цитиранията идват от страници в топ 100 органични резултати (ziptie.dev изследване).
- Пишете все едно отговаряте на въпроса, после разширявайте
- Това е модел №1 за цитиране в AI отговори

**30. Entity-first писане: дефинирайте ясно КОЙ, КАКВО, КЪДЕ**
🤖👁️ | AI моделите имат нужда от недвусмислени entity референции
- „Haide Digital е organic growth engineering компания, базирана в София, България" — ясно entity изявление
- Избягвайте начала с местоимения; назовете entity-то изрично

**31. Статистически твърдения с източници**
👁️ | AI моделите приоритизират съдържание с проверими данни
- Включвайте конкретни числа, дати, проценти С източници
- Моделът „Според [източник], [конкретно твърдение]" се цитира повече

**32. Уникално изследване, данни или first-party insights**
👁️ | AI моделите са тренирани да предпочитат оригинални източници пред агрегатори
- Ваши собствени case studies, анкети, benchmarks = магнит за цитирания
- Преработен контент от други източници = игнориран

**33. Изчерпателно топикално покритие (topical authority)**
🤖👁️ | AI моделите оценяват дълбочината на източника по темата преди да цитират
- Една тънка статия ≠ authority. Клъстер от взаимно свързано, дълбоко съдържание = authority сигнал
- Изграждайте топикални клъстери, не изолирани страници

**34. Content freshness сигнали: dateModified, честота на обновяване**
🔧⚡ | AI моделите тежат recency — остарялото съдържание се депрiоритизира
- Обновявайте съдържанието редовно и отразявайте го в schema dateModified
- Не фалшифицирайте дати — AI моделите cross-reference-ват

**35. Author страници с Person schema и sameAs верификация**
🤖 | Актуализация за 2026: E-E-A-T вече минава през публично проверим author entity
- Person schema с `sameAs` към LinkedIn, ORCID, Wikipedia, Crunchbase, GitHub (за tech автори), Google Scholar (за research)
- AI моделите оценяват author authority за решения за цитиране чрез тези verified профили
- Вътрешна author страница с credentials, експертиза, публикационна история

**36. About страница с ясна организационна entity дефиниция**
🤖⚡ | AI моделите използват вашата About страница, за да изграждат entity разбиране
- Ясно име на компанията, локация, услуги, екип, история на основаване
- Това често е първата страница, която AI моделите проверяват за entity resolution
- Включете NAP (Name, Address, Phone) консистентно — AI моделите го ползват за trust оценка

---

### КАТЕГОРИЯ 5: ТЕХНИЧЕСКА ПРОИЗВОДИТЕЛНОСТ И РЕНДИРАНЕ (Точки 37–44)

**37. Server-Side Rendering (SSR) или Static Site Generation (SSG)**
🏗️ | AI crawlers не изпълняват JavaScript — четат raw HTML
- Ако съдържанието ви се появява само след JS изпълнение, AI моделите не могат да го видят
- SSR/SSG гарантира, че съдържанието е в началния HTML response

**38. Streaming SSR и islands архитектура за намаляване на hydration cost**
🏗️ | Модерни 2026 практики за Next.js 14+, Astro, Qwik, SvelteKit
- Монолитна hydration убива INP (Interaction to Next Paint) — новият Core Web Vital от март 2024
- Islands архитектурата hydrate-ва само интерактивните компоненти, останалото остава статично
- Streaming SSR изпраща HTML на парчета, crawler-ите получават съдържание по-бързо
- Особено критично за enterprise dashboards и media сайтове

**39. Core Web Vitals: LCP, INP, CLS passing**
🔧 | Google performance сигналите — все още имат значение за crawl приоритета
- Бързите сайтове се crawl-ват по-често → по-свеж индекс → по-добър AI data source
- INP замени FID през март 2024 — проверете, че измервате правилния сигнал

**40. Time to First Byte (TTFB) под 200ms**
🔧 | Директно влияе на crawl rate — бавните сървъри се crawl-ват по-малко
- И Googlebot, и AI crawlers депрiоритизират бавни сайтове

**41. Правилни HTTP status кодове (200, 301, 404)**
🔧 | Redirect вериги, soft 404-та и 5xx грешки хабят crawl budget
- AI crawlers са дори по-непрощаващи — често не следват redirect вериги

**42. HTTPS навсякъде — без mixed content**
🔧⚡ | Базово изискване за trust сигнали
- AI моделите включват сигурността в оценката на credibility на източника

**43. Mobile-first рендирането верифицирано**
🔧 | Googlebot crawl-ва основно като mobile Smartphone agent (mobile-first rollout завършен юли 2024)
- Тествайте с mobile user agent — видимо ли е цялото съдържание?

**44. Native lazy loading + няма render-blocking ресурси над сгъвката**
🔧🏗️ | Използвайте native `loading="lazy"` — не JS-only lazy loading
- Googlebot обработва правилно native lazy loading
- Custom JS lazy loading може да скрие съдържание и от Google, и от AI crawlers
- Critical CSS inline, defer на non-critical JS

---

### КАТЕГОРИЯ 6: CRAWLABILITY И ИНДЕКСАЦИЯ (Точки 45–50)

**45. XML sitemap: чист, актуален, под 50K URL-а на файл**
🔧⚡ | Включвайте само индексируеми, canonical URL-и
- `<lastmod>` тагове с реални дати — AI crawlers ги ползват за freshness

**46. Robots.txt: без случайни блокове на критични ресурси**
🔧⚡ | Не блокирайте CSS/JS, които Google има нужда за рендиране
- Тествайте с robots.txt тестера на Google в Search Console

**47. Canonical тагове: self-referencing на всяка индексируема страница**
🔧⚡ | Предотвратява объркване с дублирано съдържание и за Google, и за AI моделите
- AI моделите могат да crawl-ят множество URL варианти и да се объркат без canonicals

**48. Вътрешна линк архитектура: 3-click дълбочина + нула orphan страници**
🔧 | Важните страници в рамките на 3 клика от началната + всяка страница с поне един вътрешен линк
- По-дълбоките страници се crawl-ват по-рядко от всички crawlers
- Orphan страниците разчитат изцяло на sitemap-и за откриване — но AI crawlers рядко ползват sitemap-и, те следват линкове
- Orphan страници = невидими за AI модели

**49. Pagination архитектура без rel="next/prev"**
🔧🏗️ | **Корекция за 2026:** Google прекрати поддръжката на rel="next/prev" още през 2019 (потвърдено от John Mueller). Не го използвайте.
- Правилен модел: self-canonical страници (page 2 сочи към себе си, не към page 1), crawlable „load more" връзки с реални `<a href>` URL-и, или инфинит scroll с History API
- AI crawlers следват линкове, не следват JS-ониран scroll

**50. Log file анализ: верифицирайте реалното crawl покритие**
🔧 | GSC данните са sampled — server logs показват ground truth
- Сравнете Googlebot vs AI crawler покритие
- Идентифицирайте страници, до които AI crawlers никога не стигат

---

### КАТЕГОРИЯ 7: AI CITATION И ENTITY ЛАЕР (Точки 51–58) — НОВО ЗА 2026

Тази категория е ядрото на GEO трансформацията. Докато Категории 1–6 покриват техническата основа, Категория 7 адресира специфичната механика на това КАК AI модели избират кого да цитират. Без тези точки, дори перфектно техничен сайт губи AI видимост.

**51. Оптимизация за AI Overviews source selection**
🤖👁️ | Front-load на отговорите, passage-level структуриране
- Директен отговор в първите 50–70 думи (не 200)
- Всяко ключово твърдение = самостоятелно извлечим параграф с атрибуция
- Scannable структура: H2/H3 секции с въпросно-отговорен формат
- Данни: ziptie.dev „Google AI Overviews source selection" + Kevin Indig citation patterns изследване
- Обвързано с точка 29 — това е по-дълбоката техническа реализация

**52. Brand entity в Knowledge Graph и Wikidata**
👁️🏗️ | Изграждане на verified brand entity през външни източници
- **Wikidata запис** за компанията с пълни properties (инстанция на, локация, индустрия, основатели)
- **sameAs граф:** Wikipedia, Wikidata, Crunchbase, LinkedIn, GitHub Organization, Twitter/X, YouTube канал
- Консистентност на организационната schema през всички property-та на сайта
- **Защо е критично:** AI моделите решават кого да цитират чрез parametric knowledge (от тренировъчните данни) + real-time retrieval. Класиране №1 в Google не гарантира цитиране, ако брандът не е разпознаваем entity в Knowledge Graph.
- Източник: iPullRank entity SEO framework, discoveredlabs.com entity recognition guide

**53. Semantic chunking за RAG системи**
👁️🤖 | Структурирайте съдържанието с ясни семантични граници
- Всеки H2/H3 блок трябва да може да стои сам по себе си без предходен контекст
- FAQ блокове, таблици, отделни definition блокове = идеални chunks за retrieval
- Избягвайте pronoun references между секциите („както споменахме по-горе…" = счупен chunk)
- Модерните RAG системи (ChatGPT browsing, Perplexity, Gemini) извличат на chunk ниво, не на ниво страница. Лошо chunking = лош retrieval = няма цитиране.
- Източник: iPullRank „Misinformation about chunking" + salt.agency RAG architecture guide

**54. ClaimReview и Claim schema за fact-checked съдържание**
🤖 | Структурирани проверими твърдения
- Имплементирайте `schema.org/ClaimReview`, `schema.org/Claim` и Rating за fact-check или expert-verified контент
- Особено ценно за B2B enterprise, advisory, research, и industry analysis съдържание
- AI моделите все по-силно приоритизират fact-checked твърдения с атрибуция
- Източник: developers.google.com/search/docs/appearance/structured-data/factcheck

**55. Мултиезична entity консистентност (критично за БГ пазара)**
👁️🏗️ | hreflang + entity метаданни синхронизирани през езиковите версии
- Една и съща Organization schema в BG и EN версиите (същия @id, същите sameAs)
- Author имена транслитерирани консистентно — „Адриан Николов" на БГ и „Adrian Nikolov" на EN версията, свързани през Person `sameAs`
- AI моделите цитират източници на езика на запитването. При несъответствие между BG/EN версии губите цитирания и на двата пазара.
- Извънредно релевантно за български enterprise брандове, които таргетират регионална + глобална публика

**56. VideoObject schema + crawlable transcript експозиция**
🤖🏗️ | Видеосъдържанието трябва да е четимо, не само гледаемо
- Имплементирайте `schema.org/VideoObject` с `transcript`, `uploadDate`, `duration`, `contentUrl`
- Транскриптите трябва да са в DOM-а, не заключени в player-а или зад JS
- AI системите извличат от видео транскрипти — заключените транскрипти са невидими за тях
- Captions/subtitles като crawlable `.vtt` файлове

**57. Семантичен HTML + ARIA като AI comprehension сигнал**
🔧👁️ | Accessibility (WCAG 2.1 AA) и AI разбиране се припокриват силно
- Правилни HTML5 landmark елементи: `<article>`, `<section>`, `<nav>`, `<aside>`, `<main>`
- ARIA роли където native semantics не стигат
- Screen-reader-friendly съдържание = AI-parser-friendly съдържание
- Това е една от малкото точки с двойна ROI: законово съответствие + AI видимост

**58. AI citation мониторинг през ChatGPT, Perplexity, Gemini**
🔧👁️ | Директна верификация на AI видимостта ви
- Ежемесечен ръчен тест: питайте ChatGPT, Perplexity, Claude, Google AI Overviews и Gemini за вашите продукти/услуги/бранд
- Проследявайте за кои заявки ви цитират и за кои — не
- Сравнявайте срещу конкурентите за същите заявки
- Ръчното проследяване покрива 80%+ от стойността; crawler analytics е единственият легитимен платен инструмент тук
- **Бюджет съвет:** не плащайте за „AI visibility" SaaS инструменти преди да сте направили 3 месеца ръчен мониторинг — ще разберете какво всъщност искате да измервате

---

### БОНУС ТОЧКИ (59–61) — За напредналите

**59. HTML size regression мониторинг в CI/CD**
🏗️ | Настройте автоматични alerts, когато HTML файлът надвиши prag (напр. 1.5MB)
- Предотвратява регресии, които тихо отрязват съдържанието ви

**60. Structured data валидация в deployment pipeline**
🏗️ | Автоматизирано schema тестване преди production push
- Хваща счупен JSON-LD преди да стигне до индекса на Google
- Инструменти: Schema.org validator API, Google Rich Results Test API

**61. Entity graph consistency monitoring**
🔧🏗️ | Автоматизирана проверка, че Organization sameAs линковете резолват (200 OK, не 404)
- Счупени sameAs = счупен entity граф = загубено доверие в AI моделите
- Пуска се седмично като cron job

---

## АВТОМАТИЗАЦИЯ СРЕЩУ РЪЧНА РАБОТА (За слайд / handout)

### Може да се автоматизира с AI инструменти 🤖 (15 точки)
Точки: 3, 8, 11, 13, 14, 15, 16, 18, 30, 33, 35, 36, 51, 53, 54
- Използвайте Claude/ChatGPT за генериране на schema markup от съдържанието на страницата
- Използвайте AI за одит на heading йерархия и структура на съдържанието
- Използвайте AI за чернови на entity-оптимизирани About/Author страници
- AI може да идентифицира passage-level цитируеми твърдения в съществуващо съдържание

### Може да се автоматизира със SEO инструменти 🔧 (26 точки)
Точки: 1, 4, 5, 9, 10, 12, 17, 26, 27, 34, 37, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 57, 58, 61
- Screaming Frog, Ahrefs, Semrush, GSC за crawl анализ
- Chrome DevTools за file size и rendering проверки
- Server log анализ за crawler проследяване
- Lighthouse и PageSpeed Insights за Core Web Vitals

### Изисква ръчна проверка 👁️ (11 точки)
Точки: 2, 7, 25, 28, 29, 31, 32, 33, 52, 55, 58
- Качество, оригиналност и citation-worthiness на съдържанието
- Session-зависими проверки на рендирането
- AI citation мониторинг (директно питане на моделите)
- Entity граф изграждане и верификация

### Нуждае се от developer имплементация 🏗️ (11 точки)
Точки: 5, 6, 37, 38, 52, 55, 56, 59, 60, 61
- SSR/SSG/streaming SSR миграция
- Build pipeline интеграция
- Инфраструктурни промени
- Entity schema архитектура

---

## ПРЕПОРЪКИ ЗА ПОТОКА НА ЛЕКЦИЯТА

### Отваряне (2 мин)
Започнете с LinkedIn пост скрийншот + реалния Google блог пост. „Това беше публикувано ДНЕС. Преди да започнем — нека ви покажа какво Google току-що ни каза за това как всъщност работи неговият crawler." Моментално внимание. Никой в залата няма този контекст.

### Акт 1: Инфраструктурната реалност (15 мин)
Разходете се през 5-те откровения. Ползвайте прости диаграми:
- Googlebot → 2MB cutoff → всичко под това = невидимо
- WRS stateless → без cookies, без session → това, което виждате ≠ това, което вижда Google
- Всеки ресурс отделно → JS под 2MB, CSS под 2MB, HTML под 2MB

**Споменете кратко:** март 2026 Core Update (Information Gain има реални зъби), Gemini 3 като default за AI Overviews.

**Опция за live demo:** Отворете Chrome DevTools на сайт на доброволец. Покажете некомпресиран HTML размер. Ако е под 100KB (при повечето ще е) — „В безопасност сте. Но нека ви покажа един, който не е." Покажете eCommerce категорийна страница с inline филтър JSON.

### Акт 2: AI пропастта (10 мин)
„Google ви казва честно какво може и какво не може да види. AI моделите не. Те просто… не ви цитират." Покажете сравнителната таблица. Demo: питайте ChatGPT за локален български бизнес. Покажете какво се случва, когато structured data липсва vs. присъства.

**Откровението за Google-Agent:** „Преди месец Google има нов fetcher, който напълно игнорира вашия robots.txt. И не е сам — ChatGPT-User, Claude-User и Perplexity-User правят същото. Епохата на блокиране на AI crawlers приключи. Въпросът е: оптимизирани ли сте ЗА тях?"

### Акт 3: Чеклистът (25 мин)
Разходете се през категориите на живо. За всяка категория покажете:
1. Как изглежда проблемът (скрийншот)
2. Как изглежда поправката (код/конфигурация)
3. Дали е автоматизирано или ръчно

**Специално внимание на Категория 7** — това е новото за 2026 и най-голямата разлика между „познавам SEO" и „познавам GEO".

**Timing за handout:** Раздайте печатния 60-точков чеклист в НАЧАЛОТО на Акт 3, не в края. Хората следват и отбелязват какво вече имат. Това създава ангажираност и честна самооценка.

### Заключение (3 мин)
„Сега имате чеклиста. Знаете кои точки са важни за Google И за AI. Знаете кои могат да се автоматизират. Въпросът е: кой ще го имплементира? Тук системите побеждават кампаниите. Това изграждаме в Haide Digital."

Без агресивна продажба. Предложете безплатен Growth Gap Review на щанда (ако е преди Balkan eCommerce Summit) или през QR код.

---

## ФОРМАТ НА HANDOUT-А (препоръка)

**Физически:** A5 сгъната карта (събира се в джоб), двустранна
- Предна страна: 60 точки по категории с checkbox-ове
- Задна страна: QR код към дигитална версия + „Безплатен Growth Gap Review" CTA с календарна връзка
- При 60 точки + Категория 7 описания вероятно ще трябва A4-сгъната до A5 формат

**Дигитален:** Интерактивен HTML чеклист (host на haide.digital/checklist)
- Checkbox функционалност, която запазва състояние
- Всяка точка линква към кратко обяснение
- Captures email за изтегляемата версия
- Става lead magnet, който надживява събитието

---

## ИЗТОЧНИЦИ ЗА СЛАЙДОВЕ

### Google първоизточници
1. **„Inside Googlebot: demystifying crawling, fetching, and the bytes we process"** — Google Search Central Blog, 31 март 2026
2. **Search Off the Record Епизод 105** — „Google crawlers behind the scenes", 12 март 2026 (Gary Illyes + Martin Splitt)
3. **Google Googlebot документация** — ъпдейт на 2MB лимита, 3 февруари 2026
4. **Google-Agent документация** — нов user-triggered fetcher, 20 март 2026
5. **„Things to know about Google's web crawling"** — Crawling Infrastructure docs, 3 март 2026
6. **Март 2026 Core Update** — Google Search Status Dashboard, 27 март 2026
7. **HTTP Archive Web Almanac** — медиани за HTML размер (33KB mobile, 151KB на 90-ти percentile)

### AI crawler първоизточници
8. **OpenAI bots документация** — developers.openai.com/api/docs/bots (GPTBot, OAI-SearchBot, ChatGPT-User)
9. **Anthropic ClaudeBot документация** — docs.anthropic.com (ClaudeBot, Claude-SearchBot, Claude-User)
10. **Perplexity crawlers документация** — docs.perplexity.ai/docs/resources/perplexity-crawlers
11. **Mistral robots документация** — docs.mistral.ai/robots
12. **Applebot-Extended** — support.apple.com (Apple Intelligence crawler guidelines)
13. **Common Crawl февруари 2026 доклад** — commoncrawl.org/blog (2.1B страници, 363 TiB)

### Стандарти и изследвания
14. **IETF AI Preferences draft** — datatracker.ietf.org/doc/html/draft-ietf-aipref-attach-04 (активен до май 2026)
15. **Kevin Indig / iPullRank** — AI citation patterns изследване 2026 (44.2% от ChatGPT цитирания от първите 30% на страницата)
16. **ziptie.dev** — „Google AI Overviews source selection" изследване (86% от цитирания от топ 100 резултати)
17. **SE Ranking llms.txt adoption study 2026** — seranking.com/blog/llms-txt
18. **schema.org спецификации** — Product, MerchantReturnPolicy, ClaimReview, VideoObject, Person
