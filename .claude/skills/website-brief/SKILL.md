# Website Brief Skill

Run this before any design or code work. The website will be as specific as your brief. A vague brief produces a generic website, every time.

## What this skill does

1. Reads any context you have already written (look for BRIEF.md, any notes, anything about the business or audience)
2. Checks it against the specificity standard
3. Asks targeted questions for anything missing or too vague
4. Actively pushes back until you hit the standard
5. Writes a complete BRIEF.md
6. Generates the build prompt

## The specificity standard

Before building starts, you must be able to fill in this sentence:

"This website is for [one specific type of person] who is currently [one specific painful feeling or situation], and they come here because they want [one specific outcome]."

Not: "business owners who want to grow."
That is not specific enough.

Good: "solo consultants who lose clients to bigger agencies because when a prospect asks for a proposal, they take three days to produce one that looks amateur — and by then the client has moved on."

The website speaks to that person. Not everyone.

## Step 1: Read existing context

Look for:
- BRIEF.md (if it exists, read it)
- Any .md files with notes about the business, audience, or offer
- Anything in the project that describes what this website is for

If nothing exists yet, that is fine — start fresh.

## Step 2: Run the context analysis

Check what you have (or don't have) against this list. Note what is missing or too vague:

- [ ] Business: what does this business actually do, in one sentence?
- [ ] Audience: who specifically is the customer? (not a broad category — a specific type of person in a specific situation)
- [ ] Main pain: what is the ONE thing they feel stuck on or embarrassed about right now?
- [ ] Desired outcome: what do they actually want to feel or have after working with this business?
- [ ] The offer: what specifically does the customer get?
- [ ] Proof: any results, testimonials, or social proof that shows it works?
- [ ] Voice: how does this business sound? (3 adjectives)
- [ ] Tone examples: any examples of writing with the right tone?
- [ ] CTA: what is the ONE action the website wants the visitor to take?
- [ ] Design direction: minimal/bold/editorial/warm/clean? (fill in DESIGN.md)

## Step 3: Interview — ask for what is missing

For each gap, ask ONE question at a time. Wait for the answer before asking the next.

Do not ask multiple questions at once. One at a time.

### Audience question (if missing or too broad):
"Who is the most likely person to hire / buy from this business? Describe one specific type of person — their job, their situation, what they are struggling with right now. Not a category like 'business owners' — describe the actual human."

If they give a broad answer, push back:
"That is still quite broad. Let's get more specific. Of all the people who might buy from this business, who would benefit most? What specific situation are they in right now that makes them need this?"

Keep pushing until it describes one person in one situation. Do not accept "people who want X" as an answer.

### Main pain question (if missing or too vague):
"What is the most painful thing this person feels right now — before they find this business? Not what they want to achieve. The thing they feel embarrassed about, frustrated by, or stuck on. In their words, not marketing language."

If they give an aspiration (what the customer wants), redirect:
"That's the outcome they want — I want the pain they feel right now, before they found this. What situation makes them feel stuck or like they're failing?"

### Offer question (if missing or too vague):
"What specifically does the customer get? Not the result — the actual thing. What do they receive, and in what timeframe?"

### Proof question (if missing):
"Do you have any results, case studies, or testimonials? Even rough numbers or one example story is useful."

If they don't have any:
"That's fine. We'll keep the proof section minimal and focus on the logic of the offer instead."

### Voice question (if missing):
"How should this website sound? Give me 3 adjectives. Examples: direct and warm and non-corporate / calm and expert and kind / bold and honest and no-fluff."

### CTA question (if missing):
"What is the ONE action you want the visitor to take on this website? Book a call, sign up for a free trial, download something, contact you? Pick one."

## Step 4: Specificity check

Before writing the brief, run this check:

Read back the audience + pain description you have collected. Can you fill in this sentence clearly?

"This website is for [person] who is currently [feeling/situation], and they come here because they want [outcome]."

If yes: continue.
If no: go back to Step 3 and ask more targeted questions. Do not proceed until this sentence is clear.

## Step 5: Write BRIEF.md

Once all questions are answered and the specificity check passes, write the file:

```markdown
# Website Brief

## Business
[what the business does in 1 sentence]

## The customer
[specific person in specific situation — the full description from the interview]

## Main pain
[the thing they feel right now, in their words]

## Desired outcome
[what they want to feel or have after working with this business]

## The offer
[what the customer gets, specifically]

## Proof
[results, testimonials, or case studies — or "none yet"]

## Voice
[3 adjectives]
[2-3 examples of writing with the right tone, pasted in]

## CTA
[the one action you want them to take]

## Copywriting angle
[which framework fits best: PAS / AIDA / Hormozi 4-box + which quadrant]
```

Write this to BRIEF.md in the project root.

## Step 6: Generate the build prompt

Once BRIEF.md is written, generate and output this prompt for the user to copy-paste into Claude Code:

---

```
You are building a website for [business name].

Read BRIEF.md for the complete context. Read DESIGN.md for the visual system.

Before writing any code:
1. Run /impeccable to install the anti-slop rules
2. Run /taste-skill to inject design personality
3. Read BRIEF.md — understand the customer, their pain, and the offer
4. Read DESIGN.md — apply it strictly, no defaults

Copywriting structure: use PAS (Problem, Agitate, Solution) for the hero and main sections.
- Problem: speak directly to [main pain from brief]
- Agitate: what happens if they stay stuck
- Solution: introduce the offer, show the outcome

Voice: [3 adjectives from brief]. No filler words. No corporate speak. No AI phrases like "unleash your potential" or "transform your business."

Build the homepage first. Sections in order:
1. Hero: headline that names the problem + CTA
2. Pain section: expand on what it feels like to be stuck
3. Solution section: what changes with this business
4. Offer section: what they get specifically
5. Proof: [testimonials/results or skip if none]
6. Final CTA

Do not build anything else until the homepage is reviewed and approved.
```

---

Tell the user: "Your brief is ready in BRIEF.md and your build prompt is above. Copy the prompt into Claude Code with Claude Code open in this project folder to start building."
