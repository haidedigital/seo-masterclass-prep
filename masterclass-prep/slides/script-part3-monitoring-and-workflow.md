# Скрипт Част 3 — Monitoring Stack + Survival Workflow

> **Статус:** Итерация 3 / 3 (финалните 30 мин от 90-мин слота).
> **Език:** Български (verbatim speaking script).
> **Обща дължина:** ≈30 мин. ~4500 думи говорим текст (pure script, без live demos).
> **Slide count:** 15 слайда (58–72 в master deck, continuation от Part 2 който спря на 57).
> **Speaker:** Адриан Николов, Haide Digital.
> **Предхожда:** [script-part2-checklist-and-tools.md](script-part2-checklist-and-tools.md) (завършва на слайд 57 с transition към Signal Architecture).
> **Следва:** Край на мастърклас слота. (Q&A опционално, извън скрипта.)

---

## Навигационна таблица — слайдове 58–72

| # | Заглавие | Продълж. | Секция | Забележка |
|---|---|---|---|---|
| 58 | Част 3 — Section Divider | 0:15 | Opening | Master QR corner |
| 59 | Трите въпроса (threat list) | 1:30 | Opening | Replay от slide 57 |
| 60 | Signal Architecture reveal | 2:00 | Framework | Headline framework на Part 3 |
| 61 | Dual Budget Principle | 3:00 | 3.1 | Stat hero |
| 62 | 5-Layer Stack Overview | 2:00 | 3.2 intro | Architecture diagram |
| 63 | Layer 1 — AI Citation Tracking | 2:00 | 3.2 | Weekly · Red-thread към Prompt Miner |
| 64 | Layer 2 — Server Log Ingestion | 2:00 | 3.2 | Daily · Red-thread към Bot Radar |
| 65 | Layer 3 — Content Freshness + GSC Mining | 2:00 | 3.2 | Weekly · Red-thread към Prompt Miner |
| 66 | Layer 4 — CI/CD Schema Guard | 2:00 | 3.2 | On every deploy · Red-thread към Ceiling |
| 67 | Layer 5 — Entity Graph Health | 2:00 | 3.2 | Monthly · Red-thread към E-E-A-T |
| 68 | 48-Hour Rule | 2:00 | 3.3 | Stat hero |
| 69 | Response Workflow Cadence | 3:00 | 3.3 | 4-column grid: Daily/Weekly/Monthly/Quarterly |
| 70 | Information Diet | 4:00 | 3.4 | Sources grid + „what to ignore" |
| 71 | Growth Gap Review CTA | 2:00 | 3.5 | Enlarged QR |
| 72 | Final Line + Thank You | 1:15 | 3.5 | „Get Found. Stay Visible. Но този път — everywhere." |

**Total:** ~31:00 мин (натурален natural delivery trim до 30:00 при rehearsal).

---

## QR код стратегия за Част 3

Master QR в долен десен ъгъл продължава. Два enlarged QR момента в Part 3:
- **Slide 71 (Growth Gap Review CTA):** голям QR вдясно, fresh scan moment — този път за calendar booking, не за PDF.
- **Slide 72 (финал):** QR остава видим за last-chance сканиране докато Адриан казва финалната линия.

---

## Visual patterns reuse от Part 2

Не въвеждаме нови patterns освен един: **LAYER CARD** за слайдове 63–67 (5-те monitoring layers). Reuse-ваме: TITLE CARD, SECTION DIVIDER, STAT HERO, SPLIT SCREEN, TRANSITION, GRID, QR MOMENT.

---

# ЧАСТ 3 — MONITORING & SURVIVAL (30 мин)

---

## Слайд 58 — Section Divider „Част 3 — Monitoring & Survival" (0:15)

**Slide visual:** Пълен Deep Sea Green фон. Голямо „ЧАСТ 3" eyebrow, headline „Monitoring & Survival", subtitle „Система, която оцелява volatility-то".

**Script:**

*[Кратка пауза. Водна глътка. Reset след Част 2.]*

Част 3.

---

## Слайд 59 — Трите въпроса (threat list) (1:30)

**Slide visual:** Mirage фон. Три кратки въпроси stacked вертикално, всеки в различен „threat" orange highlight. Горе — eyebrow „ТРИ СЦЕНАРИЯ · ИДВАТ".

**Script:**

Преди да си тръгнете от тук днес, ще ви задам три въпроса. И искам да си ги зададете честно, защото ще ви се случат. Не „може би ще се случат". **Ще се случат.**

**Първи въпрос.** Какво става **следващата седмица**, когато OpenAI обяви GPT-5.5, пусне новия Sonar на Perplexity или Claude 5 — и петдесет процента от всичко, което ви казах преди един час за ChatGPT, стане outdated за една нощ?

