# 📚 Glossary of Terms

A reference guide to common terms used throughout this guide.

> 💡 **Tip:** Use `Ctrl+F` (Windows) or `Cmd+F` (Mac) to quickly search for a term.

---

## A

### applyTo (Frontmatter Field)

A setting used in `.instructions.md` files that tells Copilot which file types the instruction applies to.

**Example:**
```yaml
applyTo: ["*.md", "*.txt"]
```

This means "only use these rules when working with Markdown or text files."

> **Analogy:** It's like setting a filter for when the rule should apply.

---

## C

### Chat Context Layers

Every Copilot chat combines three layers:

| Layer | What It Does |
| ----- | ------------ |
| **Instruction** | The standing rules (your preferences) |
| **Chat Mode** | The persona or focus for that chat session |
| **Prompt** | What you're asking Copilot right now |

Together, they determine how Copilot responds. Adjusting one layer changes the flavor of the conversation.

### Copilot Chat Modes (`.chatmode.md`)

Chat Modes define **how Copilot should act** in a chat — its personality, tools, and focus.

**Examples:**
- A **"Code Reviewer"** mode focuses on analyzing scripts
- A **"Project Manager"** mode summarizes tasks and writes updates

These modes are stored as `.chatmode.md` files with frontmatter defining their behavior. You can switch between modes as easily as switching conversation topics.

### Copilot Instructions

Instructions tell Copilot **how to behave** in all your chats or prompts. They're stored in special Markdown files.

There are three main types:

| Type | Purpose |
| ---- | ------- |
| `.github/copilot-instructions.md` | Workspace-wide guidance that applies to all chats |
| `.instructions.md` | Task- or file-specific guidance (e.g., "use British English") |
| `AGENTS.md` (experimental) | A newer, cross-platform format for defining Copilot's behavior across tools |

> **Analogy:** These are your "house rules" for how Copilot should act.

### Copilot Prompt Files (`.prompt.md`)

Reusable templates that tell Copilot **what to do** for specific tasks.

**Example:** A prompt file could say: *"Summarize all meeting notes from this folder into a single report."*

These prompts can include frontmatter (model, tools, chat mode) so that Copilot runs with the right setup every time.

> **Analogy:** Think of them as reusable recipes for AI tasks.

---

## E

### Extension / Global Prompt Files

Pre-built prompts that come with VS Code extensions or Copilot itself.

You can't edit them directly, but you can copy them locally if you want to customize them.

> **Analogy:** Think of them as ready-made templates built by others.

---

## F

### Folder

A folder is a directory within your workspace that contains related files. You can set specific configurations just for that folder.

**Example:** One folder might hold meeting notes while another holds automation scripts, each with their own settings.

### Frontmatter

Frontmatter refers to a small block of text placed at the **top of a Markdown file**, written between three dashes `---`. It contains settings or configuration options that tell Copilot how to treat that file.

**Example** (in a `.chatmode.md` or `.prompt.md` file):

```yaml
---
description: "Review code for readability and performance"
model: GPT-4o
tools: ["search/codebase", "githubRepo"]
---
```

Everything between those `---` lines is the frontmatter. It's not something Copilot "reads" like normal text — it's **metadata** that tells VS Code how to run the prompt or mode:

| Field | What It Does |
| ----- | ------------ |
| `description` | Explains what this file does |
| `model` | Defines which AI model Copilot should use |
| `tools` | Lists which features Copilot is allowed to access while running it |

> **Analogy:** Think of frontmatter like a control panel at the top of a file — it sets the parameters before Copilot actually runs the rest of the instructions below.

---

## G

### GitHub Copilot

Copilot is your **built-in AI assistant** inside VS Code. It predicts, suggests, and generates content as you type — like autocomplete, but far more capable. It can help you draft documents, write code, explain scripts, or format data.

It learns from the context of what you're doing in your workspace and can adjust based on your settings or instructions.

### GitHub Copilot Chat

This is the **conversational interface** within VS Code that lets you talk to Copilot in plain language. You can ask things like, *"Summarize this document"* or *"Find errors in this formula,"* and it will respond based on your open files.

