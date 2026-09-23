# 07 – Anti-AI editing guide: keeping the edit invisible

Scope: all line editors and reviewers of *The Last Scintilla*. Read S01 (ch 0–7) and S06 (ch 41–49) in full and sampled about 60 paragraphs from S02–S05 and S07–S09. All counts come from `/home/user/dad-book/book.md` (82k words), with HTML tags and markdown asterisks stripped. "Narrative" means the text with quoted speech removed.

Companion script: `$WORK/style/07_anti_ai_check.py` checks one edited paragraph against its original. It looks for AI-tell phrases, em-dashes, contractions in dialogue, British spelling, words the author never uses, new fragments and punch-line endings, and the size of the rewrite. Run it on every paragraph you touch:

```
python3 $WORK/style/07_anti_ai_check.py --pid 855 --edit my_edit.txt      # or: echo "..." | ... --edit -
```

The one-sentence rule: **an edited sentence must read as if the author wrote it on a very good day.** It must not read as if someone better, more modern, more American or more "literary" wrote it. Agents and AI detectors pick up changes in texture, not only content. This manuscript has a strong, consistent, slightly formal, Latinate, explanatory texture. Any 2020s creative-writing polish will stand out against it.

---

## 0. The author's baseline in numbers (what "normal" looks like here)

| Feature | Author's value | What an AI edit typically does |
|---|---|---|
| Em-dashes (—) | **0** in 82k words | adds 1–3 per page |
| Spaced dashes ( – or - ) | 30 total (23 en, 7 hyphen) | adds more |
| Semicolons | 28 total (about 1 per 3,000 words) | adds them for "rhythm" |
| Colons in narrative (not times) | 3, all introducing Portuguese speech | "Everything was as he'd hoped: bright sun, …" |
| Narrative sentence length | mean ≈14 words, median 13, 90th pct 22, SD 6 | long-long-SHORT "rhythm" patterns |
| Verbless fragments | ≈5 in the book ("Change for the worse." ch 1; "Sacred." ch 39; "Thud!!" ch 33) | "Not a word." "The windows, dark." |
| Paragraphs ending in a ≤5-word narrative sentence | 44 of 889 multi-sentence paragraphs, nearly all dialogue tags ("Benedikt commanded.", "he mumbled."); genuine punch lines ≈3 | a punch-line sentence at the end of every paragraph |
| One-line narrative paragraphs for effect | 2 (ch 52, ch 69) | splits paragraphs into dramatic one-liners |
| Paragraph length | mean 57 words, median 46; 72 over 150 words | chops long paragraphs up |
| Dialogue: "I am" vs "I'm" | **115 : 1** | "I'm" |
| Dialogue: "I will" vs "I'll" | **87 : 0** | "I'll" |
| Dialogue: "you are" / "we are" / "let us" vs contracted | 54:0 / 20:0 / 22:0 | "you're", "we're", "let's" |
| Dialogue negatives: don't / didn't / wasn't / can't | 63 / 23 / 14 / 16, all used freely | (these are fine) |
| Narrative contractions: couldn't / wasn't / didn't | 116 / 77 / 57 (the author does contract negatives in narrative) | (these are fine) |
| "said" | 21 (vs continued 95, blurted 56, announced 41, stated 39, responded 33) | changes every tag to "said" or "replied" |
| "replied" / "muttered" / "retorted" | **0 / 0 / 0** | reaches for these at once |
| "just" / "really" / "actually" | 4 / 2 / 0 | sprinkles them in dialogue |
| Spelling | American: color 17, favor 12, behavior 18, demeanor 19, center 16, -ize 61 vs -ise 0, meters 11, skeptical 4, traveler 7, pajamas 2 | switches to British "colour, realise, centre, tyres" |
| …with these Commonwealth holdovers | towards 125 vs toward 1; amongst 6 vs among 0; grey 3 vs gray 1; enquired 24 vs inquired 0; "a tad" 6; dates "14th February 2010"; "Pounds" | "toward", "among", "asked" |

**House spelling:** American spelling, but keep *towards, amongst, grey, enquire/enquired*. Keep British-order dates and "6:00 AM" times. Never introduce *colour, realise, centre, tyre, windscreen, pavement→sidewalk* swaps or *Mum*. The book has Mom 6 and Mum 0. Whether a Scottish family should say "Mum" is a question for the style-sheet report, not something to slip in silently.

---

## 1. Catalogue of AI-editing fingerprints to avoid

Each item shows the book count. **0** means the feature is absent: adding it is a fingerprint. If the author already uses it, it is allowed in moderation, and only where the original sentence already reaches for that effect.

### 1a. Vocabulary

