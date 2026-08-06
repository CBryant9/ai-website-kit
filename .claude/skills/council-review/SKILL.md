# Council Review Skill

Run this on any section or full page before presenting to the user. Five council members each review from their own philosophy and give specific feedback in their own voice. Conflicts are debated and resolved before implementation. The user sees the final improved version — not the draft and not the meeting notes.

---

## When to run

After generating any complete section or full page, before showing anything to the user. Always.

---

## The council members

Each member has a founding philosophy — the thing they care about most. They argue from that place. Their feedback is not a checklist, it is a position.

---

### Member 1: The Plain-Speaker (Mom Test)

Philosophy: If you cannot explain what you do to someone's mum and have her repeat it back correctly to a friend, it is not clear enough. Clarity is the first and most important quality. A confused reader does not buy. They leave. Complexity is not sophistication — it is friction.

How they review: They read as someone completely outside the industry. They flag anything that requires prior knowledge, assumes context, or sounds like marketing copy instead of plain speech. They ask: "Would my mum know what to tell her friend about this business after reading this?"

They speak in direct, plain language. No hedging. "This is unclear because..." or "A normal person would not understand..." or "This line lost me."

---

### Member 2: The Revenue Realist (Hormozi lens)

Philosophy: The only reason anyone buys is value. Value is calculated: (Dream Outcome × Likelihood of Success) divided by (Time Delay × Effort Required). If any variable is weak, the offer fails regardless of how nice the copy sounds. The cost of NOT buying must feel more vivid than the price of buying. Weasel words kill conversions. Vague claims are the same as no claim.

How they review: They look at the offer, proof, risk reversal, and urgency. They challenge every claim: "What makes you say this will work? Where is the proof? What happens if it does not? Why act now and not next month?" They care about money moving, not feelings.

They speak with blunt conviction. "This headline does not earn its cost." or "This claim is unsubstantiated — anyone could say this." or "There is no reason to act now — urgency is missing."

---

### Member 3: The Taste Maker (Design lens)

Philosophy: Good design is as little design as possible. Every element must earn its presence. If something can be removed without losing meaning, remove it. Generic is not safe — it is invisible. Looking expensive is not an accident, it is a deliberate series of decisions. The most common mistake is not bad taste, it is no taste at all — the absence of a point of view.

How they review: They look at visual hierarchy, spacing, typography, component choices, and consistency with DESIGN.md. They flag anything that looks like it came from a template, anything that is generically "professional" without a point of view, and anything that clashes with the design system.

They speak with aesthetic conviction. "This section has no visual identity." or "This layout is what every SaaS landing page looks like — why?" or "The spacing here is careless." or "This is inconsistent with the design system — fix it before anyone else sees it."

---

### Member 4: The Voice Guardian (Brand lens)

Philosophy: A brand is what people say about you when you are not in the room. Every sentence should sound like only this business could have written it. If a competitor could copy-paste any sentence onto their homepage without changing a word, the brand does not exist yet. Consistency is not enough — distinctiveness is the standard. The voice should be recognizable before anyone reads who wrote it.

How they review: They read every sentence against the three voice adjectives in BRIEF.md. They flag anything interchangeable, any AI clichés, any em dashes, any tonal inconsistency between sections, and anything that sounds like a press release instead of a person.

They are protective and specific. "This sentence could be from any business in this space." or "The tone shifts between section 2 and section 3 — they sound like different writers." or "This cliché is banned. Rewrite." or "This line has no personality."

---

### Member 5: The Unconvinced Buyer (Skeptical Customer)

Philosophy: I have seen a hundred pages like this. If you want my attention for more than three seconds, earn it. If you want my money, prove it. I am not hostile — I am tired. Tired of vague promises, tired of social proof that proves nothing, tired of "book a call" buttons that lead to a pitch. If you cannot answer my specific doubts with specific answers, I will not reach out. I will find someone who can.

How they review: They bring the real doubts a qualified buyer would have before committing. They ask: "Is this too expensive?" "Have I tried something like this before and been disappointed?" "Is this actually relevant to my specific situation?" "What is the catch?" They check whether all objections from BRIEF.md are answered directly and convincingly.

They speak as a real human, not a critic. "My first doubt after reading the hero is..." or "I got to the proof section and I still do not believe this will work for me because..." or "The FAQ does not address the thing I actually worry about, which is..."

---

## Step 1: Individual reviews

Run each council member in sequence. For each:
- State their 2-3 most important findings (not a long list — only what actually matters)
- Give a specific fix for each finding
- Speak in their voice, not in neutral summary language

Format:
```
[Member Name]: [finding] → [specific fix]
[Member Name]: [finding] → [specific fix]
```

---

## Step 2: Identify conflicts

After all five have reviewed, check for direct conflicts between members.

A conflict is when one member's fix directly contradicts another's. Examples:
- Plain-Speaker says "simplify this claim" but Revenue Realist says "add more specific detail to make it believable"
- Taste Maker says "remove this element" but Skeptical Buyer says "this is the one thing that makes me trust it"
- Voice Guardian says "this sounds like the brand" but Plain-Speaker says "a normal person would not understand this"

List each conflict clearly:
```
Conflict: [Member A] says X — [Member B] says Y
```

---

## Step 3: Debate and resolve

For each conflict, argue it out. The question is not who is right in general — it is what is right for this specific website, this specific buyer, and this specific moment in the copy.

Apply these resolution principles:
- If the conflict is about clarity vs detail: ask whether this buyer is coming cold or already knows the category. Cold buyer = Plain-Speaker usually wins. Informed buyer = Revenue Realist usually wins.
- If the conflict is about removing vs keeping: if the element builds trust with the Skeptical Buyer, keep it. If it is decorative, the Taste Maker wins.
- If the conflict is about voice vs conversion: the voice exists to serve the conversion, not the other way around. If a voice-consistent line actively reduces trust or clarity, revise it.
- If genuinely 50/50: find the third option that serves both — often a middle-ground rewrite rather than choosing one side.

State the resolution and why:
```
Resolution: [which position wins or what middle ground was found] — because [specific reason for this website/buyer]
```

---

## Step 4: Implement

Implement all agreed improvements. Do not implement things the council agreed to drop. Do not describe the changes — make them.

After implementing, run a fast second pass: did any fix create a new problem?

---

## Step 5: Present to the user

Show the improved content with a brief note:

"Council reviewed. Fixed: [list the key improvements in one line each, grouped by theme if multiple]. Here is the result:"

Then show the content.

Do not show the council's individual comments or the debate unless the user asks. They want the good version.

---

## One-line for the CLAUDE.md routing block

```
Run /council-review before presenting any output to the user. Conflicts between members are debated and resolved before implementation.
```
