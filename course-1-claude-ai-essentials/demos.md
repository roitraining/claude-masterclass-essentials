# Course 1 Demos: Claude.ai Essentials

**Course:** Claude.ai Essentials, Everyday Office Work, Solved
**Format:** Follow-along demos

---

## How to Use This File

This file covers the 15 demos in Course 1, in the order they appear in the deck. Demos 1 to 11 are general office demos. Demos 12 to 15 apply the same skills to fictional financial services material.

Each demo is laid out the same way:

- **Supports:** the module and learning objective the demo belongs to.
- **Files:** the exact file or files to use, if the demo needs any.
- **Context:** why the demo is in the course.
- **Steps:** what to do, in order.
- **Expected result:** what a correct outcome looks like.

Many steps include a prompt to type into Claude. Type each one exactly as shown, inside the quotation marks.

The demo files are in the `demo-files` folder next to this guide. After you download the course files in Lab 1, both are in `~/Documents/course-1-claude-ai-essentials`. Every person, company, account, and figure in them is fictional.

Some demos continue from an earlier one. Where that is true, the demo says so. Claude can produce different wording each time, so your results may differ in detail from the descriptions here. Check them against the Expected result.

---

## Demo 1: The Claude.ai Interface Tour

**Supports:** Module 3, navigating the Claude.ai interface confidently, including chat history, file uploads, Web Search, Memory, Connectors, and Projects.

**Files:** `demo-files/lakeside-returns-policy.pdf`

**Context:** This demo covers the whole interface once, as one continuous session. Every later module assumes you have seen this tour. Work through it in order.

**Steps:**

1. Open a fresh Claude.ai session. Take note of the sidebar: the list of saved chat history, the button to start a new chat, and the location of the privacy toggle.
2. Open a past conversation from the sidebar. Every conversation is saved and can be resumed. Return to a new chat.
3. Attach `lakeside-returns-policy.pdf` to the conversation. Ask: "How long do I have to return a tent, and is there a fee?" Then ask: "Which items cannot be returned?" Take note that the file stays attached to this specific conversation.
4. Turn on Web Search from the tools menu next to the message box. Ask a question that needs current information, such as a recent news item. Take note of the citations Claude returns alongside the answer.
5. Open Settings, then Connectors. Look at what a Google Workspace or Slack connector looks like from the user's side. You do not need to configure one.
6. Open a Project. Look at its separate file list and its standing instructions panel. Think about why a recurring task belongs in a Project instead of a one-off chat.
7. Look at the difference between an Artifact and an inline visual, using any existing chart or document in a sample conversation if one is available. Both return in Module 7.

**Expected result:** You can point to five things: where chat history lives, how a file attaches to a conversation, what a Web Search citation looks like, what a connector looks like from the settings side, and what makes a Project different from a regular chat. For the returns policy, Claude says a tent has a 60 day return window and no restocking fee, and lists Final Sale and custom embroidered items as not returnable.

> **Why this matters:** Every later demo assumes you have seen this tour once. A person who is still hunting for the file upload button during Module 6 loses the thread of that demo.

> **Note on plans:** Web Search, Memory, and Projects are all available on the class Pro account.

---

## Demo 2: Before and After, One Request, Two Outcomes

**Supports:** Module 4, the case for structured prompting, before teaching the framework itself.

**Context:** Seeing the same request produce two visibly different results is more convincing than any explanation. Do this demo before the course introduces POCC by name.

**Steps:**

1. Open a new conversation. Type a single, vague sentence and nothing else: "Write a client email about a delayed shipment."
2. Run it and read the output. Claude may show the result as email cards with options such as A and B, a Copy button, and an Open in Mail button, instead of plain text. Both forms are fine. In testing, the vague request produced two generic versions.
3. Open a new conversation. Run a structured version of the same request. For example: "You are a customer service lead at Lakeside Outfitters. Write an email to a customer about a delayed shipment. Order number 48213. The new delivery date is October 20. The delay was caused by a warehouse shortage of the item. We are covering the shipping cost as an apology. Keep it under 100 words, in a warm and direct tone."
4. Read the second output right after the first, so the contrast is fresh. In testing, the structured request produced one draft of about 100 words.
5. Discuss with your group or a partner: what are the concrete differences between the two outputs? Consider tone, specificity, and whether each output could be sent without editing.

