# Lab 1: Ask Your Files with the Filesystem Extension

**Course:** Claude Desktop Essentials
**Duration:** 70 minutes

---

> ## BUILD NOTE: Part 6 steps need a test on the class VM before distribution
>
> Part 6 (the custom keyboard shortcut) was written from Anthropic's Linux install documentation and standard Ubuntu behavior. It has not been run on the class VM. Before this lab goes to students, confirm four things on the VM: the Settings path and the Custom Shortcuts dialog in the installed Ubuntu release, that `Ctrl+Alt+C` is free, that running `claude-desktop` while Claude is already open raises the existing window instead of starting a second one, and that Claude is allowed to run from a shortcut command. The Windows steps in Part 6 are also untested. Delete this note after the VM test passes.

---

## Prerequisites

- [ ] A Linux VM provided by your instructor, with Claude Desktop already installed (primary path for this class)
- [ ] Your private ROI Virtual Classroom (RVC) credentials from your instructor: your RVC email address and password
- [ ] The course files, which you download from the course repository in Part 1 (Git is already installed on your VM)
- [ ] Modules 1 through 5 of today's session completed, including the Desktop Extensions walkthrough

> **You are working in a shared classroom environment.** Your VM is for today's class only. Use the class account your instructor provides, and do not sign in with a personal account on the VM.

> **Using your own machine instead?** Each step below includes a short Windows and Mac note where the steps differ. On your own machine you need Claude Desktop installed and signed in, and permission to install an extension. Linux machines must run Ubuntu 22.04 or later, or Debian 12 or later. You also need Git. Download the course files into your Documents folder with the same commands as Step 7, using Git Bash on Windows or Terminal on Mac.

> **Claude Desktop on Linux is a beta.** Dictation and computer use are not available on Linux, and Claude's own Quick Entry feature is not required for this lab. Neither affects anything you do today.

---

## Part 1: Sign In to Claude and Get the Course Files

Your class runs on a Linux virtual machine (VM) hosted on ROI Virtual Classroom (RVC). You sign in to Claude with single sign-on (SSO). Your instructor gives you private RVC credentials. Do this part the first time you log in. After you sign in to Claude, you download the course files with Git.

> **Using your own machine instead?** Skip this part and continue at Part 2. Sign in to Claude Desktop with the class account your instructor provides.

### Step 1: Sign In to ROI Virtual Classroom

Open https://rvc.roitraining.com in a web browser and sign in with the private RVC credentials your instructor gave you. Your Linux VM launches automatically after a successful sign-in.

**Expected result:** The Linux desktop of your VM is open.

### Step 2: Open Claude for Linux and Select Get Started

Open the Activities overview or the applications menu and start **Claude**. Claude for Linux is the same Claude app that you would install on Windows or Mac. When Claude opens, select **Get Started**.

**Expected result:** Claude shows a sign-in screen that asks for an email address.

### Step 3: Enter Your RVC Email Address

Enter the RVC email address that ROI provided to you. An SSO option appears: **Continue with SSO**. Select it.

**Expected result:** Your browser opens the ROILOGIN.COM SSO portal.

### Step 4: Sign In at the ROILOGIN.COM Portal

Sign in with your RVC credentials. You can choose to save the credentials. They expire at the end of this class.

**Expected result:** The portal accepts your credentials and shows a prompt about opening a link with Claude.

### Step 5: Allow Claude to Open the Link

The prompt asks "Allow this site to open the Claude link with Claude". Press **open link**.

**Expected result:** You are authenticated to Claude Desktop, also called Claude for Linux. The main Claude window is open and shows a message box where you can start a conversation.

### Step 6: Open a Terminal

Open the Activities overview, type **Terminal**, and open it.

**Expected result:** A Terminal window opens with a command prompt.

### Step 7: Download the Course Files with Git

Your instructor gives you the repository address. In the commands below, replace `<REPO_URL>` with that address, without the angle brackets. Run the commands one at a time.

```
cd ~/Documents
git clone <REPO_URL> .
```

The first command moves you into your Documents folder. The second downloads the course files into it. The dot at the end tells Git to download the files straight into the current folder.

Then run `ls` to list what you downloaded.

**Expected result:** The `ls` command lists these folders: `ROI-Lab-Files`, `demo-files`, `fin-demo-files`, `course-1-claude-ai-essentials`, and `course-2-claude-desktop-essentials`. If Git asks you to sign in, use the access details your instructor gives you.