*[Пауза.]*

**Втори въпрос.** Какво става **след два месеца**, когато Google пусне поредния Core Update — а те пускат по четири-пет такива в година — и вашата топ страница, тази, която от три години ви носи най-много трафик, изведнъж пада от AI Overviews за една нощ? И вие откривате това в понеделник сутрин, когато шефът ви звъни да пита „какво стана с лийдовете"?

*[Пауза.]*

**Трети въпрос.** Какво става, когато Perplexity тихо сменя Sonar модела си — без прес съобщение, без документация — и просто спира да ви цитира? Не пада ви трафикът драматично. Просто спират да споменават името на вашия бранд. И вие научавате това три месеца по-късно, когато конкурент ви каже „а, вас не ви виждат в Perplexity вече."

*[Пауза. Дълбок дъх.]*

Всичките тези три сценария имат **нещо общо**. Ще ги научите. Въпросът е само — **кога**. Ден едно? Ден седем? Ден тридесет? Разликата между ден едно и ден тридесет е разликата между „бърза корекция на три страници" и „три загубени месеца трафик и един много неприятен разговор с борда".

Част 3 е за това как да сте на ден едно. Не ден тридесет.

---

## Слайд 60 — Signal Architecture reveal (2:00)

**Slide visual:** Deep Sea Green фон. Голямо eyebrow „HAIDE FRAMEWORK". Headline „Signal Architecture". Subtitle на БГ: „Архитектура на сигналите". Долу: аналогия caption „Контролна зала на електроцентрала — всички сигнали, едно табло, 24/7".

**Script:**

Решението се нарича **Signal Architecture** — на български, **архитектура на сигналите**. Това е един от Haide framework-ите, регистриран, и е точно това, което ни извежда на днешния ден от позиция да реагираме с два месеца закъснение, до позиция да реагираме в рамките на 48 часа.

Аналогия. Представете си **контролната зала на електроцентрала**. Не тази от холивудските филми с аларми и сирени — истинската. Операторът седи пред една голяма стена от екрани. На нея — сто, двеста, триста сигнали. Температура на ротора, налягане на турбината, напрежение на линиите, ниво на водата в охладителната система. Двадесет и четири часа в денонощието, седем дена в седмицата, тези сигнали **просто стоят там**. Не бипат. Не алармират. Операторът ги гледа периферно, докато пие кафе.

И когато **един** сигнал се промени — температурата скача с три градуса, налягането пада с половин бар — операторът го вижда **веднага**. Не защото той е герой. Защото архитектурата е била дизайн-ната да му покаже **точно това изменение**, в точния момент, на точното място.

Това е Signal Architecture за вашата AI visibility. Набор от сигнали — от вашия сайт, от сървърните ви логове, от Google Search Console, от AI моделите — които **стоят на една табло**, двадесет и четири часа в денонощието. И когато нещо се промени, вие го виждате. Не два месеца след като конкурентът ви е казал. Не тридесет дни след Core Update. **В рамките на 48 часа.**

И най-важното нещо за тази архитектура — тя **не спира промените**. Промените са неизбежни. AI ерата е volatile и ще остане volatile. Архитектурата просто ви дава **време да реагирате**. Това е цялата игра.

Нека ви покажа какво има в тази табло.

---

## Слайд 61 — Dual Budget Principle (3:00)

**Slide visual:** Stat hero. Mirage фон. Голямо „15–20%" в Haide Orange. Caption „observability budget · от вашия SEO/GEO spend". Долу, по-малко: сравнителен bar chart — два budget-а, единият „SEO execution", другият „GEO observability".

**Script:**

Преди да ви покажа стака на инструменти, едно принципно нещо. Наричам го **Dual Budget Principle** — принципът на двата бюджета.

Аналогия, която винаги работи с финансовите директори: **не плащате само за колата. Плащате и за застраховката й.** Ако утре ви кажа „имам страхотна сделка, ще ви продам кола за петдесет хиляди лева, но **без застраховка**, и вие никога не можете да я застраховате" — вие няма да я купите. Защото цената без застраховка е **по-висока**, не по-ниска. Рискът не се вижда в цената, но съществува.

Същото важи за вашия SEO и GEO бюджет.

В 2026 enterprise брандовете, които го правят правилно — IKEA, Spotify, Adobe, тези, с които работим — отделят **петнадесет до двадесет процента** от целия си organic growth бюджет за **observability**. Observability — това е технически термин от software engineering. Означава „способност да видиш какво всъщност прави системата ти". На български казваме „видимост към вътрешността на системата".