**Expected result:** The vague-prompt output is generic and needs real editing before anyone could send it. The structured-prompt output includes the order number, the new date, the cause, and the cost handling, uses a clear tone, and has a length you did not have to trim.

> **Why this matters:** This is the point where "write better prompts" stops being vague advice. It becomes a repeatable lever you control.

---

## Demo 3: Reconstructing a Vague Request with POCC

**Supports:** Module 4, the POCC framework (Persona, Objective, Context, Constraints), the course's central prompting objective.

**Context:** This demo builds one prompt, one letter at a time, so you can see which addition causes which improvement. Results vary from run to run. Take note of what changes each time.

**Steps:**

1. Open a new conversation. Type a vague office request: "Help with the quarterly report."
2. Run it as written. Claude often returns clarifying questions. It may also return a generic outline. Either result is hard to use without more direction.
3. Add a Persona line and run the prompt again: "You are a financial analyst writing for a non-technical executive reader." Take note of the shift in tone and vocabulary.
4. Add an Objective line and run it again: "Summarize this quarter's regional sales performance in three short paragraphs." Take note of the shift in focus. With a Persona and an Objective but no data, Claude may return a draft with blanks and decline to invent figures. That is correct behavior.
5. Add Context, which is the data Claude needs. Use the Q3 2026 regional totals: North $142,700 (355 units), South $127,950 (339 units), West $167,600 (435 units). Run it again. Take note of the shift in relevance and accuracy. Context is what produces specific content.
6. Add Constraints and run it again: "Under 200 words, plain language, no bullet points." Take note of the shift in usability.
7. Compare the final output with the first output from step 2, and with the outputs from Demo 2.

**Expected result:** Outputs that get closer to something you could send each time you add a letter. The final version names the regions, uses the correct totals, follows the length and format limits, and needs little to no editing.

> **Key insight:** POCC is not a rigid checklist for every prompt. Persona matters most when tone or expertise is on the line. POCC gives you a repeatable way to check for the two things that separate a useful response from a mediocre one: enough context, and clear constraints.

> **Background:** Anthropic analyzed 100,000 real Claude.ai conversations and found a median 84 percent time savings across tasks, compared with estimated unassisted completion time. Report-compilation tasks like this one reached roughly 95 percent. Anthropic states that these are conversation-based estimates that likely overstate real-world gains, and that controlled trials found smaller effects, in the 14 to 56 percent range. Read both numbers together. Checking the larger self-reported figure against the more conservative controlled figure is the same check-the-claim habit Module 8 teaches.

---

## Demo 4: Ask Questions Against a Real Document

**Supports:** Module 6, working with files safely, and a useful document-reading capability.

**Files:** `demo-files/lakeside-vendor-contract.docx`, a fictional two-page Packaging and Fulfillment Supply Agreement between Lakeside Outfitters and Ridgeline Packaging Co.

**Context:** This demo shows a real capability, finding a specific buried detail faster than a manual read-through. It also sets up the data-handling discussion in Demo 5.

**Steps:**

1. Open a new conversation. Attach `lakeside-vendor-contract.docx`.
2. Ask: "What is the renewal date in this contract, and what happens if we miss it?"
3. Read Claude's answer. Find the matching section in the contract and confirm that Claude pulled the answer from there.
4. Ask a harder question: "What is the early termination fee and how is it calculated?" Check the contract again.
5. Type this sentence into the same conversation: "For future reference, I work in purchasing at Lakeside Outfitters and review vendor contracts every quarter." This sets up Demo 11.