> **Already downloaded the course files in an earlier lab?** Run `cd ~/Documents` and then `git pull` to get the latest files. Do not clone a second time.

> **Git says the folder is not empty?** Documents already has files in it. Run these commands instead:
>
> ```
> cd ~/Documents
> git init
> git remote add origin <REPO_URL>
> git pull origin main
> ```

---

## Part 2: Open Claude and Establish a Baseline

### Step 8: Start Claude Desktop

**Linux (VM):** Claude is already open and signed in from Part 1. Continue to the next step. If you closed it, open the Activities overview or the applications menu and start **Claude** again.

**Windows:** Open the Start menu and start **Claude**.

**Mac:** Open **Claude** from the Applications folder.

**Expected result:** The main Claude window is open and shows a message box where you can start a conversation.

### Step 9: Ask a Question About a File Claude Cannot Reach Yet

Start a new chat and type this prompt exactly:

```
Open project-tracker.csv in my Documents/ROI-Lab-Files/lab1-workspace folder and tell me how many tasks are marked Done.
```

**Expected result:** Claude tells you it cannot open files on your computer. It may ask you to attach the file or paste its contents instead.

> **Keep this answer in mind.** Claude Desktop has no access to your files until you give it access. You will repeat this exact prompt in Step 19 and compare the two answers.

---

## Part 3: Locate the Lab Files

### Step 10: Find the Folder in Your File Manager

**Linux (VM):** Open **Files**, choose **Documents**, and open **ROI-Lab-Files**.

**Windows:** Open **File Explorer**, choose **Documents**, and open **ROI-Lab-Files**.

**Mac:** Open **Finder**, choose **Documents**, and open **ROI-Lab-Files**.

**Expected result:** You see three folders named lab1-workspace, lab2-workspace, and lab2-restricted, plus a README.txt file.

### Step 11: Check the Contents of lab1-workspace

Open the lab1-workspace folder.

**Expected result:** You see four files: project-tracker.csv, meeting-notes-2026-09-30.md, client-update-draft.md, and style-guide.txt.

> **Optional terminal check on Linux and Mac.** Open a terminal and run `ls ~/Documents/ROI-Lab-Files/lab1-workspace`. You will use the same command in Step 22 to confirm a file Claude creates.

### Step 12: Read the Scenario

Open README.txt and read it.

**Expected result:** You know the scenario: you support the Lakeside Outfitters website relaunch, and today is 2 October 2026 for every question in this lab.

---

## Part 4: Install the Filesystem Extension

### Step 13: Open the Extensions Directory

In Claude Desktop, open **Settings** and choose **Extensions**. Click **Browse extensions**.

**Expected result:** A directory of extensions appears. Anthropic-reviewed extensions are visible on every plan.

### Step 14: Find the Filesystem Extension

Find the extension named **Filesystem** and open its detail page. Read the description, the publisher, and the list of permissions before you install anything.

**Expected result:** You can state in one sentence what the Filesystem extension lets Claude do, and you can name the publisher shown on the page.

> **Use the three checks from the Review Before You Install demo.** Ask yourself what the extension can see and do, whether it shows a verified publisher indicator, and whether any sign-in stays local to your device.

### Step 15: Install the Extension

Click **Install**. Read each prompt fully before you continue. When Claude asks which directories the extension may use, add this folder and no other:

```
Documents/ROI-Lab-Files/lab1-workspace
```

**Linux (VM):** The full path is `/home/<your username>/Documents/ROI-Lab-Files/lab1-workspace`. Use the folder picker to select it.

**Windows:** The full path is `C:\Users\<your username>\Documents\ROI-Lab-Files\lab1-workspace`.

**Mac:** The full path is `/Users/<your username>/Documents/ROI-Lab-Files/lab1-workspace`.

**Expected result:** The Filesystem extension finishes installing and shows as enabled in **Settings > Extensions**. The allowed directories list shows lab1-workspace and nothing else.

> **Do not add the Documents folder, your home folder, or ROI-Lab-Files.** Adding a parent folder gives Claude access to everything inside it, including the lab2-restricted folder. You will test why that matters in Lab 2.

> **Install stalled or failed?** Ask your instructor. A staged copy of the extension is available for this situation. You can also pair with a neighbor whose install succeeded.

