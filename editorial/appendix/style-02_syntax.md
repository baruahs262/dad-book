# 02 · Sentence architecture, rhythm and punctuation

Dimension report for the voice-preserving edit of *The Last Scintilla*.
Close reading: S02 (ch 8–15), S05 (ch 31–40), S09 (ch 71–85), read in full.
Statistics: all 1,422 body paragraphs in `paras.json` (175 chapter/part/dateline headings excluded), about 81,400 words. The scripts are in `$WORK/style/tmp/*.py` (`lib.py` holds the sentence splitter). The heuristic counts are marked "≈". Sentence counts for dialogue split each paragraph on quote marks, so the mixed straight and curly quotes add a little noise.

---

## 0. The rhythm in one paragraph

The author writes **evenly metered, medium-length sentences** of 9–18 words, built mainly from **subject + verb, "and", and trailing participle** rather than from subordination. Paragraphs usually **open short** (often on a flat verdict of a feeling, like "Benedikt was flabbergasted.") and **build towards a longer, cumulative closing sentence**. They almost never end on a short punch line. Punctuation is sparse. There are few commas inside the sentence (57% of narration sentences have none). The author has almost no colons, uses few semicolons (and many of those are misused), and dashes are rare and always single. The exclamation marks come in rare bursts, often doubled ("!!"). In dialogue the author prefers to **put the action beat before the speech**: *"… and with a trembling voice continued, “…”"*. Past-progressive "was/were + -ing" is a real texture of the voice at about 8 per 1,000 narration words.

---

## 1. Sentence length

### 1.1 Narration vs dialogue (words per sentence)

| Measure | Narration (pure narration paragraphs) | Narration (all narration segments, incl. tags) | Dialogue (inside quotes) |
|---|---|---|---|
| n sentences | 3,439 | 5,021 | 1,611 |
| **mean** | **14.4** | 13.5 | **8.5** |
| median | 14 | 13 | 7 |
| p10 / p25 | 7 / 10 | 6 / 9 | 3 / 5 |
| p75 / p90 / p95 | 18 / 23 / 25 | 17 / 22 / 25 | 11 / 16 / 19 |
| max | 53 | 53 | 36 |
| SD | 6.0 | 6.1 | 5.3 |

Distribution of sentence lengths in pure narration: 1–5 words 4.4% · 6–10 23.0% · **11–15 33.3%** · 16–20 23.8% · 21–25 10.8% · 26–30 3.5% · 31–40 1.2% · 41+ ≈0.03% (a single sentence).

- The spread is narrow. Only about 4.7% of narration sentences exceed 25 words, and very short ones (≤5 words) are rare too, at 4.4%. The mean absolute difference between adjacent sentences is only 6.4 words. The prose moves at a **steady medium stride** and does not swing between long and short.
- The mean is stable across the book: S01 14.4 · S02 15.6 · S03 15.3 · S04 14.8 · S05 14.1 · S06 13.6 · S07 14.5 · S08 14.1 · S09 13.4. It shortens slightly as the plot speeds up.
- The very long sentences are nearly all **comma-spliced run-ons**, not crafted periodic sentences. Examples:
  - 53 words, (ch 12): "The place was bigger than life, it had a gigantic water fountain …, an array of modern paintings were graciously covering the walls, she could see at a distance elevator guarded by biometric access and …"
  - 38 words, (ch 47): "… she had gone through, with a crowded mind and a hopeful heart she closed her eyes."
- Dialogue is clipped and formal: 33% of dialogue sentences are ≤5 words, e.g. "Good riddance." (ch 8), "What is it?" (ch 71), "Us?" (ch 85). Speech is uncontracted: **"I am" 113 vs "I'm" 1**, and **"Let us" 21 vs "Let's" 0**. Negatives are contracted ("didn't" 21, "don't", "can't"). This is character formality and belongs to the voice.

### 1.2 Paragraph length

| Measure | All body paragraphs | Narration-only paragraphs | Paragraphs containing dialogue |
|---|---|---|---|
| n | 1,422 | 679 | 743 (52%) |
| mean words | 57 | **73** | 43 |
| median | 46 | 62 | 33 |
| p90 / p95 | 116 / 151 | 139 / 172 | 84 / 111 |
| max | 417 (ch 30) | | |
| sentences per paragraph | mean 4.3, median 4 | | |

- There are 209 one-sentence paragraphs (15%), of which 64 are pure narration. These are **transitional beats** rather than stingers, e.g. "Sanchez agreed to meet them at a nearby coffee shop and raised her hand to stop an approaching taxi." (ch 71) and "The person agreed." (ch 9). The occasional reflective one-liner closes a chapter: "The time had halted for them." (ch 81).
- Chapters average 957 words (median 818) and about 17 paragraphs. The **first paragraph of a chapter is long** (mean 95 words), for setting, weather or recap. The **last paragraph is shorter** (mean 53 words).

### 1.3 Typical paragraph shape (data)

In narration paragraphs of 4 or more sentences (n = 424):

| Position | Mean words | Median |
|---|---|---|
| first sentence | **12.1** | 11 |
| middle sentences | 14.4 | 14 |
| last sentence | **16.9** | 16 |