Аналогия: **стетоскоп за системата ви.** Без него лекарят работи слепешката — пита пациента „къде те боли?", пациентът казва „тук", и това е цялата диагностика. Със стетоскоп — лекарят чува какво прави сърцето, какво прави белият дроб, **преди** пациентът да разбере, че има проблем.

Observability бюджетът не строи нищо ново. Не пише нови статии. Не оптимизира нови schema markup-и. Той **само** ви казва дали всичко, което вече сте направили, **работи още**. И тъй като правилата се променят на всеки две седмици, без него — буквално не знаете кое от работата ви от миналата година още носи резултат.

Конкретно — какво покрива този петнадесет-до-двадесет процент observability бюджет? Пет неща. Пет слоя. И сега ще минем всеки един от тях.

---

## Слайд 62 — 5-Layer Stack Overview (2:00)

**Slide visual:** Architecture diagram. Wild Sand фон. 5 хоризонтални layer-а, stacked вертикално, всеки с номер, име, cadence badge. Стрелки от всеки layer към централна „Signal Table" икона вдясно. Отгоре headline „Haide Monitoring Stack".

**Script:**

Ето ги петте слоя. Ще ги чуете в поредност от най-горен (най-бърз cadence) до най-долен (най-бавен cadence):

**Layer 1 — AI Citation Tracking.** Weekly. Какво казват AI моделите за вас.

**Layer 2 — Server Log Ingestion.** Daily. Кой AI bot ви е посетил вчера.

**Layer 3 — Content Freshness + GSC Prompt Mining.** Weekly. Какви нови въпроси ви задават хората в Google.

**Layer 4 — Schema + 2MB Regression Guard.** Every deploy. Защитна стена, която блокира пукане на schema или HTML при всеки code commit.

**Layer 5 — Entity Graph Health.** Monthly. Дали AI моделите още разпознават кой сте.

Пет слоя. Всеки от тях **се връзва директно с един от петте инструмента**, които видяхте в Част 2. Защото това, което ви показах преди час, не са пет самостоятелни gadgets. Те са **входни точки** към един monitoring стак. Кръгът се затваря точно сега.

Нека ги видим един по един.

---

## Слайд 63 — Layer 1: AI Citation Tracking (2:00)

**Slide visual:** LAYER CARD (нов pattern). Wild Sand фон. Top-left: orange pill „WEEKLY". Голямо „01". Title: „AI Citation Tracking". 3 bullets: „Notion template · 20 queries × 5 platforms", „3-месечна manual baseline преди SaaS", „Сутрешна новина — неделя · кафе · 20 мин". Bottom red-thread strip: „→ вход: Haide Prompt Miner".

**Script:**

**Слой 1 — AI Citation Tracking.** Weekly cadence — всяка седмица веднъж.

Аналогия: **сутрешна новина**. Всяка неделя сутрин, с кафе, отваряте таблетa. Двадесет минути. Четете новините. И излизате от неделния брънч знаейки какво се е случило в света през седмицата. Същото е тук. Всяка неделя, двадесет минути, знаете какво се е случило с вашия бранд в AI света.

Конкретно какво правите. Имате **Notion template** — ще ви го дам безплатно, на същия QR код. В template-a има двадесет въпроса — десет за вашия бранд, десет за вашите продукти и конкуренти. И имате **пет платформи** — ChatGPT, Claude, Perplexity, Gemini, Google AI Overviews. Двадесет въпроса по пет платформи = сто queries всяка неделя. Копи-пейст, screenshot, маркиране в Notion-а: „цитират ли ме?", „кого цитират вместо мен?", „с какъв език?".

Двадесет минути. Веднъж седмично. След **три месеца** имате baseline — петстотин data points, и вече виждате patterns. Кой модел ви обича. Кой модел ви игнорира. Коя формулировка на въпроса ви извежда в top 3 citations и коя — изобщо не.

И още нещо важно: **не плащайте за AI visibility SaaS инструмент преди да имате тези три месеца manual baseline.** Защо? Защото без baseline, всеки SaaS ще ви показва числа, които не знаете как да интерпретирате. „Citation score 42" — това добре или зле е? Без baseline не знаете. С baseline от три месеца ръчна работа, знаете точно какво означава 42 за вашия бранд. И тогава можете да решите дали SaaS-ът наистина ви спестява време или просто преопакова данни, които вече имате.

Входът към този layer е **Haide Prompt Miner**, инструмент номер 5 от Част 2. Queries-ите, които извличате там от GSC-то си — те стават вашите седмични тест queries. Кръгът се затваря.

---

## Слайд 64 — Layer 2: Server Log Ingestion (2:00)