### Step 16: Review the Extension's Tool List

Open the Filesystem extension's settings page and look at the list of tools it provides and the permission setting next to each one.

**Expected result:** You can name at least three tools the extension provides, and you can say which of them only read files and which of them can change files.

> **Write down the permission setting for each tool.** You will adjust these settings in Lab 2.

---

## Part 5: Ask Claude About Your Files

Start a new chat for this part so Claude loads the extension's tools.

### Step 17: List the Folder

Type this prompt:

```
List the files in my Documents/ROI-Lab-Files/lab1-workspace folder and describe each one in one sentence.
```

When Claude asks permission to use a tool, read the prompt, confirm it points at the lab1-workspace folder, and allow it.

**Expected result:** Claude lists the four files by name and describes each one correctly. The prompt you approved named the lab1-workspace folder.

### Step 18: Summarize the Meeting Notes

Type this prompt:

```
Read meeting-notes-2026-09-30.md and give me the three decisions and the four action items with their owners.
```

**Expected result:** Claude returns three decisions, including the launch date of 19 October 2026, and four action items assigned to Priya, Marcus, Lee, and Priya.

### Step 19: Repeat the Baseline Question

Type the same prompt you used in Step 9:

```
Open project-tracker.csv in my Documents/ROI-Lab-Files/lab1-workspace folder and tell me how many tasks are marked Done.
```

**Expected result:** Claude answers that 4 tasks are marked Done. You received an answer from the file itself with no upload step.

> **Compare the two answers.** In Step 9, Claude could not reach the file. Now it reads the file directly from the allowed folder. The only thing that changed is the extension and the folder you granted.

Now ask a follow-up:

```
Treat 2 October 2026 as today. Which tasks are overdue, who owns them, and what is blocking them?
```

**Expected result:** Claude names T-104 (Marcus, image migration) and T-105 (Dana, checkout flow). It identifies the missing gateway credentials as the blocker for T-105. T-110 is due today and is not overdue.

### Step 20: Find the Errors in the Client Draft

Type this prompt:

```
Compare client-update-draft.md to project-tracker.csv and meeting-notes-2026-09-30.md. List every statement in the draft that the other two files contradict.
```

**Expected result:** Claude finds at least three contradictions. The draft says five tasks are complete when the tracker shows four. It says the checkout flow is on track when the tracker shows it as blocked. It says load testing is complete when the tracker shows it as not started. It gives a launch date of 14 October when the meeting notes set 19 October.

> **Check Claude against the files.** If Claude reports a contradiction you cannot find, open the file and verify it yourself. Claude can be wrong, and your job is to confirm what it tells you.

### Step 21: Create a Corrected Draft

Type this prompt:

```
Using style-guide.txt, write a corrected version of the client update and save it in this folder as client-update-corrected.md.
```

Read the permission prompt before you allow it. This step asks Claude to create a file, which is a different kind of action than reading.

**Expected result:** Claude confirms it created client-update-corrected.md in the lab1-workspace folder.

### Step 22: Confirm the New File Exists

Check the file yourself without asking Claude.

**Linux (VM) and Mac:** Open a terminal and run `ls -l ~/Documents/ROI-Lab-Files/lab1-workspace`. Then run `cat ~/Documents/ROI-Lab-Files/lab1-workspace/client-update-corrected.md`.

**Windows:** Open the lab1-workspace folder in File Explorer and open client-update-corrected.md.

**Expected result:** The file is in the folder. It states that four tasks are complete, names the checkout flow blocker and what is needed to clear it, gives 19 October as the launch date, and ends with one clear request for the client.

---

## Part 6: Reach Claude From Any Application

Until now you opened Claude by finding its window. In this part you build a keyboard shortcut that brings Claude forward from inside any other application. Then you use it to ask a question without searching for a window.

### Step 23: Create a Keyboard Shortcut That Opens Claude

**Linux (VM):** Open **Settings**, choose **Keyboard**, and select **View and Customize Shortcuts**. Scroll to **Custom Shortcuts** and click the plus button. Enter the name `Open Claude` and the command `claude-desktop`. Click **Set Shortcut** and press `Ctrl+Alt+C`. If Ubuntu reports that the combination is already in use, do not replace the existing shortcut. Choose a different combination. Click **Add**.

