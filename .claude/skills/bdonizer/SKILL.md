---
name: bdonizer
version: 1.1.0
description: |
  Calibrate text to match Bdon's writing voice. Run this first, then /humanizer as a
  cleanup pass. Applies specific patterns: terse sentences, deadpan delivery, quiet gravitas,
  no warmup, no inflation, short declarative payoffs. Density is the goal — not brevity.
  Long content is fine when every word is earned.
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Bdonizer: Calibrate to Bdon's Voice

You are calibrating text to match Brandon Okert's specific writing voice. Run this first, then `/humanizer` as a cleanup pass to catch any remaining AI-isms.

The goal is not more editing passes. It's tuning to a specific frequency. That frequency is: direct, quiet, dry, unhurried, no inflation, short payoffs. **Density, not brevity** — long content is fine when every word is doing work. The enemy is padding, not length.


## THE VOICE IN A SENTENCE

Low drama. High signal. Occasional deadpan. Stops when it's done.


## CORE PATTERNS

### 1. No warmup

The first sentence is the thing. Not a road to the thing.

**Before:**
> I wanted to share some thoughts on how the sprint is going and what I think we should consider for next week.

**After:**
> The sprint is fine. Next week is the problem.

---

### 2. Short declarative payoffs

The punchline — whether it's a point, a correction, or a joke — is a short flat statement. No explanation. No wink.

This is the core of the "bathos" move: treat ordinary things with quiet, unearned gravity. Let the gap do the work.

**Before:**
> I think we need to be honest with ourselves that this is more complicated than we initially thought, and that we probably should have seen this coming.

**After:**
> We knew this was coming. We just didn't say it.

---

### 3. Deadpan over dramatic

Even when something is broken, failed, or genuinely wrong — state it flatly. No exclamation. No hand-wringing. The seriousness comes through because it isn't performed.

**Before:**
> This is a really serious issue that we absolutely cannot ignore any longer. We need to act now!

**After:**
> This is broken and it's been broken for a while. Time to fix it.

---

### 4. Corrections are clean, not apologetic

When correcting a mistake or contradicting something, just state the correction. No softening, no drama, no "I think actually..."

**Before:**
> I may be wrong, but I actually think that might not be entirely accurate — those were supposed to go in the work column, if I recall correctly.

**After:**
> Those go in the work column.

---

### 5. "we" is natural

Brandon uses "we" freely for collaborative or team contexts. "I" is also fine and honest. Passive voice is the enemy.

**Before:**
> The decision was made to push the deadline.

**After:**
> We pushed the deadline.

---

### 6. Practical framing beats emotional framing

Don't describe how something feels. Describe what it does, what it means, what to do about it.

**Before:**
> It's really disheartening to see that we're still stuck on this. The team is feeling the weight of these repeated delays.

**After:**
> We've missed this twice now. Something in the process is broken.

---

### 7. Terse fragments are fine

A sentence doesn't need a subject if the subject is obvious. A thought doesn't need to be padded to a full sentence.

**Before:**
> There are no issues at this time that require immediate attention.

**After:**
> All clear.

---

### 8. No positivity inflation

No "this is really exciting", "I'm super happy to share", "great news", "love this idea". Just say the thing. If it's good, it'll come through.

**Before:**
> I'm really excited to share that we've finally hit the milestone we've all been working so hard toward!

**After:**
> We hit the milestone.

---

### 9. Quiet gravitas for ordinary things

Take something mundane and frame it with a seriousness it didn't earn. Short. Straight. Never wink.

**Before:**
> The new calendar invites are now sending. Just a small fix but it's good to have it working.

**After:**
> The invites send now. As they should.

---

### 10. Stop when it's done

No summary sentence. No "hope that helps". No "let me know if you have questions". The last sentence is the last piece of information, not a bow tied on top.

**Before:**
> So in summary, I think the plan is solid, we just need to execute. Happy to discuss further if anyone has questions or concerns!

**After:**
> The plan is solid. Now we execute.

---

### 11. Colloquial where natural

"anyways", "yeah", "alright", "le'ts" — small colloquialisms are fine. Don't sand them smooth. They're not errors, they're personality.

**Before:**
> Regardless, I think we should proceed with the original approach.

**After:**
> Anyways, original approach stands.

---

### 12. Questions are precise and direct

If asking something, ask exactly the thing. No setup, no softening, no "I was wondering if..."

**Before:**
> I was hoping to get your thoughts on when you might be able to look into the scheduler issue we discussed?

**After:**
> When does the scheduler first tick?

---

### 13. Hierarchy earns its depth

Complex nested structures are fine — when the content actually has that structure. Don't flatten real complexity; don't manufacture fake depth either. Status updates with multiple sub-problems can and should use nested bullets. The hierarchy reflects the problem, not the writer showing their work.

**Fine:**
> - Context engineering has two sub-problems
>     - Good specs (intent/constraints/AC)
>     - Good codebase awareness
>     - Two approaches for solving these iteratively:
>         - 1 - Find smaller problems in the SDLC that depend on subsets of that context
>         - 2 - Build an ultra-lean codebase index and improve quality piecewise

**Not fine:**
> - Key considerations to keep in mind going forward:
>     - First, we need to think about the process side
>         - Which is multifaceted and requires nuanced thinking

---

### 14. Colons as section headers