> **Analogy:** It's like Teams Chat, but with an AI that knows what's in your workspace.

---

## M

### MCP Server (Model Context Protocol Server)

The MCP server is a **local bridge** that connects Copilot in VS Code to other systems you use, like Azure DevOps, Teams, or Outlook.

It allows Copilot not just to suggest actions, but to **perform them** — using your secure credentials.

**Example:** Copilot can create or update Azure DevOps work items directly, instead of just listing them.

> **Analogy:** If Copilot is your brainy assistant, the MCP server gives it *hands* to actually carry out tasks in your other apps.

### Model

In Copilot's settings or frontmatter, "model" refers to the **specific AI engine** being used (for example, GPT-4o).

Different models have different strengths: some are faster, some are more reasoning-focused.

> **Analogy:** It's like choosing between a quick brainstorm partner or a deep analyst.

---

## T

### Tools

Tools are **extensions of Copilot's abilities** — for example, `search/codebase` lets it look through your files, or `githubRepo` lets it fetch data from GitHub.

You can specify which tools a prompt or mode can use in the frontmatter. They define what Copilot has access to.

---

## U

### User Profile

Your **personal VS Code environment**. It keeps your themes, extensions, and personal prompt files that travel with you, no matter which project (workspace) you open.

> **Analogy:** Your backpack — it holds your personal preferences wherever you go.

### User Prompt Files

Your personal prompt templates that live in your **user profile**.

**Example:** A "Rephrase professionally" prompt you use in any project.

They're private and travel with your VS Code setup.

---

## V

### Visual Studio Code (VS Code)

VS Code is Microsoft's **free, lightweight workspace** for text, documents, and code. It's like a super-powered Notepad that helps you organize, edit, and search across all your project files in one place.

It's used by both developers and non-developers as a "command center" for managing documents, scripts, and AI interactions.

### .vscode Folder

A hidden folder inside your workspace that stores **workspace-specific settings**, such as:

- Which extensions are active
- What themes you use
- Where your local prompts live

You don't need to edit it manually, but it's where VS Code remembers how you've customized that workspace.

### VS Code Extension

An **add-on** that gives VS Code new powers — like spell-checking, Markdown previewing, or running Copilot Chat.

Extensions are installed from the Marketplace and can be turned on or off per workspace.

---

## W

### Workspace

A workspace is the **full set of folders and files** you've opened in VS Code — your current project view. Workspace settings apply to everything inside that open project.

> **Analogy:** Think of it as your "whole desk," where you might have multiple folders and subfolders open for one project.

### Workspace Prompt Files

Prompt templates that live in your **project folder** and are shared with everyone working in that workspace.

**Example:** A "Generate Summary" prompt for all team members.

They ensure consistent Copilot responses across the team.

---

## Quick Reference Table

| Term | One-Line Summary |
| ---- | ---------------- |
| **applyTo** | Frontmatter field that filters which file types an instruction applies to |
| **Chat Mode** | A persona/role that changes how Copilot behaves in a conversation |
| **Copilot** | AI assistant in VS Code that predicts, suggests, and generates content |
| **Copilot Chat** | Conversational interface to talk to Copilot in plain language |
| **Copilot Instructions** | Markdown files that define standing rules for Copilot behavior |
| **Extension** | Add-on that gives VS Code new capabilities |
| **Folder** | A directory within your workspace with its own settings |
| **Frontmatter** | YAML metadata at the top of a file (between `---` lines) |
| **MCP Server** | Local bridge connecting Copilot to external tools like ADO |
| **Model** | The AI engine Copilot uses (e.g., GPT-4o) |
| **Prompt File** | Reusable template telling Copilot what to do for a task |
| **Tools** | Features Copilot can access (search, GitHub, etc.) |
| **User Profile** | Your personal VS Code environment that travels with you |
| **VS Code** | Microsoft's free, lightweight code/text editor |
| **Workspace** | The full set of folders/files open in your current VS Code session |

---

[← Back to Main](README.md)

## W

**Workspace** - <!-- Definition to be added -->

---

[← Back to Main](README.md)
