# Claude MasterClass Essentials

Welcome to Claude MasterClass Essentials! This repo contains the lab guides and the files you use for two classes: Claude.ai Essentials and Claude Desktop Essentials.

**Last Update: 6 Oct 2026**

## Labs

### [Claude.ai Essentials, Lab 1: Prompt Writing Mastery](course-1-claude-ai-essentials/labs/lab-1-prompt-writing-mastery.md) (30 minutes)

Sign in to Claude.ai in Firefox on your class virtual machine, download the course files with Git, and then turn three vague, one-sentence requests into structured prompts using the POCC framework: Persona, Objective, Context, and Constraints. The three tasks are an email, a document summary, and a meeting recap. For each one you run the vague version first, rebuild it with POCC, and compare the two outputs side by side. You leave with three reusable prompts built around office scenarios. Skills practiced: writing structured prompts, spotting which POCC element is missing when a response comes back generic, and judging a first draft against a refined one.

### [Claude.ai Essentials, Lab 2: Fact-Checking and Grounding AI Output](course-1-claude-ai-essentials/labs/lab-2-fact-checking-and-grounding-ai-output.md) (30 to 40 minutes)

Deliberately try to catch Claude giving a plausible but wrong answer. With Web Search off, you ask a specific-sounding factual question, a harder and more obscure one, and a question built on a false premise, and you verify every detail against an independent source. You then write your own validation checklist and apply it to one of your Lab 1 prompts. Skills practiced: noticing how question specificity and topic obscurity change the odds of a made-up detail, checking confident answers against real sources, and building a human-in-the-loop habit instead of relying on a vague sense of caution.

### [Claude Desktop Essentials, Lab 1: Ask Your Files with the Filesystem Extension](course-2-claude-desktop-essentials/labs/lab-1-ask-your-files-with-the-filesystem-extension.md) (70 minutes)

Sign in to Claude for Linux with single sign-on, download the course files with Git, and confirm that Claude Desktop cannot see your files until you give it access. You then install the Filesystem extension and grant it a single folder. You ask Claude to list, summarize, compare, and correct four local files without uploading any of them, and to create a new file that you check yourself. You finish by building a keyboard shortcut that brings Claude forward from any application. Skills practiced: granting the narrowest folder access that works, reading permission prompts before approving them, and verifying the files Claude creates.

### [Claude Desktop Essentials, Lab 2: Permissions and Safety](course-2-claude-desktop-essentials/labs/lab-2-permissions-and-safety.md) (60 minutes)

Test the edges of what you granted. You ask about a file outside the allowed folder, then grant a second folder and have Claude read a vendor email that contains instructions aimed at an AI assistant. You temporarily widen the grant to see how a sensitive file comes within reach, then remove it, and you set the tools that change files to ask for approval first. You compare the extension with a web upload and write a five-line guardrails checklist. Skills practiced: reading what Claude does with untrusted text, understanding what a wide folder grant exposes, and controlling which actions Claude may take on its own.

---

*Materials prepared for ROI Training delivery.*