**Expected result:** For step 2, Claude says the contract renews automatically on January 1, 2028. Written notice of non-renewal is due at least 90 days before the end of the term, which is by October 2, 2027. If you miss it, a 12-month renewal term starts and the $180,000 annual minimum purchase commitment applies. For step 4, Claude says the fee is 35 percent of the Minimum Commitment remaining for the term, calculated on a monthly basis. Claude points to the relevant section each time. This is faster than reading two pages of contract language for two specific facts.

> **Why this matters:** The document you choose to upload is a judgment call, and the next demo addresses it. Keep this contract in mind. It reappears in Demo 5.

---

## Demo 5: Good Use, Bad Use, What Not to Paste In

**Supports:** Module 6, data-handling guardrails, a major learning objective for this course.

**Files:** `demo-files/lakeside-vendor-contract.docx` (the same contract from Demo 4)

**Context:** This demo does not introduce a new Claude capability. It builds judgment around the capability you just used. The goal is a simple instinct you can apply without looking anything up.

**Steps:**

1. Open the contract from Demo 4 in Word. Scan it for sensitive content before you would upload it anywhere. Look at the notice section and the payment section.
2. Take note of what you would redact or leave out: the named notice contacts with their direct phone lines and personal email addresses, and the bank account number ending 4821.
3. Discuss with your group or a partner: what would change if this document contained an unredacted Social Security number or a client's medical record instead of a renewal date?
4. Look at this two-column comparison. Safe to Share: a redacted contract, a public policy document, a de-identified dataset. Do Not Share: a real customer's SSN, unreleased financial results, a password, private medical information.
5. Add one example of your own from your industry to each column.
6. Learn the one-line heuristic: if you would not paste it into an email to a stranger, do not paste it into Claude either.

**Expected result:** You can state the heuristic in your own words and name at least one category from the Do Not Share list without checking this guide. For the contract, you identify the named contacts with phone lines and emails, and the bank account ending 4821, as the items to redact.

> **Background:** League, a healthcare software company serving health plans and providers, reports 98 percent Claude adoption company-wide, up from 80 percent at initial rollout, achieved in under one quarter. Its CEO said, "Security is the first question on everything we do, and Anthropic clearly treats it the same way." Its controls, tiered model access, connector management, and custom boundary settings, map to the instinct this demo teaches. Real guardrails, backed by admin-level controls, are what let a regulated company move fast instead of freezing.

> **Connection to Projects:** A Project, from Module 3, reduces how many times a sensitive file is uploaded across separate conversations. Fewer repeated uploads mean a smaller footprint for that file. This is a good habit to build even before an organization has a formal AI data policy.

---

## Demo 6: Summarize Multiple Source Files

**Supports:** Module 7, turning messy, scattered inputs into a usable starting point.

**Files:** `demo-files/north-region-q3.xlsx`, `demo-files/south-region-q3.xlsx`, `demo-files/west-region-q3.xlsx`

**Context:** The three workbooks are deliberately messy. They hold Q3 2026 sales for three reps per region, but the headers and layouts differ on purpose. The North file uses Sales Rep, Month, Units Sold, and Revenue USD. The South file has two title rows, different header names, text currency values, and a Total row. The West file uses lower-case headers, full month names, and a second tab named notes. Open them first if you want to see the differences.

**Steps:**

1. Open a new conversation. Attach all three workbooks.
2. Ask: "Summarize the sales performance shown in each of these three files."
3. Read the three summaries. Take note that Claude handled the different headers, the title rows, and the text currency values without being told to.
4. Ask a follow-up question that compares across the files: "Which region had the strongest quarter, and why?"

**Expected result:** Three clear, accurate summaries. North: $142,700 and 355 units. South: $127,950 and 339 units. West: $167,600 and 435 units. The combined total is $438,250 and 1,129 units. In the follow-up answer, West is the strongest quarter. North has the highest revenue per unit, about $402, compared with about $385 for West and about $377 for South. Gray and Ivy, both in West, are the top two of the nine reps, and Faye in South is the lowest.

