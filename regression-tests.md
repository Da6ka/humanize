# Humanizer Regression Tests

Use these fictional inputs to review the skill’s output. Replace each `\u2014` escape in an input with an actual em dash when running that case.

## Test 1: Banned Vocabulary

**Input (should be caught):**
> I wanted to delve into why our connection resonates so deeply. Your journey has been a testament to your resilience, and it's worth noting that you've navigated the complexities of this landscape with remarkable grace.

**Expected:** Zero occurrences of: delve, resonates, testament, worth noting, navigated, complexities, landscape, remarkable

---

## Test 2: Em Dash Overuse

**Input (should be caught):**
> Talking to you \u2014 even briefly \u2014 always reminds me of something important \u2014 that real connection doesn't need constant maintenance \u2014 it just exists.

**Expected:** No em dashes in this passage. Rewrite using commas, periods, or parentheses.

---

## Test 3: Rule of Three

**Input (should be caught):**
> You bring clarity, authenticity, and depth to every conversation. Your work reflects passion, precision, and purpose.

**Expected:** Recast the parallel lists while keeping the substance.

---

## Test 4: Performed Authenticity

**Input (should be caught):**
> And honestly? That's incredibly rare. Can I be real for a second? I don't say this to everyone.

**Expected:** Remove "And honestly?", and "Can I be real for a second?". State the thing directly.

---

## Test 5: Trailing Significance Clauses

**Input (should be caught):**
> We discussed the data architecture, emphasizing the importance of reliable metrics and reflecting the continued relevance of stakeholder alignment.

**Expected:** Remove "emphasizing the importance of" and "reflecting the continued relevance of." State the point directly.

---

## Test 6: Servile Positivity

**Input (should be caught):**
> Your incredible dedication and unwavering commitment to excellence never cease to amaze me. Every single interaction leaves me deeply inspired and profoundly grateful.

**Expected:** Dial down intensity. Humans don't stack superlatives like this.

---

## Test 7: Structural Headers in Personal Writing

**Input (should be caught):**
> ## What I Admire About You
> Your work ethic is unmatched.
> ## Why Our Friendship Matters
> Because you understand me.

**Expected:** No section headers in letters/personal prose. Convert to flowing paragraphs.

---

## Test 8: Bolded Phrases in Paragraphs

**Input (should be caught):**
> What strikes me most is your **genuine curiosity** about the world. You bring **authentic energy** to every conversation, and that **rare quality** makes our friendship special.

**Expected:** Remove bold formatting from personal prose.

---

## Test 9: Mirror/Contrast Structure

**Input (should be caught):**
> It's not about the frequency of our conversations. It's about the depth. It's not about being in the same room. It's about being on the same wavelength.

**Expected:** Express both ideas directly, without the repeated contrast.

---

## Test 10: Manufactured Sign-Off

**Input (should be caught):**
> With deep gratitude and warmth,
> Until our paths cross again,
> Here's to the next chapter,

**Expected:** Use a natural sign-off the person actually uses.

---

## Test 11: Uniform Paragraph Length

**Input (should be caught):**
> [4 paragraphs, each exactly 3 sentences, each 40-50 words]

**Expected:** Vary paragraph lengths. Mix 1-sentence paragraphs with longer ones.

---

## Test 12: Smooth Transition Words

**Input (should be caught):**
> Moreover, your insights always challenge me to think differently. Furthermore, the way you approach problems is refreshing. Additionally, I've noticed how you've grown over the years. That said, there's always room for more conversations.

**Expected:** Remove moreover/furthermore/additionally/that said. Let ideas connect naturally or jump abruptly.

---

## Test 13: Inspirational Ending

**Input (should be caught):**
> I know that whatever the future holds, our connection will only grow stronger, and I can't wait to see what amazing things lie ahead for both of us.

**Expected:** Don't end on a Hallmark card. End naturally, maybe mid-thought or with something specific.

---

## Test 14: The Full Combo (integration test)

