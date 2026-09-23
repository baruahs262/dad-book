# 01 — LEXICON & DICTION (The Last Scintilla)

Scope: full reading of S01 (ch 0–7), S04 (ch 24–30), S08 (ch 57–70). Counts come from regex and wordfreq
passes over all paragraphs in `paras.json` (81,793 running words). Counts are case-insensitive unless noted.
`[P###]` = paragraph id. Hit lists are cut off after the first dozen ids.

---------------------------------------------------------------------------------------------------

## 0. The short version (for editors in a hurry)

1. **Register:** ornate, Latinate and thesaurus-driven in narration. Dialogue is formal and rarely contracted
   ("I am" 118 : "I'm" 1; "let us" 22 : "let's" 0). The base grammar is **Indian English**: the article is dropped
   before "few" (~100 bare "few" vs 55 "a few"), the possessive 's is dropped (38 cases, e.g. "Benedikt turn"),
   "as per" 13, "zeroed down" 2, "since morning" 3, "till date" 1, "an old connect" 1, "evidences" 3,
   "miscreants" for criminals, "passed a smile" 10, "mentioned about" 4. The brief's examples "prepone", "revert",
   "do the needful" and "kindly" occur **0 times**. "ensured to" occurs **2** times [ch 1, ch 22]. "the eerie" as a
   noun occurs 3 times [ch 1, ch 28, ch 9 "a ghostly eerier"].
2. **Signature words:** the author loves states of mind and bearing, named in abstract Latinate nouns (demeanor 21,
   stature 19, outlook 19, aura 28, brooding 23, apprehension(s) 17, perturbation(s) 13, quandary 11, repose 10,
   visage 6, countenance 6). They also love verbs of hurried movement (dashed 21, sprinted 12, leaped 14,
   sauntered 17, paced 31) and said-bookisms (stated 88, blurted 56, announced 50, continued 95, **said only 21**).
3. **Misuse:** 100+ malapropisms and wrong collocations are logged in §3. The worst repeat offenders are
   *delirious* (14, nearly always meaning "agitated"), *stature* (19, meaning "posture/composure"), *outlook*
   (19, meaning "expression"), *orotund* (4), *asphyxiated* (5), *discrete/disbelieve/incidence/complimented*
   (confusable pairs), *inhabitation(s)* for inhibitions (4), *impose a question* (8), *accost* (6, meaning
   "approach or talk to").
4. **Spelling:** the author spells almost entirely in **American** style (‑ize 60+:0, ‑or 90+:0, center 16:0,
   color 17:0, traveled 10:0). The exceptions are British: *towards* 125:1, *enquire* 30:9, *grey* 3:1,
   *dialogue* 4:0, *amongst/amidst*. Recommendation: **convert to British spelling, ‑ise form** for a UK submission
   (§4).
5. **Never introduce:** delve, tapestry, testament, palpable, visceral, nuanced, a beat, etched, lingered,
   let out a breath, jaw clenched, flicker, etc. The author uses all of these **0 times** (§6).

---------------------------------------------------------------------------------------------------

## 1. REGISTER

### 1.1 Where it sits
The narration is **high-formal, Latinate and "vocabulary-forward"**, the diction of someone who learned literary
English from reading and a thesaurus rather than from speech. Three layers sit side by side:

| Layer | Examples (counts) | Notes |
|---|---|---|
| Latinate or archaic "fine" words | repose 10, quandary/‑ies 11, visage 6, countenance 6, verve 6, gelid 3, brume 1, tincture 1, frisson 2, quietude 2, solicitude 2, orotund 4, dyspneic 1, ligneous 1, crapulent 1, sedulous 1, jejune 1, stentorian 1, coruscating 1, cerulean 1, abaft 1, confetto 2 | This layer is the voice, but about a third of the rarest words are misapplied (see §3). |
| Office/managerial English | execute 53 ("execute her plan/job"), conclude 40, ensure 37, initiate 12, demonstrate 14, "as per" 13, "proceedings" (day's/past few days'), "go-forward plan" (ch 61), "span of controls" (ch 61), "escalation note" (ch 13) | This comes through in the narration ("started executing her job" (ch 3)). Thin it: it makes thriller action sound like a status report. |
| Colloquial / idiomatic | had no clue 21, goons 12, in a jiffy 4, tad 8, "Hell, no" (ch 58), chinwag (ch 30), hoopla, ginormous, boatloads, rideshare, chit-chatting (6 total, ch 11, ch 13, ch 19, ch 30, ch 31), guys 7 | This layer is sprinkled in. The slangier items clash with the high register. |

**Dialogue** is formal and full-form: "I am" 118 : "I'm" 1 (ch 69); "let us" 22 : "let's" 0; "it is" 27 : "it's" 5;
"do not" 1 : "don't" 63; "cannot" 13 : "can't" 16. The characters (Scottish siblings, a Danish-based crime boss,
Interpol) mostly speak like the narrator: "I deeply appreciate your kind gesture" (ch 2), "Let us not
underestimate her intent" (ch 6). **Voice rule:** keep "I am / let us" as the default. Contract only in moments
of panic or intimacy, and even then sparingly. Do not normalise all dialogue to contemporary contractions.

**Dialogue tags (said-bookism profile):**

| tag | count | tag | count |
|---|---|---|---|
| continued | 95 | spoke | 52 |
| stated | 88 | respond(ed) | 47 |
| blurted | 56 (+3 blurting) | enquired/queried/inquired | 34 |
| announced | 50 | instructed | 34 |
| **said** | **21** | mentioned | 19 |
| declared | 16 | screamed | 16 |
| mumbled | 14 | commanded | 8 |

"with a ___ tone/voice" occurs 78 times and "in a ___ tone/voice" 34 times, giving **112 tone/voice adverbials**
(tone 105, voice 154 overall). The author clearly avoids "said". The fix is not to swap in "said" everywhere.
Instead: (a) delete tags where the speaker is clear; (b) restore *blurted* to its real meaning (sudden,
involuntary speech); (c) let "said" carry about a third of the tags.

### 1.2 Regional (Indian-English / L2) markers, with counts

