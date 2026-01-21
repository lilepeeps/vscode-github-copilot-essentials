---
title: Your First 10 Minutes in VS Code
description: A hands-on guide to get comfortable with VS Code and GitHub Copilot basics
author: Microsoft
ms.date: 2026-01-21
ms.topic: tutorial
keywords:
  - vs code
  - github copilot
  - getting started
  - tutorial
estimated_reading_time: 10
---

# Your First 10 Minutes in VS Code

## Overview

You've installed VS Code and Copilot. Now what? This hands-on guide walks you through your first 10 minutes, getting you comfortable with the basics.

**Goal:** By the end, you'll know how to navigate VS Code, open files, and have your first conversation with Copilot.

---

## Minute 1-2: Understanding the Layout

When you open VS Code, here's what you're looking at:

```text
┌─────────────────────────────────────────────────────────────────┐
│  Menu Bar (File, Edit, View, etc.)                              │
├──────────┬──────────────────────────────────────────────────────┤
│          │                                                      │
│ Activity │                     Editor Area                      │
│   Bar    │               (where you edit files)                 │
│          │                                                      │
│  [Files] │                                                      │
│ [Search] │                                                      │
│  [Git]   │                                                      │
│  [Debug] │                                                      │
│  [Ext]   │                                                      │
│ [Copilot │──────────────────────────────────────────────────────┤
│   Chat]  │           Panel (Terminal, Output, Problems)         │
│          │                                                      │
├──────────┴──────────────────────────────────────────────────────┤
│  Status Bar (current file info, notifications)                  │
└─────────────────────────────────────────────────────────────────┘
```

### Key Areas to Know

| Area             | What It Does                      | How to Find It                       |
| ---------------- | --------------------------------- | ------------------------------------ |
| **Activity Bar** | Switch between different views    | Left side icons                      |
| **Side Bar**     | Shows files, search results, etc. | Opens when you click Activity Bar icons |
| **Editor**       | Where you read and edit files     | Center of the screen                 |
| **Panel**        | Terminal, output, problems        | Bottom (may be hidden by default)    |
| **Status Bar**   | Info about current file           | Very bottom                          |

---

## Minute 3-4: Open a Folder (Create Your Workspace)

VS Code works best when you open a **folder** (not just individual files). This becomes your "workspace."

### Try It Now

1. Click **File > Open Folder** (or `Ctrl+K Ctrl+O`)
2. Navigate to (or create) a folder for practice, such as `Documents/VS Code Practice`
3. Click **Select Folder**

You should now see:

* The folder name in the **Explorer** panel on the left
* An empty or populated file list depending on what's in that folder

> [!TIP]
> **For non-developers:** Think of opening a folder like opening a project in any other app. Everything in that folder is now accessible from VS Code's sidebar.

---

## Minute 5-6: Create and Edit a File

### Create a New File