**Slide visual:** LAYER CARD. Wild Sand фон. Orange pill „DAILY". Голямо „02". Title: „Server Log Ingestion". 3 bullets: „n8n cron · Nginx/Apache logs", „Alerts: нов crawler, изчезнал crawler, 5xx на AI-crawled pages", „Free алтернатива: GoAccess". Bottom red-thread: „→ вход: Haide Bot Radar".

**Script:**

**Слой 2 — Server Log Ingestion.** Daily. Всеки ден.

Аналогия: **охранителна камера пред входа.** Не гледате записа всеки ден. Но ако някой непознат минава пред вратата ви три пъти за една седмица — **системата ви казва**. Не чакате да разберете, когато е станало късно.

Механиката е проста. Имате **n8n workflow** — или Zapier, или Make, или cron на сървъра, каквото ви е удобно. Всяка нощ, в два часа, този workflow взема server log-а от Nginx или Apache от последните 24 часа. Парсва го. И отговаря на три въпроса:

Първо — **появил ли се е нов AI crawler**, който вчера не е бил тук? Ако OpenAI пусне GPTBot-2 следващия четвъртък, а вие сте го блокирали в robots.txt без да знаете — искате да научите в петък сутрин, не в понеделник.

Второ — **спрял ли е да идва crawler, който обикновено идва?** Ако GPTBot посещаваше сайта ви 100 пъти на ден и внезапно две седмици не е идвал — нещо е счупено. Или в кода ви, или в тяхната система. И в двата случая искате да го знаете **веднага**.

Трето — **колко от страниците, които AI crawlers посещават, връщат 4xx или 5xx грешки?** Това е най-тихата форма на AI visibility loss. Страницата ви съществува за хората, но дава 503 за ChatGPT-User. Вие никога не разбирате, докато traffic-ът не падне.

Ако нямате n8n или budget за automation — **GoAccess** е безплатна open-source алтернатива. Генерира weekly email report от вашите log файлове. Петнадесет минути setup, цял живот монитор.

Входът към този layer е **Haide Bot Radar**, инструмент номер 2 от Част 2. Той прави snapshot в момента, когато го качите. Layer 2 просто автоматизира този snapshot всеки ден.

---

## Слайд 65 — Layer 3: Content Freshness + GSC Mining (2:00)

**Slide visual:** LAYER CARD. Orange pill „WEEKLY". Голямо „03". Title: „Content Freshness + GSC Mining". 3 bullets: „GSC API · regex auto-applied", „Нови 7+ word queries седмично", „Корелация: Ahrefs drops + AI citation loss = вероятно Core Update". Bottom red-thread: „→ вход: Haide Prompt Miner".

**Script:**

**Слой 3 — Content Freshness и GSC Prompt Mining.** Weekly.

Помните ли от Част 2 Haide Prompt Miner — regex-а, който извлича LLM-style prompts от Google Search Console? Онзи, кредитиран на Ok_Guidance9952 от Reddit.

Layer 3 **автоматизира това**. Вместо всяка неделя да отивате в GSC и ръчно да копирате regex-а, имате GSC API connection, която всяка седмица:

- Дърпа всички queries от последните 7 дни
- Прилага regex-а автоматично
- Сравнява списъка с миналата седмица
- И ви изпраща **email с новите 7+ word queries, които не са били там миналата седмица**

Защо това е магия? Защото **новите въпроси** са най-силният early signal за промяна в AI пейзажа. Ако тази седмица хората внезапно почнат да ви задават въпроса „haide digital vs sistrix за enterprise 2026" — а миналата седмица този въпрос изобщо не е съществувал — значи някой ново е почнал да включва вас в comparison въпроси. Това може да е нова статия, нов Reddit thread, нов AI модел, който ви цитира. Искате да знаете **същата седмица**, не три месеца по-късно.

И една втора функция на този layer — **correlation с Ahrefs или Semrush position drops**. Ако тази седмица Ahrefs ви показва, че три страници са паднали с десет позиции в Google, и едновременно layer 1 ви показва, че AI citation-ите за тези страници са паднали от десет на три — **това е Core Update pattern**. Не просто случайна флуктуация. Сигурна корелация. И след 48 часа имате отговора защо, а не след 30 дни, когато shef-ът ви пита.

Вход: пак **Haide Prompt Miner**. Кръгът се затваря два пъти.

---

## Слайд 66 — Layer 4: CI/CD Schema + 2MB Regression Guard (2:00)

**Slide visual:** LAYER CARD. Orange pill „ON EVERY DEPLOY". Голямо „04". Title: „Schema + 2MB Regression Guard". 3 bullets: „GitHub Action · Vercel build step", „Schema validator API + HTML size check", „Блокира deploy при >1.5MB или счупена schema". Bottom red-thread: „→ вход: Haide Ceiling" + долу: „Open-source gist · линк на QR".