**Windows:** Find the **Claude** shortcut on your desktop or in the Start menu folder. If you start from the Start menu, right-click **Claude**, choose **More**, and choose **Open file location**. Right-click the Claude shortcut file, choose **Properties**, and open the **Shortcut** tab. Click in the **Shortcut key** box and press the letter C. Windows fills in `Ctrl+Alt+C`. Click **Apply**.

**Mac:** A Mac has no single system setting that opens an application with a key. Use Claude's built-in Quick Entry gesture instead. Double-tap the **Option** key from any application. To change the gesture, open Claude, choose **Settings**, choose **General**, and look for the Quick Entry shortcut setting. On a Mac, this opens a small floating window instead of the main window.

**Expected result:** On Linux, the shortcut appears in the Custom Shortcuts list. On Windows, the Shortcut key box shows `Ctrl+Alt+C`. On Mac, you know which gesture opens Quick Entry.

> **Optional: Claude's own hotkey on Linux.** Claude Desktop on Linux also offers a built-in Quick Entry hotkey, which works on the X11 display server the class VM uses. Ask your instructor whether it is turned on for your VM. The shortcut you create in this step does not depend on that beta feature, and the same idea works on every platform.

### Step 24: Test the Shortcut From Another Application

Open a different application and click inside it. Use **Text Editor** on the Linux VM, **Notepad** on Windows, or **TextEdit** on Mac. Press your shortcut.

**Expected result:** Claude comes to the front without you using the mouse or the applications menu.

> **Nothing happened?** Another shortcut may already use the same combination. Open the keyboard settings, look for a conflict, and choose a different combination. If a second Claude window opens instead of the window you already had, close the extra window and tell your instructor.

### Step 25: Ask a Question Through the Shortcut

From the other application, press your shortcut. Start a new chat so Claude loads the extension's tools, and type this prompt:

```
Which tasks does Priya own in project-tracker.csv, and what is the status of each one?
```

Read the permission prompt before you allow it, and confirm it points at the lab1-workspace folder.

**Expected result:** Claude lists four tasks. T-101 is Done, T-106 is In Progress, T-110 is In Progress and due today, and T-112 is Not Started.

### Step 26: Run It a Second Time

Switch back to the other application and press the same shortcut again. Start another new chat and type this prompt:

```
Which tasks are blocked, and what does each one need to move forward?
```

**Expected result:** Claude names T-105, the checkout flow owned by Dana, which needs gateway credentials from the vendor. It also names T-111, the customer email announcement owned by Marcus, which needs approved copy from the client. The same keystroke worked with no extra setup.

> **A shortcut that needs setup each time is not a workflow.** Running the same path twice in a row is how you confirm that you built something reusable and not a one-time trick.

---

## Part 7: Checkpoint

### Step 27: Record What You Built

Write four sentences that answer these questions. Which folder did you grant? What did Claude read, and what did it create? What was different about Step 9 and Step 19? Which keystroke now brings Claude forward from another application?

**Expected result:** Four sentences you could say aloud to a colleague. For example: "I granted Claude access to one project folder. Claude read the tracker and meeting notes and created a corrected client update. In Step 9 it could not see the file, and in Step 19 it read the file directly with no upload. Pressing Ctrl+Alt+C from any application now brings Claude forward, ready for a question about those files."

> **Checkpoint:** Before moving on, confirm with your instructor or a neighbor that the Filesystem extension is enabled, that only lab1-workspace is in its allowed directories, that client-update-corrected.md exists in that folder, and that your shortcut brings Claude forward from another application.

---

## What You Built

In this lab, you:

- Confirmed that Claude Desktop has no file access until you grant it
- Located and verified a set of lab files on your own system
- Installed the Filesystem extension and reviewed its permission prompts before approving them
- Granted access to a single folder and checked the allowed directories list
- Asked Claude to read, compare, and analyze four local files without uploading any of them
- Asked Claude to create a new file and verified the result yourself
- Built a keyboard shortcut that brings Claude forward from any application, and used it twice in a row

---

## What's Next

Lab 2, Permissions and Safety, uses the extension you installed here. You will test the boundary of the folder you granted, see what happens when a file contains instructions aimed at Claude, and adjust the extension's tool permissions.

Keep the Filesystem extension installed and keep lab1-workspace in its allowed directories until Lab 2 tells you to change it. Keep the shortcut too, since it is the quickest way back to Claude for the rest of the session.

---

*Lab 1 Complete*