| Marker | Count | Examples | Treatment |
|---|---|---|---|
| Article dropped before "few" | ~100 (93 paras) vs "a few" 55 | "after few rings" (ch 3); "He ogled her for few seconds" (ch 3); "few 100 US dollars" (ch 6); "I need few volunteers" (ch 63) | Restore "a" silently, except where "few" means "not many" (e.g. "There were few people" (ch 5) is correct). |
| Possessive 's dropped | 38 | "When Benedikt turn came" (ch 2); "Benedikt despair" (ch 3); "Damian gravelly tone" (ch 7); "Sanchez agitation" (ch 57); "Stephen anxiety" (ch 57); "the guard voice" (ch 60); "Benedikt ego" (ch 66); "Daniel disappearance" (ch 69) | Restore silently. |
| Other dropped articles | many | "in such ungodly hour" (ch 3); "in next thirty minutes" (ch 6); "landing in next hour" (ch 21); "a jean" (ch 26) | Fix silently. |
| "as per" | 13 | "as per the schedule" (ch 61) | Change to "according to" / "on schedule" in narration; allow it in officials' dialogue. |
| "ensured to + verb" | 2 | "he ensured to make every minute of the Sunday special" (ch 1); "he ensured to manage a safe distance" (ch 22) | → "made sure to" / "took care to". |
| "the eerie" as a noun | 3 | "it had that uneasiness, the eerie that was giving signs…" (ch 1); "The creeping eerie in the van" (ch 28); "the place morphed to a ghostly eerier" (ch 9) | → "eeriness" / "an eerie stillness". |
| "zeroed down (on/to)" | 2 (+1 "zeroed on") | "She zeroed down on the window" (ch 36); "I zeroed down to few names" (ch 49); "Before I zeroed on Ayr" (ch 50) | → "zeroed in on" / "settled on". |
| "since morning" / "till date" | 3 / 1 | "eyeing for since morning" (ch 59); "till date, he hadn't told her" (ch 66) | → "since the morning" / "so far". |
| "connect" (noun, meaning a contact) | 1 | "Maxwell had an old connect" (ch 70) | → "an old contact". |
| verb + redundant "about" | 7 | "mentioned about" 4 [ch 17, ch 26, ch 79, ch 80]; "explained about" 2 [ch 45, ch 61]; "regretted about" 1 (ch 63) | Drop "about". |
| uncountables pluralised | evidences 3 [ch 75, ch 84]; reasonings 1; sufferings 2; reindeers 1; mafias 1 | | → evidence / reasoning / suffering / reindeer. |
| "miscreants" for criminals | 3 as a noun [ch 8, ch 10, ch 37] | an Indian-press term | → "thugs" / "his men" / "the gang". |
| "passed a smile" | 10 | "passed a frail smile" (ch 2); "passed a gullible smile" (ch 58) | → "gave a … smile" / "smiled …". |
| "put a cursory glance" | 2 | [ch 3, ch 7] | → "cast a glance" / "glanced". |
| "prefer X than Y" | 2 | "preferred their shelters than the road" (ch 1) | → "to". |
| "multi-fold / many folds" | 4 | "increased multi-fold" (ch 2); "increased many folds" (ch 7) | → "many times over" / "grown tenfold". |
| "good fifteen minutes" | 6 | [ch 7, ch 8, ch 13, ch 24, ch 50] | British-compatible ("a good fifteen minutes"). Add the article. |
| "fellowmen" 1 (ch 63), "out of scare" 1 (ch 68), "on the feet" 1 (ch 24) | | | → "workmates", "out of her skin", "on her feet". |
| **Absent** (checked, 0 hits) | prepone, revert, do the needful, kindly, out of station, cousin-brother, discuss about, return back, "what to speak of", "itself/only" as emphatics | | Nothing to fix. |

**Also present:** American-English lexis (restroom 25 incl. washroom/bathroom, parking lot 6, gas station 3,
curb 7, trunk 2, pajamas 2, cellphone 1, "dress pants" 2, "Mom" 6 **spoken by the Scottish siblings** [ch 50,
ch 50–4, ch 53], "gotten" 3, "vacationers" 1). See §4.

---------------------------------------------------------------------------------------------------

## 2. SIGNATURE VOCABULARY (top ~65, with verdicts)

Key: **KEEP** = genuine voice, leave mostly intact · **THIN** = voice, but overused; cut to the target ·
**TIC** = mannerism; reduce hard · **FIX** = frequently misapplied (see §3).