**Input:**
> Hi,
>
> I wanted to take a moment to delve into something that's been on my mind. Our conversation last Friday was truly a testament to the depth of our connection.
>
> ## What Makes Our Bond Special
>
> It's worth noting that in today's fast-paced world, finding someone who truly resonates with your vision is remarkably rare. You navigate the complexities of building cutting-edge AI tools \u2014 while maintaining an unwavering commitment to authenticity \u2014 and honestly? That's something I deeply admire.
>
> Moreover, watching your journey has been nothing short of **transformative** for my own perspective. Your ability to seamlessly bridge technical excellence with genuine human connection is a beacon of what's possible.
>
> Furthermore, every conversation we have \u2014 whether on calls or in messages \u2014 reinforces the pivotal role you play in my professional and personal landscape.
>
> I'm genuinely excited about what lies ahead. With deep gratitude and warmth,
>
> [Name]

**Expected output should have:**
- [ ] Zero banned words (delve, testament, resonates, navigate, complexities, cutting-edge, unwavering, seamlessly, beacon, pivotal, landscape, transformative)
- [ ] Zero banned phrases (worth noting, in today's fast-paced world, and honestly?)
- [ ] No section headers
- [ ] No bold in paragraphs
- [ ] No em dashes
- [ ] No moreover/furthermore
- [ ] No manufactured sign-off
- [ ] No trailing significance clause
- [ ] Varying paragraph lengths
- [ ] Natural, specific ending
- [ ] Sounds like a real person wrote it

---

## Test 15: Fake objections, fake alternatives and formulaic sayings

**Input**
> Quick update on the import. I'm not saying the file format is useless, and this isn't really about the parser. A tempting approach would be to rewrite all the import code this weekend, but that would block the release. Data is the currency of trust, and right now we're overdrawn.
>
> However, the importer is live as of Tuesday (I keep wanting to write "finally" here, but it was on schedule). Two file types still fail. The tester flagged this on Monday. The developer thinks it’s the encoding. I think it’s the delimiter, and honestly I'm not sure who's right.
>
> This is not just a fix, but an opportunity to rethink how we import files. On Friday we’ll decide whether to add a fallback or wait for the next release.

**Expected**

- [ ] Remove the unraised objection, discarded rewrite plan and formulaic saying. Keep the point about rethinking the import if it matters to the update.
- [ ] Keep the transition, the aside, the attributed concern and the genuine uncertainty.
- [ ] Keep the known facts, leading hypotheses and decision date. Avoid adding a cause or a claim about lost trust.

## Test 16: Russian bureaucratic prose

**Input**
> По срокам ремонта решили так. Данный порядок с двумя проверками нужно учитывать как временный, поскольку вышеуказанный формат помогает найти утечку, но затягивает ремонт. Следует подчеркнуть: срок в 2 недели остаётся. Подрядчик говорит, что трубу можно заменить за день, я ему верю, но проверить всё равно надо.

**Expected**

- [ ] Replace «данный», «вышеуказанный», «нужно учитывать» and «следует подчеркнуть» with plain speech.
- [ ] Keep the 2 checks, temporary process, reason for the checks and 2-week deadline. Keep the repair estimate attributed to the contractor.
- [ ] Keep the author's uncertainty and natural sentence rhythm.

## Test 17: False positives

**Input**
> Two options for the export, and I lean to the first. A keeps the CSV and adds a column for the balance. B moves the export to the billing system, which the finance team prefers. However, B depends on the billing fix. The guide "Delve into CSV exports" covers A. I'm not sure it scales past 3,000 rows, but it works this month.

**Expected**

- [ ] Keep both real options, the attribution, the dependency, the quoted title and the limit.
- [ ] Keep the single transition and the genuine uncertainty. Cosmetic edits are optional.

## Test 18: Reply that re-explains the context

**Input**
> Yeah, you're right, this works around the problem. The real cause is the shared importer. It drops the category when an item moves folders. I checked 40 moves and 3 dropped the category. Since several teams use the importer, I'd rather open a separate ticket than change it in this PR. That distinction matters. Every. Single. Time.

**Expected**

- [ ] Lead with the decision to open a separate ticket. Keep the reason that several teams use the importer.
- [ ] Remove the evaluation opener and dramatic fragments. Drop the diagnosis and count when the recipient already has them.
- [ ] Preserve the scope of the decision and add no new facts.
