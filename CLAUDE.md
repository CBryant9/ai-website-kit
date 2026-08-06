# Website Builder Kit

This kit gives Claude Code everything it needs to build a high-quality, persuasive website.

---

## If this is a fresh project (no existing CLAUDE.md)

Everything is already set up. Start here:

Say: "Run the website brief" or "Let's start the website process."

Claude will read any context you have, identify gaps, and interview you to fill them before any code is written.

---

## If you are adding this to an existing project that already has a CLAUDE.md

Add this block to your existing CLAUDE.md (anywhere near the top):

```
## Website context

When doing any website work — design decisions, copy, building pages, planning features, or reviewing existing work:
1. Read WEBSITE-CONTEXT.md in this project first. Follow all design and brief rules there.
2. Run the website brief skill if context is missing or vague: .claude/skills/website-brief/SKILL.md
3. Do not make visual or copy decisions without checking against WEBSITE-CONTEXT.md.
```

Then rename this kit's CLAUDE.md to WEBSITE-CONTEXT.md.

That's it. Your existing CLAUDE.md now routes to the kit when doing website work.

---

## Before building anything

The brief skill runs first. Always.

Say: "Run the website brief" and Claude will:
1. Read any existing context in the project (CLAUDE.md, notes, planning docs, README)
2. Identify what is missing or too vague
3. Suggest how to improve what is already there
4. Ask targeted questions for each gap
5. Push back until the context is specific enough to build from
6. Write BRIEF.md and generate the build prompt

---

## Skills to install before writing any UI

```
npx skills add impeccable
npx skills add taste-skill
npx skills add kostja94/marketing-skills
```

Install these once, in order. Then tell Claude: "Install skills before building."

---

## Design reference

Fill in DESIGN.md before any visual work.

Fastest route: pick a brand from github.com/VoltAgent/awesome-design-md, copy their DESIGN.md into this project. 57 brands, free.

More options: styles.refero.design (2000+ systems, search by mood, vibe, or URL).

Once DESIGN.md is filled in, tell Claude: "Strictly follow DESIGN.md for all visual decisions."

---

## The build command

Once BRIEF.md and DESIGN.md are ready:

"Build the homepage using BRIEF.md for all copy and audience context, and DESIGN.md for all visual decisions. Install Impeccable and taste-skill first. Use PAS copywriting structure."