- Only 33% of these paragraphs end on a sentence shorter than the average of the sentences before it.
- Where the ≤6-word sentences fall: 93 open a paragraph, 158 sit mid-paragraph, and only 12 close one.
- Of the 131 long paragraphs (≥120 words), only 19 (15%) are followed by a short paragraph of ≤30 words.

**The author's cadence is therefore "short statement, then accumulation, then a long cumulative close".** It is not the "long description, then punch line" cadence that genre editors often impose. Typical examples:

- (ch 9) opens "Benedikt was flabbergasted." (3 words). It closes "With every passing moment, his fear of becoming a sheer mockery amongst his peers was taking a more formative shape." (20 words).
- (ch 34) opens "He was perplexed." (3 words), followed by "He couldn't afford to ruin the last three years of his sedulous plan." It closes "With no better alternative, he went after Benedikt, despaired and angered."
- (ch 79) opens "Sanchez was overwhelmed. Her emotions had no boundaries." It closes "She held on her emotions with absolute resolute and succeeded from not breaking down."
- (ch 40) and (ch 40) run 150–274 words of physical action, ending on a long reflective sentence ("He wasn't concerned, for he wanted the girl and she was in an arm's length distance from him sitting in a pool of blood.").

The punch comes at the start of the paragraph, or in a separate one-line paragraph, or as a closing chapter line ("Change for the worse." (ch 1)). It does not come as the last sentence of a long paragraph.

### 1.4 Macro-cadence within a chapter

A typical chapter has four movements:

1. Dateline.
2. A long atmospheric or recap paragraph: "The village church bell rang with a loud peal ruffling the quietness of the morning…" (ch 31); "It was pouring in Gydnia…" (ch 72).
3. Alternating medium narration paragraphs and brisk dialogue exchanges (dialogue paragraphs have a median of 33 words).
4. A closing paragraph that summarises and looks forward, e.g. "He knew his hope was pretentious, the best he could do …" (ch 40); "It was going to be a long night and she hoped for a better tomorrow." (ch 79).

---

## 2. Sentence openers

Narration sentences starting with a capital letter and at least 3 words long (n = 4,841):

| Opener | n | % | Notes / examples |
|---|---|---|---|
| Pronoun subject (He/She/They/His/Her…) | 1,705 | 35.2 | "She mustered some courage and approached the receptionist." (ch 12) |
| Noun-phrase subject (The/A/This…) | 871 | 18.0 | "The alarm clock ruffled the quietness …" (ch 10) |
| Name subject | 683 | 14.1 | "Benedikt was flabbergasted." (ch 9) |
| **Subject-first total** | **≈3,350** | **≈70%** | (plus some names and odd cases in "other") |
| It was / There was | 319 | 6.6 | "It was a beautiful Friday morning." (ch 12); "There was something in the air, an uncalled freshness …" (ch 12) |
| Other prepositional (In/On/For/Besides/Despite/Without…) | 257 | 5.3 | "Besides the moving traffic …, there was nothing …" (ch 8); "Besides" opens 33 sentences |
| After / Before | 132 | 2.7 | "Before X could Y" alone accounts for 25 (§3, T4) |
| And / But / So | 128 | 2.6 | "And then the car made a sharp turn …" (ch 8); "And then she was on the page …" (ch 12) |
| **With …** | 82 | 1.7 | "With dwindled hope and pleading eyes, she kept looking at him." (ch 15) |
| Adverb / transition (Soon, Then, Meanwhile…) | 71 | 1.5 | "Soon" opens 34 sentences, e.g. "Soon they were on their way." (ch 35) |
| **As …** | 66 | 1.4 | "As she slid down the pipe a loud screaming voice got her attention." (ch 36) |
| **Participial -ing opener** | ≈43 | ≈0.9 | "Realizing his ruse worked, a sign of relief graced his visage." (ch 8); "Taking that pretext, Sanchez excused herself …" (ch 71) (33 with a comma, 10 without) |
| Past participle / adjective / "Once convinced" | ≈54 | ≈1.1 | "Satisfied with his perusal he sprinted back …" (ch 8); "Despondent, she casually sauntered …" (ch 13); "Once convinced, she paced out …" (ch 74); "Perplexed, she pulled …" (ch 15) |
| Though / Although | 56 | 1.2 | "Though" 51 vs "Although" 4. **The author says "Though".** |
| While | 41 | 0.8 | "While she slept like a log, he struggled …" (ch 10) |
| Other subordinate (When/Once/If/Since) | 51 | 1.1 | |
| Narration questions | 15 | 0.3 | Free indirect thought, always in clusters of two: "Could this be a miscreant of Benedikt's horde? Or was it someone that she wasn't aware of?" (ch 8); also (ch 15), (ch 23) |

What the openers show:

- The subject-first chain dominates. Runs of "He … He … He" or "She … She …" are common: 281 adjacent same-opener pairs in pure narration (He 121, The 85, She 69). Seven paragraphs have runs of 4–5, e.g. (ch 9) and (ch 30).
- Front-loaded modifier openers (With, As, participial, Once convinced, Though, Before X could) together make up about 8% of sentences, roughly one every 12 sentences. They are the author's main device for varying the rhythm.
- **Dangling participles** occur in this opener slot. They are errors to fix, but keep the opener:
  - (ch 8) "Realizing his ruse worked, a sign of relief graced his visage."
  - (ch 8) "Driving alone, … his mind apprehended the mountainous task."
  - (ch 44) "Seeing her quivering with pain, the practicality of the situation sank in him."
  - (ch 8) "After taking few arbitrary turns it was evident …"