| AI-tell word or phrase | Book count | Ruling |
|---|---|---|
| delve / tapestry / testament / palpable | 0 / 0 / 0 / 0 | **Never** |
| "a beat", "for a beat", "a long moment" | 0 / 0 / 0 | **Never** |
| "something shifted / changed / broke (in him)" | 0 | **Never** ("There was something in her that was noble" ch 2 is the author's own form: "something in/about", 8×. Keep those.) |
| "the weight of" (figurative) | 0 (only "body weight" 1) | **Never** |
| "the air thick with", "hung in the air", "thick with" | 0 / 0 / 0 | **Never** |
| flicker(ed) / etched / coiled / taut-clipped-measured voice | 0 / 0 / 0 / 2-0-0 | **Never** |
| intricate | 1 (ch 22 "intricate composed character") | Do not add |
| visceral, nuance, vibrant, realm, pivotal, underscore, unwavering, steely, linger | all 0 | **Never** |
| heart hammered / pounded / thudded; pulse quickened | 0; pulse 3 (all literal: ch 22, ch 43, ch 46) | **Never**. The author's forms: "heart sank" (4), "heart was pulsating with such vigor" (3), "heart leaped into her mouth" (2), "thumping of her heart" |
| jaw tightened / clenched; swallowed; blinked; raised an eyebrow; narrowed / widened eyes; stiffened; ran a hand through his hair; leaned back | **all 0** | **Never.** This whole "body-language beat" register is foreign to the book. The author uses *visage turned pale*, *trickle of sweat on her temple*, *fidgety stature*, *a thousand emotions crossed his face* |
| let out a breath / exhaled / inhaled | 0 / 0 / 0 | Never. The author has "took a deep breath" (4) and "took a sigh of relief" (2) |
| ghost of a smile / corner of his mouth / unreadable | 0 / 0 / 0 | Never. The author's forms: "a thin smile", "a wry smile" (4), "carried a … smile" (6), "passed a … smile" (12) |
| couldn't help but | 0 | Never. The author writes "couldn't resist" (6) |
| washed over / settled over / silence stretched / silence fell | 0 / 0 / 0 / 0 | Never. The author's forms: "a wave of sadness covered her soul" (ch 49), "engulfed" (10), "consumed" |
| ominous, menacing, stunned, tranquil, swift, hasty, chilly, cozy, forlorn, utter | **all 0** | Do not use these as "better" synonyms. Author equivalents: sinister (1), frightful, shocked (8), serene (5), swiftly (12), hastily (8)/in haste (12), cold (25), eerie/ghostly |
| whispered / gaze / gently / quiet | 8 / 17 / 17 / 23 | Author-native. Fine, but do not add more |
| journey (figurative), crucial, meticulous, amidst, bustling, labyrinth, enigma, cacophony, echoed, profound | 19, 4, 3, 2, 3, 2, 2, 3, 3, 2 | Author-native. Keep where they are and add at most one per chapter |
| Moreover / Furthermore / Additionally / Ultimately / Indeed / Notably | 2 / 0 / 0 / 0 / 2 / 0 | Do not add. The author links with *Besides*, *Though*, *However* |

### 1b. Structures

| Structure | Author count | Ruling |
|---|---|---|
| **Em-dash insertion** (—) | **0** | **Absolute ban.** Where a dash seems needed, use a comma, "as", or a full stop. The author's own dash is a spaced en-dash or hyphen ("one small glitch - she didn't have…", ch 2; "an easy question for her – she had done…", ch 13). Keep the ones already there and do not create new ones. |
| "It wasn't X — it was Y" / "It wasn't X. It was Y." | 0 | **Never.** The author's contrast shape is a long single sentence: "…was not frustrating him for her misdeed, but for her disappearance" (ch 7; "not …, but" 9×). |
| "Not X. Not Y." anaphoric fragments; "To hold her. To keep her." | 0 | **Never** |
| Rhetorical "And yet." / sentence-initial "Yet" / "Still," | 0 / 0 / 0 | **Never.** Sentence-initial **"And"** is author-native (≈80×), but always leads into a full, long clause: "And without waiting for her affirmation he ordered, …" (ch 2), "And at that very moment, Benedikt's energetic stature got transformed…" (ch 49). |
| Tricolons | ≈128 "X, Y and Z" lists; "no X, no Y" 7× | Allowed, because they are the author's. Their tricolons are **cumulative and slightly unbalanced**: "thrilled, nervous, dizzy, all at once" (ch 49), "a child, a restless soul, and an honest man" (ch 49), "No smile, no widening of eyes or a trickle of sweat, not a shade of any slipping hint" (ch 2). Do not build new neat, symmetrical, rising-rhythm triads, and do not tidy the author's ragged ones into perfect parallelism. |
| Sentence-final punchy fragment or one-liner paragraph | ≈5 fragments; 2 one-line paragraphs | **Do not add.** The author ends paragraphs on explanatory sentences ("…for reasons best known to them." ch 1; "…with a crowded mind and a hopeful heart she closed her eyes." ch 47). The rare punch lines are chapter-end foreshadowing: "Change for the worse." (ch 1), "She was there for him." (ch 7). Leave those alone. |
| Short declarative sentences | common, but always subject + stative verb: "Benedikt was furious." (ch 6), "His heart sank." (ch 43), "Stephen resisted." (ch 43) | Allowed in that exact shape. Never verbless. |
| Colon lists; semicolons for rhythm | ≈0 / 28 | Do not add |
| Over-smooth parallelism, uniform "rhythm" | The author varies within 7–22 words and joins clauses with *and / as / while / with* | Keep the author's joins. Do not recast into balanced pairs ("He wanted to speak; he dared not.") |
| Present-participle openers ("Grabbing her bag, she…") | 81 | Author-native. Fine |
| Rhetorical question in narration | 14 ("Could he pull the game?" ch 2) | Keep, but do not add |
| Show-don't-tell "action beats" replacing stated emotion | The author **states** emotion: "Benedikt was puzzled", "She was famished" | Do **not** convert "He was nervous" into "His fingers drummed the table." Adding invented gestures is new imagery (see §3). |
| Sanitising all idiosyncrasy | – | Do not. See the "keep" list in §2e. |
| New similes or metaphors | "like a" 38, "as if" 44 already | Do not add a single new one. Fix broken ones by deletion. |

### 1c. Tone and register

| Shift | Author count | Ruling |
|---|---|---|
| Therapy-speak: "boundaries", "trauma", "process", "closure", "heal", "space", "valid", "toxic", "triggered", "vulnerable" | The words exist, but **never** in the therapy sense: "rage had no boundaries" (5), "bring it to a closure" (4, business sense), "traumatized state" (literal), "gave her the much-needed space" (1) | Never use the modern-psychology sense ("She needed to process it", "he respected her boundaries", "she was allowed to feel this"). |
| American casual idiom: okay, gonna, yeah, guys, folks, kinda, awesome, totally, literally, "holed up", "floored it", "out of nowhere" | okay 1, yeah 1, guys 7 (Jules and the thugs only), gonna/folks/kinda/awesome/totally/literally 0 | Do not add. Characters speak formally, even villains: "I neither have the patience nor the time." (ch 43) |
| Snark, irony, wit, knowing narrator | The narrator is earnest and never winks. Rare humour is gentle and explained ("He finally got something right even if it was by accident." ch 44) | Never add wry asides, bathos or deadpan one-liners |
| Modern thriller register (clipped, visceral, present-tense feel) | – | The book is past-tense, explanatory and courtly. Keep it so. |
| Genre-romance clichés ("his breath caught", "electricity", "butterflies") | 0 | Never. The author's own: "A sense of exhilaration…", "sent shivers through his spine" (spine 7, shiver 5) |
| "Literary" polish words (liminal, ineffable, susurrus, gossamer, sepulchral) | 0 | Never. The author's rare words (haar, brume, tincture, confetto, libretto, cataleptic) are their own. Do not add others "in the same spirit". |

---

## 2. The author's own fingerprint: reuse it so changes blend in

### 2a. Connectors and sentence openers (sentence-initial counts, narrative)

| Opener | Count | Example |
|---|---|---|
| He / She / [Name] was / had / knew | He 764, She 543, "It was" 155, "He was" 142, "There was" 84, "He knew" 42 | "Benedikt knew Sanchez needed medical attention." |
| After (a / about / few …) | ≈100 | "After about thirty minutes into the treatment…" |
| With [a / some / great …] | 67–82 | "With a dejected tone, he asked…" |
| As | 49–66 | "As he climbed the stairs he announced…" |
| Though | 45–52 | "Though he was dressed for the season, he couldn't…" |
| While | 27–41 | "While Sanchez remained disconcerted Benedikt was in peace." |
| Besides | 33–40 | "Besides his own wheezing…"; "Besides she was extremely helpful." |
| Soon | 28–35 | "Soon he disappeared…" |
| Once | 28 | "Once inside she pulled the rope in…" |
| This time | 27 | "This time the men committed no mistakes." |
| Despite | 14–18 | "Despite all the proceedings, Adriana demonstrated no penitence." |
| Without | 14–18 | "Without wasting any time…" (7) |
| However, | 11–13 | |
| By now | 17 | "By now he was next to her." |
| For the first time (that evening) | 17 | |
| Unlike (before / last time) | 9 | |
| All this while | 9 | |
| Deep inside / within / somewhere | 7 | "Deep inside he knew…" |
| No matter how | 15 | |
| It was evident | 9 | |
| Like always / like before | 9 | |

### 2b. Verbs of speech (use these, in this order of preference, when a tag must change)

*continued* 95 · *blurted* 56 · *announced* 41 · *stated* 39 · *responded* 33 · *instructed* 34 · *concluded* 27 · *enquired* 24 · *said* 21 · *asked* 18 · *screamed* 16 · *declared* 15 · *put forward* 14 · *demanded* 13 · *mumbled* 13 · *queried* 10 · *snapped* 10 · *shouted* 9 · *whispered* 8 · *informed* 7 · *uttered* 5 · *murmured* 4.
**Not in the book:** *replied, muttered, retorted, quipped, breathed, hissed.*
When a tag is the problem, **delete it** if the speaker is clear. If you must replace one, use *said, asked, responded, continued* (all author-native, and plainest). Never introduce *replied*.

### 2c. Verbs of motion

*walked* 34 · *headed* 31 · *rushed* 25 · *dashed* 21 · *hurried* 17 · *sauntered* 17 · *paced* 16 · *leaped* 14 · *slipped* 14 · *sprinted* 12 · *swung* 8 · *sprang / sprung* 7 · *scurried* 4 · *trod* 4 · *sped* 3 · "took a few long strides" 2.
**Not in the book:** *strode, padded, tumbled, scrambled (2), tugged, wrenched, slammed.*
Note: many of the author's motion verbs are **misapplied** ("sprinting out" for a stroll to the bakery, "sauntered" in urgency). Fix a misapplied one with the plainest native verb (*walked, headed, went, rushed*), never with a fresh vivid verb.

### 2d. Typical adjectives, adverbs and nouns

- Adjectives: deep 43 · clear 42 · complete 31 · dark 26 · cold 25 · confused 24 · distinct 21 · pale 20 · puzzled 18 · evident 17 · relieved 17 · frustrated 15 · meaningful 14 · delirious 14 · perplexed 13 · startled 13 · firm 13 · deserted 13 · disheveled 12 · anxious 12 · untoward 11 · sharp 11 · vast 11 · subtle 10 · faint 10 · hushed 9 · frail 9 · vigilant 8 · gravelly 7 · dilapidated 6 · arduous 6 · unwarranted 6 · eerie 5 · infectious (smile) 5 · exquisite 5 · wry 4 · ghostly 4.
- Adverbs: slowly 38 · hardly 30 · finally 27 · gently 17 · swiftly 12 · carefully 12 · clearly 12 · patiently 9 · visibly 8 · hastily 8 · miserably 8 · discreetly 7 · sheepishly 6 · profusely 4.
- Abstract nouns: brooding 23 · demeanor 19 · stature 19 (often misused for posture or state) · apprehension(s) 17 · ordeal 12 · trepidation(s) 8 · confrontation 8 · visage 6 · countenance 6 · misery 6 · hullabaloo 4 · "shade(s) of" 27 · "a sense of" 25 · "hint of" 7.

### 2e. Idioms and pet phrases (the author's "tics"): **keep, and reuse sparingly**

"with a [adj] voice / tone" (78) · "in a [adj] manner / tone" (32) · "with great [noun]" (22) · "with utmost [care / silence]" (14) · "had no clue" (21) · "a while back / not too long ago" (14) · "no option but" (9) · "every passing minute / moment" (10) · "laced with (fear)" (9) · "mind was racing" (7) · "heart sank" (4) · "renewed hope" (6) · "dwindled / dwindling hope" (8) · "without wasting any time" (7) · "sprang / sprinted to action" (7) · "in a jiffy" (4) · "the much-needed" (5) · "a tad" (6) · "gave nothing away" (7) · "for reasons best known to her / them" (2) · "cursory glance" (5) · "prying eyes" (6) · "not a soul" (6) · "engulfed" (10) · "exuded" (11) · "came to life" (6) · "faded away" (7) · "drifted" (14) · "with all his / her might" (6) · "get / got hold of" (13) · "at the earliest (possible time)" (6) · "in haste" (12) · "took a pause" · "to his / her advantage / relief / surprise" (13) · "gave away (her / its) resistance" (2) · "staring at the vacuum / void / nothingness" (11) · "a thousand emotions crossed his face" (3) · "competing thoughts" (4) · "Will you?" as a tag question in dialogue ("Leave me alone. Will you?") · "the goons" (9).

**Idiosyncrasies to keep (voice, not errors):** personified weather and light ("A dull wind was casually sauntering with a hint of laziness written over it" ch 45); formal, uncontracted dialogue; "Let us…"; stated emotions; long explanatory closing sentences; chapter-end foreshadowing ("little they knew…", 2); rare words used correctly (haar, brume, visage, countenance).
**Idiosyncrasies to fix (outright errors):** wrong word meaning ("never failed to *cease* her excitement" ch 1, "a strong *rumor*" ch 1, "it didn't *nudge*" ch 45, "exhilaration *regained* him" ch 49, "*hurled* her off the plane" ch 49), missing articles ("few feet", 140 bare *few* vs 55 *a few*; "little further"), tense slips ("He puts the spread" ch 1), double negatives ("without no trace" ch 6). Fixing grammar is invisible. Replacing voice is not.

### 2f. 50 author-native words and phrases an editor can safely draw on

When a replacement is unavoidable, take it from this list (all occur 4+ times in the book):

1. besides
2. though
3. however
4. despite
5. soon
6. by now
7. all this while
8. for the first time
9. this time
10. unlike before
11. deep inside
12. it was evident
13. no matter how
14. hardly
15. slowly
16. gently
17. swiftly
18. hastily
19. discreetly
20. sheepishly
21. continued
22. responded
23. stated
24. announced
25. enquired
26. blurted
27. mumbled
28. headed
29. rushed
30. dashed
31. paced
32. sauntered
33. leaped
34. puzzled
35. perplexed
36. startled
37. relieved
38. frustrated
39. pale
40. faint
41. distinct
42. deserted
43. disheveled
44. vigilant
45. with a gravelly voice
46. in a hushed tone
47. a sense of
48. a shade of
49. mind was racing
50. heart sank

Also safe: gave nothing away · without wasting any time · had no clue · no option but · with renewed hope · the much-needed · a tad · to her advantage · engulfed · exuded · demeanor · visage · ordeal · apprehension · trepidation · brooding.

---

## 3. Principles for minimal-footprint editing

1. **Delete before you substitute.** Most broken phrases in this book are *extra* words: "lost crucial time fleeting", "unwarranted that may be uncalled for", "the droplet of coldness had taken a half ice half water formation". Cutting leaves no new fingerprint. Substitution always does.
2. **Substitute only with author-native words** (§2f). Before introducing any word not already in the paragraph, grep book.md. If the count is 0, find another word unless the correction strictly needs it (e.g. *a few*, *budge*). The checker flags these.
3. **Keep the sentence skeleton.** Keep the same subject, the same opening word (With… / Though… / Besides…), the same clause order and the same sentence count (±1). Fix inside the skeleton.
4. **Limit scope to the broken phrase.** A paragraph with one error gets a one-phrase edit. Guideline: under 20% of tokens changed is normal, 20–35% needs a reason, over 35% is a rewrite and must be cut back or justified to the reviewer.
5. **Never add new imagery, similes, metaphors, jokes, gestures or sensory detail.** No frost patterns, no mud on the windscreen, no drumming fingers. Where an image is broken, repair it minimally ("gave away a blip sound" → "made a blip sound") or delete it. Do not swap it for a better one.
6. **Never add plot information, motive, backstory or interpretation.** No "Memories of their night together", no "or so it seemed", no hints the author did not plant. Continuity fixes belong to the analysis reports and must be flagged, not smuggled in.
7. **Never make an edit longer than the original** (checker flag: over 105% of the original word count).
8. **Keep house spelling:** American spelling with *towards / amongst / grey / enquired*; "6:00 AM"; "14th February 2010".
9. **Keep dialogue formal and uncontracted** for pronoun + be/will/us ("I am", "I will", "you are", "let us"). Negative contractions (don't, didn't, can't) are fine as the author uses them. Punctuation around quotes may be corrected to standard form (comma inside the closing quote, capital after an opening quote). That is copy-editing, not voice.
10. **Keep the author's paragraph breaks**, unless a paragraph contains two speakers' lines (e.g. ch 47 holds Benedikt's "How is the pain?" and Sanchez's "Where are you taking me?"; also ch 2, ch 21, ch 31). Then split at the change of speaker and change nothing else. Do not break long narrative paragraphs for pace. Do not create one-line paragraphs.
11. **No punctuation upgrades:** no em-dashes, no new semicolons, colons, italics for emphasis or ellipses.
12. **Keep stated emotion stated.** "Benedikt was puzzled." stays a statement. Do not dramatise it into a gesture.
13. **Leave the author's rhythm alone:** medium-length, joined sentences; openings with *With / As / Though / Besides*; endings on an explanatory clause. Do not engineer a short final beat.
14. **One problem, one fix.** If a sentence has two errors, fix both inside the same sentence. Do not treat that as licence to recast the paragraph.
15. **When in doubt, leave it.** An odd but grammatical and intelligible sentence in the author's voice is better than a smooth one in ours.

---

## 4. Self-check test for every edited paragraph

Editors run these before submitting. Reviewers rerun them on a random 1-in-5 sample and on every paragraph where more than 20% of tokens changed.

**A. The drop-in test (the main test).** Take each changed sentence on its own. Would it be out of place if dropped into an *untouched* chapter of the book (say ch 7 or ch 49)? If a reader of the untouched chapter would notice a "different hand", rewrite it closer to the original.

**B. The vocabulary test.** Every word you introduced must appear in book.md, or be a plain grammatical necessity. `grep -ciw 'word' /home/user/dad-book/book.md`. The checker lists new zero-count words automatically.

**C. The blacklist test.** No new hits from §1a or §1c, and none of: —, "a beat", "something shifted", jaw, swallowed, exhaled, flicker, "couldn't help but", replied, muttered, okay, just, really.

**D. The shape test.**
- Word count is at most the original.
- Sentence count is within the original +1.
- No new verbless fragment.
- The paragraph does not now end on a sentence of 5 words or fewer (unless the original did).
- No new one-line paragraph.
- No new em-dash, semicolon or colon.

**E. The dialogue test.** No new *I'm / I'll / you're / we're / let's / it's*. No tag changed to *replied*. Characters still sound formal.

**F. The content test.** List every noun phrase in the edit that is not in the original. Each must be a synonym for something already there. If any is a new object, image, gesture, fact or feeling, remove it.

**G. The diff test.** Token change under 20% is fine. 20–35% needs every change justified. Over 35% goes back to the editor.

**H. The read-back test.** Read the original and the edit aloud, one after the other. The edit should sound like the same person, more correct, not more stylish. If it sounds more stylish, it has failed.

Automated: `python3 $WORK/style/07_anti_ai_check.py --pid <id> --edit <file>` covers B–E and G. It exits with code 1 if any FLAG is raised.

---

## 5. Five worked examples

For each example: the original, (a) a typical AI over-edit with its fingerprints, (b) the correct author-matched edit, and the checker result.

### Example 1: domestic description with misused words (ch 1)

**Original (ch 1)**
> This Sunday was no different. Besides the cold weather, everything else was aligned with his expectations. Bright sun, resting family, and the dewiness in the air, a perfect Sunday as he wanted it to be. Following his routine, he stepped out of the house and headed to the bakery. His daughter crawled out of the bed and dashed to the window. The droplet of coldness had taken a half ice half water formation on the windowsill, battling the variance in temperature between the heated room and outside coldness. She grabbed her arm sleeves, stretched the cloth further out and used it as a perfect tool for cleaning the haze. As the window gave way to the outside view, she saw her father sprinting out humming his favorite song. A sight no matter how many times she had seen never failed to cease her excitement. She stood there, like always, waiting for her father to dissolve in the morning mist. Soon he disappeared, and she dashed back to her bed pretending to be asleep again. There was a strong rumor about both father and daughter playing this little game, but they pretended unaware of each other's ruses for reasons best known to them.

**(a) Typical AI over-edit (do NOT do this)**
> This Sunday was no different — or so it seemed. The cold aside, everything was just as he'd hoped: bright sun, a sleeping family, dew hanging in the air. He slipped out of the house and set off for the bakery. Upstairs, his daughter tumbled out of bed and padded to the window, where frost had crept across the glass in delicate, lace-like patterns. She tugged her sleeve over her fist and wiped a small circle clear. There he was, jogging down the lane, humming his favourite song. No matter how many times she watched it, the sight never failed to thrill her. She waited, as she always did, until the mist swallowed him whole. Then she scrambled back under the covers. It was their little game — one neither of them would ever admit to. Not a word.

Fingerprints: 2 em-dashes; a colon list; "or so it seemed" (new foreshadowing); "he'd"; "just"; new imagery (lace-like frost, "swallowed him whole", "down the lane"); non-native verbs (tumbled, padded, tugged, wiped, scrambled); British "favourite"; verbless punch ending "Not a word."; the author's "for reasons best known to them" is gone. Checker: 9 FLAGS, 68% of tokens changed.

**(b) Correct author-matched edit**
> This Sunday was no different. Besides the cold weather, everything else was aligned with his expectations. Bright sun, resting family, and the dewiness in the air, a perfect Sunday as he wanted it to be. Following his routine, he stepped out of the house and headed to the bakery. His daughter crawled out of bed and dashed to the window. The droplets of coldness on the windowsill had turned half ice, half water, battling the difference in temperature between the heated room and the coldness outside. She stretched her sleeve over her hand and used it to clear the haze. As the window gave way to the outside view, she saw her father sprinting out humming his favorite song. No matter how many times she had seen it, the sight never failed to excite her. She stood there, like always, waiting for her father to dissolve in the morning mist. Soon he disappeared, and she dashed back to her bed pretending to be asleep again. Both father and daughter played this little game, but they pretended to be unaware of each other's ruses for reasons best known to them.

What changed:
- "cease her excitement" (wrong meaning) became "excite her".
- "a strong rumor about" (wrong word) was deleted.
- "pretended unaware" became "pretended to be unaware".
- "the bed" became "bed".
- The droplet sentence was trimmed but keeps the author's "coldness" and "battling".
- The sleeve sentence was trimmed.

Everything else is untouched, including "sprinting" and "dissolve in the morning mist". Checker: no FLAGS, 16% of tokens changed.

### Example 2: action with grammar faults (ch 41)

**Original (ch 41)**
> He regretted his decision of running away from the situation, and between his trepidations and confusion, he knew he had lost crucial time fleeting. With that sudden urge of wisdom, he swung his car, but failed to negotiate the turn well and crashed into the paddy field. He dug the car out, and with some struggle managed to get it back on the road. The tires made a screeching noise as he pressed the accelerator with all force but was instantly forced to apply the brakes to avoid banging into an oncoming car. Adriana maintained her silence despite all the commotions happening around her. He was about to cut loose when he saw a young man rushing towards him raising his hand high signaling him to stop.

**(a) Typical AI over-edit**
> Regret hit him like a fist. He'd run — and every second he wasted was a second Sanchez didn't have. Jaw tight, he wrenched the wheel around, misjudged the turn and ploughed into the paddy field. Mud sprayed the windscreen. It took him precious minutes to rock the car free. Back on the road, he floored it, tyres shrieking, then slammed on the brakes as another car loomed out of nowhere. Beside him, Adriana said nothing. He was about to tear off again when a young man sprinted into the road, arm raised, waving him down.

Fingerprints: new simile ("like a fist"); em-dash; "Jaw tight"; "he'd"; British *ploughed / windscreen / tyres*; new detail (mud, "precious minutes"); US idiom "floored it", "out of nowhere"; "said nothing"; the author's *trepidations*, *urge of wisdom* and *maintained her silence* are gone. Checker: FLAGS, 76% of tokens changed.

**(b) Correct author-matched edit**
> He regretted his decision of running away from the situation, and between his trepidations and confusion, he knew he had lost crucial time. With that sudden urge of wisdom, he swung his car around, but failed to negotiate the turn and crashed into the paddy field. With some struggle, he managed to get the car back on the road. The tires made a screeching noise as he pressed the accelerator with all force, but he instantly had to apply the brakes to avoid banging into an oncoming car. Adriana maintained her silence despite all the commotion happening around her. He was about to speed away when he saw a young man rushing towards him, raising his hand high and signaling him to stop.

What changed:
- "fleeting" was deleted.
- "well" was deleted.
- "He dug the car out, and" was cut, because it repeats the next clause.
- "was instantly forced" became "he instantly had", to fix the grammar and the forced/force echo.
- "commotions" became "commotion".
- "cut loose" (wrong idiom) became "speed away". The author has "sped away".
- Two commas were added.

Checker: no FLAGS, 10% of tokens changed.

### Example 3: emotional interior, where AI edits go furthest (ch 44)

**Original (ch 44)**
> Benedikt was devastated as if a bolt had struck shattering him to pieces. He was a man of thousand shades, oscillating between hues of love and shadows of pain. He had waited for this moment for a lifetime and when the moment presented itself he was unable to fathom. It was surreal, and with every passing minute, it was becoming hard for him to comprehend. He wanted to embrace her, hold her forever and never let her disappear again.

**(a) Typical AI over-edit**
> Something inside Benedikt shattered. He had waited a lifetime for this moment, and now that it had come, it felt unreal — like watching his own life from somewhere far away. Love and pain warred within him, each refusing to yield. He wanted to hold her. To keep her. To never let her slip away again.

Fingerprints:
- "Something inside … shattered"
- an em-dash
- a new simile ("like watching his own life…")
- a new metaphor ("warred within him, each refusing to yield")
- an anaphoric fragment triad ("To keep her. To never…")
- the author's signature image ("a man of thousand shades … hues of love and shadows of pain") has been deleted as "purple"

Checker: FLAGS, 73% of tokens changed.

**(b) Correct author-matched edit**
> Benedikt was devastated, as if a bolt had struck and shattered him to pieces. He was a man of a thousand shades, oscillating between hues of love and shadows of pain. He had waited for this moment for a lifetime, and when the moment presented itself he was unable to fathom it. It was surreal, and with every passing minute it was becoming harder for him to comprehend. He wanted to embrace her, hold her forever and never let her disappear again.

What changed: grammar only. "struck shattering" became "struck and shattered", "thousand" became "a thousand", "fathom" became "fathom it", "hard" became "harder", and two commas were adjusted. The author's ornate register is the voice and stays. (Whether "devastated" is the right emotion for this reunion is a separate note for the author, not a silent change.) Checker: no FLAGS, 4% of tokens changed.

### Example 4: scene-setting opener with personification (ch 45)

**Original (ch 45)**
> The streetlights were appearing in a sporadic fashion on the busy roads of Lisbon. A dull wind was casually sauntering with a hint of laziness written over it. People were gracing the streets aimlessly walking with no set destination, but not Maxwell. He had a purpose, his face exuded anxiety and his mind clouded with a sense of urgency. He parked the car a street away from where Benedikt was housed a few hours ago. The porch was empty, and the place was in complete darkness. He tried opening the front door, but it didn't nudge. Frustrated he pulled out his gun, pointed to the doorknob and shot it. The silencer on the gun gave away a blip sound and the knob gave away its resistance. He flung the door open and the worst of his fears came true.

**(a) Typical AI over-edit**
> One by one, the streetlights of Lisbon flickered to life. A lazy wind drifted through the streets, where people wandered without purpose. Maxwell was not one of them. Urgency hummed beneath his skin. He parked a street away from the house where Benedikt had been holed up only hours earlier. The porch was empty. The windows, dark. The door wouldn't budge. He drew his gun, pressed the silencer to the lock and fired — a soft, flat cough — and the door swung inward. His worst fears were confirmed.

Fingerprints: "flickered to life"; a new metaphor ("Urgency hummed beneath his skin"); "holed up"; a verbless fragment ("The windows, dark."); staccato short sentences; an em-dash with new sound imagery ("a soft, flat cough"); a punch-line ending; the author's sauntering wind has been flattened to "a lazy wind drifted". Checker: FLAGS, 76% of tokens changed.

**(b) Correct author-matched edit**
> The streetlights were appearing in a sporadic fashion on the busy roads of Lisbon. A dull wind was casually sauntering with a hint of laziness written over it. People were gracing the streets, walking aimlessly with no set destination, but not Maxwell. He had a purpose. His face exuded anxiety and his mind was clouded with a sense of urgency. He parked the car a street away from where Benedikt had stayed a few hours ago. The porch was empty, and the place was in complete darkness. He tried opening the front door, but it didn't open. Frustrated, he pulled out his gun, pointed it at the doorknob and shot it. The silencer on the gun made a blip sound and the knob gave away its resistance. He flung the door open and the worst of his fears came true.

What changed:
- The comma splice was split, making "He had a purpose." That keeps the author's plain subject + verb short-sentence shape.
- "his mind clouded" became "his mind was clouded".
- "was housed" became "had stayed".
- "didn't nudge" (wrong word) became "didn't open". This is a plain native word. "budge" would be correct too, but it never occurs in the book.
- "pointed to" became "pointed it at".
- The first "gave away" became "made", removing the double "gave away".

The sauntering wind, "gracing the streets" and "gave away its resistance" are the author's and stay. Checker: no FLAGS, 6% of tokens changed.

### Example 5: romantic interiority leading into dialogue (ch 49)

**Original (ch 49)**
> Benedikt was jolted by an unexplainable sensation by her touch. A sense of exhilaration regained him, and he slowly drifted to a euphoric state. The moments he had spent with her in the past came rushing back, making him thrilled, nervous, dizzy, all at once. He controlled his surge of emotions with great difficulty and helped her sit down at the breakfast table. His mind was racing. He wanted to speak but was refrained from the fear of stating something unwarranted that may be uncalled for. And before he could decide the best course forward Sanchez's soft undertone voice broke the uncomfortable quietness. "Thank you."

**(a) Typical AI over-edit**
> Her touch sent a jolt through him. Memories of their night together came flooding back, and for a moment he was dizzy with it — thrilled, nervous, breathless. He steadied himself and guided her to the table, his heart hammering. There was so much he wanted to say. But the words wouldn't come. Before he could find them, her voice cut softly through the silence. "Thank you."

Fingerprints:
- "Memories of their night together" (new interpretation and sexual specificity)
- "came flooding back"
- an em-dash
- the author's ragged triad "thrilled, nervous, dizzy, all at once" tidied into a neat one
- "steadied himself", "heart hammering"
- a manufactured beat ("But the words wouldn't come.")
- "cut softly through the silence"

Checker: FLAGS, 82% of tokens changed.

**(b) Correct author-matched edit**
> Benedikt was jolted by an unexplainable sensation at her touch. A sense of exhilaration consumed him, and he slowly drifted to a euphoric state. The moments he had spent with her in the past came rushing back, making him thrilled, nervous, dizzy, all at once. He controlled his surge of emotions with great difficulty and helped her sit down at the breakfast table. His mind was racing. He wanted to speak but feared stating something uncalled for. And before he could decide the best course forward, Sanchez's soft voice broke the uncomfortable quietness. "Thank you."

What changed:
- "by her touch" became "at her touch".
- "regained him" (wrong verb) became "consumed him". The author uses "a sense of relief consumed his countenance" (ch 7).
- "was refrained from the fear of stating something unwarranted that may be uncalled for" (a double redundancy) was cut down to "feared stating something uncalled for".
- "soft undertone voice" became "soft voice".
- A comma was added.

"His mind was racing." and "And before…" stay. Checker: no FLAGS, 8% of tokens changed.

---

## 6. Where the temptation will be strongest (hot spots)

- **Scene-setting openers** (ch 1, ch 2, ch 3, ch 42, ch 45, ch 49). AI editors "modernise" the ornate weather and architecture. Trim errors, but keep the personification and the catalogue style.
- **Benedikt's yearning passages** (ch 7, ch 42, ch 44, ch 46, ch 47, ch 49). These are the prime targets for "something shifted / heart hammering / the weight of". Correct grammar only.
- **Love scenes** (ch 3). Do not add sensory detail. Remove only word errors ("caressed her lips", "made her fell").
- **Action set pieces** (ch 3, ch 41, ch 43). Do not add staccato fragments or new physical detail. Fix sequence and grammar.
- **Dialogue** everywhere. Keep "I am / I will / Let us / Will you?". Keep the author's tag verbs, but thin them by deletion.
- **Chapter-end lines** (ch 1, ch 7, ch 42, ch 49). These are the author's only "punch" endings. Leave them as they are, apart from grammar ("little he knew about the detour she took" is fine).
