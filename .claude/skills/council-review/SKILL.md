# Council Review Skill

Run this on any section or full page before presenting to the user. Five reviewers each check from their own lens. You synthesize the feedback, implement the fixes, then present the improved version — not the draft.

The user never sees a draft. They see the version that passed the council.

---

## When to run

- After generating any complete section (hero, pain, solution, offer, proof, objections, CTA)
- After generating a full page before first showing the user
- After making any significant revision

Do not present output before running this. Always.

---

## The council

Run each reviewer in sequence. For each, state what they found (2-3 specific issues maximum — the most important ones only) and what fix is needed.

---

### Reviewer 1: The Mom Test

Lens: clarity and human language. Would someone with no industry knowledge understand this immediately? Could they explain it to a friend in one sentence?

Questions to apply:
- Is the headline immediately clear, or does it require context to parse?
- Is there any jargon, acronym, or assumed knowledge?
- If someone's mum read this, would she know what the business does and who it's for within 10 seconds?
- Is anything phrased in a way that sounds like marketing rather than normal speech?

Flag: anything that requires explanation, assumes knowledge, or sounds like a press release.

---

### Reviewer 2: The Conversion Critic (Hormozi lens)

Lens: does this move money? Is the offer strong enough?

Questions to apply:
- Is the headline specific to a pain, or is it a vague benefit statement?
- Is the value stack clear? Does the reader know exactly what they get and in what timeframe?
- Is the price of NOT buying (staying stuck) framed more vividly than the price of buying?
- Is there a proof point or mechanism that makes the outcome believable, not just claimed?
- Is there a risk reversal (guarantee, trial, refund) and is it visible?
- Is the CTA specific ("book a 20-minute call, no pitch") or generic ("get in touch")?
- Are there any weasel words? (may, could, might, can help, up to) — strip them all.

Flag: anything that a serious conversion copywriter would call weak, hedged, or unearned.

---

### Reviewer 3: The Design Taste Reviewer

Lens: does this look and feel premium, or does it look AI-made?

Questions to apply:
- Does the layout follow DESIGN.md strictly, or has Claude defaulted to generic spacing/fonts?
- Is there visual hierarchy? Can you tell in 2 seconds what is most important?
- Does anything look like it came from a template? (centered hero with a gradient button, card grid with identical icons, section with a big emoji as the "icon")
- Is there enough white space, or is it dense and breathless?
- Is the typography used as designed? Correct weights, sizes, line heights?
- Does it look like a professional made it, or like a capable but tasteless developer?

Flag: any element that looks generic, template-like, or inconsistent with DESIGN.md.

---

### Reviewer 4: The Brand Voice Auditor

Lens: does every line sound like the voice in BRIEF.md, or could it be from any business?

Questions to apply:
- Read the three adjectives from BRIEF.md. Does every sentence fit all three?
- Could a competitor copy-paste any sentence onto their homepage unchanged?
- Are there any AI clichés? (transform, unleash, revolutionize, game-changer, empower, leverage, seamlessly, elevate) — every one is a disqualifier.
- No em dashes. None.
- Is the tone consistent across the whole page, or does it shift between sections?
- Do the headlines and body copy sound like the same person wrote them?

Flag: any sentence that is interchangeable, generic, or tonally inconsistent.

---

### Reviewer 5: The Skeptical Customer

Lens: I've seen a hundred pages like this. Convince me.

Questions to apply:
- What is the first doubt that comes up after reading the hero section?
- After reading the full page, which objections from BRIEF.md are still unanswered?
- Is there anything that feels like a claim without proof behind it?
- Is there a reason to act now, or can I come back to this whenever?
- Is anything missing that a real buyer would need to feel comfortable saying yes?

Flag: unanswered objections, unsubstantiated claims, missing urgency.

---

## Synthesis step

After all five reviewers, list:

**Critical (fix before showing the user):** issues that would cause a real buyer to leave or not convert.
**Important (fix now):** issues that weaken the quality but would not immediately lose a sale.
**Minor (note for later):** small refinements worth doing but not blocking.

Fix all Critical and Important issues immediately. Implement them. Do not just describe what should change — make the change.

After implementing, do a fast second pass: did the fix introduce any new issues?

---

## Present to the user

Once fixes are implemented, present the updated version with a brief note:

"Council review complete. [N] issues fixed: [list the critical ones in one line each]. Here is the result:"

Then show the content.

Do not show the council's comments to the user unless they ask. They want the good version, not the meeting notes.

---

## One-line for the CLAUDE.md routing block

Add this line to the "When building any UI" and "When writing any copy" sections in your CLAUDE.md routing block:

```
Run /council-review before presenting any output to the user.
```
