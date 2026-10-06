# Lab 1: Prompt Writing Mastery

**Course:** Claude.ai Essentials
**Duration:** 30 minutes
**Format:** Instructor-led, in-class hands-on lab

---

## Prerequisites

- [ ] Modules 1 through 4 completed, including the POCC framework demo
- [ ] Your private ROI Virtual Classroom (RVC) credentials from your instructor: your RVC email address and password
- [ ] Firefox, already installed on your class VM
- [ ] The course files, which you download from the course repository in Part 1 (Git is already installed on your VM)
- [ ] No installation, no coding, and no additional software required

> **Default model:** The default model on the class account is Sonnet 5.5. Every result and callout in this lab was verified on Sonnet 5.5 directly. None of it is assumed to carry over from Opus.

---

## Part 1: Sign In to Claude.ai and Get the Course Files

Your class runs on a Linux virtual machine (VM) hosted on ROI Virtual Classroom (RVC). You use Claude.ai in Firefox on that VM and sign in with single sign-on (SSO). Your instructor gives you private RVC credentials. Do this part the first time you log in. After you sign in to Claude.ai, you download the course files with Git.

> **Using your own computer instead?** Skip this part and continue at Part 2. Sign in to Claude.ai with the class account your instructor provides.

### Step 1: Sign In to ROI Virtual Classroom

Open https://rvc.roitraining.com in a web browser and sign in with the private RVC credentials your instructor gave you. Your Linux VM launches automatically after a successful sign-in.

**Expected result:** The Linux desktop of your VM is open.

### Step 2: Open Claude.ai in Firefox

On your VM, open **Firefox** and go to claude.ai. If Firefox is not already open, select **Applications** in the top-left corner of the screen and choose **Web Browser**.

**Expected result:** The Claude.ai sign-in screen is open and asks for an email address.

### Step 3: Enter Your RVC Email Address

Enter the RVC email address that ROI provided to you. An SSO option appears: **Continue with SSO**. Select it.

**Expected result:** Firefox opens the ROILOGIN SSO sign-in portal.

### Step 4: Sign In at the ROILOGIN Portal

Enter the RVC credentials your instructor provided and press **sign in**. You can choose whether to save the password. The account expires at the end of class.

**Expected result:** You are logged in to Claude.ai. The Claude.ai home page is open and shows a message box where you can start a conversation.

### Step 5: Open a Terminal

Select **Applications** in the top-left corner of the screen, then choose **Terminal Emulator**.

**Expected result:** A Terminal window opens with a command prompt.

### Step 6: Download the Course Files with Git

Run the commands one at a time.

```
mkdir -p ~/Documents/ClaudeMasterClass
cd ~/Documents/ClaudeMasterClass
git clone --filter=blob:none --sparse https://github.com/roitraining/claude-masterclass-essentials.git .
git sparse-checkout set course-1-claude-ai-essentials
ls
```

The first command creates a folder named `ClaudeMasterClass` inside your Documents folder. The second moves you into it. The third starts the download into that folder, and the dot at the end tells Git to use the current folder. The `--sparse` option makes Git fetch only the top-level files at first. The fourth command tells Git to download only the `course-1-claude-ai-essentials` folder, which holds the files for Claude.ai Essentials. You do not download the files for any other class. The last command lists what you downloaded.

**Expected result:** The `ls` command lists `README.md` and the `course-1-claude-ai-essentials` folder. That folder has a `labs` folder and a `demos` folder. If Git asks you to sign in, use the access details your instructor gives you.

> **Already downloaded the course files in an earlier lab?** Run `cd ~/Documents/ClaudeMasterClass` and then `git pull` to get the latest files. Do not clone a second time.

---

## Part 2: Before You Start

### Step 7: Recall the POCC Framework

Module 4 introduced POCC as a repeatable structure for a clear prompt:

- **Persona:** Who should Claude act as? Use this when tone or expertise matters. Skip it when the task is simple enough that a persona adds nothing.
- **Objective:** What is the specific goal of this prompt?
- **Context:** What background does Claude need to get this right?
- **Constraints:** What limits apply? Length, tone, format, what to avoid.

You will apply POCC to three real office scenarios: an email, a summary, and a meeting recap.

> **POCC is a checklist for gaps, not a script to recite.** Not every prompt needs all four elements spelled out in full sentences. The value of POCC is that it gives you a place to look when a response comes back generic or off-target: which of the four is missing?

### Step 8: Open a Fresh Claude.ai Conversation

You are already signed in to Claude.ai from Part 1. Start a new chat. Keep this conversation open for the entire lab. You will build all three tasks in it, one after another, so you can scroll back and compare outputs later.

**Expected result:** An empty Claude.ai chat window, ready for your first prompt.

