# Humanize: pattern catalog

Read [SKILL.md](SKILL.md) for the editing process, style defaults and false positives.

Sections 1-35 are adapted from [blader/humanizer](https://github.com/blader/humanizer) v2.11.2 (MIT, see [LICENSE-humanizer](LICENSE-humanizer)). The upstream skill draws on Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). Sections 36-46 add patterns from draft review and writing by Nester and Zolochevskii on AI writing patterns. Sections 18, 31 and 46 also draw on later versions of blader/humanizer.

Each pattern explains what to watch for and why. Examples use fictional situations. Unicode escape sequences represent punctuation or symbols in the examples.

---

## Content patterns

### 1. Inflated claims about importance and legacy

**Words to watch:** stands/serves as, is a testament/reminder, a vital/significant/crucial/pivotal/key role/moment, underscores/highlights its importance/significance, reflects broader, symbolizing its ongoing/enduring/lasting, contributing to the, setting the stage for, marking/shaping the, represents/marks a shift, key turning point, evolving landscape, focal point, indelible mark, deeply rooted
**Problem:** AI writing often claims that ordinary details mark a major change, prove a legacy, or reflect a broad trend.
**Before:**
> The town opened its first public reading room in 1989, marking a pivotal moment in the region's cultural evolution. The reading room occupied two rooms in the old town hall.
**After:**
> The town opened its first public reading room in 1989. It occupied two rooms in the old town hall.

### 2. Name-dropping to prove importance

**Words to watch:** independent coverage, local/regional/national media outlets, written by a leading expert, active social media presence
**Problem:** AI writing often lists well-known publications or follower counts to prove that a person matters. The list usually gives no useful context.
**Before:**
> She has been featured in newspapers, on radio shows and in widely read newsletters, cementing her status as a leading voice. Her research focuses on how renters find affordable housing.
**After:**
> She studies how renters find affordable housing.

If the source explains what the person said and where, keep that useful citation. Do not invent context for a shorter version.

### 3. Shallow analysis with -ing phrases

**Words to watch:** highlighting/underscoring/emphasizing..., ensuring..., reflecting/symbolizing..., contributing to..., cultivating/fostering..., encompassing..., showcasing...
**Problem:** AI writing often adds an -ing phrase to make a simple fact sound deeper than it is.
**Before:**
> The library painted the stairwell green to match its original tiles, reflecting the community's deep connection to its heritage.
**After:**
> The library painted the stairwell green to match its original tiles.

### 4. Sales language

**Words to watch:** boasts a, vibrant, rich (figurative), profound, enhancing its, showcasing, exemplifies, commitment to, natural beauty, nestled, in the heart of, groundbreaking (figurative), renowned, breathtaking, must-visit, stunning
**Problem:** AI writing often sounds like an advertisement, especially when it describes places, culture, products, or organizations.
**Before:**
> Nestled in breathtaking scenery, the town overlooks a lake and holds a weekly market, offering an unforgettable experience for all who visit.
**After:**
> The town overlooks a lake and holds a weekly market.

### 5. Vague sources

**Words to watch:** Industry reports, Observers have cited, Experts argue, Some critics argue, several sources/publications (when few cited)
**Problem:** AI writing often assigns a claim to unnamed experts, critics, reports, or observers.
**Before:**
> The river floods the meadow each spring. Experts believe it plays a crucial role in the regional ecosystem.
**After:**
> The river floods the meadow each spring.

Name a real source when the source text provides one. Otherwise, remove the unsupported claim. Never invent a source.

### 6. Formulaic challenges and outlook sections

**Words to watch:** Despite its... faces several challenges..., Despite these challenges, Challenges and Legacy, Future Outlook
**Problem:** AI articles often add a stock section about challenges, future prospects, or continued growth. These sections usually repeat vague claims instead of adding facts.
**Before:**
> The district's population has grown. Despite these promising developments, it faces the familiar challenges of urban life, including traffic congestion and water shortages. With a strategic location and ongoing initiatives, it continues to thrive.
**After:**
> The district's population has grown. It has traffic congestion and water shortages.

Add details such as dates or public actions only when they come from the source or the user.

## Language and grammar patterns

### 7. Overused AI words

**High-frequency AI words:** Actually, additionally, align with, crucial, delve, emphasizing, enduring, enhance, fostering, garner, gate/gated/gating (figurative; preserve established technical usage), highlight (verb), interplay, intricate/intricacies, key (adjective), landscape (abstract noun), pivotal, quietly, showcase, tapestry (abstract noun), testament, underscore (verb), valuable, vibrant
**Problem:** AI writing uses these words much more often than most people do, especially in groups.
**Before:**
> Additionally, the menu showcases dumplings filled with mushrooms. A testament to the bakery's commitment to seasonal ingredients is the apple pie, which is available only in autumn.
**After:**
> The menu includes mushroom dumplings. The bakery sells apple pie only in autumn.

### 8. Avoiding is and are

**Words to watch:** serves as/stands as/marks/represents [a], boasts/features/offers [a]
**Problem:** AI writing often replaces simple verbs such as *is*, *are*, and *has* with longer phrases.
**Before:**
> The gallery serves as an exhibition space for contemporary art. It features four rooms and boasts over 3,000 square feet.
**After:**
> The gallery exhibits contemporary art. It has four rooms and more than 3,000 square feet of space.

### 9. Not X but Y and clipped negative endings
**Problem:** AI writing overuses forms such as "Not only...but..." and "It's not just X, it's Y."

**House rule (stricter than upstream):** remove every "not X, but Y" / "не X, а Y" construction, including a single one, and every announcement of a conclusion ("here's why", "here's what this means", "и вот почему", "дело не в X"). State what the thing is. Details in §36.

It also adds clipped endings such as "no guessing" instead of writing a clear clause.
**Before:**
> It's not just about the beat riding under the vocals; it's part of the aggression and atmosphere. It's not merely a song, it's a statement.
**After:**
> The heavy beat adds to the aggressive tone.
**Before (tailing negation):**
> The options come from the selected item, no guessing.
**After:**
> The options come from the selected item without forcing the user to guess.

### 10. Forced groups of three
**Problem:** AI writing often forces ideas into groups of three to sound complete.
**Before:**
> The event features keynote sessions, panel discussions, and networking opportunities. Attendees can expect innovation, inspiration, and industry insights.
**After:**
> The event includes talks and panels. There's also time for informal networking between sessions.

### 11. Changing names and repeating sentence openings
**Problem:** AI writing handles repetition by rule instead of by ear. It may keep renaming the same person or thing. It may also start several sentences with the same subject, often *she* or *he*.

Use one clear name for the same subject. For repeated openings, merge sentences, change the subject when that helps, or begin with the action.
**Before (synonym cycling):**
> The protagonist faces many challenges. The main character must overcome obstacles. The central figure eventually triumphs. The hero returns home.
**After:**
> The protagonist faces many challenges but eventually triumphs and returns home.
**Before (repeated openings):**
> She noted the door. She noted the lock on it. She filed both away.
**After:**
> She noted the door and its lock, then filed both away.

Do not ban the repeated word. Fix the repeated sentence pattern. The remaining sentence may still start with "She."

### 12. False from X to Y ranges
**Problem:** AI writing often uses "from X to Y" when X and Y do not form a real range.
**Before:**
> Our journey through the universe has taken us from the singularity of the Big Bang to the grand cosmic web, from the birth and death of stars to the enigmatic dance of dark matter.
**After:**
> The book covers the Big Bang, star formation, and current theories about dark matter.

### 13. Passive voice and missing subjects
**Problem:** AI writing often hides who acts or drops the subject. Use active voice when it makes the actor and action clearer.
**Before:**
> No configuration file needed. The results are preserved automatically.
**After:**
> You do not need a configuration file. The system preserves the results automatically.

## Style patterns

### 14. Em and en dashes

**Default:** Replace em dashes (`\u2014`) and en dashes (`\u2013`) in rewritten prose. Use a period, comma, colon or parentheses. Keep hyphens in compounds and number ranges (11-19, 4-6 weeks). Check for spaced double hyphens used as dashes.
**Before:**
> The overnight bus\u2014which has run since May\u2014stops by the station\u2014even on holidays.
**After:**
> The overnight bus has run since May. It stops by the station even on holidays.
**Before:**
> The new policy \u2014 announced without warning \u2014 affects thousands of workers. The changes -- long overdue according to critics -- will take effect immediately.
**After:**
> The new policy, announced without warning, affects thousands of workers. The changes, long overdue according to critics, will take effect immediately.

Before returning the rewrite, check for both characters in editable prose.

### 15. Too much bold text
**Problem:** AI chatbots often bold words and phrases without a clear reason.
**Before:**
> It blends **OKRs (Objectives and Key Results)**, **KPIs (Key Performance Indicators)**, and visual strategy tools such as the **Business Model Canvas (BMC)** and **Balanced Scorecard (BSC)**.
**After:**
> It blends OKRs, KPIs, and visual strategy tools like the Business Model Canvas and Balanced Scorecard.

### 16. Lists with bold mini-headings
**Problem:** AI writing often uses vertical lists in which every item starts with a bold label and a colon.
**Before:**
> - **User Experience:** The user experience has been significantly improved with a new interface.
> - **Performance:** Performance has been enhanced through optimized algorithms.
> - **Security:** Security has been strengthened with end-to-end encryption.
**After:**
> The update improves the interface, speeds up load times through optimized algorithms, and adds end-to-end encryption.

### 17. Title case in headings
**Problem:** AI chatbots often capitalize every main word in a heading.
**Before:**
> ## Strategic Negotiations And Global Partnerships
**After:**
> ## Strategic negotiations and global partnerships

### 18. Emojis
**Problem:** AI chatbots often add emojis to headings and list items as decoration. The same goes for decorative arrows (→, ⇒, ➜) that stand in for a verb or a connector.

**House rule:** skip decorative emoji in rewritten prose. Same for decorative arrows: write "leads to" or split the sentence. Arrows inside code, commands and quoted text stay.
**Before:**
> \U0001F680 **Launch Phase:** The product launches in Q3
> \U0001F4A1 **Key Insight:** Users prefer simplicity
> \u2705 **Next Steps:** Schedule follow-up meeting
**After:**
> The product launches in Q3. User research showed a preference for simplicity. Next step: schedule a follow-up meeting.

### 19. Curly quotation marks
**Problem:** ChatGPT often uses curly quotes (“...”) where the writer or target format uses straight quotes ("...").
**Before:**
> He said “the project is on track” but others disagreed.
**After:**
> He said "the project is on track" but others disagreed.

## Chatbot patterns

### 20. Chatbot text left in the answer

**Words to watch:** I hope this helps, Of course!, Certainly!, You're absolutely right!, Would you like..., Want me to...?, Want me to give examples?, Should I continue?, let me know, here is a...
**Problem:** A chatbot's greeting, offer, or closing sometimes remains in text that should stand on its own.
**Before:**
> Sure, here's what I found. The shop opens at noon on Sundays. I hope that helps!
**After:**
> The shop opens at noon on Sundays.

### 21. Knowledge-limit disclaimers and guesses

**Words to watch:** as of [date], Up to my last training update, While specific details are limited/scarce..., based on available information, not publicly available, maintains a low profile, keeps personal details private, prefers to stay out of the spotlight, likely [grew up/studied/began], it is believed that
**Problem:** Older models may mention the date when their knowledge ends. A model may also explain that it could not find a source, then fill the gap with a plausible guess. State what the source does not show, or remove the sentence. Do not present a guess as a fact.
**Before (cutoff disclaimer):**
> While specific details about the company's founding are not extensively documented in readily available sources, it appears to have been established sometime in the 1990s.
**After:**
> The company's founding date is not documented in the available sources. (Or cut the sentence. State a date only if a source provides one.)
**Before (speculative gap-fill):**
> Information about her early life is not publicly available, suggesting she maintains a low profile and keeps personal details private. She likely grew up in a middle-class household, which shaped her later interest in education reform.
**After:**
> Her early life is not documented in the available sources. (Or omit the section.)

### 22. Overly agreeable tone
**Problem:** AI assistants often praise the user or agree before giving the answer.
**Before:**
> Great question! You're absolutely right that this is a complex topic. That's an excellent point about the economic factors.
**After:**
> The economic factors you mentioned are relevant here.

## Filler and hedging

### 23. Filler phrases

**Before → After:**
- "In order to achieve this goal" → "To achieve this"
- "Due to the fact that it was raining" → "Because it was raining"
- "At this point in time" → "Now"
- "In the event that you need help" → "If you need help"
- "The system has the ability to process" → "The system can process"
- "It is important to note that the data shows" → "The data shows"

### 24. Too many qualifiers

**Phrases to watch:** to be fair, it's also possible, could potentially, might arguably, in some cases it may, this is an inference
**Problem:** Repeated editing can add one qualifier after another until every claim sounds uncertain. Keep a qualifier only when the source supports it and the meaning needs it. Remove caveats that only repair an earlier overstatement.
**Before:**
> It could potentially possibly be argued that the policy might have some effect on outcomes.
**After:**
> The policy may affect outcomes.

### 25. Generic positive endings
**Problem:** AI writing often ends with vague optimism instead of the last useful fact.
**Before:**
> The future looks bright for the company. Exciting times lie ahead as they continue their journey toward excellence. This represents a major step in the right direction.
**After:**
> (Cut the paragraph. End on the last concrete fact instead of a send-off. If the source states real plans, use those.)

### 26. Too many hyphenated word pairs

**Words to watch:** third-party, cross-functional, client-facing, data-driven, decision-making, well-known, high-quality, real-time, long-term, end-to-end
**Problem:** AI writing often hyphenates these pairs everywhere. Keep the hyphen before a noun when grammar needs it, as in `a high-quality report`. Drop it after the noun, as in `the report is high quality`.
**Before:**
> The cross-functional team delivered a high-quality, data-driven report. The team is cross-functional, the report is high-quality, and the methodology is data-driven.
**After:**
> The cross-functional team delivered a high-quality, data-driven report. The team is cross functional, the report is high quality, and the methodology is data driven.

### 27. Pretending to reveal a deeper truth

**Phrases to watch:** The real question is, at its core, in reality, what really matters, fundamentally, the deeper issue, the heart of the matter
**Problem:** AI writing uses these phrases to make an ordinary point sound like a hidden truth.
**Before:**
> The real question is whether teams can adapt. At its core, what really matters is organizational readiness.
**After:**
> The question is whether teams can adapt. That mostly depends on whether the organization is ready to change its habits.

### 28. Announcing the next point

**Phrases to watch:** Let's dive in, let's explore, let's break this down, here's what you need to know, now let's look at, without further ado, heads up, quick note, before I forget
**Problem:** AI writing often announces the next point instead of stating it. A casual phrase such as "one thing that bit me" can have the same problem. Remove the announcement, not just its formal tone.
**Before:**
> Let's dive into how the report caches results. Here's what you need to know. The report stores the results for 10 minutes.
**After:**
> The report caches the results for 10 minutes.
**Before (casual register):**
> One thing that caught me out is that the development server leaves the cache disabled by default.
**After:**
> The cache is off by default on the development server.

### 29. A heading repeated in the first sentence

**Signs to watch:** A heading followed by a one-line paragraph that simply restates the heading before the real content begins.
**Problem:** AI writing often follows a heading with a sentence that only repeats the heading. Remove the repeated sentence.
**Before:**
> ## Performance
>
> Speed matters.
>
> When users hit a slow page, they leave.
**After:**
> ## Performance
>
> When users hit a slow page, they leave.

### 30. Writing about the previous version
**Problem:** Documentation and comments should describe the current behavior. Mention the previous version only in change logs, release notes, migration guides, and other documents about change.
**Before:**
> This function was added to replace the previous approach of iterating through all items, which caused O(n²) performance.
**After:**
> This function uses a hash map for O(1) lookups, avoiding the O(n²) cost of naive iteration.

### 31. Forced punchlines and dramatic fragments
**Watch for:** a one-line paragraph that restates the paragraph before it; "That is the real win."; "That distinction matters."; "Read that again."; a sentence after an example or number that only names what it showed ("This shows the importance of..."); pause commands; one word in ALL CAPS or with periods between the letters (every. single. day.).
**Problem:** AI writing often turns each sentence into a dramatic closing line. One short sentence can add emphasis. A row of short fragments usually feels forced. Cut a closer that repeats, including one that explains an example the reader just saw. Keep it when it adds a fact or consequence the example does not show.
**Before:**
> Then the new scoring rule arrived. It ignored symmetry. No bonus points. No automatic penalty. Symmetry no longer affected the score at all.
**After:**
> With the new scoring rule, symmetry no longer affects the score.

### 32. Formulaic sayings

**Words to watch:** X is the Y of Z, X becomes a trap, X is not a tool but a mirror, the language of, the currency of, the architecture of
**Problem:** AI writing often turns an ordinary claim into a saying that sounds deep but adds no detail. Replace the saying with the specific claim.
**Before:**
> Symmetry is the language of trust. Efficiency becomes a trap when teams forget the human layer.
**After:**
> Symmetric layouts often feel more predictable to users. Teams can over-optimize workflows and miss how people actually use them.

### 33. Fake-candid openings

**Phrases to watch:** Honestly?, Look, Here's the thing, The thing is, Let's be honest, Real talk, when used as standalone hooks or fake-candid pauses before an ordinary point.
**Problem:** AI writing often starts with a staged pause or claim of honesty before making a routine point. State the point directly.
**Before:**
> Is it worth the price? Honestly? It depends on how often you'll use it.
**After:**
> Whether it's worth the price depends on how often you'll use it.

### 34. Answering objections no one raised

**Phrases to watch:** This isn't (mainly/really) about, I'm not saying/arguing/trying to, To be clear, Don't get me wrong, This is not to say, You could argue/frame this differently but, Some might say... but
**Problem:** AI writing may answer an objection that does not appear in the text. Watch for an unattributed statement about what the writer does not mean, especially when the topic appears nowhere else. A direct claim such as "the API is not thread-safe" is not this pattern.
**Before:**
> This isn't mainly about prompt length, and I'm not arguing that documentation doesn't matter. You could categorize the problem another way, but the issue is whether the agent can use the instruction when it acts.
**After:**
> The issue is whether the agent can use the instruction when it acts.

Remove only the unsupported defense. If it contains a real claim, state that claim directly. Keep an objection when the text names its source or answers it in full.

### 35. Rejecting fake alternatives

**Phrases to watch:** A tempting option/approach would be, One might be tempted to, An obvious approach would be, You might think... but, It would be easy to just, Some would suggest
**Problem:** AI writing may introduce an option that no reader would consider, reject it in a clause, and never mention it again. This often leaves an old drafting idea in the final text. Remove the fake option and state the real constraint directly.
**Before:**
> Session tokens are rotated every 24 hours. A tempting approach would be to rotate them by restarting the auth service on a cron job, but that would drop every active session. Rotation happens in place, and clients refresh transparently.
**After:**
> Session tokens are rotated every 24 hours, in place, and clients refresh transparently.

One rejected option may be valid. Several short, unrelated rejections are a stronger sign. Ask what new information each sentence adds. If it only records an earlier edit, rewrite the paragraph around its main point.


---

## Additional English and Russian patterns

### 36. Antithesis and announced conclusions (EN and RU)

**Phrases to watch:** it's not X, it's Y; not just X but Y; more than just X; X, not Y (as a rhythm device); different layer, different ownership; here's why; here's what this means; the real reason; не X, а Y; не просто X, а Y; и вот почему; вот что это значит; дело не в X
**Problem:** The contrast frames an ordinary claim as a reveal. It can make an ordinary statement sound like a pitch. A series is a pitch pattern. Remove the negated half and the announcement; keep the claim.
**Before:**
> This isn't about the form, it's about who reviews it. This is not just a repair, but a chance to revise the review schedule. And here's why that matters.
**After:**
> We need to assign someone to review the form. We can revise the review schedule during the repair.

Do not "convert" the negation into a positive restatement of the thing nobody claimed ("The tooling is fine"). If the negated half answers no real objection, cut it. See also §34.

### 37. Echoing the interlocutor or the brief

**Signs to watch:** the first sentences restate what the recipient just said; the text names its own constraints ("for non-technical readers, it's important to..."; "as a short update...").
**Problem:** The reader remembers their own words; a restatement reads as agreement padding and doubles the length. The brief is an instruction, not content.
**Before:**
> You said the invoices had different dates in the report and the ledger. As you pointed out, the report uses the payment date and the ledger uses the invoice date. This means they record the same invoices at different times.
**After:**
> The report groups invoices by payment date. The ledger groups them by invoice date.

### 38. Evaluation openers

**Phrases to watch:** Great question; You're absolutely right; This is exactly right; Good point; Отличный вопрос; Верно подмечено; Ты прав
**Problem:** Same family as §22. Drop the evaluation opener, including in replies. Start with the substance.

### 39. Mirror composition and motivational close

**Signs to watch:** the last line echoes the first line for a "closed form" feel; the text ends on an uplifting forward-looking sentence nobody asked for.
**Problem:** School-essay moves. A message can stop at the last concrete fact or next step (§25).
**Before:**
> The team will review the failed imports on Friday. I opened with trust, and trust is where I'll close. This is how we earn it back.
**After:**
> We’ll review the failed imports on Friday.

### 40. Performed empathy, performed vulnerability, stacked praise

**Phrases to watch:** I know this is hard; this is genuinely tough; I'll be honest with you; can I be real for a second; your incredible dedication and unwavering commitment
**Problem:** The writer narrates the reader's feelings or their own honesty instead of saying the thing. Praise stacked with superlatives reads as servile. One specific compliment beats three general ones. The tell is the standalone theatrical opener; "honestly" inside a sentence is ordinary (see false positives in `SKILL.md`).

### 41. Rhetorical question with an immediate self-answer

**Phrases to watch:** Why? Because...; What does this mean? It means...; Почему? Потому что...
**Problem:** The question is a drum roll. Either ask it seriously and leave it open, or state the claim.
**Before:**
> Why did retention drop? Because the credits model changed in May.
**After:**
> Retention dropped after the credits model changed in May.

### 42. Definition and context openers

**Phrases to watch:** In today's world / landscape / era; X is a process that...; More and more, we see...; As we all know; В современном мире; Как известно
**Problem:** The text warms up instead of starting. Begin with the thing itself, a concrete scene, or the claim.

### 43. Email and letter tells

- "I hope this finds you well." Cut it.
- Manufactured sign-offs: "Warmly," "With gratitude," "With deep appreciation." Use the writer’s usual sign-off when the format calls for one.
- Compliment sandwich (praise, criticism, praise). Say the criticism.
- "Happy to jump on a call" and other self-volunteering closes, unless the conversation has earned a call. Keep a scheduling link that the original message uses as a next step.
- Section headers and bold phrases inside a letter or a personal message. Prose only.
- Bullet items with a bold label and a colon (§16) in Slack.

### 44. Extra vocabulary (merge with §7)

**English:** key, powerful, fundamental, transformative, game-changer, game-changing, seamless, robust, leverage (verb), unlock, elevate, navigate (figurative), journey (figurative), resonate, beacon, myriad, plethora, utilize, synergy, cutting-edge, holistic, multifaceted, worth noting, worth highlighting, at the end of the day, deep dive (as a noun, unironic), circle back, touch base, no fluff, let that sink in.

**Russian (канцелярит):** важно отметить, следует подчеркнуть, необходимо учитывать, в современном мире, в конечном счёте, в целом (as a filler), данный, указанный, вышеуказанный, комплексный, инновационный, эффективный, ключевой, мощный, фундаментальный, осуществлять (instead of делать), являться (instead of быть), в рамках, на сегодняшний день. Use plain verbs and untangle strings of participles. Keep long subordinate clauses when they fit the writer’s natural rhythm.

### 45. AI paragraph cadence

**Sign to watch:** "Short sentence. Long sentence. Short. Pause." repeated as a template; every paragraph the same length; a fragment closing each paragraph for drama (§31).
**Problem:** The staccato shape is already read as machine cadence even when each sentence is fine. Vary paragraph length, let one thought run long, let another be a single line, and do not end every paragraph on a punchline.

### 46. Re-explaining what the reader already has

**Signs to watch:** a short reply that restates the problem, walks through the diagnosis and lays out the evidence before it reaches the decision; a query, command or set of numbers pasted in to prove a plan will work; background the other person wrote or already agreed to; the answer sitting in the last line. Acts on replies (Slack, comments, email threads), not on standalone writing.
**Problem:** In a reply the reader already has the context, so rebuilding it adds nothing and buries the point. Each sentence can read fine alone, so this survives sentence-level cleanup. Lead with the decision. Keep only the reasoning that would change whether the reader agrees: usually one fact they lack, and any link they need to act. The full diagnosis and the proof belong in the ticket or document that follows.
**Before (hypothetical):**
> Right, this is a workaround. The fix belongs in the shared importer. It drops the category when an item changes folders. Three of the last 40 moves lost their category, so the cleanup is small. Since several teams use the importer, I'd rather open a separate ticket than change it in this PR.
**After:**
> I’ll open a separate ticket for the importer fix. Several teams use it, so the change needs its own review.

Source: adapted from blader/humanizer v3.1.0 pattern #26 (MIT). The "After" keeps the decision and the reason for the split, and drops the diagnosis and the count.