| # | Word / phrase | Count | Verdict | Target / note |
|---|---|---|---|---|
| 1 | appeared (as linking verb) | 134 | TIC | Target ~60. Often "appeared + adj" where "looked"/"was" works. |
| 2 | soon (sentence-level) | 111 | TIC | Target ~50. "Soon he…" opens too many sentences. |
| 3 | continued (tag) | 95 | TIC | Target ~40. |
| 4 | stated | 88 | TIC | Target ~20. It is official-report diction. |
| 5 | smile (noun/verb) | 90 | THIN | Many qualified smiles: wry, thin, vicious, frail, gullible, pixie, slunk, cynical simper. |
| 6 | blurted (+ blurting) | 59 | TIC + FIX | Target ≤15. Misused for calm or deliberate speech ("blurted in a subtle voice" (ch 24)). |
| 7 | execute/executing | 53 | TIC | Target ~15. "executing their preconceived plan" (ch 24). |
| 8 | announced | 50 | TIC | Target ~20. |
| 9 | as if | 44 | THIN | |
| 10 | concluded/conclude | 40 | THIN + FIX | "concluded their dinner" (ch 26); "concluded the conversation" (ch 7). Use "finished" / "ended". |
| 11 | extreme(ly) / at the extreme | 39 / 7 | TIC + FIX | "His frustration was at the extreme" (ch 30); "aggravation was at the extreme" (ch 63) → "at its height". |
| 12 | ensure(d) | 37 | THIN | "ensured to" is a fix (§1.2). |
| 13 | enquired/queried/inquired | 34 | THIN | Keep British *enquired*; cut *queried* (10) to 2–3. |
| 14 | instructed | 34 | THIN | |
| 15 | paced / pacing (meaning "walked briskly") | 31 | FIX | "paced towards the City Hall building" (ch 24); "paced out of the check gates" (ch 24). In British English *pace* means walking back and forth; use "strode", "hurried", "walked quickly". |
| 16 | aura | 28 | THIN | Target ~10. |
| 17 | rushed | 28 | KEEP | |
| 18 | a shade of / shades of | 27 | KEEP (signature) | "His tone was a shade below screaming" (ch 26) is excellent. Keep ~15; fix "shades of hesitation on some of the player's faces" (ch 2). |
| 19 | a sense of | 25 | THIN | Target ~12. |
| 20 | puzzled | 24 | KEEP | |
| 21 | brooding | 23 | THIN + FIX | Used for neutral "thinking" ("Her brooding was rattled" (ch 3); "out of her brooding" ×5). Keep for moody introspection only. Target ~10. |
| 22 | comprehend | 23 | THIN | Target ~10 ("understand", "take in", "make sense of"). |
| 23 | laced (with) | 22 | THIN + FIX | "The corridor was laced with cameras" (ch 3); "Two mariners laced with sophisticated weapons" (ch 62) → "lined", "armed". |
| 24 | demeanor | 21 | THIN | Target ~8. Spelling → *demeanour*. |
| 25 | had no clue | 21 | THIN | Colloquial in a formal frame. Target ~8 ("had no idea", "could not tell"). |
| 26 | dashed | 21 | KEEP | |
| 27 | sauntered/saunter | 21 | FIX | *saunter* means stroll idly. Correct where leisurely [ch 25, ch 63]; wrong for anxious or urgent walking: "Preoccupied in her quandaries, she sauntered towards the casino" (ch 2). |
| 28 | stature | 19 | FIX | Means height or standing, never posture or state of mind (§3). |
| 29 | outlook | 19 | FIX | Means view or prospects, never facial expression (§3). |
| 30 | behavior | 18 | KEEP (→ behaviour) | |
| 31 | inquisitive / inquisitiveness | 18 | THIN | "inquisitiveness" 9 → "curiosity". |
| 32 | higher-ups / seniors | 18 | KEEP | "seniors" is corporate-Indian; prefer "superiors" or "bosses" in narration. |
| 33 | apprehension(s) | 17 | THIN | Plural "apprehensions" 12 is non-idiomatic for feelings → "misgivings", "fears". |
| 34 | graced / gracing | 17 | THIN + FIX | The subject and object are often reversed: "her body graced a full-length black Abaya" (ch 24) → "she wore"; "the tremulous smile his face graced" (ch 19); "The walls graced plenty of tall windows" (ch 33); "the walls were graced with few Portuguese local decors" (ch 29) → "hung with". Correct in "the platinum necklace that graced her long neck" (ch 33). |
| 35 | utmost | 16 | THIN | Target ~6 ("with utmost care" ×several). |
| 36 | screamed | 16 | KEEP | |
| 37 | with great interest | 13 | TIC | Target 3. |
| 38 | calmness / quietness / coldness / anxiousness / gloominess | 13 / 10 / 8 / 9 / 4 | TIC | *‑ness* nominalisations; see §2.1. |
| 39 | delirious | 14 | FIX | Misused 13 of 14 times (§3). |
| 40 | leaped | 14 | KEEP (→ leapt in UK) | |
| 41 | mumbled | 14 | KEEP | |
| 42 | perplexed | 13 | KEEP | |
| 43 | perturb‑ (perturbation(s), perturbed) | 13 | THIN | "perturbations" plural 6 → "unease". |
| 44 | commotion | 12 | THIN | Also used for inner turmoil ("despite all the commotion she battled with" (ch 57)) → "turmoil". |
| 45 | goons / accomplice(s) / miscreants / ruffians | 12 / 12 / 6 / 2 | THIN | *goons* is fine in characters' mouths. In narration vary with "his men", "thugs", "Benedikt's people". |
| 46 | ordeal | 12 | THIN | |
| 47 | disheveled | 12 | KEEP (→ dishevelled) | |
| 48 | took a pause | 12 | TIC | → "paused" (the author already writes "paused" 7 times). |
| 49 | sprinted (+ "sprinted to action" ×5, "sprang into action", "went to action", "sprung to action") | 12 / 7 | TIC | The "sprinted to action" family is a signature tic: the concierge, the keeper, the waitress… [ch 2, ch 2, ch 3, ch 37, ch 49, ch 63]. Keep 1, and fix "went to action" (ch 63). |
| 50 | untoward | 11 | KEEP | Fix "untoward incidence" [ch 25, ch 42]. |
| 51 | respite | 11 | KEEP / THIN | |
| 52 | rattled (meaning "interrupted/startled") | 11 | FIX / THIN | "Her brooding was rattled by Benedikt's grating voice" (ch 3); "A deep-throated voice rattled their conversation" (ch 63) → "broke into", "cut through". |
| 53 | quandary / quandaries | 11 | KEEP / THIN | Target 5. "Preoccupied in her quandaries" (ch 2) → "with her misgivings". |
| 54 | exuding / exuded | 11 | THIN | |
| 55 | draped | 10 | KEEP | "draped in the shroud of silence" (ch 29) is voice. |
| 56 | repose (+ "transient repose" ×2) | 10 | KEEP / THIN | Target 4. "roused from her transient repose" (ch 3) and "The town was slowly waking up from its transient repose" (ch 1): keep one "transient repose" in the whole book. |
| 57 | whereabouts | 10 | KEEP | |
| 58 | engulfed | 9 | THIN | |
| 59 | mustered (some) courage | 8 | THIN | Target 3. |
| 60 | famished | 8 | KEEP | Stephen's running joke in ch 24–26. |
| 61 | trepidation(s) | 8 | KEEP / FIX | The plural "trepidations" (7) → singular or "fears". |
| 62 | tad | 8 | KEEP | Mildly colloquial, but consistent with the author. |
| 63 | gravelly (voice/tone) | 7 | KEEP ≤3 | "her breath was gravelly abnormal" (ch 80) is a fix. |
| 64 | fidgety | 7 | KEEP | |
| 65 | morph(ed/ing) | 7 | THIN | |
| 66 | visage / countenance | 6 / 6 | KEEP | Max 3 each. They are genuine voice ("his visage flinched" (ch 2)). |
| 67 | verve | 6 | KEEP 2–3 | |
| 68 | orotund | 4 | FIX | §3. |
| 69 | sotto voice | 4 | FIX | → *sotto voce*. "With a sotto voice" (ch 12) → "In a low voice" / "sotto voce". |
| 70 | hullabaloo (+ "hullaballoo" ×2) | 6 | KEEP 2 | Standardise spelling. |
| 71 | in a jiffy | 4 | KEEP 1 | [ch 3, ch 7, ch 36, ch 77]. |
| 72 | uncalled (meaning "unbidden") | 5 | FIX | "layers of some uncalled mist" (ch 2); "an uncalled frisson of fear" (ch 69) → "unbidden", "unwelcome". |
| 73 | gelid, frisson, haar, brume | 3, 2, 1, 1 | KEEP | Distinctive; "haar" is good Scots colour. |
| 74 | little did they know | 2 [ch 1, ch 7] | KEEP 1 | Chapter-ending foreshadowing, a genre tic. Keep one. |
| 75 | with extreme/utmost caution/urgency/care | 12 | TIC | Target 4. |

### 2.1 The ‑ness habit (lexical signature)
The author builds abstract nouns with *‑ness* where English already has a standard noun. This is distinctive and
often slightly off: anxiousness 9 (→ anxiety), quietness 10 (→ quiet, silence), calmness 13 (→ calm),
coldness 8 (→ cold, chill), gloominess 4 (→ gloom), inquisitiveness 9 (→ curiosity), curiousness 1 (ch 41),
discreetness 2 [ch 74, ch 81] (→ discretion), perfectness (ch 37) (→ perfection), evilness (ch 18) (→ evil),
hastiness 2 [ch 59, ch 77] (→ haste), dreadfulness (ch 40) (→ dread), scariness (ch 76), impassiveness (ch 2)
(→ impassivity), dewiness (ch 1), glumness (ch 26), fretfulness (ch 56), averseness (ch 15) (→ reluctance),
desirousness 3 [ch 22, ch 42, ch 81] (→ longing), abstruseness (ch 22) (→ mystery), chilliness 2,
unfriendliness (ch 74). **Treatment:** switch to the standard noun about two-thirds of the time. Keep the
occasional *calmness* or *quietness* so the texture stays.

---------------------------------------------------------------------------------------------------

## 3. MALAPROPISMS, MISUSED WORDS & WRONG COLLOCATIONS (106 entries)