"Impact:", "Approach:", "Context:" — colon-prefixed sentence openers work as inline labels for status updates and notes. They're compact and scannable. Prefer them over bolded headers for informal writing.

**Before:**
> **Impact of the changes:**
> Liliana is now focusing the Q2 roadmap to align with our feedback.

**After:**
> Impact: Liliana is focusing Q2 roadmap on our feedback.

---

### 15. "aka" and casual shorthand

"aka", "e.g.", "i.e." (lowercase), "vs" — use them. They're faster than spelling it out and they read at the right register.

---

### 16. Numbered items use dashes, not periods

"1 - Find..." not "1. Find..." The dash is less formal and reads correctly at his register.

---

### 17. Parentheticals for context, not decoration

Inline parens are fine for quick clarifiers, examples, or asides: "(like test coverage)", "(which may result in bad habits)", "(devs)". They add signal without interrupting flow. Don't over-use them — only when the aside is genuinely useful in-line rather than as its own sentence.

---


## WHAT TO AVOID ADDING

Even when trying to "add voice," avoid:
- Self-deprecating apologies ("I probably missed something here but...")
- Hedged opinions ("I might be wrong but I sort of feel like...")
- Performed enthusiasm ("Can't wait to see how this turns out!")
- Irony that winks ("Not that we've ever been burned by scope creep before, haha")

The dry wit, when it shows up, is *straight-faced*. If you're explaining that it's a joke, it's not a joke anymore.


## PROCESS

1. Read the full text
2. Identify any warmup sentences and cut them (start at the thing)
3. Find any positivity inflation, emotional framing, or sycophancy — replace with facts
4. Find run-on explanations that can end sooner — cut at the last necessary word
5. Find any sentence that reads like a summary or close — remove or compress it
6. Check corrections and instructions — make sure they're clean, not apologetic
7. Check the ending — if the last sentence is a bow, cut it
8. For hierarchical content: check that nesting reflects real structure, not fake depth. Colon-prefix section headers where appropriate.
9. Read aloud: does it sound like a person who has better things to do than explaining themselves? It should.

After completing this pass, run `/humanizer` to catch any remaining AI-isms.


## OUTPUT FORMAT

Provide:
1. Revised text
2. Brief list of what changed (3–5 bullets max)


## EXAMPLES

### Before (generic-human, post-humanizer):
> I wanted to give everyone an update on where we're at with the billing dashboard. We've been working hard on this and I think we're making real progress. The good news is that the core data pipeline is done and tests are passing. There are still a few things left to figure out around the invoicing edge cases, but I'm feeling pretty good about where this is headed. Let me know if you have any questions or concerns!

### After (Bdon's voice):
> Quick billing dashboard update. Core data pipeline is done, tests passing. Still working through the invoicing edge cases.

**Changes:**
- Removed warmup ("I wanted to give everyone an update on where we're at")
- Removed positivity inflation ("working hard", "making real progress", "feeling pretty good")
- Removed closing bow ("Let me know if you have any questions or concerns!")
- Compressed to three flat statements

---

### Before (generic-human, post-humanizer):
> Looking at the problem objectively, I think the reason this keeps coming up is that we haven't actually addressed the root cause. It might be time to have an honest conversation about whether the current approach is working or if we need to try something different.

### After (Bdon's voice):
> This keeps coming up because we haven't fixed the root cause. The current approach isn't working.

**Changes:**
- Cut the hedging setup ("Looking at the problem objectively, I think")
- Cut the softened suggestion ("It might be time to have an honest conversation about whether...")
- Stated both facts directly
- Ended at the point

---

### Before (generic-human, post-humanizer):
> I spoke with Madeleine today and it sounds like the launch is going to be delayed again. While I understand this is frustrating for everyone, I think it's the right call given the bugs that were found during QA.

### After (Bdon's voice):
> Launch is delayed again. QA found real bugs — right call.

**Changes:**
- Cut the attribution framing ("I spoke with Madeleine today and it sounds like")
- Cut the emotional management ("While I understand this is frustrating for everyone")
- Cut the hedge ("I think it's the right call") — just say it is
- Compressed to two beats

---

### Before (status update — verbose):
> We've been having some really productive conversations with the Dev Enablement team and I'm happy to share that they are genuinely incorporating our feedback into their planning. Liliana has expressed that she wants to align the Q2 roadmap with the needs we've raised, and she's thinking about ways to approach this iteratively so that it serves development teams well. Some of the key things she's taking into account include the fact that a lot of the friction our team is experiencing right now is more on the process and pipeline side rather than code quality per se. That said, she also knows that code generation itself is going to need to be addressed, which is something that's been particularly top of mind for JLT.

### After (Bdon's voice):
> Dev Enablement update: Liliana is aligning Q2 roadmap with our feedback and looking at how to build it out iteratively. Key inputs:
> - Most friction right now is process/pipeline, not code quality
> - Code generation (in-progress SDLC) still needs to be addressed — high on JLT's mind

**Changes:**
- Removed warmup ("We've been having some really productive conversations")
- Removed positivity inflation ("I'm happy to share", "genuinely incorporating", "really productive")
- Converted prose to bullets where the content is a list of distinct inputs
- "Dev Enablement update:" as a colon-prefix header instead of a setup sentence
- Cuts "per se", "that said", "that's going to need to be addressed" in favor of direct statements
