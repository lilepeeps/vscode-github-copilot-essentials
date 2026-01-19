# What is Visual Studio Code?

> 📺 **Video**: [Coming Soon - Link to YouTube video]

---

## What is it?

Visual Studio Code (VS Code) is a free, lightweight code editor from Microsoft that works as a versatile workspace, not just for programming.

Under the hood, VS Code is essentially a text editor on steroids: you open a folder or project, and VS Code presents all the files in a sidebar with powerful tools like global search, syntax highlighting, and version control support.

It's extremely customizable – you can change the theme, layout, and hotkeys, and install thousands of extensions to add functionalities (for example, support for specific languages, a markdown previewer, or integration with cloud services).

People usually use VS Code for writing and editing code (it supports debugging, Git integration, etc.), but it's not limited to code. Essentially any text-based file can be opened and edited, so many non-developers use VS Code for things like note-taking, documentation, data files (CSV, JSON), or running scripts.

It operates cross-platform (Windows, Mac, Linux) and is known for being fast and user-friendly despite its depth of features.

---

## How it works?

You install VS Code and open a folder (for example, a project folder on your OneDrive or local drive). That folder becomes your "workspace" – VS Code shows the directory structure and lets you navigate and search within all those files/folders instantly.

You can open multiple files in tabs, split the view, and have a built-in terminal if needed. The key idea is that VS Code provides a **single pane of glass** to work with all your project content.

For instance, if you're working on a customer engagement, you could have a folder with meeting transcripts, notes, spreadsheets, etc., and open it in VS Code. Now you've got quick global search across all those files, and you can edit or comment on them in one place.

This unified workspace approach helps avoid constantly switching between different applications. In fact, some of our team members (who aren't software engineers) spend most of their day in VS Code because it streamlines handling large amounts of information – it's become their "command center" for knowledge work.

---

## Understanding Where Things Live in VS Code

> 📺 **Video**: Workspaces & User Profiles in VS Code
>
> <!-- TODO: Replace with YouTube embed/link when ready -->
> 🎬 *Video placeholder: `Workspaces - User Profiles in VS Code.mp4`*

When customizing Copilot or any other VS Code feature, it helps to understand the three main places your settings and files can live: **user profile**, **workspace**, and **folder**. Each one defines a different scope for your configurations.

### User Profile

Your user profile is your personal VS Code environment — the configuration that travels with you no matter what workspace or folder you open.

It stores your preferred extensions, themes, keybindings, and Copilot customizations that you want to apply everywhere.

> [!NOTE]
> Files saved in your user profile (like your personal prompt files) are **private to you** and won't sync or apply to shared repositories. Think of it this way: if you make a change here and then share the files with other people, they won't be able to see these updates or customizations.

### Workspace

A workspace is the full context you currently have open in VS Code. It can be a single folder, or a collection of multiple folders linked together through a `.code-workspace` file.

Workspace-level settings apply to everything inside that open project. When you create files like `.github/copilot-instructions.md` or workspace-level prompt files, they'll affect all content and folders in that workspace.

### Folder

A folder is simply one of the directories inside your workspace. It can have its own `.vscode/settings.json` file and local configuration.

Folder-level settings apply only to the files in that folder. This is useful if your workspace includes multiple parts of a project (like a frontend and backend) and you want each to have slightly different Copilot or tooling behavior.

### Quick Reference

| Scope | What it affects | Example use case |
| ----- | --------------- | ---------------- |
| **User Profile** | All of VS Code, everywhere | Your personal theme and keybindings |
| **Workspace** | Everything in the current project | Shared team Copilot instructions |
| **Folder** | Only files in that specific folder | Different settings for frontend vs backend |

---

## Customization

> 📺 **Video**: Extensions in VS Code
>
> <!-- TODO: Replace with YouTube embed/link when ready -->
> 🎬 *Video placeholder: `Extensions in VS Code.mp4`*

One of VS Code's biggest strengths is that you can tailor it to your needs. The editor has a rich **Marketplace of extensions**.

For example:

- If you write a lot of documentation, you can install an extension for proofreading or for formatting text
- If you work with data, you might add extensions to preview CSV files or run SQL queries
- You can also create custom tasks – essentially macros or scripts that run with a shortcut – to automate things like converting a file format or launching a build process

Settings can be tweaked in configuration files or via a user-friendly UI, covering everything from editor font size to enabling/disabling specific IntelliSense (auto-completion) features.

In short, VS Code can be as simple or as powerful as you want: out-of-the-box it's straightforward for editing text, but with a few adjustments it can morph into an IDE, a note-taking assistant, or a data wrangling tool. This adaptability is why it's finding a place even in non-developer workflows.

> [!IMPORTANT]
> Always ensure any extensions or custom tools you add comply with your organization's IT and security policies.

---

## Common Use Cases

Traditionally, developers use VS Code for writing code in languages like Python, JavaScript, etc., because it provides smart completions and debugging.

However, in a **non-developer context**, think of VS Code as an advanced replacement for applications like Notepad or OneNote when plain text or files are involved.

### Examples for Non-Developers

| Use Case | How VS Code Helps |
| -------- | ----------------- |
| **Project Management** | Draft and organize project notes, store snippets of queries or commands, and manage to-do lists – all in one folder |
| **Meeting Notes** | Search and navigation capabilities make it great for combing through long meeting transcripts or logs to find key points |
| **Document Handling** | Preview and lightly edit Word, PDF, or Excel content via extensions (or convert them to text you can work with) |
| **AI and Automation** | VS Code is the environment where GitHub Copilot lives |
| **Collaboration** | Open a GitHub repository in VS Code, or sync with OneDrive |

In effect, VS Code lets a power user orchestrate many tasks from one interface. It's no longer just for coding – it's for **"orchestrating knowledge"** as we often say, bringing together collaboration, information, and AI into one hub.

---

[← Back to VS Code Section](README.md) | [Next: GitHub Copilot →](../02-github-copilot/README.md)