---

## 3. The author's characteristic sentence templates

These are the moulds the author reaches for. Edited or rebuilt sentences should be poured into them.

| # | Template | Frequency | Real examples |
|---|---|---|---|
| **T1** | **Verdict opener:** [Name/He/She] + *was* + [strong emotion adjective]. Then elaboration. | 43 standalone "X was ADJ." sentences, mostly paragraph-initial | "Benedikt was flabbergasted." (ch 9); "Sanchez was overwhelmed." (ch 79); "He was perplexed." (ch 34); "Marty was petrified." (ch 40); "She was thrilled." (ch 74); "Maxwell was flabbergasted." (ch 83) |
| **T2** | **Beat-then-speech:** [S] + [action] + *and with a* [adj] *tone/voice* + [continued/blurted/stated], "…" | "with a … tone/voice" ≈74–85; comma-intro before the quote 158 vs 12 without | "The man mustered some courage and with a trembling voice continued, "Chief we have the girl …"" (ch 37); "With a sotto voice, she enquired if she could meet John Patterson." (ch 12); "Benedikt finally broke the monotony and with an exhausted tone he exclaimed, "Why can't you trust me?"" (ch 76) |
| **T3** | **Interrupted continuous:** [S] *was* [V-ing] … *when* [event] / *It was* [time] *when* … | ≈22 + 9 | "She was giving herself a good look in the mirror when Stephen announced that the breakfast was ready." (ch 10); "His mind was battling hard to find the right syllables when his phone created a sudden dissonance." (ch 84); "She was in trance, floating in her own world when the signage on a passing building almost made her jump from her seat." (ch 12) |
| **T4** | **Pre-emption:** *Before* [X] *could* [react/comprehend], [Y] … | 25 | "Before he could react, she gave an elbow jab under his chin, and he collapsed to the ground unconscious." (ch 36); "Before he could comprehend what struck him, he saw Sanchez collapsing in a pool of blood." (ch 39); "Before Stephen could speak, the sound of loading guns took over …" (ch 83) |
| **T5** | **Concessive frame:** *Though/Despite/No matter how* [clause], [clause]. | Though 51, Despite 18, No matter 13 | "Though the Peugeot was dissolving at times on the busy streets of Zurich, it kept resurfacing back, confirming their apprehensions of being trailed." (ch 8); "No matter how much he tried, he couldn't keep his agitation curbed." (ch 9) |
| **T6** | **Attendant "With" opener:** *With* [adj] [noun](, ) [S] [V]. | 82 | "With dwindled hope and pleading eyes, she kept looking at him." (ch 15); "With no better alternative, he went after Benedikt, despaired and angered." (ch 34); "With extreme caution, she opened the global address list …" (ch 14) |
| **T7** | **Participial tail:** [main clause], [V-ing …]. The cumulative close. | ≥137 sentence-final; most common in paragraph-final sentences | "…, it kept resurfacing back, confirming their apprehensions of being trailed." (ch 8); "With no verbal exchange, the place morphed to a ghostly eerier, making Damian visibly uncomfortable." (ch 9); "She looked around and was relieved …" |
| **T8** | **Causal "for":** [clause], *for* [he/she] [knew/was] … | ≈30 | "She paced out of the room as fast as she could, for she didn't want to show her gullible side." (ch 66); "…too powerful to chase them in such discreet manner" (ch 8); "He wasn't concerned, for he wanted the girl …" (ch 40) |
| **T9** | **Brisk transition:** *Soon* [they] *were* … / *And soon* … / *And then* … | Soon 34, And then/soon ≈23 | "Soon they were back inside the warehouse." (ch 74); "and soon they were on their way to Adriana's house." (ch 33); "And then a thought crossed her mind." (ch 83) |
| **T10** | **Paired-adjective coda:** …, [adj] *and* [adj]. (sometimes doubled) | ≈11 exact, many variants | "Sanchez looked at him with blurry eyes, agape and lost." (ch 10); "He appeared like a dethroned king, lost and dismayed, aloof and confused." (ch 76); "She left the warehouse, saddened and anxious." (ch 73); "He was worried, perspired and perplexed." (ch 83) |
| **T11** | **Wistful exclamative:** *How she wished* … (sometimes *and how she desired* …) | 8 | "How she wished what she witnessed was nothing but a bad dream." (ch 76); "How she wished Stephen could read her mind, but …" (ch 37); "How she wished she never had to approach Benedikt for help, and how she desired some miracle to happen in her favor." (ch 74) |
| **T12** | **Verb chain:** [S] [V-ed] X, [V-ed] Y(,) and [V-ed] Z. | ≈38 three-verb chains | "She dropped her shoulders …, passed a frail smile to Stephen, and closed her eyes." (ch 8); "They thanked Jules, hugged him and decided to leave." (ch 31); "She did everything she could do …, walked around, played with her phone, scribbled on paper but nothing helped." (ch 78) |

Secondary moulds, each used often enough to count as a habit:

- *It (appeared/was) as if …*: 43 uses of "as if", e.g. "It appeared as if the house managed to abate a colossal tempest." (ch 39).
- *All [s]he could [V] was …*: 10.
- *Once convinced/satisfied, …*: 12.
- *There was X, a/an Y that …* (appositive restatement): "There was a newfound zeal, a whim that was irresistibly infectious." (ch 77).
- *…, to say the least*: 4.
- *[S] mustered some courage and …*: 8.

