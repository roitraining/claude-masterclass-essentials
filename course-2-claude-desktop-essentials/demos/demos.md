# Claude Desktop Essentials: Demos

**Course:** Claude Desktop Essentials (Course 2 of 4, Claude MasterClass Essentials)
**Contents:** Nine demos. Demos 1 to 6 are the core demos. Demos 7 to 9 are financial services demos.

---

## About this guide

This file covers nine follow-along demos for Claude Desktop. Work through them in order, Demo 1 to Demo 9. Demos 7 to 9 sit under the "Financial Services Demos" heading and build on earlier demos.

Each demo has the same layout: a slide reference and a supports line, a Files line when the demo uses files, a short context paragraph, numbered steps, an Expected result, and a Why this matters note. Windows and Mac notes follow the steps where those platforms differ.

The files live next to this guide:

- `demo-files` holds `expense-sample.csv`, `budget-notes.txt`, and `messy-contact-list.csv`. All three are fictional.
- `fin-demo-files` holds the financial services files used in Demos 7 to 9.

Both folders are in `~/Documents/ClaudeMasterClass/course-2-claude-desktop-essentials/demos` after you download the course files in Lab 1, Part 1.

> **Linux first, then Windows, then Mac.** Each demo gives the Linux steps first. Where Windows or Mac differ, a short note follows. Claude Desktop on Linux is a beta. Voice dictation and computer use are not available on Linux.

---

## Prerequisites

- [ ] Claude Desktop installed and signed in on a Linux VM (the class VM, which uses the Xfce desktop)
- [ ] A keyboard shortcut bound to `Ctrl+Alt+C` that runs `claude-desktop`, created and tested (the same steps as Lab 1, Step 23)
- [ ] A second application open and visible for Demo 1 (Mousepad, or a spreadsheet application if the VM has one)
- [ ] `messy-contact-list.csv` from the `demo-files` folder, ready to open as the screenshot target for Demo 2
- [ ] The `demo-files` folder from the course files in `~/Documents/ClaudeMasterClass/course-2-claude-desktop-essentials/demos`, holding `expense-sample.csv`, `budget-notes.txt`, and `messy-contact-list.csv`
- [ ] The Filesystem Desktop Extension available to install in Demo 5
- [ ] A web browser on the VM for the cross-device sync check in Demo 3

> Test each demo on the actual VM before you rely on it. A shortcut that collides with another shortcut, or an extension install that stalls, costs more time than any other problem in this guide.

---

## Demo 1: The Shortcut Icebreaker

**Slide reference:** Slide 6. **Learning objective tie-in:** reaching Claude from any application without hunting for a window or a browser tab.

### Context

This demo shows the shortcut before it is explained. Stay in your own work, press one key combination, and have Claude in front of you. Notice how little effort it takes compared with finding a browser tab.

### Steps

1. Open Mousepad or a spreadsheet application and stay mid-task in it. Do not have Claude Desktop visible.
2. Keep working in that application for a few seconds.
3. Without using the mouse or the applications menu, press `Ctrl+Alt+C`.
4. When Claude comes to the front, type a playful, low-stakes request, such as: "Write a two-line limerick roasting Monday mornings."
5. Press Enter and let Claude answer.
6. Switch back to the first application. Take note that you never went looking for Claude, never opened a browser tab, and used one keystroke.

**Files:** none.

**Expected result:** Claude comes to the front within a second of the keystroke and returns a short, playful answer. No browser opens and no menu is used.

> **Windows:** Use the shortcut key you set in the Claude shortcut's Properties, `Ctrl+Alt+C`. The result matches the Linux version.

> **Mac:** Double-tap the Option key to open Quick Entry, a small floating window that appears on top of your other application. The other application keeps focus. Change the gesture in Settings > General if it collides with another shortcut.

> **Why this matters:** Every later step in this course, the custom shortcut, Desktop Extensions, and the labs, exists to remove the friction this demo makes visible: alt-tabbing to a browser, finding the right tab, and pasting context back and forth.

> **Nothing happened?** Another shortcut may already use `Ctrl+Alt+C`. Open the keyboard settings, look for a conflict, and choose a different combination.

---

## Demo 2: Screenshot Roast

**Slide reference:** Slide 15. **Learning objective tie-in:** first hands-on use of screenshot sharing.

### Context

Run this right after Demo 1, or on its own. A screenshot works here before the feature has a formal name.

### Steps

