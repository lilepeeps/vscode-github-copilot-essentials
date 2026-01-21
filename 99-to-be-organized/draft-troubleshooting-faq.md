# ❓ Troubleshooting & Frequently Asked Questions

> **STATUS:** Draft - needs review
>
> **PROPOSED LOCATION:** Could be a standalone page or appendix section

---

## Overview

Running into issues? This page covers the most common problems beginners face with VS Code and GitHub Copilot, along with quick solutions.

---

## VS Code Issues

### "I can't find my files in VS Code"

**Problem:** You opened VS Code but don't see any files.

**Solution:**
1. You need to open a **folder** first
2. Go to **File > Open Folder**
3. Navigate to the folder containing your files
4. Click **Select Folder**

> [!TIP]
> VS Code works best with folders (workspaces), not individual files. Always open the parent folder of your project.

---

### "The interface looks different from the screenshots"

**Problem:** Your VS Code doesn't match what you see in tutorials.

**Possible reasons:**
- Different color theme
- Sidebar is hidden
- Different extensions installed
- VS Code version differences

**Solutions:**
| Issue | Fix |
| ----- | --- |
| Want to change theme | `Ctrl+K Ctrl+T` to browse themes |
| Sidebar missing | Press `Ctrl+B` to toggle |
| Panel missing | Press `Ctrl+J` to toggle |
| Want default layout | **View > Appearance > Reset Layout** |

---

### "VS Code is running slowly"

**Problem:** VS Code feels sluggish or freezes.

**Solutions:**
1. **Close unused tabs** — too many open files use memory
2. **Disable unused extensions** — go to Extensions, disable ones you don't need
3. **Restart VS Code** — sometimes it just needs a refresh
4. **Check for large files** — VS Code can struggle with very large files (100MB+)

---

### "I accidentally closed something and can't get it back"

**Problem:** You closed a panel, sidebar, or file and don't know how to restore it.

**Quick fixes:**

| What You Lost | How to Restore |
| ------------- | -------------- |
| Sidebar | Press `Ctrl+B` |
| Terminal/Panel | Press `Ctrl+J` |
| Explorer view | Press `Ctrl+Shift+E` |
| A closed file | `Ctrl+Shift+T` (reopens last closed) |
| Everything looks wrong | **View > Appearance > Reset Layout** |

---

## GitHub Copilot Issues

### "Copilot isn't giving me any suggestions"

**Problem:** You're typing but no gray suggestions appear.

**Checklist:**
1. ✅ Is Copilot enabled? Check the status bar (bottom right) for the Copilot icon
2. ✅ Are you signed in? Look for prompts to authenticate
3. ✅ Is your subscription active? Check with your organization or GitHub account
4. ✅ Is the file type supported? Copilot works best with common file types

**To manually enable Copilot:**
1. Click the Copilot icon in the status bar
2. Select **Enable Completions**

---

### "Copilot keeps asking me to sign in"

**Problem:** You've signed in but keep getting prompted again.

**Solutions:**
1. **Sign out and back in:**
   - Open Command Palette (`Ctrl+Shift+P`)
   - Type: `GitHub Copilot: Sign Out`
   - Then: `GitHub Copilot: Sign In`

2. **Check your GitHub account:**
   - Make sure you're using the account with Copilot access
   - If using a work account, verify Copilot is enabled for your organization

3. **Clear credentials:**
   - Open Command Palette
   - Type: `Clear Editor History`
   - Restart VS Code

---

### "Copilot suggestions are not helpful"

**Problem:** Suggestions don't match what you want.

**Tips to improve suggestions:**
1. **Add more context** — Copilot uses surrounding text to predict
2. **Write a comment first** — describe what you want, then let Copilot generate
3. **Be specific in file names** — `meeting-notes-january.md` gives more context than `notes.md`
4. **Use Copilot Chat instead** — for complex requests, chat is often better than inline suggestions

**Example:**
```markdown
<!-- Instead of just typing, add a comment first: -->

<!-- Write a professional email declining a meeting due to schedule conflict -->

Dear [Name],
```

Copilot will use your comment to generate more relevant content.

---

### "Copilot Chat isn't responding"

**Problem:** Chat panel is open but Copilot doesn't reply.

**Solutions:**
1. **Check your internet connection** — Copilot needs internet access
2. **Wait a moment** — sometimes responses take a few seconds
3. **Restart the chat** — click the `+` to start a new conversation
4. **Reload VS Code** — `Ctrl+Shift+P` > `Developer: Reload Window`

---

### "Copilot gave me incorrect information"

**Problem:** Copilot's response was wrong or outdated.

**Important to remember:**
- Copilot is an AI assistant, not a fact-checker
- It can make mistakes or have outdated information
- Always verify important information from other sources

**Best practices:**
- ✅ Use Copilot for drafts, formatting, and brainstorming
- ✅ Review and edit all AI-generated content
- ❌ Don't rely on Copilot for critical facts without verification

---

## Workspace & Settings Issues

### "My settings aren't being applied"

**Problem:** You changed a setting but nothing happened.

**Check the scope:**
- **User settings** — apply everywhere (your personal defaults)
- **Workspace settings** — apply only to this project
- Workspace settings override user settings

**To check:**
1. Open Settings (`Ctrl+,`)
2. Look at the tabs: **User** vs **Workspace**
3. Make sure you're editing the right one

---

### "My Copilot instructions aren't working"

**Problem:** You created a `copilot-instructions.md` file but Copilot ignores it.

**Checklist:**
1. ✅ Is the file in the right location? Should be `.github/copilot-instructions.md`
2. ✅ Is the folder open as a workspace? Instructions only apply to open workspaces
3. ✅ Is the file named correctly? Must be exactly `copilot-instructions.md`
4. ✅ Is Copilot Chat using it? Instructions apply to Chat, not always inline suggestions

---

## General FAQ

### "Do I need to be online to use VS Code?"

**VS Code itself:** Works offline for editing files.

**GitHub Copilot:** Requires internet connection — it sends requests to AI servers.

---

### "Is my data safe with Copilot?"

GitHub Copilot:
- Sends code/text snippets to cloud servers to generate suggestions
- Check your organization's policies on AI tools
- For sensitive content, consider disabling Copilot temporarily

> [!IMPORTANT]
> Review your organization's guidelines on using AI assistants with confidential information.

---

### "Can I use Copilot for languages other than English?"

Yes! Copilot can:
- Understand prompts in many languages
- Generate content in various languages
- Translate between languages

Try asking: "Write this in French" or "Translate to Spanish"

---

### "How do I update VS Code and Copilot?"

**VS Code:**
- Usually updates automatically
- Or: **Help > Check for Updates**

**Copilot extension:**
- Go to Extensions (`Ctrl+Shift+X`)
- If an update is available, you'll see an **Update** button
- Or: Click the `...` menu > **Check for Extension Updates**

---

## Still Stuck?

If your issue isn't covered here:

1. **Search the Command Palette** — type what you're trying to do
2. **Check VS Code documentation** — [code.visualstudio.com/docs](https://code.visualstudio.com/docs)
3. **Search online** — "VS Code [your problem]" usually finds answers
4. **Ask Copilot!** — Try asking Copilot Chat about your VS Code question

---

## Video Tutorials

> 📺 **Video placeholders for this section:**
> - Common beginner mistakes and how to fix them
> - Troubleshooting Copilot connection issues
> - Resetting VS Code to defaults