> **Claude.ai now formats many replies as interactive cards, not plain text.** An email or a recap often renders inside its own card with a subject line and Copy or Open in Mail buttons, and a first, vague request sometimes comes back as two selectable options instead of one answer. This is normal. Read the card's content the same way you would read plain text, and compare content and structure between drafts, not the container it arrives in.

> **A "Recalled memory" note may appear above the very first response, even in a brand new chat.** Claude.ai's memory feature can pull in something from an earlier, unrelated conversation on this account. It does not affect this lab's exercise. If a recalled detail looks distracting on a shared or instructor screen, clear or pause memory in Settings before class.

---

## Part 3: Task 1, The Email

### Step 9: Write and Run a First-Draft Email Prompt

Without thinking about POCC yet, type a single, vague sentence describing an email you actually need to write. Use a real scenario from your own job if you can. If nothing comes to mind, use this stand-in scenario:

```
Write an email to a client about a delayed shipment.
```

Run it. Read the entire response.

**Expected result:** A generic email. It will likely be polite and grammatically correct, but vague: no specific delay reason, no specific date, no specific tone matched to your actual relationship with this client. You would need to fill in bracketed placeholders, or edit it heavily, before sending it.

> **A well-organized generic draft is still a generic draft.** Current Claude models write cleanly even from a one-line prompt, so this first email may already read as competent, even polished. Judge it on specifics, not polish: does it name an actual reason for the delay, an actual date, or anything about this particular client? A vague prompt cannot produce those details, no matter how well the sentences are written.

### Step 10: Rebuild the Same Email Using POCC

Now write a structured version of the same request. Fill in each POCC element with real specifics from your own situation. If you are using the stand-in scenario, a structured version looks like this:

```
Persona: You are a customer account manager writing to a long-term client.

Objective: Write a short email informing the client that their order
(order #48291, three industrial sensors) will arrive five business days
later than the original delivery date, and explain why without sounding
defensive.

Context: The delay is caused by a supplier shortage, not anything the
client did. This client has ordered from us for three years and values a
direct, no-excuses tone. The new expected delivery date is next Friday.

Constraints: Under 150 words. Professional but warm tone. Include the new
delivery date explicitly. Do not use the word "unfortunately" more than
once. End with a direct offer to answer questions.
```

Run it. Read the entire response.

**Expected result:** An email that states the new delivery date, explains the delay in one or two sentences without sounding evasive, matches a warm but professional tone, and stays under the word limit. You should be able to send this with little or no editing.

> **Watch what Claude does with "next Friday."** This prompt deliberately never gives an exact calendar date, only "next Friday." Across repeated tests, on Opus, Sonnet 5.5, and again on Sonnet 5.5, Claude consistently resolved this to the Friday nine days out rather than the nearest upcoming Friday, and usually flagged the guess itself, asking you to confirm the date. Do not silently accept whatever date lands in the draft. Check it against an actual calendar before you treat this as ready to send. This is a real, repeatable example of exactly the habit Lab 2 is built to teach, and it comes from this lab's own stand-in prompt, not a contrived trap.

### Step 11: Compare the Two Outputs

Scroll back and read both email drafts side by side.

Ask yourself:

- Does the structured version include information the vague version could not have included, because you never gave Claude that information?
- Would you send the vague version to a real client without editing it? Would you send the structured version?
- Which POCC element made the biggest difference for this particular task?

> **Key insight:** The quality gap between your two email drafts is not about Claude getting smarter between prompts. It is entirely explained by the information and constraints you supplied the second time. This is the same lesson from the Module 4 demo, now applied to your own scenario instead of the instructor's.

---

## Part 4: Task 2, The Summary

### Step 12: Choose a Document to Summarize

Pick a real document you have on hand: a report, an article, meeting notes, or a policy document. If you do not have one ready, use the sample document `lakeside-q3-operations-update.txt`. You downloaded it in Part 1. It is in `~/Documents/ClaudeMasterClass/course-1-claude-ai-essentials/labs/lab-files`. Open it in **Mousepad** (**Applications**, **Accessories**, **Mousepad**, then **File**, **Open**), select all of the text, and copy it.

Paste the text into a new message in your conversation, or upload the file as a document.

### Step 13: Write and Run a First-Draft Summary Prompt

Type a single vague sentence:

```
Summarize this.
```

Run it.

**Expected result:** A summary that is technically accurate but generic in focus. It may already read as reasonably well organized, since current Claude models tend to structure even a one-line request into clear paragraphs. Look past the organization and check the actual focus: it follows the source document's own order and priorities, not yours, because Claude had no way to know what you actually needed the summary for.

### Step 14: Rebuild the Summary Prompt Using POCC

Write a structured version that specifies what the summary is for and who will read it. For example:

```
Persona: You are a research assistant preparing a briefing for a busy
executive who has not read the source document.

Objective: Summarize the document above in a way this executive can read
in under a minute and act on immediately.

Context: The executive cares about decisions and numbers, not background
or methodology. They will use this summary to decide whether to approve
a related budget request this week.

Constraints: Five bullet points maximum. Each bullet under 20 words. Lead
with the single most important takeaway. No jargon.
```

Run it.

**Expected result:** A tightly scoped summary, five bullets or fewer, that leads with the most decision-relevant point rather than the first point made in the source document. Compare this against Step 13's output. The structured version should be usable as-is in a real briefing.

### Step 15: Compare the Two Summaries

Look at both summaries and note what changed. Did specifying the audience change which details got included? Did the length constraint force a genuinely better prioritization, rather than just a shorter version of the same content?

---

## Part 5: Task 3, The Meeting Recap

### Step 16: Gather Rough Meeting Notes

Use real rough notes from a recent meeting if you have them. Rough, unpolished notes work best for this exercise, since that is the realistic starting point. If you do not have real notes, use this stand-in:

```
notes from standup - q3 planning
- mike: backend api delayed, needs 2 more weeks, waiting on vendor contract
- sara: design mockups done, in review with legal
- budget question raised, nobody had the number, follow up needed
- launch date still sept 30 per leadership, team thinks that's tight
- action items unclear, need to assign owners
```

Paste these notes into your conversation.

### Step 17: Write and Run a First-Draft Recap Prompt

Type a single vague sentence:

```
Turn this into a recap.
```

Run it.

**Expected result:** A recap that restates the notes in fuller sentences but does not clearly separate decisions from open questions, and may not surface action items as its own distinct section, since you never asked for that structure.

> **If today's date happens to match a date in your notes, Claude may comment on it directly.** The stand-in notes above name a launch date of September 30. Running this lab on that actual date can prompt Claude to flag the coincidence on its own, unprompted. This is a harmless side effect of Claude having access to the current date, not a lab error, and it can work as a live example of how specific and situationally aware a response can get even from a vague prompt.

### Step 18: Rebuild the Recap Prompt Using POCC

Write a structured version that specifies the recap's audience and required structure. For example:

```
Persona: You are a project coordinator writing a recap for team members
who missed the meeting.

Objective: Turn these rough standup notes into a clean recap that
separates what was decided from what is still open.

Context: This is a Q3 planning standup. The launch date is a firm
commitment from leadership. The budget question and action item owners
are unresolved and need follow-up before the next standup.

Constraints: Three sections: Decisions, Open Questions, Action Items.
Under 150 words total. Plain language, no meeting jargon.
```

Run it.

**Expected result:** A recap with three clear sections. Decisions should list the launch date as a firm commitment. Open Questions should include the budget number and the tight timeline concern. Action Items should either list specific owners, if the notes gave you any, or flag explicitly that owners still need to be assigned. This structure should be usable to send to the team without rewriting.

### Step 19: Compare the Two Recaps

Note whether the structured version actually separated decisions from open items, and whether a teammate who missed the meeting could act on the recap without asking follow-up questions.

---

## Part 6: Checkpoint

### Step 20: Confirm What You Built

Before moving on, check that you have all three of the following in your conversation, scrollable and ready to reuse:

- [ ] A structured POCC prompt for a work email, and a response you would send with little or no editing
- [ ] A structured POCC prompt for a document summary, and a response scoped to a specific audience and use
- [ ] A structured POCC prompt for a meeting recap, and a response that separates decisions from open items

If any of the three still reads as generic, go back and check which POCC element is thin. A generic result almost always traces back to missing Context or missing Constraints, not a failure of the framework itself.

**Expected result:** Three working prompts you would actually reuse on a real task this week, each built from a scenario close to your own job.

> **Save your prompts.** Claude.ai has no built-in feature for saving a prompt as a permanent template. Copy your three finished POCC prompts into your own notes now, before you close this conversation. If you have a Pro account and expect to repeat one of these tasks regularly, consider setting the winning prompt as standing instructions inside a Project instead.

---

## What You Built

In 30 minutes, you:

- Drafted a vague, single-sentence prompt and a fully structured POCC prompt for the same task, three times, across an email, a summary, and a meeting recap
- Compared first-draft output against refined output for each task and identified which POCC element drove the improvement
- Left with three working, reusable prompts built around your own real office scenarios, not the instructor's examples

---

## What's Next

This lab covered a single conversation at a time. Lab 2, Fact-Checking and Grounding AI Output, also runs in class. It picks up where Module 8's group exercise leaves off: spotting a plausible-but-wrong answer on your own, without an instructor pointing it out. You will reuse one of the prompts you built here.

---

*Lab 1 Complete*