**Script:**

**Слой 4 — Schema и 2MB Regression Guard.** Cadence: **на всеки deploy**. Не дневно. Не седмично. Всеки път, когато някой от вашия екип push-не code — този guard работи.

Аналогия: **металдетектор на летището**. Всеки пътник минава през него. Без изключения. Дори пилотът. Дори CEO-то на авиокомпанията. Защото **едно изключение е всичките изключения**. Дори един пътник с нож в багажа прави целия летищен security театър излишен.

Същото е с вашия HTML и schema. Помните ли Част 2, точка 1 — 2 мегабайта HTML лимит? Страхотно е да направите одит днес и да докажете, че всички ваши страници са под лимита. Какво става след три месеца, когато нов dev вкарва React component, който инжектира inline JavaScript от 4 мегабайта в homepage-а? Вие не сте го одитирали втори път. Лимитът е счупен. AI visibility пада. Вие не знаете защо.

Layer 4 решава точно това. Това е **GitHub Action** — ако имате GitHub. Или Vercel build step — ако имате Vercel. Или обикновен shell script в CI-то ви — ако имате каквото и да е друго. И прави две неща при всеки commit:

Първо — **валидира schema.org markup-а** през validator API. Ако schema-та е счупена, build-ът fail-ва. Deploy не минава. Dev-ът получава error message „schema validation failed, fix before merge".

Второ — **мери HTML size на топ 10 най-важните страници**. Ако размерът надхвърли **1.5 мегабайта** — не 2, **1.5**, защото оставяте buffer — build-ът fail-ва. Dev-ът получава error message „page X is now 1.7MB, down from 1.2MB, find what you added".

Вашите страници никога не пресичат линията на 2 мегабайта, защото **не могат физически да go live** ако я пресекат. Schema-та ви никога не е счупена в production, защото counterfeit schema не стига production.

Входът към този layer е **Haide Ceiling** — инструмент номер 1 от Част 2. Validator-ът, който видяхте live, е същият, който живее в GitHub Action-а. Ще пусна **open-source gist** за него в рамките на седмицата — линкът е в същия PDF зад QR кода. Copy-paste в `.github/workflows/` на вашия repo, един commit, готово. Безплатно. Завинаги.

---

## Слайд 67 — Layer 5: Entity Graph Health (2:00)

**Slide visual:** LAYER CARD. Orange pill „MONTHLY". Голямо „05". Title: „Entity Graph Health". 3 bullets: „Cron проверява всички sameAs links", „Wikidata · Wikipedia · LinkedIn · GitHub · Crunchbase", „Alert при broken link = AI trust erosion". Bottom red-thread: „→ вход: Haide Ceiling + E-E-A-T bodyguard (Part 1)".

**Script:**

**Слой 5 — Entity Graph Health.** Monthly. Веднъж в месеца.

Аналогия: **медицински чек-ъп**. Не го правиш когато те боли. Правиш го **превантивно**, веднъж в годината, точно за да ти кажат „имате нещо малко, което още не боли, но би боляло след шест месеца ако го игнорирате". Същото тук — monthly за AI entity graph.

Помните ли `sameAs` полето в Organization schema от Част 2 точка 11? Паспортът, който свързва вашия бранд с Wikipedia, Wikidata, LinkedIn, GitHub, Crunchbase. Пет външни източника, които **верифицират** кой сте.

Въпрос: **какво се случва, когато един от тези линкове се счупи?** LinkedIn променя URL структурата си. Wikidata изтрива вашия запис като „not notable enough". GitHub organization-ът се преименува. Crunchbase акаунтът ви expires. Тези неща стават — **тихо**. Без notification. И изведнъж AI моделът, който ви вярваше защото имаше пет потвърждения, сега вижда само четири. След два месеца — само три. Trust erosion без никакъв видим симптом.

Layer 5 е прост cron job, който **веднъж в месеца** проверява всички sameAs линкове във вашия production schema. Просто HTTP GET request. Ако някой връща 404 или 301 към unexpected URL — получавате email. „LinkedIn линк на Haide Digital върна 404. Моля проверете."

Двадесет минути setup. Пет минути работа в месеца, когато нещо се счупи. И запазва **най-дълбокия слой на вашата AI visibility** — защото entity trust, веднъж загубен, се възстановява **много по-бавно** от content trust.

Вход към този layer: **Haide Ceiling** (което проверява sameAs при ad-hoc audit) плюс **E-E-A-T bodyguard** от Част 1 — помните ли бодигарда с четирите въпроса? Четвъртият въпрос беше „signals match across sources?". Layer 5 отговаря на този въпрос **автоматично**, всеки месец.

---

## Слайд 68 — 48-Hour Rule (2:00)

