# ⏱️ Your First 10 Minutes in VS Code

> **STATUS:** Draft - needs review
>
> **PROPOSED LOCATION:** `01-visual-studio-code/first-10-minutes.md` or part of getting started section

---

## Overview

You've installed VS Code and Copilot. Now what? This hands-on guide walks you through your first 10 minutes, getting you comfortable with the basics.

**Goal:** By the end, you'll know how to navigate VS Code, open files, and have your first conversation with Copilot.

---

## Minute 1-2: Understanding the Layout

When you open VS Code, here's what you're looking at:

```
┌─────────────────────────────────────────────────────────────────┐
│  Menu Bar (File, Edit, View, etc.)                              │
├──────────┬──────────────────────────────────────────────────────┤
│          │                                                      │
│  Activity│           Editor Area                                │
│   Bar    │     (where you edit files)                          │
│          │                                                      │
│  [Files] │                                                      │
│  [Search]│                                                      │
│  [Git]   │                                                      │
│  [Debug] │                                                      │
│  [Ext]   │                                                      │
│  [Copilot│──────────────────────────────────────────────────────┤
│   Chat]  │           Panel (Terminal, Output, Problems)         │
│          │                                                      │
├──────────┴──────────────────────────────────────────────────────┤
│  Status Bar (current file info, notifications)                  │
└─────────────────────────────────────────────────────────────────┘
```

### Key Areas to Know

| Area | What It Does | How to Find It |
| ---- | ------------ | -------------- |
| **Activity Bar** | Switch between different views | Left side icons |
| **Side Bar** | Shows files, search results, etc. | Opens when you click Activity Bar icons |
| **Editor** | Where you read and edit files | Center of the screen |
| **Panel** | Terminal, output, problems | Bottom (may be hidden by default) |
| **Status Bar** | Info about current file | Very bottom |

---

## Minute 3-4: Open a Folder (Create Your Workspace)

VS Code works best when you open a **folder** (not just individual files). This becomes your "workspace."

### Try It Now

1. Click **File > Open Folder** (or `Ctrl+K Ctrl+O`)
2. Navigate to (or create) a folder for practice — e.g., `Documents/VS Code Practice`
3. Click **Select Folder**

You should now see:
- The folder name in the **Explorer** panel on the left
- An empty or populated file list depending on what's in that folder

> [!TIP]
> **For non-developers:** Think of opening a folder like opening a project in any other app. Everything in that folder is now accessible from VS Code's sidebar.

---

## Minute 5-6: Create and Edit a File

### Create a New File

1. In the Explorer panel, right-click and choose **New File**
2. Name it `my-notes.md` (the `.md` means it's a Markdown file)
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
- The file tab shows a **dot** (●) meaning unsaved changes
- Press `Ctrl+S` (or `Cmd+S` on Mac) to save

---

## Minute 7-8: Try Copilot Inline Suggestions

Now let's see Copilot in action!

### Experiment 1: Let Copilot Complete Your Thoughts

1. At the bottom of your file, type: `## My goals for this week`
2. Press Enter and start typing: `- Finish the`
3. **Watch for gray text** — that's Copilot suggesting how to complete your sentence
4. Press `Tab` to accept, or keep typing to ignore

### Experiment 2: Let Copilot Generate a List

1. Type: `## Meeting agenda for project kickoff`
2. Press Enter and type: `1.`
3. Copilot may suggest entire agenda items — accept what makes sense!

> [!NOTE]
> Copilot learns from context. The more you type, the better its suggestions become.

---

## Minute 9-10: Have Your First Chat with Copilot

The Chat interface is where Copilot really shines for non-developers.

### Open Copilot Chat

1. Click the **Copilot Chat icon** in the Activity Bar (left side)
   - Or press `Ctrl+Alt+I` (Windows) / `Cmd+Option+I` (Mac)
2. A chat panel opens

### Try These Prompts

Type any of these and press Enter:

| Prompt | What Copilot Will Do |
| ------ | -------------------- |
| "Summarize this document" | Gives you a summary of the open file |
| "Rewrite this as bullet points" | Reformats selected text |
| "What file types can I create in VS Code?" | Answers your question |
| "Help me write a professional email about project delays" | Drafts content for you |

### Pro Tip: Select Text First

1. In your editor, **select some text** (highlight it)
2. Then ask Copilot: "Make this more concise"
3. Copilot will rewrite just the selected portion

---

## 🎉 Congratulations!

In 10 minutes, you've learned to:

- ✅ Navigate the VS Code interface
- ✅ Open a folder as your workspace
- ✅ Create and edit files
- ✅ Use Copilot's inline suggestions
- ✅ Chat with Copilot

---

## What's Next?

| Want to... | Go to... |
| ---------- | -------- |
| Learn keyboard shortcuts | [Essential Shortcuts](draft-keyboard-shortcuts.md) |
| Understand workspaces better | [Understanding Where Things Live](../01-visual-studio-code/what-is-visual-studio-code.md#understanding-where-things-live-in-vs-code) |
| Customize Copilot's behavior | [Copilot Chat – Instructions, Prompts and Modes](../02-github-copilot/copilot-chat-instructions-prompts-modes.md) |

---

## Video Tutorials

> 📺 **Video placeholders for this section:**
> - Tour of the VS Code interface
> - Creating your first workspace
> - Your first Copilot conversation