---

## 4. Punctuation habits

Per 1,000 words, over the 81.4k-word body:

| Mark | Count | Per 1k | Usage and verdict |
|---|---|---|---|
| Comma | 3,320 | 40.8 | 0.55 per sentence. In pure narration, 57% of sentences have **no** comma, 33% one, 8% two and 2% three or more. Light, clause-chaining with "and" ("and" occurs 1,955 times in narration, "but" 356). |
| Semicolon ; | 28 | 0.34 | Rare. **About half are misused**: in place of a comma ("The moment she disappeared behind the lancet; he scurried …" (ch 4); "several unanswered questions; many unresolved mysteries" (ch 11)) or in place of a colon or dash ("One thing she indisputably understood; TransPacific recognized talent" (ch 18); "something to cheer about; a purpose to chase" (ch 13)). The correct ones join two short related clauses: "The parking lot was quiet; given it was a weekend …" (ch 8); "The man was fast approaching; he shot another fire …" (ch 39). |
| Colon : | 3 in prose | ≈0.04 | Effectively none in narration. Used only in letter salutations and two Portuguese dialogue lines [ch 24]. |
| Spaced en dash " – " | 22 (+1 unspaced) | 0.28 | **The author's dash.** It is always **single**, placed at the end of a clause to amplify, explain, list or reveal. There are **no paired parenthetical dashes anywhere.** Examples: "That was an easy question for her – she had done an exhaustive research on TransPacific." (ch 13); "He tried the number again and nothing changed – no one answered the phone." (ch 34); "various instruments a professional cartographer uses – plotters, beams, large rulers …" (ch 31); "Let me ask you – why should I trust you?" (ch 76). |
| Spaced hyphen " - " | 7 | 0.09 | The same function as the en dash, typed as a hyphen: "One thing was evident - Benedikt had a soft corner for her." (ch 47); "the reason is - I love you." (ch 72); "and the pristine weather - all made the village appear …" (ch 33); list-summary use in (ch 1). |
| Em dash — | **0** | 0 | Never used. |
| **All dashes combined** | **≈30** | **≈0.37** | About one every 2,700 words, or one per three chapters. |
| Ellipsis ... / … | 8 + 5 = 13 | 0.16 | **Only in dialogue**, for trailing off *and* for interruption: "Please… you are my only hope." (ch 15); "Chief we were in a situation..." before he could finish (ch 37); "I... I told the Russians" (ch 76). Spacing is inconsistent ("I ….”" (ch 28); "believe...,”" (ch 9)). |
| Exclamation ! | 45 | 0.55 | Rare, but clustered at crisis moments. **12 instances of "!!"** across 10 paragraphs: "Thud!!" (ch 33); "They are here!!" (ch 34); "We saw them entering the house!!" (ch 35); "SANCHEZ!!" (ch 39); "Damn!! I was this close from nabbing her!!" (ch 21). Narration exclamations: "and there it was!" (ch 13); "There she was! Sacred." (ch 39). |
| Question ? | 316 | 3.9 | Mostly dialogue. Frequent **question marks on statements**: "…if you see anything unusual call me?" (ch 34); "Tell me more about yourself?" (ch 13); "We want to ensure you are safe?" (ch 83); "He was irritated for sure, but was unable to discern the reason behind it?" (ch 23). |
| Double quotes | curly " 661 / " 636; **straight " 285** | | Mixed within paragraphs (e.g. (ch 8) opens with " and closes with "). Mechanical normalisation needed. |
| Apostrophes | curly ' 683; straight ' 154 | | Mixed. Normalise. |
| Single quotes ' ' | 9 | | Only in the diary section ch 50, closing each entry ("…see it for yourself'."). |
| Parentheses | 14 | 0.17 | Only for English glosses of Portuguese dialogue: "("Did you sleep well?")" (ch 31). |
| Non-breaking spaces | 418 | | An artefact of the conversion from the source file (e.g. "After breakfast, the family" (ch 1)). The Markdown also shows double spaces after full stops. Clean them mechanically. |

### 4.1 Commas: the error patterns

1. **Missing comma after an introductory clause or phrase.** This is the most frequent punctuation error. By opener word (no comma anywhere in the sentence / total): *As* 19/66, *Once* 10/30, *After* 15/99, *While* 8/41, *Though* 6/51. The heuristic count of intro clauses with no comma before the main-clause subject is ≈82 (about 2/3 true on a hand check). **Estimate: 60–80 instances.** Examples:
   - "As she slid down the pipe a loud screaming voice got her attention." (ch 36)
   - "Once convinced she emailed it …" (ch 13)
   - "As he moved forward the car zoomed away leaving Sanchez behind." (ch 40)
   - "After taking few arbitrary turns it was evident …" (ch 8)
   - "If this was Benedikt's creation it was beyond her comprehension" (ch 8)

   The author is **inconsistent** here: the same openers usually do take a comma ("Though…," 45/51; "After…," 84/99). So these are errors, not a stylistic principle.
