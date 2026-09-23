# 06 — Systematic Grammar & Usage Errors (line-editing taxonomy)

Scope: recurring, *mechanical or near-mechanical* errors in the manuscript. The findings come from a close read of S03, S08 and S09 (ch16–23, ch57–70 and ch71–85, about 28k words) and from regex/python counts over all 1,597 paragraphs in `$WORK/paras.json`, with formatting counts taken from `/home/user/dad-book/book.md`.
Vocabulary malapropisms ("orotund", "jejune", "apposite", "schmaltz") are touched on only where they are collocation or real-word-typo errors. Another report covers register and diction.

How to reproduce a count: `python3 g.py '<regex>' <N>`. The helper script (scratchpad `g.py`) runs the regex over `paras.json` and prints `[P###]` hits plus a total. "Est." means that the regex is a heuristic and that I adjusted the total after manually reviewing its hits.

**Ranking** = (book-wide frequency) × (how badly it marks the prose as non-native or unedited to an agent's eye). Section numbers are the rank.

| # | Pattern | Est. book-wide | Mechanical? |
|---|---|---|---|
| 1 | Missing indefinite article ("few feet", "little out of place", "couple of", "lot of") | ~130 | Mostly yes |
| 2 | Dialogue punctuation and quote-mark hygiene | ~250 punctuation faults + 111 mismatched quote pairs | Yes |
| 3 | Comma splices and fused sentences | ~60–80 | Semi |
| 4 | Missing possessive 's / stray apostrophes | ~70 | Yes |
| 5 | Preposition and verb-complement errors | ~110 | Yes (pattern list) |
| 6 | Tense: present-tense slips, "would" in time/if clauses, missing past perfect, would/will in speech | ~90 | Semi |
| 7 | Missing comma after an introductory clause | ~60–75 | Yes |
| 8 | Collocation / idiom errors | ~100 | Semi |
| 9 | Typos, misspellings, real-word errors, name inconsistencies | ~60 | Yes |
| 10 | Agreement and number (incl. uncountables as plurals) | ~25 | Yes |
| 11 | Pronoun-reference ambiguity | ~25 | No (judgement) |
| 12 | Word-order faults (inversion, embedded questions, "the more…the more", "ensure to") | ~30 | Yes |
| 13 | Dangling / misattached modifiers | ~10 | Semi |
| 14 | Fragments that don't work; "Though…, yet" | ~12 | Semi |
| 15 | Capitalisation | ~40 | Yes |
| 16 | Superfluous "the" / hyphenation of compound modifiers | ~30 | Yes |
| 17 | Formatting and house-style inconsistencies | ~600 (whitespace) + headings/datelines | Yes (scriptable) |

---

## 1. Missing indefinite article (a/an) before quantifiers — ~130

**Description.** This is the author's single most frequent error. "Few" and "little" are used without "a" where the sense is *some* rather than *hardly any*. The article is also dropped from "couple of", "lot of", "such + singular noun" and "next/past/first few". The result reads like translation.

**Frequency and regexes.**
- `(?<!\ba )(?<!\bA )(?<!\bthe )(?<!\bvery )(?<!\bso )(?<!\btoo )(?<!\bquite )(?<!\bThe )\b[Ff]ew\b` gives **111 bare "few"**, against 77 correct uses (a few / the few / very few). About 10 of the 111 are legitimate "few = not many" (ch 5, ch 16, ch 19, ch 22, ch 33 "the fittings were few"), so **~100 need "a"**.
- The article is also missing from "next/past/first few": **7** (ch 9, ch 13, ch 18, ch 21, ch 24, ch 49, ch 73).
- `\b[Ll]ittle (shy|out|further|less|more|away|busier|over|differently|startled|embarrassed)\b` without "a" gives **15** (ch 2, ch 2, ch 4, ch 8, ch 12, ch 13, ch 19, ch 21, ch 24, ch 37, ch 67, ch 78).
- `(?<!\ba )\b[Cc]ouple of\b` gives 3 real errors (ch 18, ch 32, ch 73). `(?<!\ba )\b[Ll]ot (of|had)\b` gives 4 (ch 9, ch 14, ch 18, ch 85).
- `\bsuch (?!a |an )\w+ (manner|hour)\b` gives 5 (ch 3, ch 8, ch 38, ch 62, ch 83).
- `\b(in|for) (next|past) …` without "the" gives 5 (ch 13, ch 21 ×2, ch 73). Also "It was wee hours / early hours" (ch 19) and "at far left" (ch 20).

**Examples.**
- (ch 1) "The car came to a full stop few feet away from the town square."
- (ch 2) "was looking little out of place in her gorgeous black evening gown."
- (ch 17) "She was confident for few reasons."
- (ch 18) "After about couple of long minutes he stated…"
- (ch 78) "The drive to Smolensk was little less than an hour."
- (ch 83) "It was unlike Benedikt to act in such imprudent manner."

**Fix pattern.**
- few → **a few** unless the sense is clearly negative ("there were few people on the streets" stays).
- little + adj/adv/prep → **a little**.
- couple of → **a couple of**. lot of → **a lot of**; "lot had happened" → **a lot had happened**.
- such X → **such an X**.
- in next few hours → **in the next few hours**. First few months → **The first few months**.
- Litmus test: if "a small number of / a small amount" fits, add "a". If "hardly any" fits, leave it.

---

## 2. Dialogue punctuation and quote-mark hygiene — ~250 + 111 mismatched pairs

**Description.** Speech tags are punctuated at random: a comma is often missing before the closing quote, a full stop is used before a lowercase tag, tag commas sit outside the quotes, and there is no comma between the tag and the opening quote. Speech that begins a new sentence often opens in lowercase. Straight and curly quotes are mixed inside the same paragraph, which leaves many quote pairs that don't match.

**Frequency and regexes.**
- No comma before the closing quote + tag: `[a-zA-Z0-9][”"] +(he|she|Benedikt|…|came|declared|blurted|said)\b` gives **25**. `[a-z]” (he|she|…)` gives 28.
- Full stop before a lowercase tag: `[.][”"] +[a-z]` gives **11**. Full stop + capitalised tag (`.” He said`, `.” The doctor announced`) gives **8+**.
- Comma outside the quote: `[”"],` gives **38**, against `,”` **21** (the order should be `,”`).
- No comma between the tag and the opening quote: `[a-z] [“"](?=[A-Za-z])` gives **52** (for example "whispered in a soft tone “Hold for a second”").
- Lowercase opening of a new utterance: `(?:^|[,:] )[“"][a-z]` gives **24** (about 20 are genuine; some are legitimate continuations).
- Straight `"` gives **285**, straight `'` **154**, against curly `’` 683. There are **111 mismatched pairs** (`“…"` or `"…”`), and **138 paragraphs** have unbalanced curly quotes.
- `!!` gives 12. A question mark closes a statement 6 times (ch 23, ch 60, ch 62, ch 69, ch 83, ch 81).

**Examples.**
- (ch 20) "“Go on” Benedikt senses were alert…" (no comma after the speech, and a missing possessive)
- (ch 21) "“Nothing so far.” came the reply from Damian."
- (ch 16) "he stated in a rough dejected tone, “why don’t you leave me alone."
- (ch 63) "“…I cannot turn the ship.” He said with a flat voice."
- (ch 60) "“Why don’t you go and look for yourself,” his tone was overtly casual?"
- (ch 21) "“Damn!! I was this close from nabbing her!!”"

**Fix pattern.**
- `“Speech,” he said.` / `“Speech?” he asked.` / `“Speech.” He turned away.` An action beat is its own sentence.
- A tag followed by speech takes a comma: `he whispered, “Hold on.”`
- A new utterance starts with a capital. A continuation after a mid-sentence interruption stays lowercase.
- Run a global conversion to curly quotes (U+201C/U+201D, U+2018/U+2019) and then fix pairs by hand in the 111 flagged paragraphs.
- Reduce `!!` to `!`. Replace a question mark on a declarative sentence with a full stop, or rephrase it as a real question.

---

## 3. Comma splices and fused (run-on) sentences — ~60–80

**Description.** Two independent clauses are joined with only a comma, often three or four in a row. There is also a fixed fused pattern, "He looked at his watch it was…", where no punctuation joins the clauses at all.

**Frequency and regexes.** A tight heuristic, "sentence starts subject+verb … `, (he|she|it|they|there|his X) (was|had|…)` with no conjunction before it", returns 27 hits and ~17 true splices. A loose version returns 113 hits and ~35% true. The sample rate gives **~60–80 book-wide**. The fused watch pattern, `looked at his watch (it|and time) was`, gives 3 (ch 20, ch 21).

**Examples.**
- (ch 3) "Her time was running out, she had to get out of the place before the break of the dawn."
- (ch 19) "There was a big apartment complex on the left, he peeked at the entrance as he went past it…"
- (ch 19) "Sure, enough the lights were off, and his conjecture was accurate, they were reposing."
- (ch 20) "Benedikt looked at his watch it was 4:00 AM in the morning."
- (ch 83) "Benedikt reversed the car with urgency, the tires made a screeching sound as he drove…"
- (ch 38) "Francis was clueless, he was frustrated, but all he could manage was a nod…"

**Fix pattern.** Use the lightest repair that keeps the author's rhythm: (a) a semicolon where the clauses are tightly linked; (b) "and"/"but"/"so"; (c) a full stop. Watch pattern: "He looked at his watch: it was 4:00 AM." For a list of short clauses (ch 38, ch 39), keep the list but make it grammatical: "Francis was clueless and frustrated, but…"

---

## 4. Missing possessive 's, and stray apostrophes — ~70

**Description.** Character names and nouns are used attributively without 's, which yields "Benedikt turn", "Sanchez agitation" and "the guard voice". The reverse also occurs: apostrophes are added to plain plurals or to verbs.

**Frequency and regexes.**
- `\b(Benedikt|Sanchez|Maxwell|Stephen|Daniel|Damian|Kosovo|Jules|…|waitress|guard|doctor) (presence|tone|mind|face|annoyance|disappearance|curiosity|voice|turn|eyes|lips|senses|ego|hopes|countenance|uneasiness|vigilance|anxiety|agitation|last|house|mother|study|…)\b` gives **69 hits**. After removing ~8 false positives ("giving Damian jitters", "made Sanchez smile", "police officer friend", "the whole Sanchez episode"), about **~60 are real**.
- Time nouns: `\b(day|evening|days) (commotion|episode|proceedings)\b` gives 4 (ch 57 "the day commotion", ch 58 "the previous day episode", ch 66 "the past few days proceedings", ch 67 "the last evening episode").
- Stray apostrophes: `\w+s[’'] (significantly|set)` gives 2. `[A-Z]\w+[’']s(?= in|\.)` gives 3 (ch 26 "the Roberto’s", ch 59 "TransPacific’s in the court", ch 61 "Maserati’s").

**Examples.**
- (ch 2) "When Benedikt turn came, he raised the bet…"
- (ch 2) "The waitress eyes were infusing an exquisite smile…"
- (ch 21) "“Isn’t Sanchez last name also Roberto?”"
- (ch 60) "the guard voice was firm"
- (ch 2) "With other players’ significantly down…"
- (ch 17) "helped the participants’ set up their presentation"

**Fix pattern.** Name + noun that it owns → **Name’s** (Sanchez’s, Jules’s: pick one form for s-final names and keep it). Time phrase → **the day’s commotion, the previous day’s episode, the past few days’ proceedings, the previous evening’s episode**. Remove the apostrophe from plurals and verbs (players, participants, Robertos, Maseratis, TransPacific).

---

## 5. Preposition and verb-complement errors — ~110 across ~30 recurring frames

**Description.** The author has a stable set of wrong prepositions, missing particles and wrong complements. Because each frame repeats, the whole class can be fixed mechanically from a list.

| Frame (regex) | Count | Example | Fix |
|---|---|---|---|
| `pick(ed)? (the\|his\|her\|a)` without **up** | 14/15 (the book never uses "picked up") | (ch 21) "no one picked the phone"; (ch 20) "picked his travel bag" | picked **up** the phone / answered |
| `continued further` | 20 | (ch 76) "Benedikt continued further," | continued / went on |
| `mention(ed)? about`, `explained about`, `regretted about`, `confirmed about`, `least mentioned about` | 8+ | (ch 80) "I mentioned about Daniel"; (ch 63) "Finch regretted about the way…" | drop "about" |
| `gaz(e\|ing) the` | 4 | (ch 16) "kept gazing the floor"; (ch 80) "gazing the lone road" | gazing **at** |
| `(knock\|tap)(ped)? the … door` | 2 | (ch 65) "decided to knock the bedroom door" | knock **on** |
| `insist(ed)? (her\|Sanchez\|you) to` / `insist to` | 4 | (ch 73) "He insisted Sanchez to rest"; (ch 74) "insist to come" | insisted **that** Sanchez rest / insisted **on** coming |
| `demanded (him\|her) to`, `inhibiting them to` | 5 | (ch 78) "the situation demanded him to exhibit" | required him to / **from** speaking |
| `good in` (skill) | 4 | (ch 59) "I am good in accounting"; (ch 17) | good **at** |
| `preferr?ed … than` | 2 | (ch 1) "preferred their shelters than the road"; (ch 53) | preferred X **to** Y |
| `enamou?red by` | 2 | (ch 2), (ch 49) "enamored by his charm" | enamored **of/with** |
| `Sitting left to` | 1 | (ch 2) "Sitting left to Robinson was Andrea" | **To the left of** Robinson sat Andrea |
| `across (him\|her\|them)` (position) | ~5 | (ch 16) "sat on the chair right across him" | across **from** him |
| `seeking for`, `eyeing for` | 2 | (ch 16), (ch 59) | drop "for" |
| `reach to`, `answer the police` | 3 | (ch 17) "a medium to reach to Evan Slender"; (ch 16) | reach; answer **to** the police |
| `comprised of` | 1 | (ch 17) | comprised / consisted of |
| `succeed(ed) getting/to/from` | 3 | (ch 66) "succeeded getting on"; (ch 79) "succeeded from not breaking down" | succeeded **in** getting; managed **not to** break down |
| `averse from`, `deter X to`, `close from` | 3 | (ch 67), (ch 84), (ch 21) | averse **to**; deter X **from** putting; close **to** |
| `go/went pass` | 5 | (ch 8), (ch 30), (ch 40), (ch 50), (ch 71) | go/went **past** |
| `at loose`, `in the same lines`, `by any score`, `trust on` | 4 | (ch 85), (ch 62), (ch 18), (ch 64) | **on the** loose; **along** the same lines; **on** any score; trust **in** |
| `on (his\|her) mind` = *in* the mind | ~6 of 9 | (ch 62) "replaying the plan on her mind" | **in** her mind |
| `explain you` | 1 | (ch 15) | explain **to** you |
| `enquired her about` | 1 | (ch 18) | asked her about |
| `disembarked the taxi` | 1 | (ch 19) | got out of the taxi |
| `(accepted\|concluded\|detested the idea\|interested\|assured) to V` | 6 | (ch 69) "accepted to come along"; (ch 85) "not interested to let Daniel go"; (ch 74) "concluded to exercise" | agreed to come; interested **in letting**; decided to; hated the idea **of meeting** |

**Fix pattern.** Apply the table. When unsure, choose the standard British/US literary collocation and keep the author's verb.

---

## 6. Verb tense and form — ~90

### 6a. Present tense leaking into past narrative / failed back-shift — ~25

**Description.** In past-tense narration, subordinate clauses of reported thought slip into the present ("once he leaves", "until she meets", "provided he gets"). Occasionally a main verb slips too ("He puts the spread", "she rejoinders").

**Regex.** Quotes are stripped first, then `\b(he|she|they|it|Name)\s+(is|are|has|does|leaves|meets|gets|becomes|succeeds|shows|misses|earns|comes|wants|puts|rejoinders|…)\b` returns 31 hits, of which ~25 are real in narration.

**Examples.**
- (ch 1) "He puts the spread on the table before waking everyone."
- (ch 2) "she rejoinders with a distinct smile"
- (ch 20) "If he leaves now he can be in Zurich by 6:30."
- (ch 69) "She couldn’t leave the ship until she meets Albert."
- (ch 69) "why she becomes bereft whenever it concerns Benedikt?"
- (ch 83) "He knew once he is in Russia Maxwell could do no harm."

Also ch 2, ch 8, ch 15, ch 18, ch 30, ch 49, ch 50, ch 69, ch 74, ch 78, ch 79, ch 81, ch 83 and ch 85.

**Fix.** Back-shift one step: leaves → left, can → could, is → was, meets → met, will → would. For habitual past (ch 1), use "He **would put** / He put". "Rejoinders" is a noun, so use "**rejoined**".

### 6b. "would" inside time / condition clauses — ~15

**Regex.** `\b(until|unless|once|when|before|after|if)\b (\w+ ){1,3}would` returns 21 hits, ~15 real.

**Examples.**
- (ch 2) "no one could leave until one of them would be declared the winner"
- (ch 4) "unless someone would be within few yards"
- (ch 43) "if he would have decided to stay close to her"
- (ch 69) "her safety could be only confirmed when she would leave the ship"
- (ch 85) "Once he would secure their safety, he would think…"
- (ch 84) (dialogue) "If we would have killed him at that time…"

Also ch 24, ch 25, ch 30, ch 32, ch 36, ch 42, ch 51 and ch 68.

**Fix.** Use the simple past or the past perfect in the subordinate clause: "until one of them **was** declared", "unless someone **came** within a few yards", "if he **had** decided", "when she **left**", "Once he **had secured**", "If we **had** killed him".

### 6c. Missing past perfect for earlier events — est. ~40

**Regex.** This is not reliably greppable. Probes: `It was over \w+ (days|minutes) she was`, `was in this room many times`, `the car was returned`, `he implanted the day before`.

**Examples.**
- (ch 21) "the car was returned a while back" → had been returned
- (ch 22) "the transmitter he implanted the day before" → had implanted
- (ch 59) "It was over twenty minutes she was into it" → She had been at it for over twenty minutes
- (ch 71) "It was over three days she was on that ship" → She had been on that ship for over three days
- (ch 82) "He was in this room many times before" → had been
- (ch 71) "A lot happened since she had boarded" → had happened

**Fix.** A past action before the narrative "now" takes had + participle. It is usually enough to use one "had" to open a flashback and the simple past after that.

### 6d. would/will and had in dialogue — est. ~15

**Examples.**
- (ch 16) "soon you would need to answer the police" → will
- (ch 16) "No one would know anything." → will
- (ch 85) "the Russians would be at loose" → will be on the loose
- (ch 83) "His men had shot me once" → shot
- (ch 85) "I had collected enough evidence" → I have collected

**Fix.** In speech, use will for the future and the simple past or present perfect for completed events.

### 6e. Wrong verb forms — ~15

**Examples.**
- (ch 3) "made her fell on his lap" → fall
- (ch 2) "to raised the stake" → raised the stake
- (ch 69) "She was struggled hard" → struggled
- (ch 66) "He retrospect on" → He looked back on / reflected on
- (ch 36) "How dare you entered" → enter
- (ch 19), (ch 59) "reality sunk in" → sank
- "sprung" as a past tense: 6 (ch 3, ch 25, ch 37, ch 40, ch 43, ch 49) → sprang
- "laid back / laid flat" (ch 28, ch 36) → lay back / lay flat
- Participial adjectives: "firmed tone" (ch 22, ch 23) → firm; "keep his stature calmed" (ch 21) → calm; "with dwindled hope" (×4: ch 2, ch 7, ch 12, ch 15) → dwindling hope

---

## 7. Missing comma after an introductory clause — ~60–75

**Description.** Long introductory subordinate clauses or participial phrases run straight into the main clause. This causes misreadings ("While she was languidly flipping through the pages something caught her attention").

**Regex.** Sentences (quotes stripped) that start with `When|While|As|After|Before|Once|If|Though|Although|Since|Because|Despite|Without|Upon|With|Seeing|Hearing|Knowing|Taking|Watching`, are 9 words or longer, and contain no comma: **77 of 513** such sentences (15%). A handful of short prepositional openers are acceptable without a comma.

**Examples.**
- (ch 16) "While she was languidly flipping through the pages something caught her attention."
- (ch 1) "While the Roberto family was expecting this to be yet another Sunday of love and bonding little they knew…"
- (ch 19) "After passing the first two blocks he saw the car neatly parked…"
- (ch 25) "As he walked across the waiting area his wary eyes caught some unusual activity."
- (ch 43) "As he regained his senses he became aware that he was captured."
- (ch 77) "After a mile long run she looped back to the hotel…"

**Fix.** Put a comma at the end of any introductory clause that has its own verb, or of any introductory phrase over about 4 words. Also add the comma after one-word or elliptical openers that currently lack one ("Frustrated she decided…" (ch 62), "Once convinced she emailed…" (ch 13)).

---

## 8. Collocation and idiom errors — ~100

**Description.** The author reaches for an idiom and gets one element wrong, or builds a stock collocation that native prose does not use. These are highly visible to a reader. Each one needs a like-for-like idiomatic substitute, not a paraphrase.

| Pattern (regex) | Count | Example | Fix |
|---|---|---|---|
| `pass(ed)? a … (smile\|grin\|look)` | 11 | (ch 22) "he passed a gentle smile" | gave / flashed a smile; smiled gently |
| `was at the extreme` | 7 | (ch 63) "Benedikt’s aggravation was at the extreme" | was at its peak / had reached its limit |
| `(the\|his\|her) stature` = composure/body | 7 | (ch 59) "to calm her stature"; (ch 76) "a glimpse of his stature" | calm herself; his face/figure |
| `(went\|swung\|sprung) to action` | 5 | (ch 63) "He went to action" | sprang into action |
| `impos(e\|ing) … questions/requests` | 4 | (ch 21) "impose few questions to Damian" | put a few questions to |
| `took a sigh of relief` | 2 | (ch 23), (ch 3) | breathed / heaved a sigh of relief |
| `took (the) decision` | 2 | (ch 19), (ch 40) | made the decision |
| `put a deaf ear` / `fell on the deaf ears of` | 3 | (ch 24), (ch 85), (ch 61) | turned a deaf ear to; fell on deaf ears |
| `multi-fold` | 4 | (ch 2), (ch 23), (ch 53) | manifold / many times over |
| `held to its spot` | 1 | (ch 1) "the Land Rover held to its spot" | held its spot / stayed put |
| `broke the monotony` (= silence) | 2 | (ch 61), (ch 76) | broke the silence |
| `(good\|patient) listening` | 2 | (ch 69) "give me a good listening" | hear me out |
| `(He\|she) sure (was\|had)` | 9 | (ch 21) "He sure wasn’t a happy campaigner" | He certainly wasn’t a happy camper |
| `invariably` = inadvertently/repeatedly | 6 | (ch 61) "the words came out invariably" | involuntarily / unbidden |
| `at her wits` | 1 | (ch 58) | at her wits’ end |
| `splitting hair`, `epiphany moment`, `denouncing her defeat`, `hard bolts` | 4 | (ch 17), (ch 16), (ch 17), (ch 16) | racking her brains; an epiphany; admitting defeat; hard knocks |
| `the same` as pronoun | 3 | (ch 18) "custodian of the same" | of it |
| `with a … (tone\|voice)` | 104 | pervasive | not an error, but vary with "in a … voice" |
| `blurted` | 56 | pervasive tag | not a grammar error; flagged for the diction report |

---

## 9. Typos, misspellings and real-word errors — ~60

**Method.** A spell-check pass extracted all distinct tokens and checked them against the `pyspellchecker` English dictionary. That gave 183 unknown tokens, which I reviewed by hand: Portuguese/Danish/German dialogue, names and contraction stems (`couldn`, `wasn`) were excluded. Because a dictionary check can't catch real-word errors, I also ran a targeted confusable-word grep. `/usr/share/dict/words` is not present on this machine.

**A. Non-words and misspellings**

| Token | Where | Fix |
|---|---|---|
| Somlensk | (ch 83) (ch 84) (ch 85) (datelines) | Smolensk |
| Benedkit | (ch 78) | Benedikt |
| Curz | (ch 7) (elsewhere "Cruz") | Cruz |
| Gribin | (ch 15) (elsewhere "Girbin") | Girbin |
| Gydnia | (ch 72) | Gdynia |
| Liozona / Liozna | (ch 85) vs (ch 81) | Liozna (pick one) |
| Kroners / Kruns | (ch 4) / (ch 7); elsewhere "Kronor" | Kronor (confirm the street name) |
| badested | (ch 4) "executive floor’s badested ridge" | unclear, so query the author (probably "balustraded"?) |
| casted (adj.) | (ch 33) | cast |
| faired | (ch 13) "how she faired" | fared |
| gloomed | (ch 6) (ch 56) | gloomy |
| palpations | (ch 80) | palpitations |
| uncomforting | (ch 7) | discomfiting / unsettling |
| absolvent | (ch 43) | query (distraught?) |
| averseness | (ch 15) | reluctance |
| infuriation | (ch 25) | fury |
| slepp | (ch 31) "você slepp bem" (Portuguese) | "Você dormiu bem?" |
| inhabitation(s) | (ch 40) (ch 53) (ch 72) (ch 85) | inhibition(s) |
| disbelieve (as noun) ×7 | (ch 25) (ch 28) (ch 37) (ch 39) (ch 43) | disbelief |
| 5’0 Clock | (ch 72) "the 5’0 Clock green shadow" | five o’clock shadow |
| wrap-up / faceoff as verbs | (ch 59) (ch 61) / (ch 40) (ch 61) | wrap up / face off |
| over indulgent | (ch 16) | overindulgent |
| follow up (adj.) | (ch 80) | follow-up |

**B. Real-word errors (these pass a spell-checker)**

| Written | Intended | Where |
|---|---|---|
| right way | right away | (ch 2) |
| dames | madam / ma’am | (ch 2) "your drink dames!!" |
| statutes | statues | (ch 71) |
| discrete (×3) | discreet | (ch 9) (ch 25) (ch 50) (also "discrete steps" (ch 62)) |
| apposite (×2) | opposite? / accurate | (ch 17) "looking stark apposite", (ch 59) |
| complimenting | complementing | (ch 21) |
| despise | despite | (ch 18) "but despise the thoughts" |
| hangers | hangars | (ch 45) |
| weary steps | wary steps | (ch 75) |
| flair | flare (up) | (ch 63) "to flair her antsy emotions" |
| enquires | enquiries | (ch 61) |
| captivate / captivated (= capture) | capture / captured | (ch 21) (ch 76) (also "captivation" (ch 34)) |
| stooped | dropped | (ch 4) "The temperature had stooped" |
| hard bond books | hardbound books | (ch 17) |
| cobble-webbed | cobbled | (ch 71) |
| dejected the thought | rejected | (ch 80) |
| rationale argument | rational | (ch 84) |
| subornation | rumination | (ch 21) |
| definitive | definite / certain | (ch 34) |
| incidence (×4) | incident | (ch 18) (ch 22) (ch 25) (ch 42) |
| gore | blood | (ch 63) "He has lost a lot of gore" |
| put a coy / a drab / gutter it down | ploy / damper / dampen it | (ch 80) (ch 80) |
| chauffeured driven | chauffeur-driven | (ch 60) |
| Am I am avoiding | Am I avoiding | (ch 67) |
| a 6 feet frail looking | a six-foot, frail-looking | (ch 75) (also (ch 29)) |

**C. Facts and consistency found in the same pass** (hand these to continuity): "Stockholm, **Denmark**" ×7 in datelines (Stockholm is in Sweden; the ch2 casino scene reads as Danish, so check the city); "Range Rover" (ch 1) → "Land Rover" (ch 1); "‘Sub Rosa’" vs "‘sub rosa’" vs "“sub rosa”" ((ch 21) (ch 23)); "Market Square" (ch 67) vs "market square" (ch 69).

---

## 10. Subject–verb agreement and number — ~25

**Examples.**
- (ch 58) "The guards watching​ the area was puzzled" → were
- (ch 66) "the barriers he experienced all the while was nothing, but an illusion" → were nothing but
- (ch 24) "a corpulent person …, who with few of his companions were guarding" → was guarding, with a few of his companions,
- (ch 2) "she observed two things, which was different" → were
- (ch 31) "the paper he had scribbled were shredded" → papers … were
- (ch 2) "I like when someone put their mind to work" → puts

**Number errors on nouns**
- (ch 17) "the five division of TransPacific" → divisions
- (ch 17) "The forces of natures" → nature
- (ch 35) "every one of his belief" → beliefs
- (ch 15) "one of the agent’s phone" → one of the agents’ phones
- (ch 60) "serve the guest" → guests

**Uncountable nouns pluralised**
- "evidences" ×3 ((ch 75) (ch 84)) → evidence / pieces of evidence
- "reasonings" (ch 78) → reasoning
- "inhabitations" (see §9)

**Pronoun number**
- (ch 83) "get all the guns and put it in the car trunk" → them
- (ch 85) "The words found its way out" → their
- (ch 17) "recess lights … illuminating the room with its dim yellow glow" → their

**Regex probes.** `\b(evidences|reasonings)\b`; `\bwhich was\b` after a plural noun; `\bput it\b` after a plural noun. Most hits here came from reading.

---

## 11. Pronoun-reference ambiguity — est. ~25 (judgement call)

**Description.** "He/him/his" refers back to the wrong male character, often across a change of scene or speaker. The problem is concentrated in scenes with two or three men (Benedikt/Maxwell/Stephen, Benedikt/Anatoly, Maxwell/taxi driver).

**Examples.**
- (ch 79) "Sanchez's father was not in any confinement. During his conversation with Anatoly, he mentioned…" (he = Benedikt, but the father is the only male antecedent)
- (ch 80) "This time his grin faded permanently" (his = Anatoly; the previous subject is Benedikt)
- (ch 85) "She couldn’t believe Stephen would hide such a thing from **him**. … He knew if he escapes from the Russians, he would be followed" (him should be her; the first "he" is Benedikt and the second is Daniel)
- (ch 85) "took the seat next to him" (him = Benedikt; the last male mentioned is Stephen)
- (ch 19) "The cab arrived on time. He instructed him to turn on the ride meter"
- (ch 64) "Although she confirmed about her safety, he wasn’t convinced" (he = Maxwell; the last named male is Stephen)

**Fix.** Replace the first pronoun after any change of speaker or scene with the name. When two men are present, name one and use a pronoun for the other consistently. Don't overcorrect: the name should appear at most once per sentence.

---

## 12. Word-order faults — ~30

| Pattern (regex) | Count | Example | Fix |
|---|---|---|---|
| No inversion after a negative/limiting adverb: `(Never once\|little\|Neither) (he\|she\|they)` | 5 | (ch 60) "Never once she assumed"; (ch 1) "little they knew"; (ch 19) "Neither he had the verve, nor any energy" | Never once had she assumed; little did they know; He had neither the verve nor… |
| Embedded question inverted: `(know\|sure) (which\|what) \w* (are\|is) (they\|he)` | 2 + 2 | (ch 22) "I want to know which flight are they on?"; (ch 21) "not sure what are they constructing"; (ch 75) "Would you know where in Russia is, he?" | which flight they are on. / where in Russia he is? |
| Direct question not inverted | 2 | (ch 63) "How serious it is?"; (ch 67) "Why my heart breaks when he talks harshly?" | How serious is it? / Why does my heart break…? |
| Comparative correlative missing "the": `(, \|\. )(the )?[Mm]ore (he\|she)` | 7 | (ch 62) "The more she weighed the options, more she unraveled flaws"; (ch 47) "More she weighed on the thought, more she was convinced" | The more…, the more… |
| `ensure(d) (not )?to V` | 6 | (ch 1) "he ensured to make every minute… special"; (ch 78) "He ensured not look too persuasive" | made sure to…; took care not to look… |
| `than what` / `more … than` misuse | ~5 | (ch 50) "giving away way too much detail than what was required" | far more detail than was required |

---

## 13. Dangling / misattached modifiers — ~10

**Regex.** A sentence-initial participle or elliptical clause + comma + a non-person subject: `^(\w+ing|Once|Though|Seeing|…)[^,]{0,70}, (the|his|her|its|it|there)\b` returns 45 hits, ~8 real.

**Examples.**
- (ch 59) "Watching Benedikt entering the room, her feet turned cold"
- (ch 8) "Realizing his ruse worked, a sign of relief graced his visage."
- (ch 44) "Seeing her quivering with pain, the practicality of the situation sank in him."
- (ch 26) "Keeping the tradition of the Fado alive, there was a solo singer…"
- (ch 80) "The way his eyes rolled on him, it failed to abstain his wide grin." (both the attachment and the verb are wrong)
- (ch 68) "The dark clouds were looming over the rough sea made the port city look exquisite" (two finite verbs: → "The dark clouds looming over the rough sea made…")

**Fix.** Make the doer of the participle the grammatical subject: "Watching Benedikt enter the room, she went cold." "Realizing his ruse had worked, he smiled with relief."

---

## 14. Fragments that don't work; "Though…, yet" — ~12

**Examples.**
- (ch 1) "Brewing black coffee with select beans crushed at home, scrambled eggs, peanut butter sandwiches, and freshly squeezed orange juice." (a list with no verb)
- (ch 71) "…He was baffled and concerned. And promised himself to be extra prudent…" (no subject)
- (ch 85) "And promised if found guilty, he would not be spared."
- (ch 71) "Something she had learned about during her school days in Ayr." (acceptable as style, but here it follows a factual clause and reads as an error)
- (ch 16) "Though she had a new lead, yet there were more questions than answers." Also (ch 2).
- (ch 61) "Benedikt's suspicious behavior, her inability to quiz the workers and void of a no go-forward plan, she was like a boat…" (a hanging list followed by an unrelated subject)

**Regex.** `(?:^|[.!?] )And (promised|decided|…)` gives 2. `(?:^|[.!?] )Something (he|she|…)` gives 4. `(Though|Although)[^.]{3,80}, (yet|but)` gives 2.

**Fix.** Attach the fragment to the preceding sentence with a comma or dash, or give it a subject ("He promised himself…"). Delete "yet"/"but" after "Though/Although". Keep deliberate one-line fragments at chapter ends; they are part of the voice.

---

## 15. Capitalisation — ~40

| Pattern | Count | Example | Fix |
|---|---|---|---|
| `\bPounds\b` (currency) | 9 (vs "pounds" ×2) | (ch 2) "chips worth million Pounds" (also no article) | a million pounds |
| `Million` mid-sentence; `\d+M Pounds` | 1 + 2 | (ch 2) "7.5 Million pounds"; (ch 2) "10M Pounds"; (ch 17) "5M pounds" | 7.5 million pounds; £10 million (prose) |
| Lowercase start of an utterance after a tag | ~20 | (ch 16) “why don’t you…”; (ch 62) “would you have…” | capitalise |
| Capital after a speech tag or mid-sentence | ~15 | (ch 63) "…ship.” He said"; (ch 19) "Maxwell Parked the Audi"; (ch 63) "And Above all"; (ch 23) "Gosh Am I in love?"; (ch 16) "What Package?"; (ch 17) "One of the Judges"; (ch 21) "private transfer Tarmac"; (ch 61) "Jousting"; (ch 85) "Liozona Border" | lowercase |
| Common nouns inside place names | mixed | "Lisbon Airport"/"the airport", "Market Square"/"market square" | apply one rule: capitalise only official names |
| Rubles / Kronor | (ch 74) "500 Rubles" | lowercase currency names: 500 rubles |

**Regex.** `(?<=[a-z,;] )([A-Z][a-z]+)\b` where the lowercase form also appears ≥2 times gives the list above (manual review).

---

## 16. Superfluous "the"; hyphenation of compound modifiers — ~30

**Superfluous or odd "the"** (`\bthe (destiny|fate|reality|everything|shiver|break of the dawn)\b`): 9.
- (ch 77) "I will tell you the everything"
- (ch 72) "let the destiny lead us"
- (ch 42) "the fate had brought"
- (ch 73) "send the shiver through her spine" → a shiver
- (ch 3) (ch 72) "before the break of the dawn" → the break of dawn
- (ch 61) "fell on the deaf ears of Sanchez"

**Compound modifiers without hyphens**: `\b(strange|elderly|fragile|pretty|frail|disheveled) looking\b` gives 8 (ch 15, ch 22, ch 36, ch 37, ch 59, ch 74, ch 75), against 3 hyphenated. Also "mile long run" (ch 77), "night long brooding" (ch 71) and "a long fifteen minutes wait" (ch 74) (vs "fifteen minutes’ drive" (ch 61)). Fix: strange-looking, mile-long, night-long, fifteen-minute wait.

---

## 17. Formatting and house-style inconsistencies (book.md)

| Issue | Count | Evidence / regex | Fix |
|---|---|---|---|
| Double space at sentence breaks (a space plus a no-break space) | **217** sentence gaps; **190** space+NBSP pairs; 437 NBSP total | `[.!?”] ?\xa0 ?\S` | normalise to a single space; strip all U+00A0 from body text |
| Zero-width spaces | **12** | U+200B, e.g. (ch 58) "watching​ the area", (ch 58) "relieved​, she realized​" | delete |
| Trailing whitespace | **59** lines | `[ \xa0]+$` | strip |
| Stray `\` scene-break markers | **16** (11 standalone `**\**` lines + 5 glued to paragraph ends: book.md lines 291, 631, 2015, 2444, 2518) | `\*\*\\\*\*` | replace with one centred scene break (`* * *` or `#`) on its own line; remove the trailing ones |
| Chapter headings | 82 `**Chapter N**` + **3** with a trailing NBSP (`**Chapter N\xa0**`) + 1 trailing space ("Chapter 62 ") | | strip |
| Part headings | `**PART I**`, `**Part II**`, `**Part III**`, `**PART IV**`, `**PART V**` | `^\*\*(PART\|Part)` | one case throughout (PART) |
| Dateline style | **18** bold-italic with `<sup>` ordinals (ch1–18: `***6:00 AM 14<sup>th</sup> February 2010, …***`) vs **67** bold with plain ordinals (ch19–85: `**4:00 AM 15th April 2014, …**`); **6** have no time | `<sup>` count = 18 | pick one style (recommended: italic, no superscripts, "6:00 AM, 14 February 2010 — Girbin, Scotland") and apply to all 85 |
| Dateline typos and logic | "Somlensk" ×3; "Stockholm, Denmark" ×7; out-of-order dates (ch17 (ch 17) "1st May 2012" follows 18 June; ch22 "16th April" follows ch21 "17th April"; ch80 dated the same day as ch78 but narrated as "the next day") | | fix spelling; send the dates to continuity |
| Numbers | Small numbers in digits in narrative ×8 ((ch 9) "first 4 hours", (ch 19) "7-10 blocks … 8 apartments", (ch 66) "5 minutes", (ch 75) "6 feet") vs 143 in words; "160 KM/HR" (ch 21); "five KM" (ch 29); "few 100 US dollars" (ch 6) | `\b([2-9]\|1[0-9]) (minutes\|hours\|…)` | spell out numbers under 100 in prose; km/h; "a few hundred US dollars" |
| Redundant time phrase | 3 | "4:00 AM in the morning" (ch 20), "2:20 AM in the morning", "2:00 PM in the afternoon" (ch 34) | drop "in the morning/afternoon" |
| Dashes | spaced en dash ` – ` ×22 vs spaced hyphen ` - ` ×7 ((ch 1), (ch 2), (ch 47), (ch 72)…) | | one dash style (spaced en dash or closed em dash) |
| Ellipses | `...` ×8 vs `…` ×13 paras (mixed) | | one form |
| Spelling system | US spellings throughout (favor 14, realiz- 18, center 16, behavior 18) but "towards" 123/0, "amongst" 6, "enquire" 30 vs "inquire" 9, "grey" 3 vs "gray" 1, "gotten" 3, "Ok/ok" 9 vs "OK" 1 | | the house decision is US spelling (the manuscript's majority). Standardise enquire→inquire (or keep enquire, but only one), OK. Keep "towards" (acceptable in US literary prose) |
| Quote glyphs | straight `"` ×285, straight `'` ×154 | | convert all to curly (see §2) |

---

## Mechanical checklist for line editors (34 items)

Apply in order. Each item is a regex search plus a decision rule. **Stop and query the author** when the fix would change meaning.

1. [ ] Strip U+200B (zero-width spaces) and U+00A0 (NBSP); collapse multiple spaces to one; strip trailing whitespace.
2. [ ] Convert every straight `"` and `'` to curly; then open each paragraph with unbalanced `“`/`”` and fix the pairs.
3. [ ] Replace the 16 `**\**` markers with one standard scene-break line; delete the 5 glued to paragraph ends.
4. [ ] Normalise headings: `PART I`–`PART V`, `Chapter N`, no trailing spaces.
5. [ ] Normalise all 85 datelines to one format (no `<sup>`, same italics/bold, time always or never); fix "Somlensk", and flag "Stockholm, Denmark" and the out-of-order dates.
6. [ ] `\b[Ff]ew\b` without a/the/very: add "a" unless the meaning is "hardly any".
7. [ ] `\b[Ll]ittle (shy|out|further|less|more|away|over|busier|differently|startled|embarrassed)`: add "a".
8. [ ] `(?<!a )couple of`, `(?<!a )lot of`, `such + singular noun`, `in next/for past`: add the missing article.
9. [ ] Speech tags: `word” he said` → `word,” he said`; `.” he said` → `,” he said`; `.” He said` (tag) → `,” he said`; `”,` → `,”`.
10. [ ] Tag followed by an opening quote without a comma (`blurted “`, `tone “`): insert a comma.
11. [ ] Capitalise the first word of each new utterance; lowercase the tag verb after the closing quote.
12. [ ] `!!` → `!`; remove "?" from declarative sentences (ch 23, ch 60, ch 62, ch 69, ch 81, ch 83).
13. [ ] `Name + noun` possessive list (§4 regex): add 's; fix "day/evening commotion/episode/proceedings" → the day's… etc.
14. [ ] Remove apostrophes from plurals (players’, participants’, Roberto’s, Maserati’s, TransPacific’s).
15. [ ] `pick(ed) the/his/her` → picked up / answered.
16. [ ] Delete "about" after mention/explain/regret/confirm/discuss.
17. [ ] `continued further` → continued / went on.
18. [ ] `gazing the` → gazing at; `knock the door` → knock on the door; `good in` (skill) → good at.
19. [ ] `insisted X to` → insisted that X…; `demanded him to` → required him to; `inhibiting them to` → from speaking.
20. [ ] `preferred X than Y` → to Y; `enamored by` → enamored of; `across him/her` (seating) → across from.
21. [ ] `go/went pass` → past; `at loose` → on the loose; `close from` → close to; `averse from` → averse to.
22. [ ] Narration in the past: back-shift present verbs in subordinate clauses (once he leaves → left, until she meets → met, can → could, will → would).
23. [ ] `(until|unless|once|when|if) … would`: → simple past / past perfect.
24. [ ] Flashbacks: first verb → had + participle ("was returned a while back" → had been returned).
25. [ ] Dialogue future: "would" → "will" where the speaker means the future.
26. [ ] Verb forms: sprung → sprang; sunk in → sank in; laid back → lay back; firmed → firm; dwindled hope → dwindling hope; made her fell → fall.
27. [ ] Comma splices: in any sentence with two subject+verb clauses joined only by a comma, choose a semicolon, a conjunction or a full stop; "looked at his watch it was" → colon.
28. [ ] Introductory clause over 4 words, or with its own verb, and no comma: add a comma.
29. [ ] Collocation table (§8): passed a smile, at the extreme, stature, went/swung to action, impose questions, took a sigh, deaf ear, multi-fold, broke the monotony, good listening, "He sure".
30. [ ] Real-word error list (§9B): right way, dames, statutes, discrete, despise, hangers, weary, flair, enquires, captivate(d), incidence, gore, inhabitation(s), disbelieve (noun).
31. [ ] Name spellings: Smolensk, Benedikt, Cruz, Girbin, Gdynia, Liozna, Kronor (search each variant).
32. [ ] Plural/uncountable: evidences → evidence; the five division → divisions; "put it" after plural → them.
33. [ ] Negative inversion and embedded questions: Never once she… → Never once had she…; which flight are they on → which flight they are on; the more…, more → the more…, the more.
34. [ ] Mid-sentence capitals (Pounds, Million, Judges, Package, Tarmac, Parked, Above, Am, Jousting, Border) → lowercase; spell out numbers under 100 in narration; hyphenate "X-looking", "mile-long", "fifteen-minute".

*Don't mechanise:* pronoun reference (§11), danglers (§13), fragments (§14) and past-perfect insertion (§6c). Each needs a reading of the sentence in context. Flag them in the margin for the author instead.