1. Open `messy-contact-list.csv` from the `demo-files` folder in Mousepad, or in a spreadsheet application if the VM has one. It is intentionally messy fake data.
2. Press the Print Screen key. The Xfce screenshot tool opens. Choose the active window or a region of the screen, then save the screenshot or copy it to the clipboard. `Alt+Print` captures the active window and `Shift+Print` captures a region.
3. In a Claude conversation, attach the screenshot with the attach button, or paste it into the message box.
4. Ask a playful, low-stakes question about it, such as: "Roast my spreadsheet in one sentence."
5. Read Claude's response. Look for details from your screenshot in the answer.

**Files:** `messy-contact-list.csv`, in the `demo-files` folder.

**Expected result:** Claude responds with a short, specific comment that clearly reacts to details visible in the screenshot, for example naming an actual column or a specific odd value. This shows it saw the real content rather than guessing generically.

> **Windows:** Press `Windows+Shift+S`, drag to select the area, and paste the result into the message box with `Ctrl+V`.

> **Mac:** Press `Command+Shift+4` and drag to select the area. The screenshot saves to the Desktop. Attach it with the attach button, or drag it into the message box.

> **Why this matters:** Describing a messy spreadsheet in words takes longer and loses precision. Showing it is faster and more accurate. The screenshot tool belongs to the operating system, so this works the same way for any application on screen.

---

## Demo 3: Guided Tour, Shortcut, Sessions and Sync

**Slide reference:** Slides 11 to 15. **Learning objective tie-in:** four things Claude Desktop can do that a browser tab cannot match: a system-wide shortcut, multiple sessions, cross-device sync, and screenshot sharing.

### Context

This demo is one continuous tour of four features. Work through the steps in order.

### Steps

1. **The shortcut in depth.** Open the Application Shortcuts tab: Applications, Settings, Keyboard, Application Shortcuts. Find the `claude-desktop` entry. Take note that a shortcut is a command and a key combination. This one runs the Claude Desktop command, and you choose the combination so it does not collide with one you already use. Press it from another application once more.
2. **Multiple sessions.** Open a second, unrelated chat session inside Claude Desktop alongside the first. Ask a question in the first session, switch to the second, ask an unrelated question, then switch back to the first session. Check that its context is still intact.
3. **Cross-device sync.** In the VM's web browser, open claude.ai and start a new conversation. Type one message in the browser.
4. Switch to Claude Desktop and open that same conversation. Check that the message you sent from the browser is already visible there.
5. Continue the conversation from inside Claude Desktop. Check that the reply appears normally, as if the whole exchange had happened on one device.
6. **Screenshot sharing.** Repeat the mechanic from Demo 2 briefly. Capture a screenshot of anything on screen, attach it, and ask Claude what it sees.

**Files:** none.

**Expected result:** You see, in order: a custom shortcut bring Claude forward from inside another application, two independent chat sessions holding separate context at the same time, and the identical conversation history appearing in both the browser and the desktop app without any manual export or import step.

> **Windows:** Open the Shortcut key box on the Claude shortcut's Properties, then press the combination. **Mac:** Double-tap Option to open Quick Entry, and find the Quick Entry shortcut setting in Settings > General.

> **Why cross-device sync matters:** Every conversation and every Project appears the same way in the browser and on the desktop. That makes it safe to start a task on one device and finish it on another.

---

## Demo 4: Drag a File Into the Conversation

**Slide reference:** Slide 16. **Learning objective tie-in:** one more desktop input method, and a contrast with Demo 5, where no file is dragged at all.

### Context

Voice dictation is not available on Linux, so this demo uses drag and drop instead. Complete this demo before Demo 5. Demo 5 makes more sense after you have done the manual path.

### Steps

1. Open **File Manager** and go to the `demo-files` folder in `Documents/ClaudeMasterClass/course-2-claude-desktop-essentials/demos`. Find `expense-sample.csv`. Place the File Manager window and the Claude window side by side.
2. In Claude, start a new conversation.
3. Drag `expense-sample.csv` from Files into the Claude message box. Check that the file is attached to the message.
4. Type: "Which three expenses are the largest, and what do they add up to?" and send it.
5. Read Claude's answer. Open the file and check the three amounts and the total yourself.
6. Take note that the file went into this one conversation only. To use it again tomorrow, you would drag it in again.

**Files:** `expense-sample.csv`, in the `demo-files` folder of the course files on the VM.

**Expected result:** Claude names the three largest expenses, $1,240.00 to Northline Travel, $865.40 to Northline Travel, and $399.00 to Brightwave Software, and gives a total of $2,504.40.

> **Windows and Mac:** The steps are the same. Drag the file from File Explorer (Windows) or Finder (Mac) into the message box.