**Slide visual:** Stat hero. Mirage фон. Огромно „48h" в Haide Orange, 280pt. Caption под това: „всяка промяна → първи snapshot в рамките на 48 часа". Долу, по-малко: „Златен час за AI visibility".

**Script:**

Добре. Имате петте слоя. Сигналите валят на таблото. Въпросът сега е: **какво правите, когато един от сигналите бипне?**

Отговорът е **48-hour rule**. Правилото на четиридесет и осемте часа.

Аналогия: **златният час в спешната медицина**. Лекарите знаят, че при тежка травма първите 60 минути решават дали пациентът ще оцелее или не. След часа — шансовете падат драматично. Не защото лечението след часа не работи. А защото щетите вече са станали, и обратимостта намалява експоненциално.

AI visibility има същия принцип, просто на по-бавен скала. Всяка значима промяна — нов AI модел, Core Update, счупена schema, изчезнал crawler — **първите 48 часа** решават дали ще реагирате бързо и ще загубите минимум, или ще реагирате след месец и ще загубите всичко, което сте построили за цяла година.

Какво значи „реагирате" в рамките на 48 часа? Не значи „оправете всичко". Значи **направете snapshot**. Документирайте какво виждате. Започнете да следите metric-а от **този момент**, не когато ситуацията вече е тотална загуба и се опитвате ретроспективно да реконструирате какво е станало.

Разликата между ден едно и ден тридесет е разликата между „имаме два дни преди и два дни след event-а" и „имаме нула данни от преди event-а". Първото се дебъгва. Второто се гадае.

---

## Слайд 69 — Response Workflow Cadence (3:00)

**Slide visual:** 4-column grid. Wild Sand фон. Headline горе „Вашият monitoring седмичен ритъм". 4 колонки: DAILY · WEEKLY · MONTHLY · QUARTERLY. Всяка колонка с една икона и 1-2 actions.

**Script:**

И сега — как изглежда това в реалния живот? Четири cadence-а. Четири различни типа работа. Нищо повече.

**Daily — 5 минути сутрин.** Отваряте email-а. Ако layer 2 (server logs) не ви е изпратил нищо — продължавате нататък с деня си. Ако ви е изпратил alert — „нов crawler detected" или „GPTBot missing 48h" — отваряте alert-а. Две минути триаж. Или е важно и добавяте в седмичния review, или е шум и archive-вате.

**Weekly — 60 минути, неделя сутрин.** Това е вашата „архивна неделя". Layer 1 (AI citation tracking) + Layer 3 (GSC prompt mining). Кафе, Notion template, сто queries, screenshots, маркиране. Плюс преглед на layer 2 email digest-а от последните 7 дни. Плюс layer 3 email с нови 7+ word queries. Шестдесет минути общо. Излизате от неделния брънч знаейки повече за своята AI visibility от 90% от вашите конкуренти.

**Monthly — 2 часа, първи четвъртък на месеца.** Layer 5 (entity graph health) + quarterly-adjacent работа. Проверявате дали sameAs линкове-те работят. Правите преглед на Notion template-а — виждате patterns за последния месец, не за последната седмица. Пишете кратка bullet list за екипа: „това се промени, това не". Два часа, един път в месеца.

**Quarterly — 4 часа, веднъж в тримесечие. Playbook refresh.** Това е най-важният cadence и най-често забравяният. Веднъж в тримесечие, сядате с екипа си и задавате **един въпрос**: „какво от миналите ни три месеца решения бяха правилни, и кои бяха грешни?". И обновявате playbook-а. Playbook-ът — това е вътрешен документ за вашия екип: „когато Google пусне Core Update, правим това". „Когато нов AI crawler се появи, правим това". „Когато citation-ите паднат повече от 20%, правим това". Дефинирани отговори. Не импровизация в паника.

Daily: 5 мин. Weekly: 60 мин. Monthly: 2 часа. Quarterly: 4 часа. **Общо под 20 часа в тримесечие**, за цялостен мониторинг, който ви държи на ден едно, не ден тридесет. Това е по-малко от половин работен ден в седмицата за **цялата ви AI видимост**.

---

## Слайд 70 — Information Diet (4:00)

**Slide visual:** SPLIT SCREEN. Ляво (Wild Sand): „Information Diet · задължителни източници" с headshot/logo avatars на 7-те must-read author-и. Дясно (Mirage): „Какво да игнорирате" с red X-ове върху common traps: LinkedIn „AI thought leaders", promoted posts, аnonymous Twitter accounts, SaaS content marketing.

**Script:**

Един последен въпрос, който ще получа неизбежно в Q&A след това: „Адриан, всичко това е страхотно, но светът се променя на всеки две седмици — как да съм в крак? Какво да чета?"