---

## Demo 7: Combine Summaries Into a Report

**Supports:** Module 7, the module's central objective: moving from scattered inputs to one polished deliverable.

**Context:** This demo continues from Demo 6. It shows where the Artifact and inline-visual distinction from Module 3 pays off. A report meant to be kept and shared belongs in an Artifact, so you do not copy it out of the chat window by hand.

**Steps:**

1. Stay in the Demo 6 conversation. Ask Claude to combine the three regional summaries into one short written report with an overall conclusion.
2. Read the first draft. By default, the report appears as plain chat text. Find one specific weakness, such as a section that is too long, a missing transition, or a conclusion that buries the main finding.
3. Ask Claude to revise based on that feedback. For example: "Shorten the regional detail and lead with the overall conclusion."
4. After the revision, type: "Save this report as an artifact."
5. Take note of the Artifact card that appears. Look at its "Only you" label and its Share button.

**Expected result:** A short, readable report that states an overall conclusion up front, backed by the three regional summaries, saved as an Artifact that you can download or share with someone else.

> **Background:** HubSpot reports a 40 percent productivity increase across web development and content-creation workflows from using Claude Projects and Artifacts to centralize context and accelerate content creation. Its CMO, Kipp Bodnar, said, "One of the things we love about Claude is that it has really good taste, and marketing's all about taste." The gather, summarize, combine chain in this demo is the same shape of work HubSpot's marketing team runs at company scale.

---

## Demo 8: Generate a Chart

**Supports:** Module 7, turning consolidated figures into a first-look visual.

**Context:** Inline charts are labeled beta. Confirm the label and the results in your own account. This models the verify-before-you-rely-on-it habit Module 8 teaches.

**Steps:**

1. Stay in the Demo 6 and 7 conversation. Ask: "Create a bar chart comparing the regional Q3 sales totals."
2. Let the chart render. Claude may produce it inline in the conversation or as an Artifact. Take note of which one you get.
3. Take note of any beta label on the chart.
4. Check the chart against the source numbers. The bar heights and labels should match $142,700 for North, $127,950 for South, and $167,600 for West.

**Expected result:** A basic, readable chart that matches the figures. West is the tallest bar and South is the shortest. If anything looks off, ask Claude to correct it. That correction is part of the demo.

---

## Demo 9: Web Search With Citations

**Supports:** Module 8, turning "trust me" into "check me."

**Context:** This demo continues the interface tour from Demo 1. A cited answer is not automatically correct. The citation gives you a concrete starting point to verify it.

**Steps:**

1. Open a new conversation. Web Search is on by default. Open the tools menu next to the message box to confirm.
2. Ask: "What did the most recent U.S. Consumer Price Index release show for the 12-month inflation rate? Give the release month and the figure."
3. Read the answer and look at its citations. Take note that the citations may point to a landing page or a non-official site.
4. Open at least one citation. Check the figure against the official source, bls.gov.

**Expected result:** Claude returns an answer with visible source citations, and at least one citation you check supports the specific claim it is attached to. In testing on October 5 to 6, 2026, Claude reported the August 2026 release, published September 11, 2026, with 3.4 percent for all items and 2.4 percent excluding food and energy. This figure changes monthly. Verify it on bls.gov. The next release is scheduled for October 14, 2026.

> **Why this matters:** Citations are a starting point for verification, not proof of accuracy. The next demo shows why that distinction matters.

---

## Demo 10: Spotting a Plausible But Wrong Answer

**Supports:** Module 8, spotting plausible-but-wrong AI answers, a major learning objective for this course.

**Files:** `demo-files/plausible-answer-to-review.docx` and `demo-files/lakeside-vendor-contract.docx`

**Context:** This is the hardest kind of error to catch. The answer is not obviously broken. It reads fluently and looks correct. That is why checking anything you plan to act on has to become a habit.