> **Mac only, optional:** On a Mac running macOS 14 or later, voice dictation is a second desktop input method. Dictation has to be turned on in Claude's settings first, and it uses the Caps Lock key. It is a Mac-only feature, so it does not work on Linux or Windows.

> **Why this matters:** Claude can be wrong about a sum. A thirty-second check against the file is cheaper than a wrong figure in a report. Make the check a habit.

---

## Demo 5: Install a Local Extension, Then Ask a Question Against a Local File

**Slide reference:** Slides 20 and 21. **Learning objective tie-in:** installing and configuring a Desktop Extension to connect Claude to local files.

### Context

This demo sets up both labs. Read every permission prompt as it appears. Grant only the `demo-files` folder, the same single-folder habit you practice in Lab 1.

### Steps

1. Open Settings > Extensions inside Claude Desktop and choose Browse extensions.
2. Find the Filesystem extension in the directory and open its detail page.
3. Click install. As each permission prompt appears, stop and read it before clicking through. Work out exactly what the prompt asks to access and why the extension needs that access.
4. When Claude asks which directory the extension may use, select only the `demo-files` folder: `/home/<your username>/Documents/ClaudeMasterClass/course-2-claude-desktop-essentials/demos/demo-files` on the VM. Do not select Documents, ClaudeMasterClass, or your home folder.
5. Complete the install and confirm the extension shows as active in Settings > Extensions.
6. Open a new Claude Desktop conversation.
7. Ask a question that needs the extension to read a local file, without attaching anything: "What does budget-notes.txt in my demo-files folder say about Q3 spending?"
8. Look at the response. Take note that no file was dragged, pasted, or uploaded. Claude reached the content directly through the extension.
9. Compare this with Demo 4. In Demo 4 you dragged a file into the conversation. Here you dragged nothing. The answer is the same kind, and the path to it is different.

**Files:** `budget-notes.txt`, in the `demo-files` folder of the course files on the VM.

**Expected result:** The extension installs and shows as active with no errors. Claude's answer states that total Q3 spend was $88,000, with marketing at $42,500, travel at $18,200, and software licenses at $27,300, and it may mention the travel overage. This confirms it read the live file rather than guessing.

> **Windows:** The folder path is `C:\Users\<your username>\Documents\ClaudeMasterClass\course-2-claude-desktop-essentials\demos\demo-files`. **Mac:** The folder path is `/Users/<your username>/Documents/ClaudeMasterClass/course-2-claude-desktop-essentials/demos/demo-files`. Calendar extensions in the directory vary by platform, so use the Filesystem extension for this demo on every platform.

> **Why read every permission prompt:** Clicking through prompts quickly builds a habit that is risky later. Reading what each prompt grants, every time, is the main lesson of this demo. The access a local extension can request is broader than a single file upload.

> **Install stalls or fails?** Try these fallbacks: use a staged copy of the extension on the VM, follow a recorded install walkthrough if one is available, or pair with a neighbor whose install succeeded.

---

## Demo 6: Review Before You Install

**Slide reference:** Slide 27. **Learning objective tie-in:** comparing the data-access risk profile of local extensions to web uploads, and applying the right guardrails.

### Context

Demo 5 installed smoothly. That can suggest a wrong assumption: if it installed easily, it must be safe by default. This demo walks through what to check before you click install, using the extension's own detail page.

A web upload sends one file's content into one conversation. A local extension can potentially see an entire folder or system. That difference is the reason for the review.

### Steps

1. Open the Extensions directory again and click into the detail page of an extension. Do not install it yet.
2. Find the permissions list on the detail page and read it. Describe in plain terms what the extension asks to see and do, as you would to a colleague.
3. Find the code-signing indicator on the detail page. A verified publisher indicator means the extension's publisher identity has been confirmed, similar to a verified signature on a downloaded application.
4. Look for what the page says about local credentials. If an extension needs you to sign in to a calendar or file service, the documented position is that the credential stays on your device and is never sent to or stored by Anthropic. Treat this as a documented fact to confirm against the source, not a general reassurance.
5. After all three checks, either install the extension to see the full flow, or choose not to install it. Write down your reasoning either way.
6. Discuss with your group or a partner: what would make you decline an install, and why does a broader permission need closer review?

**Files:** none.

**Expected result:** You can point to a specific permissions list, a specific code-signing indicator, and a specific statement about local credential handling on the extension's own detail page. You can explain in your own words what each one tells you before you click install.

> **Nothing runs unless invoked.** An installed extension never acts on its own. It responds only when a conversation calls on it. Nothing happens without a prompt.

