# Russian AI-writing markers

Companion to the 35 patterns in `SKILL.md`. Those describe English text; this file
describes what the same models produce in Russian.

Sources: [Википедия: Признаки сгенерированности
текста](https://ru.wikipedia.org/wiki/Википедия:Признаки_сгенерированности_текста), the Russian
counterpart of the English page the main skill is built on, plus a practitioner survey of markers
([vc.ru, 2026](https://vc.ru/ai/2936857-markery-neurosetevogo-teksta)).

Read this together with the main file. The structural patterns there — inflated importance, shallow
analysis, formulaic challenges-and-outlook, chatbot leftovers — appear in Russian unchanged. What
follows is what differs.

## 1. Vocabulary that signals inflated importance

**Watch:** играет важную / значительную / ключевую роль · подчёркивает / выделяет его важность ·
символизирует его устойчивое влияние · ключевой / поворотный момент · неизгладимый след ·
выступает / служит напоминанием · непоколебимо преданный своему делу · вековое наследие

Same failure as §1 in English: an ordinary fact is dressed as a turning point.

**Before:** Институт статистики Каталонии был основан в 1989 году, что стало поворотным моментом
в эволюции региональной статистики и подчеркнуло важность децентрализации.
**After:** Институт статистики Каталонии основан в 1989 году в ходе децентрализации управления.

## 2. Sales language

**Watch:** богатый, яркий, разнообразный · может похвастаться · продолжает очаровывать ·
потрясающая природная красота · расположенный в самом сердце · имеет художественное /
культурное значение

## 3. Verbs that animate the inanimate

**Watch:** обеспечивает · выделяет · подчёркивает · отражает · демонстрирует · содействует ·
соответствует

A fact or an event cannot *подчеркнуть* anything; only a person can. Russian Wikipedia names this
specifically: действия приписываются не людям, а фактам или событиям.

## 4. Verbal nouns opening a sentence

Russian editors avoid starting a sentence with a verbal noun (*обеспечение*, *проведение*,
*осуществление*); models do it constantly. **Before:** Осуществление проверки конфигурации
производится ежедневно. **After:** Конфигурацию проверяют каждый день.

## 5. Hedging and modality

**Watch:** может стать · может повлиять · способен обеспечить · призван решить · важно / необходимо
отметить · стоит учесть / запомнить · значения могут варьироваться

Keep a hedge the evidence requires. Cut the ones that only soften a claim nobody made.

## 6. Parallel constructions

**Watch:** Не только… но и… · Это не просто…, это… · Несмотря на… · сталкиваются с рядом проблем ·
Перспективы на будущее · В заключение · Подводя итог · Вкратце · В целом

*Не только… но и…* is ordinary Russian grammar. It is a tell only when stacked, the way §9 treats
*not X but Y*.

## 7. Synonym-swapping to avoid repetition

**Watch:** главный герой · ключевой игрок · ведущий персонаж, used in place of a name already
introduced.

Russian style tolerates repeating a name far better than English does. Models substitute an
epithet on every mention, which reads like a school essay. This is §11 in Russian dress.

## 8. Merism: false ranges

**Watch:** от лёгкого до тяжёлого · от классики до авангарда, where the two poles are not a real
scale. Same test as §12: does the range have a middle?

## 9. Rhythm

Two opposite failures, both current:

- **Even mid-length sentences** throughout, with no short ones and no long ones.
- **Chains of clipped fragments:** *Коротко. Точно. Отдельно.* — the 2025-2026 style, along with
  pseudo-Socratic *Зачем? Потому что.* and the therapeutic register *Ты не ошибаешься, что так
  чувствуешь.*

## 10. Word order

Russian permits inversion; models write rigid subject-verb-object as if translating from English.
A paragraph with no inversion at all reads translated. This has no English equivalent, because
English word order is fixed anyway.

## 11. Calques

**Watch:** основание науки (should be *основы науки*) · уточните маркетинговые усилия (should be
*доработайте маркетинг*) · релевантный опыт · сфокусироваться на

## 12. Missing idiom

Human Russian reaches for set expressions; models avoid them. Their absence across a long text is
weak evidence on its own, but it fits the pattern. Do not *insert* idioms to fake a voice — that
violates the skill's rule against inventing.

## Punctuation: what differs from §14, §17, §19

**Dashes (§14).** Both things are true, and the rule must hold both:

- The dash is **required** between nominals with no copula — *Москва — столица России* — and in
  dialogue attribution and generalizing constructions. Deleting it is a grammatical error.
- **Overuse is still a tell.** Russian Wikipedia: «ИИ злоупотребляют длинным тире (—), используя
  его шаблонно и слишком часто», because models trained on literary prose reach for a dash where a
  person would use a comma, parentheses or a colon.

So: keep every dash the grammar demands, cut the decorative ones. Do not run §14's blanket search
and delete over Russian text.

**Headings (§17).** Applies, and for the same reason English does not need it to. Russian headings
use sentence case, so a model writing *Ранняя Жизнь и Образование* is copying English title case.
Russian Wikipedia lists this explicitly.

**Quotation marks (§19).** Russian Wikipedia does not list quotation marks as an AI marker at all,
so treat this as typography rather than detection: Russian prose uses «ёлочки» with „лапки" nested.
Normalizing them to ASCII quotes is a downgrade, not a fix.

**Bold and lists (§15, §16).** Apply unchanged. Russian Wikipedia names the same two habits:
meaningless bolding, and list items that open with a bold heading and a colon.