**Steps:**

1. Open `plausible-answer-to-review.docx`. It is a polished one-page summary of the Lakeside vendor contract for a purchasing team. It contains one incorrect detail.
2. Work alone or in pairs to find the incorrect detail. Check each number, date, and name against `lakeside-vendor-contract.docx`.
3. Discuss with your group or a partner: why was the error easy to miss? Consider plausible phrasing, correct-sounding structure, and a detail that fits the surrounding context.
4. Write a one-line validation habit in your own words. For example: before I act on a number, name, or date from Claude, I check it against the source.

**Expected result:** The error is the non-renewal notice period. The summary says at least 60 days before the end of the term. The contract says 90 days. Everything else in the summary is correct. Many people miss the error on the first pass, and that is the point of the exercise. By the end, you can state the validation habit in your own words.

> **Why this matters:** A confidently wrong answer that reads well is more dangerous than an obviously broken one, because nobody stops to double-check a broken-looking answer. Lab 2, Fact-Checking and Grounding AI Output, which runs in class, extends this exercise with more challenging examples.

---

## Demo 11: Memory Callback

> **TO FIX LATER: Do not run this demo for the time being.** In a test on October 6, 2026, Claude did not recall a detail shared minutes earlier, and it answered from older memory on the account instead. Recall is not reliable on the same day. This demo needs to be redesigned before it is used. Leave the steps below as they are until then.

**Supports:** Module 9, a capstone demonstration of a feature introduced earlier in the day.

**Context:** This is a short close to the interface features. It shows Memory, introduced in Module 3, working across separate conversations instead of within one.

**Steps:**

1. Open a brand new conversation, separate from anything used earlier.
2. Ask: "What kind of work do I do, and which vendor contract did we review?"
3. If Memory is on, Claude may recall your work description from Demo 4 without being told again.
4. Memory summaries can lag behind a very recent conversation, so a miss is possible on the same day. If Claude does not recall, open Settings, then Memory. Confirm that Memory is on and look at what is saved. Then tell Claude the detail again and ask it to remember it.

**Expected result:** Claude answers using context from the earlier session, with no re-explanation from you. Confirm in your own account. This recall behavior varies, and a miss on the same day does not mean Memory is broken.

---

# Financial Services Demos

These four demos repeat skills the course already teaches, using fictional financial services material. They suit people in banking, lending, and wealth management. Each one names the existing demo it follows. Do it right after that demo so you see the same skill applied to financial services work.

Every person, company, account, and figure in the demo files is fictional. The rules and thresholds used here are invented teaching examples. They are not legal or compliance advice. Have a compliance team review the wording before using these demos with financial services staff.

The files for these demos are in the `demo-files` folder next to this guide, in `~/Documents/course-1-claude-ai-essentials`.

---

## Demo 12: The Compliant Client Email

**Supports:** Module 4, the POCC framework, and its Constraints element in particular. Do it after Demo 3.

**Files:** `demo-files/communication-rules-card.txt`

**Context:** In Demo 3 the Constraints element limits length and tone. In financial services, Constraints also carry the firm's rules about what a client may be told. Claude does not know those rules unless you supply them. This demo shows what changes when you do, and what still needs a human reviewer.

**Steps:**

1. Open a new conversation. Type a vague request: "Write a short email to a client who is worried about the market dropping this month." Run it and read the draft.
2. Discuss with your group or a partner: which sentences would a compliance reviewer want to stop or rewrite? Write down two or three.
3. Open `communication-rules-card.txt` and read the seven rules. These are the firm's rules. Claude has never seen them.
4. Start a new message and paste the POCC version below. Replace the bracketed line with the full text of the rules card.