Format: quote [P###] → intended or suggested fix. The fix is always the smallest change that keeps the author's
register.

### 3.1 Confusable pairs (spelling-level; fix silently)
1. "looking **contempt** and regaled" (ch 26) → content (and replete)
2. "they **dawned** a different look" (ch 24) → donned
3. "as it was **taxing** on the tarmac" (ch 24) → taxiing
4. "in a **discrete** and surreptitious manner" (ch 25); also "discrete life" (ch 9), "discrete about" (ch 50), "with discrete steps" (ch 62), "discretely follow" (ch 85) → discreet / discreetly (5 cases)
5. "with **disbelieve** and consternation" (ch 25); "in a state of disbelieve" [ch 28, ch 37, ch 43]; "with disbelieve" [ch 39, ch 43] → disbelief (6 cases)
6. "any untoward **incidence**" [ch 25, ch 42]; "report the incidence" (ch 22); "the incidence repeat" (ch 18); "past incidences" (ch 15) → incident(s) (5 cases)
7. "white stucco **complimented** well with…" (ch 29); "interiors complimented the exteriors" (ch 42); "surroundings complimented the derelict house" (ch 43); "aptly complimenting his demeanor" (ch 21) → complemented / complementing (4 cases; ch 2 and ch 13 are correct)
8. "Shaving off all **inhabitations**" (ch 40); "without any inhabitations" (ch 85); "without inhabitation" (ch 72); "all inhabitation expunged" (ch 53) → inhibition(s) (4); ch 53 intends "everything else fell away"
9. "the long **impeding** strenuous silence" (ch 28) → impending; better: "the long, strained silence"
10. "they searched for their own **solicitude**" (ch 29) → solitude (ch 28 "his friend's solicitude" is correct)
11. "Her **palpations** were dissolved" (ch 80) → palpitations
12. "how she **faired**" (ch 13) → fared
13. "when I **fleeted**" (ch 43) → fled
14. "**Creek, creek!!**" (ch 3); "the occasional creeks of the seagulls" (ch 26) → creak; for gulls, "cries"
15. "As the light was **sipping** out of the window" (ch 3) → seeping
16. "a fast-approaching limousine **curbed** around the cobbled pavement" (ch 2) → curved / swung
17. "She **cramped** out of the cut-out window" (ch 3); "Maxwell cramped the car" (ch 43) → crawled / squeezed; crammed / squeezed
18. "The temperature had **stooped** to single digits" (ch 4) → dropped (from "stooped", a slip for "slumped")
19. "She **wielded** from her repose" (ch 5) → woke / stirred
20. "Benedikt **aroused** from his disheveled state" (ch 6) → roused himself / awoke
21. "in his **last ditched** attempt" (ch 27) → last-ditch
22. "a **sotto voice**" [ch 12, ch 26, ch 77] → sotto voce / a low voice
23. "a **Bonnie** hat" (ch 24) → beanie (or bonnet)
24. "with a **daemon** outcry" (ch 43) → demonic
25. "the tall **casted** shadows" (ch 33); "the casted shadows" (ch 33) → cast
26. "a **firmed** tone" [ch 22, ch 23] → firm (ch 53 "had firmed her mind" → "had made up her mind")
27. "He tried not to sound **rile**" (ch 45) → riled
28. "**trifled** down" (ch 80) → "brushed aside" / "thwarted"
29. "the ship … `soon" (ch 60) → stray backtick (typo)
30. "the **taxa** he had kept" (ch 4) → taxi; "badested ridge" (ch 4) → unclear, probably "balustraded ledge"; "Cabeco embossed" (ch 26) → "Cabeço"

### 3.2 Wrong word (sense error)
31. "never failed to **cease her excitement**" (ch 1) → never failed to thrill her / to excite her
32. "There was a strong **rumor** about both father and daughter playing this little game" (ch 1) → suspicion / It was an open secret that…
33. "impassiveness was the **unwarranted** protocol of the game" (ch 2) → unwritten
34. "in his most **uncanny** way, he uttered" (ch 2); "in a most uncanny way" (ch 15); "Her tone was uncanny and definitive" (ch 56) → in his most urbane / disarming way; awkward; strange
35. "The **En Welch** clock **rhymed**" (ch 2) → "the clock chimed" (the maker's name is unclear, so query the author: "Welch" is a US clock maker; maybe "the Westminster chime")
36. "The waitress eyes were **infusing** an exquisite smile" (ch 2); "chauffeured driven, infusing an aura" (ch 60) → "The waitress's eyes smiled" / "radiating"; "chauffeur-driven, exuding an aura"
37. "your drink **dames**!!" (ch 2) → madam / mademoiselle (dame is not a form of address)
38. "a **frivolous** tone" (ch 2) → playful / teasing
39. "she **rejoinders** with a distinct smile" (ch 2); "too tired to rejoinder" (ch 26) → rejoined; retort / reply
40. "continued her conversation with an **embodied** tone" (ch 3); "a deep embodied voice" (ch 15) → emboldened / measured; full-bodied / deep, rich voice
41. "a **windshield** jacket" (ch 4) → windcheater (UK) / windbreaker
42. "**Demurred** by the chaos" (ch 6) → Unnerved / Rattled
43. "I am not a fool to get **winded** in her deception" (ch 6) → taken in by / wound up in
44. "the way she **dour** him" (ch 7) → rebuffed / snubbed
45. "he couldn't **abstain from not praising** her" (ch 7) → couldn't help admiring / couldn't refrain from praising
46. "his mind had morphed into a **confetto**" [ch 7, ch 41] → a jumble / a whirl (confetto is the Italian sugared almond)
47. "a **cynical simper**" (ch 7) → a knowing smirk (a simper is coy, never cynical)
48. "a luxury **grandiose**" (ch 2) → a grand luxury hotel
49. "The gown was **snugging** well" (ch 2) → fitted snugly
50. "a member only **arcade**" (ch 2) → a members-only club / room
51. "**the eerie** that was giving signs" (ch 1); "The creeping eerie" (ch 28); "a ghostly **eerier**" (ch 9) → eeriness / an eerie hush
52. "This was well **endorsed** by the people who preferred…" (ch 1); also [ch 12, ch 26, ch 42, ch 48] → borne out by / confirmed by (5 cases)
53. "**Irritant** self" (ch 6); "an irritant tone" (ch 15) → irritable / irritated
54. "the sunbeam was forming a **tincture**" (ch 1) → tint / wash of colour (keep "haar"; "tincture" can stay if the author insists, but "tint" is the sense)
55. "Sanchez was **superfluous** and vigilant" (ch 24) → watchful / alert (probably a slip for "suspicious")
56. "trying hard to match Sanchez **wayward careen**" (ch 24) → brisk pace / headlong stride
57. "She was **dyspneic**" (ch 24) → breathless
58. "spoke with an **oscillating** tone" (ch 24) → unsteady / uneven
59. "which **resembled well with** the garb she wore" (ch 24) → which went well with
60. "The white-laced blouse **embellished** her bosom" (ch 24) → adorned / set off
61. "she **put a deaf ear** to his request" [ch 24, ch 85] → turned a deaf ear
62. "Her preoccupied **stature** was in deep perturbation" (ch 24); "With a calm stature" (ch 24); "his stature reflected uneasiness" (ch 25); "She took a few deep breaths to calm her **stature**" (ch 59); "a mesmerized stature" (ch 54); "a puzzled stature" (ch 80) → manner, bearing, composure, nerves, posture, look (19 cases; *stature* means height or standing)
63. "a small tone" (ch 24) → a quiet voice
64. "Maxwell wanted to confront on their **incessant** behavior" (ch 25); "the incessant behavior Benedikt was demonstrating" (ch 80) → insolent / high-handed; erratic
65. "she didn't put her **vigilance guards** off" (ch 26) → she didn't let her guard down
66. "Stephen resisted but **resigned on** Jules's **consistent insistence**" (ch 26) → gave in to Jules's persistent urging
67. "five minutes of **incredulous** search" (ch 26); "his incredulous gasping" (ch 59) → frantic; involuntary gasp
68. "From his **delirious** appearance" (ch 27); "made him delirious" [ch 35, ch 59]; "his mind was delirious" (ch 9); "She was delirious" (ch 15); "Her over indulgent mind was delirious" (ch 16); "such delirious state" (ch 38) → agitated, frantic, beside himself, livid, restless (13 of 14 uses; only ch 44/ch 50 are close to the true sense)
69. "his **demeanor implausible**" (ch 28) → his face incredulous
70. "which concealed any trickle of emotions from any **puerile guessing**" (ch 28) → prying eyes
71. "a bunch of inept people I have as a part of my **defunct** team" (ch 28) → useless / dysfunctional
72. "Benedikt left Francis in complete **shackles**" (ch 28) → left Francis rooted to the spot / hanging
73. "his monologue draped with an **emphatic outlook**" (ch 28); "more considerate and **emphatic**" (ch 50); "an emphatic attempt to decipher" (ch 67) → empathetic manner; empathetic; earnest
74. "which added to his **endowed** Greek like appearance" (ch 29) → Greek-god looks
75. "the recent tribulations … demanded her to be more **imperturbable**" (ch 29) → watchful (the sense is "on guard", not "calm")
76. "The **edifices** were designed using bricks" (ch 29) → window frames / grilles
77. "twenty **pesos** for seven days" (ch 29) → euros (Portugal); a factual slip that sits in the diction
78. "to make **on** the lost time" (ch 30) → make up
79. "The street **by large** was quiet" (ch 30) → by and large
80. "to avoid any **circumstantial** misfortune" (ch 30) → accidental / needless
81. "the slunk smile on his face" (ch 58) → sly
82. "He passed a **gullible** smile" (ch 58); "his gullible voice" (ch 55); "her gullible side" (ch 66) → genial / sheepish; boyish; vulnerable
83. "She was **at her wits** to find a way out" (ch 58) → at her wits' end
84. "Before she could **assimilate** her thoughts" (ch 58) → collect / gather
85. "despite several attempts to **deviate** his mind" (ch 59) → divert
86. "Maybe he was **inadvertently** keeping it away from me" (ch 59) → deliberately
87. "The information was irrefutably **apposite**" (ch 59); "looking stark apposite" (ch 17) → damning; looking sharp / dapper
88. "For a moment she was **disillusioned**" (ch 59); "Disillusioned, she came back" (ch 65); "dazed and disillusioned" (ch 51) → disoriented; disappointed; dazed
89. "caught with her **miscreant**" (ch 59); "his miscreant heart" (ch 66); "her miscreant thoughts" (ch 56); "a miscreant of Benedikt's horde" (ch 8) → misdeed; errant heart; wayward / dark thoughts; one of Benedikt's men
90. "**void of a no go-forward plan**" (ch 61) → with no plan for going forward
91. "he was **innately** hoping" (ch 61) → inwardly / secretly
92. "the words came out **invariably**" (ch 61); "John's name invariably scribbled" (ch 16); "invariably missed calling him" (ch 71) → involuntarily; repeatedly; kept missing
93. "It wasn't in my **span of controls**" (ch 61) → It was out of my hands
94. "He looked at her with a **galling** stare … expressed a **pretentious** look" (ch 62) → glowering stare … feigned a blank look
95. "to **flair** her antsy emotions … to restore the lost **glare**" (ch 63) → inflame her frayed emotions … lost trust / lustre
96. "his inability to **accost** her" (ch 63); "the wait to accost her" (ch 23); "to use the travel time to accost her" (ch 72); "to accost the moment" (ch 81); "courage to accost him" (ch 57) → approach / confront / talk to; seize the moment (6 cases; *accost* means to approach aggressively)
97. "the screaming siren broke his **subtle** brooding" (ch 63); "blurted in a subtle voice" (ch 24); "a subtle sarcasm" (ch 66) → quiet; low; faint. *subtle* (10) is used as "soft".
98. "rushing towards the **abaft**" (ch 63) → the stern / aft deck (abaft is a preposition)
99. "he **retracted** his steps" (ch 63); "retraced back" (ch 47) → retraced
100. "He has lost a lot of **gore**" (ch 63); "a good amount of gore was lost" (ch 42) → blood
101. "making her **overtly** uncomfortable" (ch 65); "his tone was overtly casual" (ch 60) → acutely; studiedly / pointedly
102. "She was in some deep **retrospections**" (ch 65); "He **retrospect** on the past few days" (ch 66) → deep in thought; He looked back on / reflected on
103. "She checked the **sanctity** of the uploaded files" (ch 66) → integrity
104. "rattled her from her **reminiscence**" (ch 66) → reverie
105. "his **perilous** demeanor" (ch 66); "his perilous probing" (ch 50) → erratic / volatile behaviour; intrusive questions
106. "a **surreptitious** smile **encountered** him" (ch 66) → a secret smile crossed his face
107. "couldn't attribute to any **convulsive** answer" (ch 67) → couldn't arrive at any conclusive answer
108. "wearing his **pixie** smile" (ch 67) → boyish / impish
109. "the most genuine words he could **ravel**" (ch 68) → muster / find
110. "kept her in an **ambivalent** disposition" (ch 69); "made her ambivalent" (ch 5) → uneasy / on edge
111. "she **naively** accepted to come along" (ch 69) → reluctantly agreed (also "accepted to" → "agreed to")
112. "her fidgety **deportment**" (ch 69); "insistent inexorable deportment" (ch 78) → manner / fidgeting; unbending insistence
113. "why she becomes **bereft** whenever it concerns Benedikt" (ch 69) → unsettled / undone
114. "any **riposte** to pacify his intrusive mind" (ch 70) → answer
115. "He went into a deep **subornation**, 'Am I **oversubscribing** to a fear…'" (ch 21) → rumination; giving in to / buying into
116. "trace and **captivate** two people" (ch 21); "the day your father was **captivated**" (ch 76); "Sanchez **captivation**" (ch 34); "He himself was in captivation" (ch 47) → capture / captured / capture; in thrall (ch 47 is arguably right)
117. "she resisted **denouncing** her defeat" (ch 17) → conceding / admitting
118. "she couldn't **concede** her emotions anymore" (ch 15) → contain
119. "looked **asphyxiated** and shaky" (ch 15); "he sounded asphyxiated" (ch 23); "her asphyxiated voice" (ch 71); "an asphyxiated tone" (ch 80) → choked / strangled (5 cases; ch 45 "He felt asphyxiated" = suffocated, OK)
120. "in an **orotund** voice she exclaimed" (ch 16); "his orotund voice" (ch 35); "A sharp orotund voice" (ch 40); "bellowed with an orotund voice" (ch 50) → booming / full / ringing (*orotund* also means pompous. "Sharp orotund" is self-contradictory.)
121. "he **blazoned**" (ch 16); "she blazoned the words" (ch 80) → blurted / flung
122. "The **ligneous** house" (ch 33) → wooden / timber
123. "it appeared **aberrantly** unusual" (ch 34) → strangely quiet (tautology)
124. "his **sedulous** plan" (ch 34) → painstaking
125. "**insentient**" [ch 37, ch 43]; "**cataleptic** state" (ch 43) → unconscious / senseless
126. "to **descry** the Peugeot" (ch 8); "Before he could descry" (ch 51) → to shake off the Peugeot; Before he could react
127. "cleared every **scathe** of its existence" (ch 71) → trace
128. "woke up a tad **crapulent**" (ch 71) → groggy (crapulent = hung-over from drink)
129. "restless and **jejune**" (ch 76) → flustered / callow
130. "her incoherent **conjuncture**" (ch 15) → confusion
131. "let me **straightway** come to the point" (ch 15) → come straight to the point
132. "the **congruent** smile" (ch 12) → same fixed smile
133. "**equivocally** expressed agreement" (ch 31); "in an equivocal note" (ch 49) → unequivocally; teasing / playful note
134. "some **concurrences** from them" (ch 53) → agreement / a sign of agreement
135. "a **desolated** bus stop" (ch 33) → deserted
136. "an unusual quietness **impinged** inside the van" (ch 49) → settled over
137. "She tried hard to **oppress** her **avidity**" (ch 50) → suppress her longing
138. "his **diminutive** state" (ch 51) → reverie / daze
139. "what future **beholds**" (ch 53) → holds
140. "hold on to her **schmaltz**" (ch 79) → composure
141. "your **runic** spell" (ch 80) → riddles / cryptic silences; "her breath was **gravelly abnormal**" (ch 80) → ragged
142. "trepidations were **expunging**" (ch 44); "relieved to expunge out of the situation" (ch 48) → ebbing; extricate himself
143. "a **gratuitous** excitement" (ch 16); "any gratuitous situation" (ch 22) → unbidden; untoward
144. "He appeared **absolvent**" (ch 43) → distraught / absent (non-word)
145. "with clear **averseness**" (ch 15) → reluctance
146. "Her heart … she **cogitated** it would explode" (ch 13) → thought / feared
147. "an **unperturbed** dissonance" (ch 23); "an unperturbed exhilaration" (ch 54) → a jarring interruption; an untroubled joy
148. "**resurrect** them from the situation" (ch 8); "The only way he could resurrect" (ch 28) → rescue; redeem himself
149. "it was time to **evade**" (ch 3); "the evade strategy" (ch 24) → escape; evasion plan
150. "**curtail** any noise" (ch 3); "his voice was curtailed" (ch 37) → muffle; cut short
151. "**impose** the question" (ch 7); "imposed his question" (ch 7); "impose few questions" (ch 21); "imposing questions" [ch 65, ch 74, ch 78] → pose / put / press (8 cases)
152. "**uncalled** mist" (ch 2); "an uncalled frisson of fear" (ch 69) → unwelcome; unbidden
153. "**nature's caper**" (ch 1) → nature's game / play
154. "the flutter of **avian species**" (ch 3) → birds
155. "a **dilapidated** pair of jeans" (ch 15) → worn-out / tattered
156. "a **benign** bow" (ch 55) → courteous bow
157. "a **pernicious** behavior" (ch 51) → boorish / wretched
158. "**Twenty pesos**" is listed above. Also the "Stockholm, Denmark" headings (7 chapters): Stockholm is in Sweden. This is a fact error, flagged for the continuity agent. It also affects the lexicon: "Danish coffee", "Kronor/Kroner".

(Numbering runs past 106 because several entries group multiple instances. Total distinct misuse types ≈ 130;
total instances ≈ 250.)

### 3.3 Collocation slips (right word, wrong partner) — spot list
- "visibly tall" (ch 2) → strikingly tall · "chiseled shape face" (ch 2) → chiselled face
- "donned a poker face" (ch 2) → wore/kept a poker face
- "raising the mercury to the height of insanity" (ch 2) → sending the tension sky-high
- "made her fell" (ch 3) (grammar) · "a surged vengeance" (ch 5) → renewed vengeance
- "the Land Rover held to its spot" (ch 1) (the car is a Range Rover in (ch 1); continuity)
- "a sense of relief consumed his countenance" (ch 7) → spread across his face
- "Past few days were nothing but feet on the streets" (ch 24) (keep; vivid)
- "left them looking contempt and regaled" (ch 26) (see 1)
- "put forward a leading question" (ch 58) → an innocent / probing question
- "meekly put down by him" (ch 58) → quietly rebuffed
- "restore the lost glare" (ch 63) (see 95)
- "she hardly minced her words" (ch 61) → she did not mince her words
- "spend some time in desirousness" (ch 42) → longing
- "the ship flagged off from Tallinn" (ch 62) → cast off / sailed from (IE "flag off")
- "a frisson of hope" (ch 59) (OK, keep)

---------------------------------------------------------------------------------------------------

## 4. SPELLING CONVENTION

### 4.1 Counts

| Pair | US form | UK form |
|---|---|---|
| ‑ize / ‑ise (realize, recognize, organize, apologize, scrutinize, mesmerize, memorize, jeopardize, etc.) | **60+** (realize family 19) | **0** |
| color / colour (incl. colored, colorful) | 17 | 0 |
| favorite / favourite | 5 | 0 |
| favor(ed) | 4 | 0 |
| behavior | 18 | 0 |
| demeanor | 19 | 0 |
| vigor / fervor / clamor / humor / honor / rumor / neighbor / labor / armor / harbor / odor | 7/2/2/2/3/1/4/2/1/6/— | 0 |
| center | 16 | 0 |
| meter(s) / kilometer | 12 | 0 |
| traveled / traveling / traveler | 10 | 0 |
| spiraled, signaled | 4, 1 | 0 |
| offense | 1 | 0 |
| skeptic(al) | 4 | 0 |
| mustache | 1 | 0 |
| pajamas | 2 | 0 |
| program | 4 | 0 |
| gray / grey | 1–2 | 3–5 (grey, greyish ×2) |
| toward / **towards** | 1 | **125** |
| inquire / **enquire** | 9 | **30** |
| dialog / **dialogue** | 0 | 4 |
| while / whilst | 107 | 0 |
| among / amongst; amid / amidst | 0 / 0 | 6 / 2 |
| forward / forwards | 56 | 0 (both fine in UK) |
| gotten | 3 | — |
| disheveled | 12 | — (UK: dishevelled) |
| leaped | 14 | — (UK prefers leapt; both acceptable) |
| OK / okay | 10 | — |

Lexis (not spelling): elevator 20 vs lift 2; restroom/washroom/bathroom 25 vs toilet 0; parking lot 6 vs car
park 0; gas station 3 vs petrol 0; curb 7; trunk 2 vs boot 3; highway 13 vs motorway 5; line(s) (queue sense) 11
vs queue 5; cab 20 vs taxi 36; apartment 19 vs flat 8; **Mom 6 vs Mum 0 (spoken by Scots)**; pants 2 vs trousers 2.

### 4.2 Recommendation: **British spelling, ‑ise form**, applied mechanically
Why:
1. **Market.** The brief targets a Penguin-level edit and UK agents and publishers. UK trade fiction houses
   (Penguin General / Michael Joseph / Cornerstone et al.) set British spelling. Most use ‑ise; some (OUP-style)
   use ‑ize. American spelling in a submission reads as "not yet prepared for this market".
2. **Setting and characters.** The heroine and her brother are Scottish (Girbin, Ayr; 59 Scotland/Ayr/Scottish
   mentions). The rest of the book is in Europe, and there is no American point-of-view character. "Mom",
   "restroom", "parking lot" in a Scot's mouth are errors of voice, not style.
3. **The author is already half-British.** *towards* (125:1), *enquire* (30:9), *grey*, *dialogue*,
   *amongst/amidst*, "good fifteen minutes", "tad", "chinwag", "motorway" are all British or Commonwealth. The
   American layer is spelling habit, probably from US-locale software, not voice. Indian English is itself
   British-spelled, so the conversion *restores* the author's natural base.
4. **Voice-neutral.** Spelling changes are invisible to voice. There are about 230 tokens, all mechanical.

Operational rules:
- ‑ize → ‑ise (realise, recognise, organise, apologise, scrutinise, mesmerise, memorise, jeopardise, empathise,
  rationalise, antagonise, traumatise, synchronise, specialise, visualise, tantalising, agonising, analysing).
  **Exceptions:** *size, capsize, seize, prize* stay.
- ‑or → ‑our (colour, favour(ite), behaviour, demeanour, vigour, fervour, clamour, humour, honour, rumour,
  neighbour, labour, armour, harbour, odour). **Not** in: error, horror, terror, mirror, stupor, languor,
  tremor, pallor, anchor, visor, vapor → *vapour*.
- ‑er → ‑re: centre, metre(s), kilometre(s), theatre.
- Double l: travelled/travelling/traveller, signalled, spiralled, dishevelled, levelled, fuelled, cancelled.
- offence, sceptic(al), moustache, pyjamas, programme (non-computer), grey (all), dialogue (keep), towards (keep),
  whilst (**do not introduce**; the author never uses it), leapt (optional, prefer leapt), "gotten" → "got".
- Lexis in British settings or British mouths: Mom → **Mum**; restroom → toilets / ladies' room / washroom (in
  airports "toilets"); parking lot → car park; gas station → petrol station; curb → kerb; trunk → boot;
  cellphone → mobile; pajamas → pyjamas; dress pants → trousers; line (queue) → queue; vacationers → holidaymakers.
  In neutral European narration keep **elevator → lift** only in the UK scenes. In continental hotels either is
  acceptable, but choose one; recommended **lift** throughout for consistency.
- Keep "cab" and "taxi" both (the author alternates; both are British-acceptable).
- Enquire/inquire: British house usage is *enquire* for asking and *inquiry* for formal investigations. The
  author already prefers *enquire* (30), so convert the 9 *inquire* to *enquire*, except "inquiry" in a formal
  sense [ch 25 "a formal inquiry"].

Fallback: if the team queries US agents, reverse every rule above. **Never mix.**

---------------------------------------------------------------------------------------------------

## 5. NUMBERS, CAPITALISATION, TIME & DATE

### 5.1 Numbers
- **Durations are overwhelmingly in words:** "five minutes" 19, "fifteen minutes" 18, "thirty minutes" 17,
  "twenty minutes" 16, "ten minutes" 15… 157 word-form durations vs 13 digit-form ("20 minutes" ×5 [ch 5, ch 25,
  ch 30…], "30 minutes" ×2, "72 hours", "4 hours", "5 years", "24 hours", "5 minutes" (ch 66)).
  → **House rule:** spell out numbers one to one hundred and round numbers in narration and dialogue (Chicago-
  and Penguin-style fiction). Convert the 13 digit-form durations.
- Measurements: "6 feet tall" (ch 29) vs "over six feet tall" (ch 2); "160 KM", "30 KM", "five KM" (ch 29) → spell
  out and use "kilometres"; never "KM". Feet and metres are mixed (feet 26, meters 10). That is acceptable
  (British usage mixes them), but convert "meters" → "metres".
- Money:
  - "10M Pounds" (ch 2) → "ten million pounds" (or "£10 million")
  - "worth million Pounds" (ch 2) → "worth a million pounds"
  - "7.5 Million pounds" (ch 2) → "seven and a half million pounds"
  - "one million and two hundred thousand Pounds" (ch 2) → "one point two million pounds" / "£1.2 million"
  - "five hundred-thousand-pound blind" (ch 2) → "a five-hundred-thousand-pound blind"
  - "a hundred thousand bets" (ch 2) → "a bet of a hundred thousand"
  - "whopping thirty-five million Pounds!!" (ch 2) → "a staggering thirty-five million pounds"

  → **House rule:** in the poker chapter, spell sums out in words with lower-case "pounds". Use "£" only in
  documents or on screens. Never "10M" / "5M" (ch 17).
- Other currencies: "euros" lower case (5, already correct); "Kronor" 2 / "Kroners" 1 (ch 4) / "Kroner"
  → **kronor** (Swedish) or **kroner** (Danish), depending on how the Stockholm/Denmark error is resolved; lower
  case; no "‑s". "US dollars" fine. "twenty pesos" → euros.
- Ordinals in prose: "the 15th floor" (6), "16th century", "18th-century" → **fifteenth floor**,
  **sixteenth century** in narration (Penguin style); keep figures only in chapter headings.
- Card values: "7 of spades and 10 of spades", "8 and 9 of spades" (ch 2) vs "five of hearts and seven of clubs"
  (ch 2) → words throughout.

### 5.2 Capitalisation habits
- **Pounds** capitalised 9 of 11 times ("million Pounds") → **pounds**. "Million" capitalised once (ch 2) → lower.
- Mid-sentence caps: "The Elevator opened" (ch 3), "pointed Arch" (ch 3), "the Bellman" (ch 6), "the Jacuzzi"
  (ch 6) (brand; lowercase "jacuzzi" in UK style), "black Abaya" (ch 24) → abaya, "the Airport" (7) → airport
  unless part of a name, "And Above all" (ch 63) → above, "the Internet" 3 → "the internet" (UK), "T-Shirt"
  (ch 26) → T-shirt.
- Kin and titles: "Aunt Naiena" (correct as a name). "Chief" (6) as an address to Benedikt: keep capitalised
  in dialogue ("Chief, we lost her" (ch 28)). Use lower case in narration ("his chief").
- Dialogue openings are frequently lower case after the tag: "he uttered, "she is with me"" / ""don't be sorry
  it wasn't your fault,"" (ch 2); "with a raised voice… "where is it written"" (ch 2). This is a punctuation
  matter for the grammar agent.

### 5.3 Time & date
- **Chapter headings** (79): the format is `H:MM AM|PM Dth Month YYYY, Town, Country` (e.g. "6:00 AM 14th
  February 2010, Girbin, Scotland" (ch 1)). It is internally consistent (all ordinal dates, all "AM/PM" in caps
  with a space). **Keep it as-is.** It is a house device of the book. Optionally drop ":00".
- In running prose: "It was past 2:00 AM" (ch 3), "2:30 AM" ×2, "at 7:30 AM, 30 minutes before" (ch 58),
  "Around 10:00 in the night" (ch 57), "Around 11:00?" (ch 67), "past nine pm" (ch 29) (lower case once),
  "quarter past eight" (ch 26), "half-past one" (ch 81).
  → **House rule for prose:** use words: "just after two in the morning", "half past seven", "ten o'clock at
  night". The book uses **0 "o'clock"**, so introduce it only sparingly. "past two in the morning" is closer to
  the author than "at 0200". Replace the IE-flavoured "in the night" (3) with "at night" / "in the evening".
- "2:20 AM in the morning" (ch 3) is redundant → "twenty past two in the morning".

---------------------------------------------------------------------------------------------------

## 6. BLACKLIST — words an editor must NOT introduce

Every item was grepped against the whole book. The author's count is shown; 0 means it would be an intrusion.

### 6.1 "Writerly-AI" vocabulary (author count 0 unless shown)
| Word/phrase | Count | | Word/phrase | Count |
|---|---|---|---|---|
| delve | 0 | | tapestry | 0 |
| testament (to) | 0 | | palpable | 0 |
| visceral | 0 | | nuanced / nuance | 0 |
| a beat / for a beat | 0 | | juxtapose | 0 |
| ethereal | 0 | | tendril(s) | 0 |
| symphony / dance of | 0 | | etched | 0 |
| linger(ed/ing) | 0 | | the weight of | 0 |
| hung in the air | 0 | | let out a breath / exhaled | 0 |
| a breath she didn't know she was holding | 0 | | hitched / hitch in her breath | 0 |
| jaw (clenched, tightened) | 0 | | clench | 0 |
| flicker (of) | 0 | | something shifted | 0 |
| kaleidoscope | 0 | | orchestrate | 0 |
| realm | 0 | | underscore | 0 |
| pivotal | 0 | | vibrant | 0 |
| robust / seamless / leverage / honed | 0 | | gossamer | 0 |
| ghost of a smile | 0 | | silence stretched | 0 |
| eyebrow (raised) | 0 | | grimace | 0 |
| cadence / timbre | 0 | | eerily / haunting | 0 |
| unspoken | 1 (ch 72) | | navigate | 1 (ch 43) |
| landscape | 1 (ch 13) | | intricate | 1 (ch 22) |
| myriad | 1 (ch 13) | | echo(ed) | 3 |
| resonate | 1 (ch 61) | | thrum | 1 (ch 4) |

**Do not raise the count** of the single-use items either (unspoken, navigate, myriad, thrum, echo, resonate,
intricate). **Also avoid** these AI-style structures, for which the author has no precedent: "It wasn't X. It
was Y." reframes; one-word paragraphs for effect; em-dash asides (the author uses the spaced hyphen " - " and
" – "); triadic lists of sensory adjectives; "Something in her…"; "the air thick with…"; "she didn't know
whether to laugh or cry".

