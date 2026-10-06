# Lab 2: Fact-Checking and Grounding AI Output

**Course:** Claude.ai Essentials
**Duration:** 30 to 40 minutes
**Format:** Instructor-led, in-class hands-on lab, run after Module 8

---

## Prerequisites

- [ ] Module 8's group exercise on spotting a plausible-but-wrong answer completed earlier in this class
- [ ] Lab 1 completed
- [ ] The Claude.ai account provided for class, the same one you used in Lab 1
- [ ] A modern web browser with internet access
- [ ] No installation, no coding, and no additional software required

> **Why this lab follows the group exercise:** Module 8 walked through one pre-built example together as a group, with the instructor guiding you to the error. This lab asks you to find errors on your own, without that guidance, using prompts designed to be more challenging than the group example. Work through it on your own, and ask the instructor for help only after you have made your own attempt.

---

## Part 1: Why This Lab Exists

### Step 1: Recall the Module 8 Exercise

In class, you reviewed a pre-generated Claude answer and found one subtly incorrect detail, a number, date, or name that did not match reality but read fluently enough to pass a casual glance. The lesson was not "Claude is unreliable." The lesson was that a confidently wrong answer is harder to catch than an obviously broken one, and that checking anything you plan to act on has to become a habit.

This lab extends that same skill to prompts you generate yourself, in your own conversations, without an instructor flagging the error in advance.

> **The goal is not to catch Claude making mistakes for sport.** The goal is to build a repeatable checking habit you will actually use on real work, the same way you check a number in a spreadsheet before putting it in front of a client.

### Step 2: Open a Fresh Claude.ai Conversation

Start a new chat. You will run several prompts in this lab designed to surface plausible-but-wrong details. Keep the conversation open so you can review your own work at the end.

> **Turn off Web Search before Part 2.** Open the tools menu next to the message box and confirm Web Search is off. With it on, Claude checks its own claims against a live source before answering, which is genuinely useful day to day, but it defeats this specific exercise: nearly every question in Part 2 comes back correct and cited, and you never see the failure mode the lab is built to teach. Part 2 is about what Claude says from its own training, unaided. Turn Web Search back on for Part 3 and for your normal work afterward.

---

## Part 2: Hunting for Hallucinations

### Step 3: Ask a Specific-Sounding Factual Question

Ask Claude a question that requires a precise fact you can independently verify, something with a specific number, date, or name attached. Use a topic from your own field if possible. If nothing comes to mind, try one of these:

```
What year was [a specific product, law, or event you know something about]
introduced, and what were its three main features at launch?
```

Read the response carefully. Note every specific number, date, and name Claude gives you.

### Step 4: Verify Every Specific Detail Independently

For each specific detail from Step 3, check it against an independent source. If you have Web Search available, turn it on and ask Claude to verify its own answer with citations. Otherwise, search the detail yourself using a source you trust.

Keep a running list as you go:

| Detail Claude stated | Verified against | Correct? |
|---|---|---|
| (example) "launched in 2019" | official product page | Yes |
| (example) "originally named X" | company history page | No, actual name was Y |

**Expected result:** Most details check out. At least one prompt in this lab, across the steps below, should surface a detail that is wrong, slightly off, or unverifiable. If everything checks out perfectly on the first try, continue to Step 5 and try a harder, more specific question. Precise, narrow facts are more likely to expose a gap than broad, general ones.

> **A clean result here is normal, not a sign you did something wrong.** Current Claude models, with Web Search off, are well calibrated on well-documented facts: they tend to answer correctly, or to say plainly that they are not confident, rather than confidently guessing. Do not force a verdict of "wrong" onto a detail that checks out. Move to Step 5 and Step 6, which are built specifically to find the gap this step may not.

> **Why this matters:** A wrong detail hiding among several correct ones is exactly the failure mode Module 8 taught. If your first question happens to come back fully accurate, that does not mean the habit is unnecessary. It means this particular question was not a good test of it.

### Step 5: Ask a Harder, More Obscure Question

Repeat Step 3 and Step 4 with a narrower, more obscure question, something with fewer easily indexed sources, such as a detail about a smaller company, an older event, or a niche technical specification. Narrower and more obscure topics are more likely to produce a plausible-but-wrong answer, since there is less reliable material for the model to draw on.

**Expected result:** A noticeably higher chance of catching an inaccurate detail than in Step 3. Record what you found in your table from Step 4.

> **Obscurity alone is not a reliable trigger either.** An older, narrow, well-documented fact, a specific software version's release date and feature list, for example, can still come back completely correct, because it was well covered in text the model trained on. Obscurity raises the odds; it does not guarantee a miss. If Step 5 also checks out clean, that is a real result worth recording, not a failed exercise. Step 6 is designed to succeed where Step 3 and Step 5 do not.

### Step 6: Ask a Question With a Built-In Trap

Some prompts invite a wrong answer by their own phrasing, for example by asking about something that does not actually exist, or by assuming a fact that is not true. Current Claude models tend to handle an "edition" or "criticism" style trap well: asked about a second edition that does not exist, they usually say so rather than inventing one. A trap built around a real, still-unreleased or newly rumored product tends to work better, because the question does not sound like a trap at all. Try this pattern:

```
What is the battery life of [a specific, real product's next unreleased or
newly rumored version, such as a rumored "3" or "next generation" model],
on a single charge?
```

Pick a product line with a real, well-known predecessor and a next version that is rumored but not yet officially released. Ask for a specific, ordinary spec, battery life, weight, storage capacity, rather than an opinion, since a specific number invites a specific, confident answer.

If you want to try the edition-style version instead, or in addition:

```
What was the main criticism of [a specific report, policy, or product]
in its second edition?
```

Use a real second edition if one exists, or deliberately reference something that does not have a second edition, to see how Claude responds.

**Expected result:** With the unreleased-product version, Claude often states a specific, confident spec for a product that has no officially released specs to state, without questioning whether the product exists yet. With the edition-style version, Claude may confidently describe a second edition that does not exist, or it may correctly flag that it is not aware of one. Either outcome from either version is useful, but do not be surprised if the edition-style version comes back clean. If Claude confidently invents detail about something nonexistent, that is a clear, self-produced example of the exact failure mode this lab is teaching you to catch.

> **This is the hardest trap to notice in real work.** A prompt that assumes a false premise can pull a fluent, wrong answer out of Claude, because the model is completing your sentence, not fact-checking your assumption. Read your own prompts with the same skepticism you apply to Claude's answers.

> **Switching to a smaller or faster model is not a shortcut to a wrong answer.** It is tempting to assume Haiku will hallucinate more readily than Opus, but with Web Search off, both tend to behave the same way on these two trap patterns: they answer confidently on the unreleased-product pattern, and they hedge or decline on the edition pattern. Model choice was not the lever that mattered here. Whether Web Search was on, and which pattern of trap question was asked, were.

> **A hedge is not the same as catching the trap.** On one run, Haiku declined to state a specific battery-life number for the unreleased product, saying it did not want to guess, but then stated as settled fact that the product "was released in 2024," which is itself false. The caution applied to the specific number, not to the false premise the whole question rested on. When you check Claude's answer, check the assumption underneath a confident-sounding hedge too, not only the number it declined to give.

---

## Part 3: Building a Human-in-the-Loop Validation Workflow

### Step 7: Write Your Own Validation Checklist

Based on what you found in Part 2, write a short checklist you would actually use before sending or acting on a Claude-generated answer at work. Keep it to four or five items. A starting point, to adapt in your own words:

```
Before I act on a Claude answer:
1. Does it contain a specific number, date, name, or claim I plan to use
   in a report, email, or decision?
2. If yes, can I trace that detail back to a source I trust, either a
   citation Claude provided or my own independent check?
3. Did my own prompt assume something might not be true? If so, did I
   confirm the assumption itself, not just the answer built on it?
4. Would I be comfortable if someone asked me "how do you know that" about
   this specific detail?
5. If I cannot answer item 4, either verify the detail or remove it
   before sending.
```

**Expected result:** A short, personal checklist, in your own words, that names specific trigger conditions rather than a vague reminder to "double-check things." You should be able to apply it in under a minute to a real answer.

### Step 8: Apply Your Checklist to a Real Task

Pick one of the three prompts you built in Lab 1, the email, the summary, or the meeting recap, and run it again. Apply your Step 7 checklist to the output before deciding whether you would actually send it.

**Expected result:** You can state, item by item, whether the output passes your checklist. If it does not pass on the first item you check, you know exactly which detail to verify or cut before using the output for real.

> **If Part 2 came back clean, this step will not.** The Lab 1 email prompt asks for a delivery date of "next Friday" without ever giving Claude a calendar to check it against. Across repeated runs, on more than one model, Claude picked a specific date, said so plainly, and usually asked you to confirm it, but the date it picked was not always the nearest actual Friday. Run your checklist against whatever date comes back. Item 2 (can you trace it to a source) and item 4 (could you defend it if asked) both fail on a guessed date, even when Claude sounds confident and even flags the guess itself.

---

## Part 4: Reflection

### Step 9: Answer These Questions in Your Own Notes

You do not need to submit anything. Write brief answers for yourself:

1. Which type of question, in Part 2, was most likely to produce a wrong detail: the broad question, the obscure question, or the trap question?
2. Did Web Search citations, if you used them, make verification faster, or did you still need to open the source yourself to confirm the specific claim?
3. Name one real task at work where a plausible-but-wrong detail from Claude could cause a real problem if it reached a customer or a manager unchecked.

> **Why this matters:** The specific example you write down for question 3 is the one most likely to make this habit stick. A general warning to "be careful" is easy to forget. A specific memory of your own near-miss is not.

---

## What You Built

In this lab, you:

- Deliberately hunted for plausible-but-wrong details across broad, obscure, and trap-style questions, and verified each one independently
- Saw firsthand how question specificity and topic obscurity change the odds of catching a hallucinated detail
- Wrote a personal, checklist-based human-in-the-loop validation workflow instead of relying on a vague sense of caution
- Applied that checklist to one of your own reusable prompts from Lab 1

---

## What's Next

You now have three working prompts from Lab 1 and a validation habit from this lab. Keep your checklist from Step 7 and run it the next time you reuse one of your prompts at work.

---

*Lab 2 Complete*