```
Persona: You are a client service associate at Lakeshore Wealth Partners writing to a long-time client.

Objective: Write a short email to Mr. Alvarez, who called this week worried about the recent market drop. Acknowledge his concern and offer a conversation.

Context: Lakeshore Wealth Partners has the communication rules below. The email must follow every one of them.
[paste the full text of communication-rules-card.txt here]

Constraints: Under 150 words. Plain language. Warm tone. Include the required disclosure line exactly as written in rule 5.
```

5. Run it and read the draft. Check it against the rules card one rule at a time. The first draft often already follows most of the rules. The rule most often missed is rule 5, the required disclosure line, so check that line word for word against the card.

**Expected result:** The second draft contains the line `[Required disclosure language from Compliance]` exactly as written, makes no promise about future performance, avoids the words "safe" and "risk-free", names no specific security, stays under 150 words, and ends with an offer to talk instead of a request for a decision. The first draft usually reassures the client in ways the rules card would not allow.

> **If Claude breaks a rule, keep the draft.** Models sometimes slip on one rule even when all seven are in the prompt. A slip is the best part of this demo. Find the sentence. Claude drafted it, and a person owns the check. Fix it by pasting the rule back and asking for a revision.

> **Why this matters:** Constraints are where a firm's rules enter the prompt. Giving Claude the rules makes the draft much closer to usable, and it does not replace the human who checks it. Compliance still completes the disclosure placeholder before anything is sent.

---

## Demo 13: Ask the Loan Agreement

**Supports:** Module 6, working with files safely, and Module 8, checking an answer against its source. Do it after Demo 4.

**Files:** `demo-files/loan-term-sheet.docx`, a fictional three-page term sheet for a $4,500,000 equipment and real estate loan.

**Context:** Demo 4 showed Claude finding buried details in a contract. This demo adds a trap. The final question asks about a clause the document does not contain, so you can see the difference between a grounded answer and an invented one.

**Steps:**

1. Attach `loan-term-sheet.docx` to a new conversation.
2. Ask: "What is the maturity date, and what is due on that date?" Read the answer. Find the matching line on page 1.
3. Ask: "Which financial covenants must the borrower meet, and how often is each one tested?" Read the answer. Find each covenant on page 2.
4. Ask: "How many days does the borrower have to deliver quarterly financial statements, and who signs the compliance certificate?" Check page 2 again.
5. Ask the trap question: "What prepayment penalty applies if the borrower repays the loan early?"
6. Read the answer. Then open the term sheet and search it for the word "prepay". Confirm that nothing is found.

**Expected result:** Claude answers steps 2 to 4 correctly. The maturity date is October 15, 2031, when the unpaid balance of principal and interest is due in full. The three covenants are a debt service coverage ratio of at least 1.25 to 1.00 and a ratio of total funded debt to EBITDA of no more than 3.50 to 1.00, both tested annually, plus unrestricted cash of at least $400,000, tested each quarter. Quarterly statements are due within 45 days after each quarter end, and an officer of the Borrower signs the compliance certificate. For the trap question, a good answer says the term sheet does not mention prepayment and suggests checking the full loan agreement or asking the lender.

> **Take note of how the trap answer is worded.** After saying the term sheet is silent, Claude may describe common prepayment structures. That is fine as long as it says clearly that the term sheet does not mention prepayment. The failure is a percentage or a schedule stated as if it came from the document.

> **Why this matters:** A wrong answer that reads well is more dangerous than a missing one. The check is cheap: find the line, or search for the word. In real credit work the full agreement is longer than three pages, and a lawyer or credit officer decides what it means. Claude is a reading aid that points you to where to look.

---

## Demo 14: Redact Before You Paste

**Supports:** Module 6, data-handling guardrails, a major learning objective for this course. Do it after Demo 5.

**Files:** `demo-files/customer-export.csv` and `demo-files/customer-export-redacted.csv`. Open the first file to look at it only. Never upload it.

**Context:** Demo 5 covered what not to paste into an AI tool. This demo makes the rule practical with a customer export. The question to ask is not "may I use AI on this file?" but "which columns does the question need?"