> **Why this matters:** A smooth install says nothing about safety. The three checks, permissions, publisher identity, and credential handling, give you a reason for each decision.

---

# Financial Services Demos

These three demos repeat skills the course already teaches, using fictional financial services material. They suit work in banking, lending, and wealth management. Each one follows the demo it supports.

Every person, company, account, and figure in the files is fictional. The policy and thresholds are invented teaching examples, not legal or compliance advice. Have a compliance team review the wording before using these demos with a client's staff.

The files are in the `fin-demo-files` folder next to this guide, in the course files on the VM. Add it to the Filesystem extension's allowed directories, the same list you read in Lab 2, Step 1. Add this folder and no other. If Demo 5 left `demo-files` in the list, you can leave it there.

## Demo 7: Reconcile Two Ledgers

**Supports:** The Desktop Extensions module. Do it after Demo 5.

**Files:** `bank-statement-2026-09.csv` and `general-ledger-2026-09.csv`, both in the `fin-demo-files` folder. Both show September 2026 for a fictional company, Harborview Supply Co. In both files a negative amount is a payment out and a positive amount is money in.

**Context:** Demo 5 showed Claude reading a file with no upload. This demo gives it a real finance task, comparing a bank statement to a company's ledger, and then asks it to write the result to a file. That shows the second kind of permission, creating a file, which differs from reading one.

**Steps:**

1. Open both files in Mousepad, one beside the other. The bank statement has 16 lines of transactions and the ledger has 17. Someone does this comparison by hand every month.
2. In Claude, start a new conversation so the extension's tools load. Type: "Compare bank-statement-2026-09.csv and general-ledger-2026-09.csv in my fin-demo-files folder. List every transaction that appears in one but not the other, and every pair where the amounts differ. Do not change any file yet."
3. When Claude asks permission to use a tool, read the prompt, confirm it points at `fin-demo-files`, and allow it.
4. Read Claude's list. Check it against the six expected differences below.
5. Type: "Write these exceptions to a file named exceptions.md in the same folder. Give each one a line and a suggested next step."
6. Read this permission prompt before you allow it. Take note that this one asks to create a file.
7. Confirm the file yourself. On the Linux VM, open a terminal and run `cat ~/Documents/ClaudeMasterClass/course-2-claude-desktop-essentials/demos/fin-demo-files/exceptions.md`.
8. Optional: ask, "After accounting for these items, what should the true cash balance be?" Work the arithmetic yourself before you read Claude's answer.

**Expected result:** Claude finds all six differences.

| # | Item | What the files show |
|---|---|---|
| 1 | Freight Northline Freight, September 12 | The bank shows -4,560.00 and the ledger shows -4,650.00. The difference is 90.00 and looks like transposed digits. |
| 2 | Invoice 10388 Brightwave, September 19 | The ledger records -812.40 twice. The bank shows it once. |
| 3 | Check 4471 Delta Packaging, September 26 | The ledger shows -1,250.00. The bank has no matching item. This is an outstanding check. |
| 4 | Customer payment Corbel Retail, September 30 | The ledger shows +9,800.00. The bank has no matching item. This is a deposit in transit. |
| 5 | Monthly service fee, September 30 | The bank shows -35.00. The ledger has no matching item. |
| 6 | Interest earned, September 30 | The bank shows +12.38. The ledger has no matching item. |

The file `exceptions.md` is created in the folder with one line per exception. For the optional question, both sides reconcile to 21,415.70. The bank closes at 12,865.70, so add the 9,800.00 deposit in transit and subtract the 1,250.00 outstanding check. The ledger closes at 20,535.92, so add 90.00 for the transposition, add 812.40 for the duplicate, subtract 35.00 for the fee, and add 12.38 for the interest. Both opening balances are 42,000.00.

> **On the 90.00 difference, check who is right.** Claude cannot know from two files whether the bank or the ledger holds the correct figure. A good answer flags the difference and says the vendor invoice settles it. Treating the bank as correct is a reasonable working assumption if Claude states it.

> **Windows:** Check the new file by opening the folder in File Explorer and opening `exceptions.md`. **Mac:** Use the terminal command from step 7 or open the file in Finder.

> **Why this matters:** Reconciliation is routine, repetitive, and easy to get subtly wrong, which makes it a good first task for Claude and a task that still needs a person. You have the answer key, so nobody has to take Claude's word for it.

---

## Demo 8: The Approval Threshold Lookup

**Supports:** The course's core idea, reaching Claude without leaving your work, together with the fact-checking habit. Do it after Demo 7.

