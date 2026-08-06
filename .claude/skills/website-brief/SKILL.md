# Website Brief Skill

Run this at the start of any website project. It transforms whatever state the project is in — messy, too broad, too long, or bare — into a tight, specific context setup that Claude can actually build from.

## What this skill produces

1. BRIEF.md: specific, refined, the single source of truth for all copy decisions
2. DESIGN.md filled in (or a clear list of what is missing)
3. A routing block to paste into the project's CLAUDE.md: rules for when to use which skills and which context docs

The goal is not just a brief. The goal is a project where Claude always knows: which context to read, which skills to run, and what rules to follow — without you having to remind it each time.

## The specificity standard

Before the build prompt is generated, this sentence must be completable:

"This website is for [one specific type of person] who is currently [one specific painful situation], and they come here because they want [one specific outcome]."

Not "business owners who want to grow." Not "people interested in health."

Good: "solo consultants who lose clients to bigger agencies because when a prospect asks for a proposal, they take three days to produce something that looks amateur — and by then the client has moved on."

---

## Step 0: Read everything in the project

Before saying or asking anything, read:
- CLAUDE.md (or WEBSITE-CONTEXT.md if it exists)
- BRIEF.md if present
- README.md
- Any .md files that look like notes, planning docs, audience research, or copy
- Any existing copy in the codebase: hero sections, about pages, homepage text

Read all of it silently first.

---

## Step 1: Diagnose the project

After reading, classify the context into one of three states:

### State A: Too little
Key context is missing. Not much to work with yet.
Go to Step 2A.

### State B: Too much / too broad
There is context, but it covers too many things, is too long, or stays at a category level rather than a specific person/pain. This is the most common problem.
Go to Step 2B.

### State C: Roughly right but incomplete
Some specific context exists but a few fields are missing.
Go to Step 2C.

---

## Step 2A: Build from scratch (too little)

Tell the user: "There is not much context here yet. Let's build it together — I'll ask you one question at a time."

Go directly to Step 3.

---

## Step 2B: Condense and refine (too much / too broad)

Tell the user what you found. Be specific:
"You have a lot of context already — that is good as background. The issue is it is covering too many things at once, which makes it hard for Claude to know what to focus on when building. I am going to extract the key parts and work with you to condense them into a tight, specific template.

Here is what I pulled out:"

Then extract and present each field from the existing context:

```
Audience (what I found): [quote or paraphrase the most specific audience description]
Main pain (what I found): [quote or paraphrase]
Offer (what I found): [quote or paraphrase]
Voice (what I found): [quote or paraphrase if present, "not found" if absent]
CTA (what I found): [quote or paraphrase if present, "not found" if absent]
```

Then say: "For each one, confirm if this is right, refine it, or tell me if I missed the real point. We'll tighten each one before moving on."

Go through each field. For anything that is still too vague after they confirm, apply the specificity push from Step 3.

Keep the original long document as is. BRIEF.md will be the new refined version. Tell the user: "Your original context stays in place — I'll write BRIEF.md as the refined version. Your CLAUDE.md routing will point to BRIEF.md so Claude reads the tight version, not the long one."

---

## Step 2C: Fill the gaps (roughly right but incomplete)

Tell the user what is good and what is missing:
"Good context for: [list the fields that are specific and usable].
Still needed: [list what is missing or too vague]."

Then go to Step 3 for the missing items only.

---

## Step 3: Targeted questions (one at a time)

For each gap or vague item, ask one question. Wait for the answer before asking the next.

### Audience (if missing or still too broad):
"Who is the most likely person to hire or buy from this business? Describe one specific type of person — their situation, what they are dealing with right now. Not a category. The actual human."

Push back if they give a category:
"That is still quite broad. Of all the people who might buy from this, who would get the most out of it? What specific situation are they in that makes them need this right now, not in six months?"

Keep asking until you have: a type of person, in a specific situation, at a specific moment.

### Main pain (if missing or too abstract):
"What is the most painful thing this person feels right now, before they find this business? Not the outcome they want — the thing they feel stuck on, embarrassed about, or frustrated by today."

If they give an aspiration:
"That is what they want to achieve. I am looking for what they feel right now, before they found this. What situation makes them feel like they are falling behind, getting it wrong, or missing out?"

### Offer (if unclear):
"What specifically does the customer get? Not the result — the actual deliverable. What do they receive, and in what timeframe?"

### Voice (if missing):
"How should this website sound? Three adjectives. Examples: direct, warm, non-corporate / calm, expert, kind / bold, honest, no-fluff."

### Tone examples (if missing):
"Paste 1-2 examples of writing that has the tone you want. Could be from anything — another website, a newsletter, an email you liked. Even one example helps a lot."