**Steps:**

1. Open `customer-export.csv` in a spreadsheet or text viewer. Look at the ten column names: customer_name, account_number, tax_id, date_of_birth, email, product, branch, balance, tenure_years, last_contact_note.
2. Sort the columns into three groups: fine to share, never share, and depends. Work alone or with a partner, then compare your groups with another pair. Write your answers down before reading step 3.
3. Compare your groups with the usual sorting. Name, account number, tax ID, date of birth, and email identify a person directly, so they go in the never group. The contact note is free text that can hold health, family, and money details, so it also goes in the never group. Product, branch, and tenure carry little risk. Balance depends, because a rare balance in a small group can point to one person.
4. Open `customer-export-redacted.csv`. Take note that it keeps only a reference number, product, branch, balance, and tenure. Take note of how it was made: someone deleted the columns locally in a spreadsheet before anything went to an AI tool.
5. Upload `customer-export-redacted.csv` to a new conversation. Ask: "Which product has the highest average balance, and which branch has the most customers?"
6. Ask a second question: "How many customers have been with us 10 years or more?"
7. Think about what the answers would have been on the full export. They would be identical, because the questions never needed names.

**Expected result:** Claude answers that Certificate has the highest average balance, $49,900.00, and that Eastgate has the most customers, with 5. Harbor Street has 4 and Northfield has 3. Four customers have tenure of 10 years or more. All four answers match the file.

> **Redaction is a habit, not a guarantee.** Removing direct identifiers does not make a small dataset anonymous. With twelve customers, an unusual balance and a branch could still identify someone. Your firm's policy decides what may leave your systems, and your compliance team owns that policy. Use the course slide on account types and training settings for what the course says about how each account type treats your data.

> **Why this matters:** Most analysis questions need patterns, not people. Deleting the identifying columns first costs a minute and removes the largest risk. The mistake to avoid is pasting the full file and asking the AI tool to clean it up, because the paste is the exposure.

---

## Demo 15: The Stale Rate

**Supports:** Module 8, turning "trust me" into "check me." Do it after Demo 9.

**Context:** Demo 9 showed Web Search adding citations. This demo shows why that matters for numbers that change. A rate is correct only on the day it is published, and a model without search answers from what it learned earlier.

**Steps:**

1. Open the tools menu next to the message box and turn Web search off. Web Search is on by default, so this step is required.
2. Look up the current federal funds target range on the Federal Reserve Open Market Operations page. Write it down. On October 5, 2026, the page showed 3.75 to 4.00 percent, effective September 17, 2026, after a quarter-point increase, per the Federal Reserve's September 16, 2026 statement. Check again, since this figure changes. If you are outside the United States, use your country's central bank policy rate instead.
3. Open a new conversation and confirm that Web search is still off.
4. Ask: "What is the current federal funds target range set by the Federal Open Market Committee?"
5. Compare Claude's figure with the one you wrote down.
6. Turn Web search on from the tools menu. In testing, the in-chat "Turn on web search" button did not switch it on, so use the tools menu. In the same conversation, ask: "Search the web and answer again, with a source."
7. Open the cited source. Confirm that it is the Federal Reserve or a news report that quotes it, and that the figure matches the one you wrote down.

**Expected result:** With Web Search off, Claude may state a range with confidence that does not match your figure, or it may say that it cannot know the current rate. In testing, Claude gave 3.50 to 3.75 percent (December 2025) with a hedge. With Web Search on, Claude gives the figure you wrote down and links a source you can open.

> **If the first answer happens to match your figure,** switch to a figure that changes weekly, such as the average 30-year fixed mortgage rate that Freddie Mac publishes. Look up the live figure first and use the same steps.

> **Why this matters:** In financial services, a stale rate in a client email or a model is a real error. The habit is to ask where the number came from and when it was published before you act on it. A confident tone is not evidence of freshness.

---

*End of Course 1 demo guide.*