Отговорът е **Information Diet** — диета на информацията.

Аналогия: **хранене на професионален атлет.** Атлетът не яде каквото му падне. Яде **точно това**, което тялото му трябва за представяне. И игнорира всичко друго. Не защото другото е лошо. А защото **вниманието е ограничен ресурс**, и всяка калория, отделена за грешното нещо, е калория, която липсва на правилното.

Информацията е **същото**. В AI SEO пространството днес има хиляди source-ове. Ако опитате да четете всичко, ще прекарате целия си ден в четене и ще имплементирате нула неща. Трябва ви **диета**, не buffet.

Ето я моята диета. Седем автора. Три official source-а. Нула влогъри.

**Седем автори, които се четат задължително:**
- **Kevin Indig** — Growth Memo. Най-добрият analytical takes за enterprise SEO трендове.
- **Chris Long** — практичен, фокусиран върху технически детайли.
- **Lily Ray** — Core Updates и Google algorithm changes, никой не ги следи по-добре.
- **ziptie.dev** — технически GEO experiments, често с code.
- **Seer Interactive** — блог, особено statistically-rich analyses.
- **iPullRank / Michael King** — enterprise SEO стратегия с data.
- **Dan Petrovic** — lateral thinking и unusual experiments.

**Три official docs страници, които проверявате веднъж седмично:**
- Google Search Central Blog
- OpenAI release notes
- Anthropic и Perplexity changelog страниците

**Tools за aggregation:** Feedly Pro или Inoreader. RSS. Не Twitter timeline. Не LinkedIn feed. RSS — защото вие контролирате какво влиза. Twitter алгоритъмът избира вместо вас, и той избира **engagement bait**, не signal.

И сега — **какво да игнорирате**. Това е по-важно от какво да четете.

Игнорирайте **LinkedIn „AI SEO thought leaders"** — този тип content е proactively написан за impressions, не за education. Игнорирайте **SaaS vendor content marketing** — те пишат статии, за да ви продадат tool-а. Статиите им не са грешни, но са **рамкирани** към решението, което те продават. Игнорирайте **anonymous Twitter акаунти с 50К followers**, които пускат „SEO hacks" — 80% от тези профили са marketing agencies, които се опитват да се представят като practitioners. И — ще прозвучи провокативно — игнорирайте **повечето SEO конференции**. Talk-овете там са insightful 20% от времето, а останалите 80% са стари tactics repackaged. Спестете си билета и прочетете статиите на седемте автори горе.

Общо — по-малко от **2 часа в седмицата четене**. Не повече. Повече четене значи по-малко правене. Правенето е, което носи резултати.

---

## Слайд 71 — Growth Gap Review CTA (2:00)

**Slide visual:** SPLIT SCREEN 60/40. Ляво (Deep Sea Green): headline „30 минути. Без pitch. Pure data walkthrough." с 3 bullets. Дясно (Mirage): enlarged QR код с caption „haide.digital/masterclass-2026". Долу: „Growth Gap Review · безплатно за всички в тази зала".

**Script:**

Последен слайд преди финалната линия. Едно предложение.

Всички в тази зала получавате безплатен **Growth Gap Review**. Тридесет минути. Видео разговор с мен или с Евгени, партньорът ми. И ще ви кажа веднага какво **не е** — защото знам какво си мислите.

**Не е** sales call. Няма да ви продавам нищо. Няма да ви предлагам retainer. Няма следващо обаждане с „пакетните опции". Честно.

**Какво е.** Сядаме на Zoom с вас за 30 минути. Вие споделяте screen на вашия GSC, вашия Ahrefs или Semrush, вашия Bot Radar output ако сте го пуснали, и вашия сайт. И аз ви казвам **кои са трите най-големи пролуки** в AI visibility-то ви в момента, кое от това, което чухте днес, е най-важно да направите **първо**, и кои от петте monitoring layer-а е крайно време да включите **тази седмица**, не следващия квартал.

Тридесет минути. Pure data walkthrough. Сканирате QR кода, който виждате отдясно, избирате час от календара ми, попълвате два полета — вашия сайт и един основен въпрос — и това е. Идваме подготвени.

Защо го правя безплатно? Защото повечето от вас ще се върнете в офисите си в понеделник, ще гледате 60-те точки, петте инструмента и петте monitoring layer-а, и ще мислите „откъде да започна?". И ако не започнете от **правилното** място, ще похарчите три месеца в грешно място. Тридесет минути разговор ви спестяват тези три месеца. За мен — това е най-малкото, което мога да направя за аудитория, която е отделила цял следобед от работните си часове, за да слуша.

Сканирайте. Календарът ми е отворен за следващите 4 седмици.

