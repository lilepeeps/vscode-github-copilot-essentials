# MCP Server – Tools to Extend Your Copilot Chat Experience

---

## Making Sense of the MCP Server

The term "MCP server" might sound technical, but in practice, it's quite simple. You can think of it as a **local "bridge"** that helps VS Code and GitHub Copilot work together with other systems you use—like Azure DevOps, Teams, or Outlook.

Normally, Copilot helps you write text or code. The MCP server takes that one step further: it lets Copilot actually **do things** in other tools, using your own secure access.

**Example:** Copilot can not only suggest a list of tasks from your meeting notes—it can also, through the MCP server, go ahead and **create those tasks in Azure DevOps (ADO)** for you.

### How It Works

In this context, "MCP" is the integration layer we use so Copilot can talk to Azure DevOps. It:

- Runs **locally inside VS Code**
- Uses your **authenticated session** to act on your behalf
- Lets Copilot safely perform real actions—like creating or updating work items in ADO—without you needing to switch tools or copy-paste anything

---

## Why Would We Want to Use an MCP Server

Think of how much time gets lost moving information from one place to another:

1. You summarize a meeting in Teams
2. Then manually create tasks in Azure DevOps
3. Update their statuses
4. Add notes

It's repetitive, it's easy to make mistakes, and it takes you out of focus.

### The MCP Difference

MCP server provides you the tools to **automate that "last mile" of work**. Instead of just giving you suggestions, Copilot can now follow through and get things done.

It uses your credentials to perform actions securely in your connected systems—**no separate logins, no special tokens to manage**.

| Without MCP | With MCP |
| ----------- | -------- |
| Copilot suggests "Here are five follow-up tasks from the meeting" | Copilot suggests the tasks |
| You manually create each task in ADO | You type "approve" |
| You set parent/child relationships | MCP creates the tasks automatically |
| You add tags and links | Tasks appear on your board with relationships, tags, and links |

> [!TIP]
> It's the difference between Copilot being a **smart assistant** and being an **actual teammate** who can carry out the plan.

---

## Combining MCP with Copilot Customization in VS Code

While Copilot Chat defines **how you interact** with the AI, the MCP server defines **what the AI can actually do** inside and beyond VS Code.

When you bring these together, you get a powerful setup that's not only personalized to your workflow but also capable of taking real actions in your connected tools—like Azure DevOps, Teams, or Outlook.

### The Simple Way to Think About It

| Component | What It Does |
| --------- | ------------ |
| **Copilot Instructions, Prompts, and Chat Modes** | Tell Copilot *how to think and respond* |
| **MCP Server** | Gives Copilot *hands*—the ability to act in your other tools |

By combining the two, you can create a workflow where Copilot not only **understands your intent** but can also **carry it out automatically**, within your rules and context.

---

## Example: A Custom Copilot Workflow with MCP

Imagine you're a **Technical Program Manager** responsible for maintaining the data quality of work items in Azure DevOps.

### Your Setup

**1. Chat Mode:** You've set up a Chat Mode called **"Data Quality Analyst Mode"** that tells Copilot to focus on identifying gaps, inconsistencies, and naming issues across ADO items.

**2. Copilot Instruction:** You've created a workspace-level instruction file that says:

> *"Always follow Azure DevOps naming conventions, flag incomplete fields, and prepare bulk updates for approval."*

**3. Prompt File:** You have a prompt file called `review-work-item-quality.prompt.md` that summarizes your intent:

> *"Review all ADO work items in the current sprint for missing estimates, inconsistent titles, and non-standard tags. Summarize issues and prepare correction suggestions."*

### How It All Comes Together

```
┌─────────────────────────────────────────────────────────────────┐
│  1. Open VS Code workspace connected to your ADO project        │
├─────────────────────────────────────────────────────────────────┤
│  2. Switch Copilot into "Data Quality Analyst Mode"             │
│     → Activates the behaviors defined in that chat mode         │
├─────────────────────────────────────────────────────────────────┤
│  3. Run the review-work-item-quality prompt                     │
│     → Asks Copilot to analyze your ADO backlog                  │
├─────────────────────────────────────────────────────────────────┤
│  4. Copilot reads your workspace Instructions                   │
│     → Reports missing values, standardizes field names,         │
│       generates correction suggestions                          │
├─────────────────────────────────────────────────────────────────┤
│  5. Review results in chat, make edits, type "Approve"          │
├─────────────────────────────────────────────────────────────────┤
│  6. MCP server steps in                                         │
│     → Uses your Azure credentials to apply updates directly     │
│       in Azure DevOps (fixing titles, filling fields,           │
│       adding tags)                                              │
└─────────────────────────────────────────────────────────────────┘
```

### The Result

The process feels natural and controlled:

- You define **how Copilot behaves** (via the chat mode and instructions)
- You define **what it should do** (via the prompt)
- **MCP takes care of executing** those updates securely in Azure DevOps

> [!NOTE]
> What used to take an afternoon of manual review and editing now happens in **minutes**, with full traceability and consistent standards across your team's backlog.

---

## 🌟 Connecting to MCP + Prompt Files

> 📺 **Video**: Connecting to MCP + Prompt Files
>
> <!-- TODO: Replace with YouTube embed/link when ready -->
> 🎬 *Video placeholder: `Connect to MCP + Prompt Files.mp4`*

---

[← Back to GitHub Copilot](README.md) | [← Previous: Copilot Chat](copilot-chat-instructions-prompts-modes.md)