### 6.2 Too modern / too American-colloquial (author count 0)
gonna, wanna, gotta, awesome, super (intensifier), totally, literally, basically, vibe (1, (ch 49): leave it),
dude, freaked (out), sucker, "reach out", "circle back", "process (emotions)", "unpack", "trauma-informed" terms,
"closure", "gaslight", "space" (emotional), "boundaries", "toxic", "on the same page".
**Also avoid British slang** that the author doesn't use (count 0): bloody, knackered, gobsmacked, mate,
cheers, brilliant (interjection), "fancy" (verb, "I fancy him"). The UK conversion is spelling-level only;
don't Britishise the idiom.

### 6.3 Too modern-writerly punctuation/diction the author never uses
"whilst" (0; don't introduce in the UK conversion), semicolon-heavy periodic sentences (the author runs clauses
with commas and "and"), sentence fragments for rhythm, italics for thought (the author puts thought in quotation
marks: ""Looks like it's Alberto's day today." That's how Rita felt" (ch 2)).

### 6.4 Words the author already overuses — do not add more
blurted, stated, announced, appeared, soon, aura, brooding, demeanor, execute, extreme, utmost, comprehend, "a
sense of", "with great interest", "had no clue", "took a pause", "sprinted to action", smile-with-adjective,
"with a … tone/voice".