2. **Missing comma before a vocative in speech**: "Mr. Patterson let me straightway come to the point." (ch 15); "Listen I am calling you because I trust you." (ch 9); "Maxwell our goals have not changed" (ch 53).
3. **Comma splices.** The heuristic flagged 58 candidates, about 30% true on a hand check, and many further splices go unflagged. **Estimate: 40–70.** Examples:
   - "He had a six of clubs, eight of diamonds and nine of hearts, it was straight!" (ch 2)
   - "He was delirious, he screamed with frustration and tears rolled down his eyes." (ch 39)
   - "Francis was clueless, he was frustrated, but all he could manage was a nod" (ch 38)
   - "…a sense of bereavement that bothered him, it was as if he had lost a loved one." (ch 9)
   - "The first John was a vice president of international operations, she ruled him out" (ch 14)
   - "Soon it was evening, she had planned beforehand to stay back late." (ch 15)
   - "The place was bigger than life, it had a gigantic water fountain …, she could see …" (ch 12)
4. **Spurious comma**: after a coordinator ("But, with the job she had found a purpose" (ch 15); "But, that was the prime intent" (ch 13)), and between subject and verb in a few places.
5. **Commas the author deliberately omits** after very short time or sequence openers: "Soon they were…" (24/34 with no comma), "By now Sanchez was captivated" (9/10), "In twenty minutes, he was all done" (mixed). **This is voice and consistent with standard style. Leave it.**

### 4.2 Dialogue punctuation