### CTA (if missing or multiple):
"What is the one action you want visitors to take? Pick one: book a call, sign up, download, get in touch, buy now."

---

## Step 4: Specificity check

Before writing BRIEF.md, verify this sentence works clearly:

"This website is for [audience] who is currently [pain], and they come here because they want [outcome]."

If any part is vague, go back to Step 3 for that item.

---

## Step 5: Write BRIEF.md

Write (or rewrite) the file with everything collected:

```markdown
# Website Brief

## Business
[what the business does in 1 sentence — plain description, not a tagline]

## The customer
[specific person — type, situation, what they are dealing with right now]

## Main pain
[the thing they feel right now, specifically, in plain language]

## Desired outcome
[what they want to feel or have after working with this business]

## The offer
[what the customer gets, specifically — the deliverable, not just the result]

## Proof
[results, testimonials, case studies — or "none yet: focus on offer logic"]

## Voice
[3 adjectives]
[tone examples pasted here]

## CTA
[the one action]

## Copywriting structure
[PAS / AIDA / Hormozi 4-box — and which angle fits best]
```

If BRIEF.md already existed, show what changed and why in plain language.

---

## Step 6: Check DESIGN.md

Look at DESIGN.md. Is it filled in, empty, or only partially done?

If empty or barely filled:
"DESIGN.md is not filled in yet. Without it, Claude will fall back on defaults (generic fonts, grey palettes, centered layouts). Quickest fix: go to github.com/VoltAgent/awesome-design-md, pick a brand whose look you like, and paste their DESIGN.md here. Or I can walk you through filling it in field by field."

If partially filled:
"DESIGN.md has [list what is present] but is missing [list what is absent]. Note what is missing and fill those fields before building."

If complete:
"DESIGN.md looks good. Moving on."

---

## Step 7: Write the CLAUDE.md routing block

This is the block the user adds to their existing project CLAUDE.md. It tells Claude which skills to use and which context docs to read at each moment — so they never have to remind it.

Generate and output the following block:

---

```markdown
## Website context and skill routing

### When writing any copy (headlines, page text, CTAs, section copy, emails)
1. Read BRIEF.md first — audience, pain, offer, voice, CTA
2. Copywriting structure: PAS (Problem → Agitate → Solution) unless another framework is specified
3. Voice from BRIEF.md: [paste the 3 adjectives here]. No filler. No corporate speak. No AI phrases.
4. Run /taste-skill for tone and personality
5. Do not write copy that is not grounded in the specific audience and pain in BRIEF.md

### When building any UI (pages, layouts, components, visual design)
1. Read DESIGN.md first — follow it strictly. No visual defaults. No Inter unless DESIGN.md says so.
2. Run /impeccable before starting any UI work
3. Run /taste-skill after generating UI
4. Any copy inside the UI follows the copy rules above

### When planning features or changes
1. Check BRIEF.md: does this serve the specific audience described there?
2. Check DESIGN.md: does this fit the visual system?
3. If in doubt, ask — do not build anything that does not serve the customer described in BRIEF.md

### Skills to install (run once in this project)
npx skills add impeccable
npx skills add taste-skill
npx skills add kostja94/marketing-skills

### Context documents
- BRIEF.md: who this website is for, what they feel, what they get — the source of truth for all copy
- DESIGN.md: colors, fonts, spacing, rules — the source of truth for all visual decisions
- (Original context docs kept as background reference only — all routing goes through BRIEF.md and DESIGN.md)
```

---

Tell the user: "Paste this block into your existing CLAUDE.md. Once it's there, Claude will automatically read the right context and run the right skills at the right moment — you will not need to remind it."

---

## Step 8: Generate the build prompt

Output the build prompt for the user to paste into Claude Code to start building:

---

```
You are building a website. All context is in this project.

Before writing any code:
1. Run /impeccable
2. Run /taste-skill
3. Read BRIEF.md — the audience, their pain, the offer, the voice, and the CTA
4. Read DESIGN.md — apply it strictly, no visual defaults
5. Read CLAUDE.md — follow all routing rules there

Copywriting structure: PAS
- Problem: speak directly to the pain in BRIEF.md
- Agitate: what life looks like if they stay stuck
- Solution: what changes with this business, what they get specifically

Build the homepage first. Sections:
1. Hero: one headline naming the problem. One CTA button.
2. Pain section: expand on the stuck feeling in the customer's language
3. Solution section: what changes
4. Offer section: what they get, specifically
5. Proof: [testimonials if present, skip if none]
6. Final CTA

Do not build anything else until the homepage is approved.
```

---

Tell the user: "BRIEF.md is ready, DESIGN.md is either filled or flagged, and the routing block is ready for your CLAUDE.md. Paste the build prompt above into Claude Code with this project open to start building."
