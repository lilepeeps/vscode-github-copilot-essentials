# What GitHub Copilot Can Do

> 📺 **Video**: What Can GitHub Copilot Do?
>
> <!-- TODO: Replace with YouTube embed/link when ready -->
> 🎬 *Video placeholder: `What can GitHub Copilot do.mp4`*

---

## Overview

Here's what Copilot does at a high level:

| Capability | What it does |
| ---------- | ------------ |
| **Inline Suggestions** | Real-time text/code suggestions as you type |
| **Code & File Generation** | Generate larger blocks of content from prompts |
| **Adjusting Existing Content** | Refactor or reformat existing code/text |
| **Chat** | Conversational Q&A with awareness of your workspace |

---

## Inline Suggestions

As you type, Copilot can suggest the next bit of code or text in real-time. It uses context from the current file and related files to predict what you might want.

**Example:** If you start writing a comment like `// function to calculate sum…`, Copilot might automatically suggest the entire function implementation. Or if you're editing a PowerShell script and type a command, Copilot could propose the subsequent commands.

These suggestions show up **faded right in your editor**; you can accept them (press `Tab` or `Enter`) or ignore them.

> [!TIP]
> It feels like autocomplete on steroids – sometimes even multi-line snippets or boilerplate code just appear, saving you from looking up syntax.

---

## Code & File Generation

You can also ask Copilot to generate larger blocks of content. By writing a descriptive comment or prompt, you might get an entire file or function generated.

**Example:** If you have a JSON outline for a report, Copilot might help flesh it out into a draft document structure.

It's trained on a wide array of coding patterns and text, so it can produce anything from:

- HTML code for a webpage
- Configuration files
- Structured data formats
- Documentation templates

> [!NOTE]
> **For non-developers:** Think of it as having an AI that knows how to write in many "languages" – not just human languages, but programming languages and structured text formats. It tries to optimize your work by handling the repetitive or template-like parts for you.

---

## Adjusting Existing Content

Copilot isn't only for new text – it can help **refactor or adjust existing code**.

**Example:** You can select a block of code and write a comment like `// simplify this logic` and Copilot will attempt to rewrite the code in a simpler or different way.

Similarly, if you have a chunk of text (say a list of tasks in bullet form) and you want them in a different format (like a JSON list or slightly reworded), Copilot can often do that via the chat interface.

> [!TIP]
> This feature is very handy for quickly applying repetitive changes or trying out improvements without manually retyping everything.

---

## Chat

In addition to inline suggestions, GitHub Copilot offers a **Chat mode** (via the GitHub Copilot Chat extension in VS Code).

This opens a side panel where you can have a conversational Q&A or command session with the AI – akin to using a chatbot like Copilot in M365, but with **deep awareness of your code/workspace**.

### What You Can Do with Chat

| Action | Example |
| ------ | ------- |
| **Ask questions** | "Hey Copilot, how does this function work?" |
| **Find issues** | "Find errors in my spreadsheet formula" |
| **Give instructions** | "Add comments to this code explaining each step" |
| **Get explanations** | "What does this script do?" |

Copilot will analyze the open files to answer, then output results which you can review and accept.

> [!NOTE]
> **For non-developers:** This mode is great because you don't need to know the exact code or command; you can describe what you want in plain English and Copilot tries to do it or guide you.

We'll dive into how to customise the chat in the [next section](copilot-chat-instructions-prompts-modes.md).

---

[← Back to GitHub Copilot](README.md) | [Next: Copilot Chat →](copilot-chat-instructions-prompts-modes.md)