**Files:** `wire-approval-policy.md`, in the `fin-demo-files` folder. It is a fictional wire approval policy for Harborview Supply Co. with numbered sections.

**Context:** Checking an approval limit is the kind of small interruption that costs a minute many times a day. This demo uses the keyboard shortcut and the extension together, then asks a question the policy cannot answer.

**Steps:**

1. Open Mousepad and start typing a short email to a vendor. Stay mid-task.
2. Press `Ctrl+Alt+C` to bring Claude forward. Start a new conversation.
3. Type: "Using wire-approval-policy.md in my fin-demo-files folder, can I approve a $48,000 wire to an existing vendor by myself? Quote the section you rely on."
4. Read the answer. Open the policy and check the section Claude quoted.
5. Type: "What changes if the beneficiary is new?" Check the answer against Section 3.
6. Type: "What if the wire is exactly $50,000?" Check the answer against Section 2.
7. Type the trap question: "What is the process for recalling a wire after it has been released?"
8. Read the answer. Open the policy and search it for the word "recall". Take note that nothing is found.
9. Return to the email with the shortcut or the mouse. You asked a policy question without losing your place.

**Expected result:** For the first question, Claude says no. Section 2.2 requires two approvers for a wire of $10,000 up to and including $49,999.99, and at least one approver must be a Finance Manager or above. For a new beneficiary, Claude cites Section 3: a call-back to a phone number already on file is required at every amount, in addition to the approvals in Section 2. For exactly $50,000, Claude applies Section 2.3, which needs two approvers and the CFO's written approval. For the trap question, a good answer says the policy does not address recalling a wire.

> **Watch the boundary.** $49,999.99 and $50,000 fall under different rules. An answer that blurs them is a real error, and the quoted section is how you catch it. Always ask Claude to quote the section.

> **Windows:** Press the shortcut key you set on the Claude shortcut's Properties instead of `Ctrl+Alt+C`. **Mac:** Double-tap Option to open Quick Entry instead.

> **Why this matters:** A quoted section turns a claim into something you can check in ten seconds. A made-up section number is the failure to watch for when a policy is silent. The people who own the real policy, not Claude, decide how it applies.

---

## Demo 9: Read the Dashboard, Then Check It

**Supports:** Screenshot sharing. Do it after Demo 3, or after Demo 2 if you have only done Demo 2.

**Files:** `portfolio-dashboard.png` and `portfolio-data.csv`, both in the `fin-demo-files` folder. The dashboard shows a fictional portfolio, Cedar Ridge Balanced Portfolio, and it contains one planted error.

**Context:** Demo 2 showed Claude reacting to what is on screen. This demo adds a check. The dashboard's headline total does not match its own rows. The question is whether you, and Claude, notice.

**Steps:**

1. Open `portfolio-dashboard.png` in **Ristretto Image Viewer** (**Applications**, **Graphics**, **Ristretto Image Viewer**) at full size.
2. Press Print Screen, capture the window, and attach the screenshot in Claude, the same way as in Demo 2.
3. Ask: "Summarize this dashboard in three sentences for a client meeting." Read the answer.
4. Ask: "Check the numbers on this dashboard against each other. Does anything not add up?"
5. If Claude does not flag the total, ask: "Add up the six market values and compare the sum to the total market value."
6. Open `portfolio-data.csv` and look at the TOTAL row.
7. Optional: ask, "Is the YTD return consistent with the six holdings?"

**Expected result:** The summary describes the allocation and returns accurately. The six market values add up to $2,428,000, but the banner at the bottom reads $2,482,000, a difference of $54,000 that looks like transposed digits. The percentages add up to 100.0 percent. `portfolio-data.csv` shows the correct total of $2,428,000. For the optional question, a market-value-weighted YTD return from the six rows is about 4.3 percent, which matches the dashboard.

> **Claude may not volunteer the flaw.** Reading a picture and checking a picture are different requests. The summary in step 3 is usually fluent and correct, and the problem appears when you ask for a check. If Claude gets the arithmetic wrong in the optional question, add the numbers yourself and compare.

> **Windows:** Press `Windows+Shift+S`, drag to select the dashboard, and paste into the message box with `Ctrl+V`. **Mac:** Press `Command+Shift+4`, drag to select the dashboard, and attach the file saved to the Desktop.

> **Why this matters:** A wrong total on a client dashboard is a real finance error, and an AI summary will repeat it politely. The habit is to check any number you will repeat against the data behind it, whether a person or a model produced it.

---

*End of Demos: Claude Desktop Essentials*
