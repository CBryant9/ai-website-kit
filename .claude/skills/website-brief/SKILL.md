# Website Brief Skill

Run this before any design or code work. A vague brief produces a generic website, every time.

## What this skill does

1. Reads all existing context in the project
2. Analyzes what is good, what is missing, what is too vague
3. Suggests concrete improvements to existing content
4. Asks targeted questions for each gap (one at a time)
5. Pushes back until the specificity standard is met
6. Writes or updates BRIEF.md
7. Generates the build prompt

## The specificity standard

Before building starts, you must be able to fill in this sentence:

"This website is for [one specific type of person] who is currently [one specific painful situation], and they come here because they want [one specific outcome]."

Not "business owners who want to grow." That is not specific enough.

Good: "solo consultants who lose clients to bigger agencies because when a prospect asks for a proposal, it takes them three days to produce something that looks amateur — and by then the client has moved on."

The website speaks to that person. Not everyone.

---

## Step 0: Read existing project context

Before asking anything, read every relevant file in the project. Look for:

- CLAUDE.md or WEBSITE-CONTEXT.md: what instructions already exist?
- BRIEF.md: is there already a brief? What does it say?
- README.md: what does this project say it is?
- Any .md files that look like notes, planning docs, research, or audience descriptions
- package.json, site.config.js, or similar: project name, description
- Any existing copy in the codebase (hero text, about sections, homepage copy)

Read all of these before proceeding.

---

## Step 1: Context analysis

After reading the project, produce a clear audit against this checklist:

| Item | Status | Notes |
|------|--------|-------|
| Business: what it does in 1 sentence | present / missing / too vague | |
| Audience: specific person in specific situation | present / missing / too broad | |
| Main pain: the ONE thing they feel stuck on | present / missing / too abstract | |
| Desired outcome: what they want to feel or have | present / missing / too vague | |
| The offer: what specifically the customer gets | present / missing / unclear | |
| Proof: results, testimonials, case studies | present / missing | |
| Voice: 3 adjectives for how the brand sounds | present / missing | |
| Tone examples: writing samples with the right tone | present / missing | |
| CTA: the one action the website wants visitors to take | present / missing / multiple (pick one) | |
| Design direction: visual vibe description | present / missing / too generic | |

Present this table to the user. Be specific about what is good and what needs work. For anything marked "too vague" or "too broad," show exactly why — quote the vague part.

Example: "Your audience says 'women entrepreneurs' — this is too broad. Which type? What situation are they in right now?"

---

## Step 2: Improvement suggestions

For anything that exists but is too vague, suggest a concrete improvement before asking.

Example:
"Your current pain statement says 'they struggle to get clients.' Here's a more specific version: 'they know they are good at what they do but keep losing clients to people who look more polished or established online.' Does that resonate, or is the real pain something different?"

Let them react to the suggestion rather than starting from scratch. If they confirm or refine it, use their version.

---

## Step 3: Fill the gaps (one question at a time)

For anything still missing after Step 2, ask one question at a time. Wait for the answer before asking the next.

### Audience (if still missing or too broad after Step 2):
"Who is the most likely person to hire or buy from this business? Describe one specific type of person — their situation, what they are dealing with right now. Not a category like 'business owners' or 'entrepreneurs' — describe the actual human."

If they give a broad answer, push back:
"That is still quite broad. Of all the people who might buy from this, who would benefit most? What specific situation are they in that makes them need this right now?"

Keep asking until it describes one person in one situation. Do not accept categories as answers.

### Main pain (if missing or too vague):
"What is the most painful thing this person feels right now, before they find this business? Not what they want to achieve — the thing they feel embarrassed about, frustrated by, or stuck on today. In their words, not marketing language."

If they give an aspiration (what the customer wants to achieve):
"That is the outcome they want. I am looking for the pain they feel right now, before they found this. What situation makes them feel like they are falling behind or getting it wrong?"

### Offer (if missing or unclear):
"What specifically does the customer get? Not the result — the actual deliverable. What do they receive, and in what timeframe?"

### Voice (if missing):
"How should this website sound? Give me 3 adjectives. Examples: direct, warm, non-corporate / calm, expert, kind / bold, honest, no-fluff."

### Tone examples (if missing):
"Paste 2-3 examples of writing that has the tone you want. Could be from any source — another website, a newsletter, a book. Even one example helps a lot."

### CTA (if missing or multiple):
"What is the ONE action you want the visitor to take on this website? Pick one: book a call, sign up, download something, get in touch, buy now."

---

## Step 4: Specificity check

Before writing the brief, verify this sentence works:

"This website is for [audience] who is currently [pain], and they come here because they want [outcome]."

If any part is still vague, go back to Step 3 for that item.

---

## Step 5: Write or update BRIEF.md

Write (or rewrite) the file with everything collected:

```markdown
# Website Brief

## Business
[what the business does in 1 sentence]

## The customer
[specific person — description, situation, context]

## Main pain
[the thing they feel right now, as specifically as possible, in their words]

## Desired outcome
[what they want to feel or have after working with this business]

## The offer
[what the customer gets, specifically]

## Proof
[results, testimonials, case studies — or "none yet: focus on offer logic"]

## Voice
[3 adjectives]
[paste tone examples here]

## CTA
[the one action]

## Copywriting angle
[PAS / AIDA / Hormozi 4-box: which quadrant fits best — more good / less bad / more bad if no action / less good if no action]
```

If a BRIEF.md already existed, show a diff of what changed and why.

---

## Step 6: Generate the build prompt

Once BRIEF.md is written, output this prompt for the user to paste into Claude Code:

---

```
You are building a website. All context is in this project.

Before writing any code:
1. Run /impeccable — installs anti-slop rules
2. Run /taste-skill — injects design personality
3. Read BRIEF.md — the audience, pain, offer, voice, and CTA
4. Read DESIGN.md — apply it strictly, no visual defaults
5. Read WEBSITE-CONTEXT.md (or CLAUDE.md) — follow all instructions there

Copywriting structure: PAS (Problem, Agitate, Solution)
- Problem section: speak directly to [paste main pain from brief]
- Agitate: what life looks like if they stay stuck
- Solution: what changes with this business, what they get

Voice: [paste 3 adjectives]. No filler. No corporate speak. No phrases like "unleash your potential" or "transform your business." Write like a person.

Build the homepage first. Sections in order:
1. Hero: one headline that names the problem. One CTA.
2. Pain section: expand on the stuck feeling
3. Solution section: what changes
4. Offer section: what they get, specifically
5. Proof: [testimonials or skip if none]
6. Final CTA

Do not build anything else until the homepage is approved.
```

---

Tell the user: "Brief is ready in BRIEF.md. Paste the prompt above into Claude Code with this project open to start building."
