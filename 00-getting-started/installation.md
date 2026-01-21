# 🚀 Getting Started: Installing VS Code & GitHub Copilot

This guide walks you through installing Visual Studio Code and GitHub Copilot from scratch. No technical experience required.

**Time needed:** ~10-15 minutes (core setup) | ~20-30 minutes (with optional tools)

## What's Covered

| Section | Required? | Who Needs It |
| ------- | --------- | ------------ |
| [Part 1: Installing VS Code](#part-1-installing-visual-studio-code) | ✅ Yes | Everyone |
| [Part 2: Installing GitHub Copilot](#part-2-installing-github-copilot) | ✅ Yes | Everyone |
| [Part 3: Signing In & Authentication](#part-3-signing-in--authentication) | ✅ Yes | Everyone (especially enterprise users) |
| [Part 4: Verify Everything Works](#part-4-verify-everything-works) | ✅ Yes | Everyone |
| [Part 5: Optional Tools](#part-5-optional-tools-advanced) | ⚪ Optional | Users wanting Git or advanced features |

---

## Part 1: Installing Visual Studio Code

### Step 1: Download VS Code

1. Go to [code.visualstudio.com](https://code.visualstudio.com/)
2. Click the big **Download** button (it auto-detects your operating system)
3. Save the installer file

### Step 2: Run the Installer

**On Windows:**
1. Double-click the downloaded `.exe` file
2. Accept the license agreement
3. **Recommended:** Check these options during setup:
   - ✅ Add "Open with Code" action to Windows Explorer file context menu
   - ✅ Add "Open with Code" action to Windows Explorer directory context menu
   - ✅ Add to PATH
4. Click **Install** and wait for it to complete
5. Click **Finish** to launch VS Code

**On Mac:**
1. Open the downloaded `.zip` file
2. Drag **Visual Studio Code** to your **Applications** folder
3. Open VS Code from Applications

### Step 3: First Launch

When VS Code opens for the first time:
- You may see a **Welcome** tab with tips and tutorials
- The interface might look overwhelming at first — that's normal!
- Take a moment to look around, but don't worry about understanding everything yet

> [!TIP]
> If VS Code asks about themes, pick whichever looks comfortable. You can always change it later in **File > Preferences > Color Theme**.

---

## Part 2: Installing GitHub Copilot

### Prerequisites

Before installing Copilot, you need:
- ✅ VS Code installed (done above)
- ✅ A GitHub account ([create one free](https://github.com/signup) if you don't have one)
- ✅ A GitHub Copilot subscription (check with your organization or [sign up](https://github.com/features/copilot))

### Step 1: Open the Extensions Panel

1. In VS Code, look for the **Extensions** icon in the left sidebar (it looks like four squares)
2. Or press `Ctrl+Shift+X` (Windows) / `Cmd+Shift+X` (Mac)

### Step 2: Search for GitHub Copilot

1. In the search box at the top, type: `GitHub Copilot`
2. You'll see several results — look for **"GitHub Copilot"** (the main extension by GitHub)
3. Click **Install**

### Step 3: Sign In to GitHub

1. After installation, you'll see a prompt to sign in to GitHub
2. Click **Sign in to GitHub**
3. A browser window will open — log in with your GitHub credentials
4. Authorize VS Code to access your account
5. Return to VS Code — you should see a confirmation

### Step 4: Install GitHub Copilot Chat (Optional but Recommended)

1. Go back to Extensions (`Ctrl+Shift+X`)
2. Search for: `GitHub Copilot Chat`
3. Click **Install**

> [!NOTE]
> GitHub Copilot Chat gives you the conversational interface we discuss throughout this guide. It's highly recommended!

---

## Part 3: Signing In & Authentication

Getting signed in correctly is crucial, especially if you're using VS Code within a company or organization. There are multiple accounts you may need to connect.

### Understanding the Different Accounts

| Account Type | What It's For | When You Need It |
| ------------ | ------------- | ---------------- |
| **GitHub Account** | Copilot access, GitHub repos | Always (for Copilot) |
| **Microsoft Account (Work/School)** | Company resources, Azure, M365 integration | If using enterprise features |
| **Microsoft Account (Personal)** | Settings Sync, personal Azure | Optional |

### Signing Into Your Microsoft/Company Account

If you're using VS Code for work and need access to company resources (like Azure DevOps, SharePoint, or company-specific extensions), you'll want to sign in with your work account.

**Step 1: Access Account Settings**
1. Click on the **Accounts icon** at the bottom of the Activity Bar (left sidebar — looks like a person silhouette)
2. Or click the **gear icon** (Manage) at the bottom of the Activity Bar and select **Backup and Sync Settings...**

**Step 2: Choose Your Account Type**
1. Click **Sign in with Microsoft**
2. A browser window will open
3. Select your **work or school account** (typically ends in `@yourcompany.com`)
4. Complete your organization's sign-in process (may include MFA/2FA)

**Step 3: Verify Connection**
- Once signed in, you'll see your account name in the bottom-left corner
- A badge may appear on the Account icon showing you're connected

> [!TIP]
> **For enterprise users:** Signing in with your work account enables:
> - Settings Sync across devices
> - Access to company extensions
> - Integration with Azure DevOps
> - Company-managed Copilot policies

### Managing Multiple Accounts

You may need both a GitHub account (for Copilot) and a Microsoft account (for company resources). You might even need multiple GitHub accounts — for example, a personal account and a work account.

**How accounts work in VS Code:**
- Each feature (Copilot, Settings Sync, extensions) connects to the account it needs
- You can have multiple GitHub accounts and multiple Microsoft accounts signed in simultaneously
- VS Code keeps track of which account is used for which service

**To see your connected accounts:**
1. Click the **Accounts icon** (bottom of Activity Bar)
2. Your signed-in accounts appear at the top of the menu
3. You'll see entries like "username (GitHub)" or "email@company.com (Microsoft)"

**To add another account (e.g., a second GitHub account):**

VS Code adds accounts when features or extensions request them. To add another GitHub or Microsoft account:

1. Use a feature that requires authentication (e.g., clone a repo, access Azure resources)
2. When prompted, choose to sign in with a **different account** rather than an existing one
3. The new account will appear in your Accounts menu

Alternatively, for GitHub accounts specifically:
1. Open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`)
2. Type: `GitHub: Sign In to GitHub.com`
3. When the browser opens, sign in with your additional GitHub account

> [!TIP]
> This is useful if you have both a personal GitHub account and a work GitHub account, or if you need to switch between organizations.

**To manage which account is used for what:**
1. Click the **Accounts icon**
2. Select **Manage Extension Account Preferences...** to control which account extensions use
3. Select **Manage Language Model Access...** to control Copilot account preferences

**To sign out of an account:**
1. Click the **Accounts icon**
2. Click on the account you want to sign out of
3. Select **Sign Out**

### Troubleshooting Authentication

| Issue | Solution |
| ----- | -------- |
| "Sign in failed" | Check your internet connection; try again |
| Can't see work account option | Contact your IT department — they may need to enable VS Code access |
| MFA/2FA issues | Complete authentication in browser; return to VS Code |
| Wrong account signed in | Sign out via Account icon, then sign in with correct account |
| "Your organization has disabled this feature" | Talk to your IT admin about enabling VS Code or Copilot |

---

## Part 4: Verify Everything Works

### Test Copilot Inline Suggestions

1. Create a new file: **File > New File**
2. Save it as `test.md` (or any filename)
3. Start typing something like: `# My first`
4. If Copilot is working, you should see a **gray/faded suggestion** appear
5. Press `Tab` to accept the suggestion, or keep typing to ignore it

### Test Copilot Chat

1. Look for the **Copilot Chat** icon in the left sidebar (speech bubble icon)
2. Or press `Ctrl+Alt+I` (Windows) / `Cmd+Option+I` (Mac)
3. Type a question like: "What can you help me with?"
4. If Chat is working, Copilot will respond!

### Verify Your Accounts

1. Click the **Account icon** (bottom-left)
2. Confirm you see:
   - Your GitHub account (for Copilot)
   - Your Microsoft work account (if applicable)
3. Check the **Copilot icon** in the status bar (bottom-right) — it should show as active

---

## Part 5: Optional Tools (Advanced)

The core VS Code + Copilot setup is complete. The following tools are **optional** but unlock additional capabilities, especially if you want to:

- **Collaborate on shared projects** — Work on the same files as colleagues without emailing documents back and forth or worrying about overwriting each other's changes
- **Track changes over time** — See what changed, when it changed, and who changed it (like "Track Changes" in Word, but more powerful)
- **Install specialized tools** — Some advanced Copilot features (like MCP servers) require additional software to run
- **Connect to online code storage** — Download projects from GitHub or Azure DevOps, or upload your own work to share with others

> [!NOTE]
> These tools are commonly used by developers, but non-developers can benefit from them too. If you're not sure whether you need them, you can always come back and install them later.

---

### First: Understanding the Terminal

Before installing these tools, it helps to understand what the **terminal** is and why you'll see "commands" mentioned throughout this section.

**What is the terminal?**

The terminal (also called "command line" or "PowerShell" on Windows) is a text-based way to interact with your computer. Instead of clicking buttons and icons, you type instructions. It looks like a blank screen with a blinking cursor waiting for you to type something.

VS Code has a built-in terminal. To open it:
- Press `Ctrl+J` (Windows) or `Cmd+J` (Mac)
- Or go to **View > Terminal**

**What are commands?**

A command is just an instruction you type and then press Enter to run. For example:

| You Type | What It Does |
| -------- | ------------ |
| `git --version` | Asks "is Git installed, and what version?" |
| `node --version` | Asks "is Node.js installed, and what version?" |
| `npm install` | Installs the tools/packages a project needs |

**Why use the terminal instead of clicking?**

- Some tools only work through the terminal (no buttons to click)
- It's faster once you know the commands
- Instructions are easier to share ("type this" vs. "click here, then here, then...")

> [!TIP]
> You don't need to memorize commands. Copy and paste them from instructions, and over time you'll remember the ones you use often.

---

### Optional Tool 1: Git (Version Control)

**What is Git?**

Git is a version control system that tracks changes to your files over time. Think of it like "Track Changes" in Word, but for any type of file and much more powerful.

**Why you might want it:**

| Use Case | How Git Helps |
| -------- | ------------- |
| Collaborating with others | Everyone can work on the same project without overwriting each other |
| Tracking your own changes | See what changed, when, and revert if needed |
| Using GitHub/Azure DevOps repos | Required to clone (download) and push (upload) projects |
| Working with shared Copilot configurations | Prompt files and instructions are often stored in Git repos |

**Installing Git:**

**On Windows:**
1. Go to [git-scm.com/download/win](https://git-scm.com/download/win)
2. Download the installer
3. Run the installer — the default options are fine for most users
4. **Important:** When asked about the default editor, you can select **Visual Studio Code**
5. Complete the installation

**On Mac:**
1. Open **Terminal** (search for it in Spotlight)
2. Type: `git --version`
3. If Git isn't installed, macOS will prompt you to install it
4. Follow the prompts to install

**Verify Git is installed:**
1. In VS Code, open the Terminal (`Ctrl+J` or `Cmd+J`)
2. Type: `git --version`
3. You should see a version number (e.g., `git version 2.43.0`)

**Configure Git with your identity (required):**

Before you can use Git, you must tell it who you are. This information is attached to every change you save (called a "commit"), so your team knows who made what changes.

1. In VS Code, select **Terminal > New Terminal** to open a terminal
2. Type these two commands (replace with your actual name and email):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@company.com"
```

3. Press Enter after each command (they won't show any output — that's normal)

> [!IMPORTANT]
> This is a one-time setup. If you skip this step, Git will ask for it later, or your commits may show up as "unknown author."

**About Git Credential Manager:**

When you installed Git on Windows, it included **Git Credential Manager** — a tool that securely stores your login credentials so you don't have to enter your password every time you interact with GitHub or Azure DevOps.

The first time you try to clone a repository or push changes, Git Credential Manager will open a browser window asking you to sign in. After that, it remembers your credentials securely.

> [!TIP]
> Once Git is installed and configured, VS Code's **Source Control** panel (the branch icon in the Activity Bar) becomes much more useful — you can see changes, commit them, and sync with remote repositories.

---

### Optional Tool 2: Node.js (Package Management)

**What is Node.js?**

Node.js is a runtime that lets you run JavaScript outside of a web browser. For our purposes, the important part is that it comes with **npm** (Node Package Manager), which is widely used for installing the tools and dependencies that projects need to run.

**Why you might want it:**

Many projects you download or collaborate on will include a file called `package.json` that lists all the tools and packages the project needs. When you run `npm install` in a project folder (see [Understanding Where Things Live in VS Code](../01-visual-studio-code/what-is-visual-studio-code.md#understanding-where-things-live-in-vs-code) for more on folders and workspaces), npm reads that file and automatically installs everything for you. Without Node.js/npm, you'd have to manually find and install each tool yourself.

| Use Case | How Node.js/npm Helps |
| -------- | --------------------- |
| Working with shared projects | Run `npm install` to get all the tools a project requires |
| Using advanced extensions | Some VS Code extensions require Node.js to run |
| Installing specialized tools | Many developer tools (including some MCP servers) are distributed via npm |
| Building web-based projects | If you ever work with web content or automation scripts |

**Installing Node.js:**

**On Windows:**
1. Go to [nodejs.org](https://nodejs.org/)
2. Download the **LTS (Long Term Support)** version (recommended for most users)
3. Run the installer
4. Accept the defaults — this installs both Node.js and npm
5. **Optional:** Check the box to install additional tools if prompted

**On Mac:**
1. Go to [nodejs.org](https://nodejs.org/)
2. Download the **LTS** version
3. Open the downloaded `.pkg` file
4. Follow the installation prompts

**Verify Node.js is installed:**
1. In VS Code, open the Terminal (`Ctrl+J` or `Cmd+J`)
2. Type: `node --version`
3. You should see a version number (e.g., `v20.10.0`)
4. Type: `npm --version`
5. You should see the npm version (e.g., `10.2.3`)

> [!TIP]
> You don't need to understand Node.js or JavaScript to use npm. Think of npm as an "app store" for developer tools — you just type `npm install [package-name]` to install things.

---

### Quick Reference: Optional Tools Summary

| Tool | What It Does | Install If You Want To... |
| ---- | ------------ | ------------------------- |
| **Git** | Version control | Collaborate on projects, use GitHub/ADO repos, track file changes |
| **Node.js** | JavaScript runtime + npm | Install MCP servers, use npm packages, run automation scripts |

---

## Troubleshooting

| Problem | Solution |
| ------- | -------- |
| "Sign in" keeps appearing | Make sure you're signed into the correct GitHub account with Copilot access |
| No suggestions appearing | Check that Copilot is enabled (look for Copilot icon in bottom status bar) |
| "Copilot is not available" | Your organization may need to enable Copilot for your account |
| Extension won't install | Try restarting VS Code and trying again |
| Can't sign into work account | Contact IT — your organization may need to allow VS Code |
| Git commands not recognized | Restart VS Code after installing Git; ensure Git is in your PATH |
| npm commands not recognized | Restart VS Code after installing Node.js |

---

## What's Next?

Now that you have VS Code and Copilot installed:

1. **Open a folder** to create your first workspace
2. **Try the Chat** by asking Copilot a question about your work
3. **Explore the interface** — hover over icons to see what they do

➡️ Continue to: [What is Visual Studio Code?](../01-visual-studio-code/what-is-visual-studio-code.md)

---

## Summary Checklist

Before moving on, confirm you have:

- [ ] VS Code installed and running
- [ ] GitHub Copilot extension installed
- [ ] GitHub Copilot Chat extension installed
- [ ] Signed into GitHub (for Copilot)
- [ ] Signed into Microsoft work account (if using enterprise features)
- [ ] Verified Copilot suggestions are working
- [ ] *(Optional)* Git installed
- [ ] *(Optional)* Node.js installed

---

## Video Tutorials

> 📺 **Video placeholders for this section:**
> - Installing VS Code (Windows/Mac)
> - Installing GitHub Copilot extension
> - Signing in and verifying setup
> - Signing into your Microsoft work account
> - Installing Git (optional)
> - Installing Node.js (optional)

---

[← Back to Section Overview](README.md) | [Next: What is Visual Studio Code? →](../01-visual-studio-code/what-is-visual-studio-code.md)
