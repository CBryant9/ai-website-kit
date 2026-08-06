# Website Builder Kit

This project is set up to help you build a high-quality, persuasive website with Claude Code.

## Before you touch any code

Run the brief skill first. Every time. Without a complete, specific brief, Claude will default to generic.

```
Run .claude/skills/website-brief/SKILL.md
```

Or just say: "Let's start the website process" or "Run the website brief."

Claude will interview you, push back on anything too broad, and produce a tight brief before any building begins.

## The standard this kit enforces

You must be able to describe: one specific person, with one specific painful problem, who wants one specific outcome.

Not "business owners who want to grow." That is not specific enough.
Specific: "solo consultants who lose clients to bigger agencies because they can't produce a professional proposal fast enough."

The brief skill will not let you move on until you get there.

## Skills installed in this kit

- website-brief: the context interview (run this first, always)

## Skills to install before building

Run these in Claude Code before you start generating any UI:

```
npx skills add impeccable
```
- Impeccable: catches AI slop (generic gradients, Inter font everywhere, default shadows). Run at the start of every session.

```
npx skills add taste-skill
```
- taste-skill: injects design personality (variance, motion, density dials). Run after Impeccable.

```
npx skills add kostja94/marketing-skills
```
- Landing page copy, SEO, page structure skills.

## Design reference

Fill in DESIGN.md before prompting Claude to build anything visual.

Options:
- Copy a design system from github.com/VoltAgent/awesome-design-md (57 brands, free)
- Browse styles.refero.design for 2000+ design systems by mood
- Use SkillUI to extract the system from a site you love

Tell Claude: "Strictly follow DESIGN.md for all visual decisions."

## Once brief and design are ready

Tell Claude: "Build the homepage using the brief in BRIEF.md and the design system in DESIGN.md. Use PAS copywriting structure. Install Impeccable and taste-skill first."
