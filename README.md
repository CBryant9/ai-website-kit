# AI Website Kit

A starter kit for building high-quality, persuasive websites with Claude Code.

## The problem this solves

AI produces generic websites when you give it vague context. This kit solves that by forcing the right context before any code is written.

## How to use it

1. Clone this repo into your website project folder (or copy the files in)
2. Open the project in Claude Code
3. Say: "Run the website brief" or "Let's start the website process"
4. The brief skill interviews you, narrows your audience, identifies the core pain, and produces a tight brief
5. Fill in DESIGN.md (or copy one from github.com/VoltAgent/awesome-design-md)
6. Use the generated build prompt to start building

## What's in the kit

- `CLAUDE.md` — tells Claude Code to run the brief before building
- `DESIGN.md` — template for your visual system (colors, fonts, spacing, rules)
- `.claude/skills/website-brief/SKILL.md` — the context interview skill

## Skills to install before building

Run these in Claude Code:
```
npx skills add impeccable
npx skills add taste-skill
npx skills add kostja94/marketing-skills
```

## Design reference

If you don't know what to put in DESIGN.md, pick a brand you like from:
- github.com/VoltAgent/awesome-design-md (57 brands, free)
- styles.refero.design (2000+ systems, search by mood or URL)

## The specificity standard

The brief skill enforces this before building starts:

"This website is for [one specific person] who is currently [one specific painful situation], and they come here because they want [one specific outcome]."

Generic context = generic website. The skill will keep asking until you get specific.

## Which model to use

- **Building (code, layouts, components):** Sonnet is fine. Fast and capable.
- **Writing copy (hero headline, pain section, offer section):** Use Fable. Better at maintaining consistent tone over long-form content and avoids slipping into generic AI voice.
- **Reviewing copy after build:** Run /impeccable and /taste-skill first. Then ask Fable to "read this page as a skeptical customer and tell me what doesn't land."

The single biggest cause of bad results is vague context, not model choice. A well-briefed Sonnet produces better copy than an unbriefed Fable.