---------------------------------------------------------------------------------------------------

## 7. REPLACEMENT PALETTE (30 most common problem words)

Each alternative stays in the author's formal, slightly old-fashioned register. None is slangy or AI-flavoured.
Use the first option by default and rotate.

| # | Problem word (count) | In-register alternatives |
|---|---|---|
| 1 | blurted (59) | said · burst out · broke in · (drop the tag) |
| 2 | stated (88) | said · replied · told him · (drop the tag) |
| 3 | announced (50) | said · declared · told them · called out |
| 4 | continued (95) | went on · added · (drop the tag) |
| 5 | appeared (134) | looked · seemed · was · (restructure) |
| 6 | soon (111) | before long · shortly · presently · in a moment |
| 7 | with a ___ tone/voice (112) | quietly / sharply (single adverb) · his voice low · (drop) |
| 8 | execute(d) (53) | carry out · put into action · go through with · pull off |
| 9 | conclude(d) (40) | finish · end · wind up · bring to a close |
| 10 | ensure(d) (37) | make sure · see to it · take care that |
| 11 | extreme / at the extreme (39) | great · intense · at its height · beyond bearing |
| 12 | utmost (16) | great · every (care) · the greatest |
| 13 | comprehend (23) | understand · take in · make sense of · grasp |
| 14 | stature (19, misused) | bearing · composure · manner · posture |
| 15 | outlook (19, misused) | look · expression · air · manner |
| 16 | demeanor (21) | manner · bearing · air · face |
| 17 | visage (6) | face · features |
| 18 | countenance (6) | face · expression · features |
| 19 | aura (28) | air · atmosphere · presence · feel |
| 20 | brooding (23, as "thinking") | thoughts · reverie · musing · preoccupation |
| 21 | delirious (14, misused) | frantic · beside himself · distraught · restless |
| 22 | sauntered (21, when hurried) | walked · strolled (only if leisurely) · made her way · wandered |
| 23 | paced (31, as "walked briskly") | strode · hurried · walked briskly · made his way |
| 24 | apprehension(s) (17) | misgiving(s) · unease · fear(s) · foreboding |
| 25 | perturbation(s) (13) | unease · disquiet · agitation · anxiety |
| 26 | trepidation(s) (8) | trepidation (singular) · dread · fears · nerves |
| 27 | repose (10) | rest · sleep · slumber · stillness |
| 28 | quandary / quandaries (11) | dilemma · predicament · uncertainty · doubts |
| 29 | rattled (11, as "interrupted") | broke into · cut through · startled · jolted |
| 30 | laced (22) | lined · edged · tinged · shot through (with) |
| 31 | graced / gracing (17) | adorned · hung · lit (a face) · crossed (a smile) |
| 32 | had no clue (21) | had no idea · could not tell · was at a loss |
| 33 | accost (6, misused) | approach · confront · talk to · take aside |
| 34 | impose (a question) (8) | put · pose · press · ask |
| 35 | orotund (4) | booming · ringing · full · resonant |
| 36 | asphyxiated (5) | choked · strangled · breathless · constricted |
| 37 | goons / miscreants (18) | thugs · henchmen · Benedikt's men · heavies |
| 38 | anxiousness / quietness / calmness / coldness (40) | anxiety · quiet/silence · calm · chill |
| 39 | inquisitiveness / inquisitive (18) | curiosity · curious · searching (eyes) |
| 40 | took a pause (12) | paused · fell silent · stopped |

(40 listed because several pairs are near-tied at the 30th slot.)

---------------------------------------------------------------------------------------------------

## 8. NOTES FOR EDIT AGENTS

- **Density, not replacement.** The voice *is* the Latinate noun plus a slightly formal verb. Thin to about
  half, and don't flatten to plain modern English. A paragraph that loses every "visage/aura/demeanour" no
  longer sounds like this author.
- **Fix misuse first, then thin.** A misused rare word (orotund, delirious, stature) should become a correct
  word of *similar* register (booming, frantic, bearing), not a plain one (loud, upset, body).
- **Keep the good oddities:** "a shade below screaming" (ch 26), "draped in the shroud of silence" (ch 29), "haar"
  and "brume" (ch 1), "Past few days were nothing but feet on the streets" (ch 24), "hullabaloo", "in a jiffy"
  (once), "famished" (Stephen's joke), "a frisson of hope".
- **Silent fixes** (no author query needed): articles, possessives, confusable pairs (§3.1), spelling (§4),
  number and capital style (§5).
- **Author query needed:** sense errors where the intended meaning is unclear (e.g. "badested ridge" (ch 4),
  "absolvent" (ch 43), "runic spell" (ch 80), "superfluous and vigilant" (ch 24)).