- **Structure.** 429 of the 743 dialogue paragraphs open with **narration first** (beat or tag, then the speech); 314 open with the quote. Of the quote-first paragraphs, 208 have a trailing beat or tag and 94 are bare speech.
- **Speech verbs** (counted over the whole text): *continued* 95 (including "continued further" 18), *blurted* 56, *spoke* 47, *announced* 41, *stated* 39, *responded* 33, *told* 30, *enquired* 24, *said* 21, *mentioned* 19, *asked* 18, *screamed* 16, *declared* 15, *mumbled* 13, *snapped* 10, *queried* 10. "said" is rare. The author's dialogue grammar is beat plus a "manner" verb.
- **Errors, with counts:**

  | Pattern | Count |
  |---|---|
  | comma outside the closing quote: "…", she … | 38 (vs 21 correct ,") |
  | **no punctuation** before the closing quote, then a tag or beat: "We have a lot to do" Sanchez announced (ch 31) | ≈66 |
  | full stop then lowercase tag: ".” she knew …" (ch 74), "…few minutes back." the officer mentioned (ch 34) | 11 |
  | capitalised pronoun after a comma or question: ", The tone though gentle …" (ch 76); ", She blurted" (ch 72); "?” He" when it is a tag | ≈10+ |
  | misplaced opening quote: ",” The evidences …" (ch 75); "continued,” I have a fair idea" (ch 77) | handful |
  | missing opening quote | (ch 33) |
  | missing closing quote | (ch 76) "What was your guilt? Sanchez snapped." |
  | tag glued into the quote | "…Let me get a taxi”. and soon they were …" (ch 33) |

- **Speech introduced by a verb**: comma before the quote 158 times, no comma 12 times, colon 2 times. The comma is the author's convention; keep it.

---

## 5. Fragments, repetition, lists

### 5.1 Fragments (≈12–15 in the whole book, about 1 per 6,000 words)

The author uses fragments sparingly and in three functions:

- **Dramatic chapter or paragraph sting**: "Change for the worse." (ch 1), which ends Chapter 1; "There she was! Sacred. Sitting in the corner, hiding behind the sofa." (ch 39) ("Sacred" is a typo for "Scared").
- **Inventory lists**: "The known faces, the rumpus town, the choir group." (ch 11); "Scattered papers, unkempt piles of books, dust-ridden computer and tons of cartographic instruments." (ch 39); "Brewing black coffee with select beans crushed at home, scrambled eggs, peanut butter sandwiches, and freshly squeezed orange juice." (ch 1); "Bright sun, resting family, and the dewiness in the air, a perfect Sunday as he wanted it to be." (ch 1); "A dress pants she got for her concert…" (ch 13).
- **Appositive afterthoughts**: "He ogled her for few seconds. Long enough to arouse her." (ch 3); "A ray of hope, distinct and clear in the midst of all the madness." (ch 49); "Sometimes by error, but mostly because of her emotional worn out state." (ch 71); "A blend of innumerable voices all trying hard to explain something with urgency." (ch 67).

**Verdict: voice. Keep them all** (fix only the typos and articles inside them). **Do not add more.** Keep to no more than about one per chapter.

### 5.2 Repetition for effect (voice; keep)

- Incremental action repetition: "He called the number… He tried the number again and nothing changed… He tried the number again. This time the phone line was cut… He tried the number again and this time he got directly to the voicemail." (ch 34)
- Anaphora in pairs: "No one can corrupt it. No one can do anything about it" (ch 9); "Too many affluent people were involved and too much was at stake." (ch 9); "everything appeared new, everything was poignantly altered." (ch 11); "I respected you, I admired you" (ch 76).
- "no X, no Y" series (6): "There was no fear, no apprehension …" (ch 40); "There were no greetings, no introductions" (ch 48); "no baggage, no commitment to honor and no strings" (ch 72).
- Anaphoric tricolon: "She cried, she laughed, and she screamed." (ch 13).
- The doubled intensifier "too X too Y" (3): "Her mission got curtailed too fast too soon." (ch 36); "Everything was happening too fast too quick." (ch 83); "It was happening too fast too soon." (ch 59). The doubling is voice. The missing comma and "too quick" are errors.
- Doubled paired adjectives: "lost and dismayed, aloof and confused" (ch 76).

**Unintentional repetition** is a different matter. Examples are "perturbation(s)" twice in ch 8, and "disheveled" three times in ch 15. That is lexical, not rhythmic; leave it to the diction report.

### 5.3 Lists and tricolons

- Tricolons and longer lists are frequent: ≈45 "A, B and C" patterns in narration, plus many four- to seven-item catalogues. Examples: (ch 13) (a 7-item company summary after a dash); (ch 12); (ch 54) "spiraling apprehensions, surging hopes, and fretful uncertainties".
- The serial comma is **inconsistent**: ≈26 with the Oxford comma vs ≈55 without. This is a house-style decision (see §7).
- Rising triads of emotion nouns in speech tags: "there was anxiety, fear and a blend of hope in those words." (ch 75); "There were anticipation, curiosity, and love in his blue eyes." (ch 72).

---

## 6. Tense and aspect

| Feature | Count | Rate | Verdict |
|---|---|---|---|
| Past progressive *was/were + V-ing* (narration) | 545 | **8.0 per 1k narration words** | Mostly **voice**. It is heavy by the norms of modern thrillers, but it is a defining texture. Top verbs: looking 25, making 18, waiting 18, standing 14, running 14, getting 13, wearing 13, expecting 10. |
| *kept + V-ing* | 36 | | Voice ("She kept tossing and turning for hours" (ch 71)) |
| *started + V-ing* | 31 | | Voice, but trim stacks |
| *would* (narration) | 146 | | Habitual (voice: "He would cook the specials." (ch 1)), future-in-past, conditional |
| *would have / could have* | 20 / 15 | | Voice ("On a regular day, Stephen would have extended his sleep …" (ch 10)) |
| *had* (all uses) | 572 | | Past perfect is **under-used** at flashback entries (see below) |
| **Present-tense slips** in narration | ≈15–20 | | **Error** (sequence of tenses) |

**Where the progressive is voice:**

- Scene-setting and ambient states: "The streetlights … were making way to the early morning sunshine" [ch 1, the book's first line]; "The morning shimmering hue found its way …" (ch 71).
- The interrupted-continuous template (T3).
- Inner states: "His mind was spinning." (ch 9); "Her senses were working on steroids" (ch 37).

**Where it is an error or weakness:** the progressive is used for completed or punctual actions, or stacked three or more deep in one paragraph. Examples:

- "Sanchez was warily observing everything that was happening around her." (ch 8)
- "Stephen was trying hard to comprehend where she went wrong" alongside "Though the Peugeot was dissolving at times …" ch 8
- "Maxwell was flabbergasted… As he was contemplating…" (ch 83)
- "She was intercepting his moves" (ch 9)
- "The conversation was progressing as she anticipated." (ch 15)

**Present-tense slips and failed backshift** occur almost always in an *if / once / until / so that* clause after a past-tense verb:

- "He knew once he leaves the city it would take …" (ch 8)
- "He knew once he is in Russia Maxwell could do no harm." (ch 83)
- "He also threatened her for consequences if she comes after him." (ch 15)
- "He tilted his head so that he can be close to her ears" (ch 78)
- "until she finds the answers" (ch 49)
- "to ensure he gets Benedikt this time" (ch 81)
- "before anyone notices her fidgety being" (ch 14)
- "how much she misses him" (ch 79)
- the habitual "He puts the spread on the table" (ch 1)

**Missing past perfect at flashback entries:**

- "She replayed in her mind everything that happened during her final dash from the hotel." (ch 8)
- "everything that happened since Sanchez's arrival" (ch 8)
- "where she went wrong" (ch 8)
- "the passionate indulgence they had" (ch 9)

**Conditional *would have* for *had***: "If we would have killed him at that time" (ch 84) is in Benedikt's speech. Fix it in narration; in dialogue, fix it unless the editor deliberately wants a non-native tic for that character. It is not established as one.

---

## 7. Voice (keep) vs error (fix)

| Keep: VOICE | Fix: ERROR |
|---|---|
| Medium, even sentence stride (mean ≈14, most 9–18 words) | Run-on and comma-spliced "sentences" over 30 words ((ch 12), (ch 47); in speech (ch 53)) |
| Paragraph shape: short verdict opener, then a longer cumulative close | Dangling participle or "After…" openers ((ch 8), (ch 8), (ch 44), (ch 8)) |
| The T1–T12 templates, including "Before X could…", "With …,", "How she wished…", "…, for she knew…", "Soon they were…" | Missing comma after long introductory clauses (60–80) |
| Beat-before-speech dialogue with a comma before the quote | Punctuation of dialogue tags (comma outside the quote, no comma before the tag, capitalised tag, broken quotes) |
| Rare single amplifying dash at the end of a clause | Spaced hyphen " - " used as a dash (7); mixed dash glyphs |
| Rare, clustered exclamation at crisis points | "!!" (12); question marks on statements |
| Ellipsis for faltering speech | Ellipsis spacing ("I ….", "believe...,") |
| Few semicolons, joining short clauses | Semicolons standing in for a comma or colon (≈12–14 of the 28) |
| Past progressive for atmosphere and interrupted action | Progressive for punctual or completed acts; stacks of 3 or more per paragraph |
| Habitual "would", counterfactual "would have" | Present-tense slips in subordinate clauses; missing past perfect at flashback entry |
| Formal dialogue ("I am", "Let us"; no "I'm"/"Let's") | — |
| Sparse fragments; anaphora; "no X, no Y"; tricolons; paired-adjective codas | Unpunctuated doubling ("too fast too quick"); comma after "But,"; missing vocative commas |
| Free-indirect question pairs (rare) | — |
| Mixed straight and curly quotes, non-breaking spaces | Mechanical: normalise all of them |

---

## 8. RULES FOR THE EDITOR: keeping the author's rhythm

### A. Sentence length and structure

1. **Target narration mean 13–16 words per sentence** after editing (currently 14.4; median 14). Dialogue should stay at about 7–10 (currently 8.5).
2. **Keep at least 25% of narration sentences at 10 words or fewer, and at most 5% over 25 words.** Do not write sentences over 30 words (currently 1.2% of sentences). Treat any existing sentence over 30 words as a candidate to split.
3. **Split run-ons with a full stop, not with a semicolon or dash.** Each resulting piece should land in the 8–20-word band. For (ch 12):
   - Before: "The place was bigger than life, it had a gigantic water fountain …"
   - After: "The place was bigger than life. It had a gigantic water fountain positioned in the center, rising to an almost 100-foot ceiling. An array of modern paintings graciously covered the walls. At a distance she could see an elevator guarded by biometric access, and an elegantly designed reception desk armed with gorgeous damsels."
4. **Fix comma splices in the author's own ways**, in this order of preference: (a) a full stop; (b) ", and"; (c) a subordinator the author already likes (as, for, though, while). Examples:
   - "He was delirious, he screamed with frustration and tears rolled down his eyes." becomes "He was delirious. He screamed with frustration, and tears rolled down his eyes."
   - "…bothered him, it was as if he had lost a loved one." becomes "…bothered him, as if he had lost a loved one."

   **Do not use semicolons to fix splices.**
5. **Do not convert coordination into heavy subordination.** The author chains with "and" and trailing participles; "which/who" relatives are relatively rare (84 and 51). Avoid "which meant that …", "whereupon", nested relatives, and absolute constructions the author never uses.
6. **Keep subject-first as the norm (about 70%).** When breaking up monotonous He/She runs of 4 or more, use the author's own openers (With …, As …, Before X could …, Once convinced, …, Though …, Soon …). Do not use openers the author never uses: inverted "Gone was …", "Only then did …", cleft sentences, or "Having done X, …" stacks. The participial opener (about 1 in 100 sentences) must not become more frequent than it is now; leave it at about 1 per 2,000 words.
7. **Repair dangling openers by changing the main-clause subject, not by deleting the opener.** "Realizing his ruse worked, a sign of relief graced his visage." becomes "Realizing his ruse had worked, he felt a sign of relief grace his visage." (or keep the author's image: "…, he let a sign of relief grace his visage").

### B. Paragraph cadence

8. **Keep the "short verdict, then build, then long cumulative close" shape.** **Do not add one-line punch sentences at the end of long paragraphs.** The author does this in fewer than 3% of paragraphs (12 of about 420), and it is the fastest way to make the prose sound "edited". Emphasis goes at the **start** of the paragraph (T1), in a **standalone one-line paragraph**, or at the **chapter end**.
9. **Preserve paragraphing.** Narration paragraphs have a median of about 60 words and a p90 of about 140. Split only paragraphs over about 250 words ((ch 30) at 417, (ch 3) at 298, (ch 40) at 274), and split them at a natural beat. Do not merge dialogue paragraphs.
10. **Keep the long atmospheric first paragraph of each chapter.** Trim words inside it if needed, but not its position or function.

### C. Punctuation norms (house-style normalisation at matching frequency)

11. **Dashes.** The author's dash is a **single, spaced, sentence-final amplifier**. Never introduce **paired, parenthetical dashes**: there are none in the book.
    - **Recommendation:** the spelling is American (color, realized, center, favorite; no -our or -ise forms). For a US agent or publisher (Penguin Random House US / Chicago), normalise all 23 en dashes and 7 spaced hyphens to the **closed em dash** ("…for her—she had done an exhaustive research…"). If the target is Penguin UK, use the **spaced en dash** " – " instead; that is what the author already types 22 times, so it is a near-zero change. **Pick one and apply it globally.** Either way, convert every " - " used as a dash to that form ((ch 1), (ch 2), (ch 33), (ch 47), (ch 53), (ch 72); ch 24 is a Portuguese gloss).
    - **Frequency cap:** keep the book-wide total at about 25–40 dashes (≈0.3–0.5 per 1,000 words; currently ≈30), and no more than one per paragraph. Do **not** replace commas, colons or semicolons with dashes unless the author's own sentence has the "X – explanation" shape.
    - Where a misused semicolon or colon introduces an explanation, use the dash. "One thing she indisputably understood; TransPacific recognized talent" (ch 18) becomes "One thing she indisputably understood—TransPacific recognized talent", matching the author's own "One thing was evident - Benedikt had a soft corner for her." (ch 47).
12. **Semicolons: do not add any.** Fix the misused ones (to a comma, a full stop or a dash). The book should end up with the same or fewer: at most 28, probably about 15.
13. **Colons: do not introduce colons in narration.** The author has none. Use a dash or a full stop instead. Colons stay only in letter formats and for the two Portuguese lines if house style requires them.
14. **Exclamation marks:** reduce every "!!" to "!" (12 cases). Keep the single "!" where the author placed it (about 45). Do not add new ones in narration.
15. **Question marks:** remove them from declaratives and indirect questions ("call me?" (ch 34); "Tell me more about yourself?" (ch 13), which becomes a full stop or "Tell me more about yourself."; (ch 23); (ch 69); (ch 60)). Keep them on genuine rhetorical question pairs in free indirect thought.
16. **Ellipses:** normalise to one house form (the single character "…" or spaced ". . ." per the publisher), with no stray spaces. Keep the author's use for faltering speech ((ch 15), (ch 15), (ch 41), (ch 75), (ch 76)). For speech **cut off by another person** ((ch 37), (ch 37), (ch 21)), US house style expects an em dash ("Chief, we were in a situation—"). This is optional; the ellipsis is acceptable. Do not add new ellipses.
17. **Quotes and apostrophes:** convert all straight marks to curly. Use double quotes for dialogue and letters, and single quotes only for quotes nested inside quotes. Remove the stray closing single quotes in the diary entries ((ch 50), (ch 50)) or apply them consistently. Remove non-breaking spaces and double spaces.
18. **Commas:**
    - Add the missing comma after an introductory clause of 5 or more words, or any clause with its own subject and verb ("As she slid down the pipe, a loud …").
    - Leave short openers bare where the author does ("Soon they were…", "By now Sanchez was…").
    - Add vocative commas ("Mr. Patterson, let me…").
    - Remove the comma after sentence-initial "But,".
    - **Do not add commas around restrictive elements or other fussy commas.** Keep the light-comma texture: roughly 57% of narration sentences have no comma, and that should still be true after the edit.
19. **Serial comma:** follow house style. For US Chicago that means adding the Oxford comma (currently about 26 with vs 55 without). It barely affects rhythm, so apply it consistently.

### D. Dialogue architecture

20. **Keep beat-before-speech** ("X did Y and, with a trembling voice, continued, "…"") as the dominant pattern. There are 429 narration-first dialogue paragraphs vs 314 quote-first. Do not flip beats to after-quote "she said" tags wholesale. Trimming the "with a … tone" formula is a diction question (about 80 uses); if you trim it, replace it with an action beat, not with "said + adverb".
21. **Tag punctuation:**
    - Put the comma inside: "…," she said.
    - Tags after a closing quote are lowercase: "…?" he asked.
    - Action beats get a full stop and a capital: "…." He rubbed his hands…
    - Fix broken or missing quote marks.
22. **Keep speech formal and uncontracted** ("I am", "Let us", "It is"). Do not add "I'm", "let's" or "gonna"-style contractions. The negative contractions the author uses (didn't, can't) can stay.
23. Keep dialogue sentences short. When correcting grammar in speech, do not lengthen it: the median is 7 words.

### E. Tense and aspect

24. **Reduce, do not eliminate, the past progressive.** Convert it to the simple past where the action is punctual or completed, or where there are three or more progressives in one paragraph. Keep it in scene-setting, inner states, and the T3 template. **Target: about 5.5–6.5 per 1,000 narration words** (from 8.0), roughly a 20–30% reduction, concentrated in action scenes.
25. **Fix every present-tense slip in narration** (backshift after a past-tense verb: *leaves → left, is → was, comes → came, can → could, finds → found, misses → missed, notices → noticed, puts → put/would put*).
26. **Add the past perfect only at the entry point of a flashback or earlier action** ("everything that had happened during her final dash…"), then let the passage return to the simple past. Do not pile up "had had" constructions.
27. Keep habitual *would* and counterfactual *would have / could have*. Fix "If we would have…" to "If we had…".

### F. Devices

28. **Fragments:** keep the existing 12–15. Add none. The exception is where a split run-on naturally leaves an inventory list, which is in keeping with (ch 11) and (ch 39).
29. **Keep the doubling devices** ("too fast, too soon"; "lost and dismayed, aloof and confused"; "no X, no Y"; incremental repetition as in (ch 34)). Add the missing comma inside them, and change "too quick" to "too soon" so the formula matches its other two uses.
30. **Tricolons and verb chains (T12)** are native to the voice, so use them when rebuilding sentences. Do not invent balanced antitheses ("not X, but Y"), chiasmus, or aphoristic one-liners. These are absent from the author's toolkit and read as a different writer.

### Quick checklist per edited passage

- [ ] Narration mean is still about 14 words, with no new sentence over 30 words.
- [ ] No new semicolons, colons, paired dashes or ellipses.
- [ ] Dash count per chapter is 0–1, in one glyph only.
- [ ] No short stinger added at the end of a paragraph.
- [ ] Openers come from the author's inventory (subject, With, As, Before X could, Though, Soon, Once convinced).
- [ ] Dialogue: beat before speech, comma before the opening quote, comma inside the closing quote, "I am" and "Let us" kept.
- [ ] Past progressive trimmed only where it marks a punctual action, and no present tense left in narration.