1. In the Explorer panel, right-click and choose **New File**
2. Name it `my-notes.md` (the `.md` means it's a [Markdown](https://www.markdownguide.org/basic-syntax/) file)
3. Press Enter

### Write Something

In the editor, try typing:

```markdown
# My First VS Code File

This is a test document.

## Things I want to learn
- How to use VS Code
- How to use Copilot
- How to be more productive
```

Notice:

* The file tab shows a **dot** (●) meaning unsaved changes
* Press `Ctrl+S` (or `Cmd+S` on Mac) to save

---

## Minute 7-8: Try Copilot Inline Suggestions

Now let's see Copilot in action!

### Experiment 1: Let Copilot Complete Your Thoughts

1. At the bottom of your file, type: `## My goals for this week`
2. Press Enter and start typing: `- Finish the`
3. **Watch for gray text**, that's Copilot suggesting how to complete your sentence
4. Press `Tab` to accept, or keep typing to ignore

### Experiment 2: Let Copilot Generate a List

1. Type: `## Meeting agenda for project kickoff`
2. Press Enter and type: `1.`
3. Copilot may suggest entire agenda items, accept what makes sense!

> [!NOTE]
> Copilot learns from context. The more you type, the better its suggestions become.

### Optional: Try Inline Chat

Inline Chat lets you work with Copilot directly in your document. You can generate new content, edit existing text, or reformat content you've pasted from other sources.

**To open Inline Chat:** Press `Ctrl+I` (Windows) / `Cmd+I` (Mac)

#### Generate New Content

1. Place your cursor where you want to add content
2. Press `Ctrl+I` and type: "Add a section about team members"
3. Copilot inserts the response directly into your document

#### Edit or Reformat Existing Text

1. **Select some text** in your document
2. Press `Ctrl+I` and try prompts like:
   * "Reformat this as a numbered list"
   * "Make this more concise"
   * "Fix the grammar in this paragraph"

#### Real-World Use Case: Converting Pasted Content

Copied text from a Word doc or email that looks messy? Select it and ask Copilot:

* "Convert this to proper Markdown formatting"
* "Turn this into a bulleted list"
* "Create a table from this data"

> [!TIP]
> Inline Chat is perfect for quick, targeted edits without switching to the full Chat panel.

---

## Minute 9-10: Have Your First Chat with Copilot

The Chat panel is where GitHub Copilot becomes your AI assistant for longer conversations and complex tasks.

### Open Copilot Chat

1. Click the **Copilot Chat icon** in the Activity Bar (left side)
   * Or press `Ctrl+Shift+I` (Windows) / `Cmd+Shift+I` (Mac)
2. A chat panel opens on the side

### Understand the Chat Interface

Before typing, notice a few key elements at the top of the chat input bar at the bottom:

| Element            | What It Does                                                    |
| ------------------ | --------------------------------------------------------------- |
| **Mode selector**  | Choose between Agent, Ask, Edit, or Plan mode depending on your task |
| **Model selector** | Pick which AI model powers GH Copilot (e.g., GPT-4o, Claude)    |

For now, leave these at their defaults. You can explore different modes and models later.

### Try These Prompts

First, add your file to the chat context:

1. Look for the **📌 (pin) icon** in the chat input area
2. Click it and select your `my-notes.md` file
3. The file now appears as an attachment, giving Copilot explicit access to its contents

Now try these prompts:

| Prompt                                       | What Happens                                     |
| -------------------------------------------- | ------------------------------------------------ |
| "What is this file about?"                   | Copilot reads the attached file and summarizes it |
| "Add three more items to my learning list"   | Suggests content based on your existing list     |
| "Explain what Markdown is in simple terms"   | Answers general questions                        |

### Using Context: The # Symbol

Want Copilot to reference something specific? Use `#` to add context:

* `#file` to reference a specific file
* `#selection` to reference highlighted text
* `#codebase` to search across your workspace

Example: Type `#file:my-notes.md rewrite the goals section to be more specific`

---

## Congratulations!

In 10 minutes, you've learned to:

* ✅ Navigate the VS Code interface
* ✅ Open a folder as your workspace
* ✅ Create and edit files
* ✅ Use Copilot's inline suggestions
* ✅ Chat with Copilot

---

## What's Next?

| Want to...                      | Go to...                                                                                                                  |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Learn keyboard shortcuts        | [Essential Shortcuts](../99-to-be-organized/draft-keyboard-shortcuts.md)                                                  |
| Understand workspaces better    | [Understanding Where Things Live](what-is-visual-studio-code.md#understanding-where-things-live-in-vs-code)               |
| Customize Copilot's behavior    | [Copilot Chat – Instructions, Prompts and Modes](../02-github-copilot/copilot-chat-instructions-prompts-modes.md)         |

---

## Video Tutorials

> 📺 **Video placeholders for this section:**
>
> * Tour of the VS Code interface
> * Creating your first workspace
> * Your first Copilot conversation

---

[← Back to VS Code Section](README.md) | [Next: What is VS Code? →](what-is-visual-studio-code.md)