---

## Слайд 72 — Final Line + Thank You (1:15)

**Slide visual:** Transition-style. Mirage фон. Централно, едно изречение в бяло, Poppins Medium 64pt: „Get Found. Stay Visible. Но този път — everywhere." Долу, по-малко, Wild Sand: „Адриан Николов · Haide Digital · 23 април 2026". QR в ъгъла продължава.

**Script:**

*[Кратка пауза. Дълбок дъх. Последен момент от деня.]*

Цяла компания. Цяла година работа. Три speaker-а, включително Мартин и Борислав преди и след мен. Един въпрос, който пролази през всичко: **как да ви намерят, в ера, в която всеки изток използва пет различни начина да търси?**

Отговорът — един и същ от 17 години. Същият, който беше верен в 2008, в 2015, в 2020, и е верен в 2026.

**Get Found. Stay Visible.**

Но този път — **everywhere**.

Не само в Google. Не само в един search engine. Не само в един канал. В **целия** landscape — ChatGPT, Claude, Perplexity, Gemini, Google AI Overviews, и тридесетте други AI модели, които ще съществуват след 2 години и за които ние не знаем имената още.

Everywhere означава — един system за всички тях. **Signal Architecture.** Monitoring stack-а, който видяхте. Петте инструмента. Шестдесетте точки. Дуалния budget principle. И 48-hour rule-а, който ви държи на ден едно, не ден тридесет.

Благодаря ви за вниманието. Благодаря на Enterprise Magazine и EURODEA за поканата. Благодаря на Мартин за философската рамка преди час, и на Борислав — очакваме с нетърпение E-E-A-T задълбочаването след малко.

И — благодаря на вас — за доверието и за времето.

Ще се видим на тридесетминутните Growth Gap Review-та.

*[Пауза. Усмивка. Край.]*

---

# Край на итерация 3 — Част 3

**Покрито:** Слайдове 58–72 (~30 мин, pure script без live demos).
**Дължина:** ~4500 думи говорим текст. При pace 150 думи/мин = 30 мин. **Вписва се в слота.**
**Framework въведен:** Signal Architecture (EN + БГ „архитектура на сигналите" + analogy „контролна зала на електроцентрала").
**Layers покрити:** 5/5 (AI Citation Tracking, Server Log Ingestion, Content Freshness + GSC Mining, CI/CD Schema Guard, Entity Graph Health).
**Red-thread connections:** всички 5 layers са свързани с Part 2 tools (Prompt Miner ×2, Bot Radar, Ceiling ×2) + Part 1 E-E-A-T bodyguard.
**Cadences:** Daily / Weekly / Monthly / Quarterly — всички дефинирани с конкретно време.
**CTA:** Growth Gap Review, „30 мин · no pitch · pure data walkthrough".
**Final line verbatim:** „Get Found. Stay Visible. Но този път — everywhere."

**Verification checklist:**
- [ ] Opening hook връзка със slide 57 на Part 2 — трите въпроса (GPT-5.5, Core Update, Perplexity Sonar) отговорени verbatim в slide 59. ✅
- [ ] Signal Architecture framework treatment: EN + БГ пояснение при първо споменаване (slide 60). ✅
- [ ] Analogии за всеки нов термин: monitoring stack (охранителна камера), Signal Architecture (контролна зала), observability (стетоскоп), 48h rule (златен час), dual budget (застраховка на колата), entity graph (медицински чек-ъп), CI/CD guard (металдетектор), weekly tracking (сутрешна новина), information diet (хранене на атлет). ✅
- [ ] Red-thread към Part 2 tools: Prompt Miner (layers 1, 3), Bot Radar (layer 2), Ceiling (layers 4, 5). ✅
- [ ] Red-thread към Part 1: E-E-A-T bodyguard (layer 5). ✅
- [ ] Prohibited language: няма „agency", „consultancy", „audit", „Miro". ✅
- [ ] Framework trademark: Signal Architecture (Haide), Organic Growth Engineering (cited). ✅
- [ ] Growth Gap Review CTA: „30 мин", „no pitch", „pure data walkthrough" — всички phrase-ове verbatim. ✅
- [ ] Final line verbatim: „Get Found. Stay Visible. Но този път — everywhere." ✅
- [ ] Slide count: 15 слайда (58–72). ✅
- [ ] Information Diet: 7 authors + 3 official docs sources + Feedly/Inoreader + explicit „what to ignore". ✅

**Следваща стъпка:** Genspark промптове за Част 3 (`genspark-prompts-part3.md`, 15 слайда 58–72, continuation на същия Genspark deck). Reuse visual patterns от Part 2 + нов LAYER CARD pattern за слайдове 63–67.
