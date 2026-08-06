# Setup Guide

## Option A: Fresh project (no existing CLAUDE.md)

Clone this repo and start building. Everything is already configured.

```bash
git clone [repo-url] my-website
cd my-website
```

Open in Claude Code. Say: "Run the website brief."

---

## Option B: Adding to an existing project that already has a CLAUDE.md

### Step 1: Copy the kit files into your project

Copy these into your existing project root:
- `DESIGN.md` (the design system template)
- `.claude/skills/website-brief/` (the brief skill folder)

### Step 2: Rename this kit's CLAUDE.md

Rename `CLAUDE.md` to `WEBSITE-CONTEXT.md` so it does not conflict with your existing CLAUDE.md.

### Step 3: Add one routing block to your existing CLAUDE.md

Add this anywhere near the top of your project's existing CLAUDE.md:

```markdown
## Website context

When doing any website work — design decisions, copy, building pages, planning features, reviewing what exists:
1. Read WEBSITE-CONTEXT.md first. Follow all design and brief rules there.
2. Run the website brief skill if context is missing or vague: .claude/skills/website-brief/SKILL.md
3. Do not make visual or copy decisions without checking WEBSITE-CONTEXT.md.
```

### Step 4: Install skills

In Claude Code, run:
```
npx skills add impeccable
npx skills add taste-skill
npx skills add kostja94/marketing-skills
```

### Step 5: Fill in DESIGN.md

Either fill it in manually (see the template) or copy a brand design system from github.com/VoltAgent/awesome-design-md.

### Step 6: Run the brief

Say: "Run the website brief." Claude will read your existing project context, show you what is missing or too vague, and guide you from there.

---

## What the brief skill reads in your project

When you run the brief skill, Claude scans for:
- Your existing CLAUDE.md or WEBSITE-CONTEXT.md
- Any existing BRIEF.md
- README.md
- Any .md planning or notes files
- Existing homepage copy in your codebase (hero text, about sections)

It audits all of this against the context checklist and tells you what is good, what is missing, and what is too vague before asking you anything.

---

## Context quality checklist

Claude will check your context against these. Each one needs to be specific:

- Business: what it does in one sentence (not a tagline, a plain description)
- Audience: one specific type of person in one specific situation (not a category)
- Main pain: the one thing they feel embarrassed about or stuck on right now (not a goal they want to achieve)
- Desired outcome: what they want to feel or have afterward
- Offer: what they specifically get (not the result, the deliverable)
- Proof: results or testimonials (or acknowledged absence)
- Voice: 3 adjectives + 1-2 tone examples
- CTA: one action (not multiple)
- Design direction: visual vibe in 2-3 sentences

If any item is missing, the skill asks. If any item is too vague, the skill pushes back.
