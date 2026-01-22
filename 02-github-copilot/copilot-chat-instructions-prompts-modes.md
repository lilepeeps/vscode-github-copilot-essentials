# GitHub Copilot Chat – Instructions, Prompts and Chat Modes

GitHub Copilot Chat is a specific interface of Copilot that lets you interact using natural language chat. Think of it as an **AI agent within VS Code** that you can talk to about your code or content.

What makes Copilot Chat particularly powerful is the ability to customise its behaviour through different layers of context. In Copilot Chat, three concepts work together: **Prompts**, **Chat Modes**, and **Copilot Instructions**. Understanding each will help you get the most out of the AI and know when to use which.

> 📺 **Video**: Navigating the Chat UI
>
> <!-- TODO: Replace with YouTube embed/link when ready -->
> 🎬 *Video placeholder: `GitHub Copilot Chat - Navigating the Chat UI.mp4`*

---

## Copilot Instructions

> 📺 **Video**: Using Instruction Files in GitHub Copilot
>
> <!-- TODO: Replace with YouTube embed/link when ready -->
> 🎬 *Video placeholder: `Using Instruction Files in GitHub Copilot.mp4`*

These are preferences that apply in your Copilot interactions. There are three different types of instructions that can be created for GitHub Copilot:

### `.github/copilot-instructions.md`

Instructions files that **automatically apply to all chat requests** in the workspace. They are stored within the workspace.

### `.instructions.md`

Instructions created for **specific tasks or files**. The `applyTo` format defines which file types this instruction file should be applied to (e.g., you can develop instructions that only apply when markdown `.md` files are being used). They are stored in the workspace or the user profile.

### `AGENTS.md` (experimental)

Instruction files that can work **cross-platform**. Think of them as a format commonly showing up across other chat-based code assistants. It's like a `copilot-instructions.md` file but can be set centrally and then used across other tools (like VS Code, OpenAI/Codex CLI, Roo Code, Cursor, Zed, Claude Code).

### Instructions Comparison

| Type | Description | Scope / Applies To | Storage Location | Unique Features |
| ---- | ----------- | ------------------ | ---------------- | --------------- |
| **`.github/copilot-instructions.md`** | A workspace-level instructions file that applies to all chat interactions automatically. Defines general behavior, tone, and preferences for Copilot within that workspace. | All chat requests in the workspace | Within the workspace (usually in `.github` folder) | Default and most common instructions file; automatically recognized without configuration |
| **`.instructions.md`** | One or more files that define targeted or task-specific guidance. Can use the `applyTo` frontmatter to specify which files or file types they apply to. | Specific files or tasks defined via `applyTo` | Stored either in workspace or user profile | Granular control—lets you tailor Copilot's behavior for different folders, languages, or scenarios |
| **`AGENTS.md`** (experimental) | A single root-level file that defines guidance for multiple AI agents operating within a workspace. | All AI agents in the workspace | Root of the workspace | Useful when working with multiple agent platforms; ensures consistent shared context across them |

---

## Copilot Prompt Files

> 📺 **Video**: Prompts in GitHub Copilot
>
> <!-- TODO: Replace with YouTube embed/link when ready -->
> 🎬 *Video placeholder: `Prompts in GH Copilot.mp4`*

These are **reusable templates** that define how Copilot should respond to specific types of requests. Prompt files are written in Markdown (`.prompt.md`) and can include metadata that specifies which chat mode, model, and tools Copilot should use when executing them.

They allow you to **standardize and reuse complex prompts** without retyping them each time.

There are three main types of prompt files:

### Workspace Prompt Files

Shared across everyone working in the same project or repository. They live inside the workspace (commonly in `.vscode/prompts/` or `.github/prompts/`) and are automatically loaded when the workspace opens.

They can include frontmatter that defines the model, tools, and chat mode to use for specific tasks (for example, "use GPT-4o with the code search tool in agent mode").

> [!TIP]
> **Ideal for:** Shared, team-wide tasks such as generating summaries, writing documentation, or reviewing pull requests.

### User Prompt Files

Your personal prompt files stored in your user profile. They travel with your VS Code environment and are available across all workspaces.

You can use them to automate frequent tasks like explaining code, generating test cases, or formatting markdown. They also support the same metadata fields as workspace prompts, so you can lock in preferred models or tools globally.

### Extension or Global Prompt Files

Prompts bundled with VS Code extensions or Copilot itself. They provide ready-made templates (for example, "Generate unit test" or "Add docstring").

They appear automatically when the extension is installed and can't be edited directly, but you can copy them into your workspace or user prompt folder and customize the model, toolset, or behavior.

### Prompt Files Comparison

| Type | Description | Scope / Applies To | Storage Location | Tool / Model / Mode Support | Unique Features |
| ---- | ----------- | ------------------ | ---------------- | --------------------------- | --------------- |
| **Workspace Prompt Files** | Markdown prompt templates shared across a project or repo. Can define specific Copilot modes, tools, and models for consistent task execution. | All users in the same workspace | Within the workspace (typically `.vscode/prompts/` or `.github/prompts/`) | ✅ Full support via frontmatter: mode, model, tools | Enables team-wide consistency; can pre-define specialized modes or tool access (e.g. code search or repo fetch) |
| **User Prompt Files** | Personal prompt templates that travel with your VS Code profile and can be used across any workspace. | Individual user | In user profile directory (`~/.config/Code/User/prompts/` or `%APPDATA%\Code\User\prompts/`) | ✅ Full support via frontmatter | Lets you keep personal productivity prompts without affecting shared workspaces |
| **Extension / Global Prompt Files** | Prompt templates packaged with VS Code or extensions that appear automatically in chat. | Any workspace where the extension is enabled | Extension directory (read-only) | ✅ Generally supported but defined by the extension developer | Provide prebuilt, ready-to-use prompt templates; can be cloned and customized locally |

---

## Copilot Chat Modes

Chat Modes define **how Copilot behaves** during a conversation — the role it takes, the tools it can use, and even which model it runs on.

They let you create focused "personas" for Copilot so that you can quickly switch between, for example, a code reviewer, a debugging assistant, or a planning advisor.

Chat Modes are defined using `.chatmode.md` files written in Markdown with frontmatter that specifies configuration details.

There are three main ways chat modes can be created and applied:

### Workspace Chat Modes

Chat mode files that live inside your project or repository and are available to everyone working in that workspace. They're typically stored in a `.github/chatmodes/` or `.vscode/chatmodes/` folder and automatically load when the workspace is opened.

You can define properties such as `description`, `model`, and `tools`, as well as custom guidance for how Copilot should act in that mode.

> [!TIP]
> **Ideal for:** Creating shared personas like "Project Architect" or "QA Reviewer"

### User Chat Modes

Personal chat modes stored in your user profile and available across all workspaces. They let you define your own reusable roles and preferred setups, such as "Fast Drafting Mode" or "Explain Like I'm Five Mode."

Because they live in your user profile, they don't sync to repositories or affect teammates.

### Extension or Global Chat Modes

Some extensions or tools can bundle their own chat modes. These modes appear automatically when the extension is active and provide pre-configured contexts — for instance, a Python extension could include a "Data Analysis Mode" that gives Copilot access to notebook tools.

While you can't edit these directly, you can copy them into your workspace to customize or expand them.

### Chat Modes Comparison

| Type | Description | Scope / Applies To | Storage Location | Tool / Model / Configuration Support | Unique Features |
| ---- | ----------- | ------------------ | ---------------- | ------------------------------------ | --------------- |
| **Workspace Chat Modes** | Define shared, project-level Copilot "personas" that can switch how chat behaves. Can specify tools, models, and behavior directly in frontmatter. | Everyone working in the same workspace | Inside the workspace (typically `.vscode/chatmodes/` or `.github/chatmodes/`) | ✅ Full frontmatter support for description, model, tools, and behavior rules | Enables consistent team-wide roles or workflows such as "Code Reviewer" or "Documentation Assistant" |
| **User Chat Modes** | Personal chat modes available across all your workspaces. Let you create your own preferred roles or shortcuts. | Individual user | In user profile directory (`~/.config/Code/User/chatmodes/` or `%APPDATA%\Code\User\chatmodes/`) | ✅ Full frontmatter support | Private to you; great for creating reusable "mental modes" that fit your personal workflow |
| **Extension / Global Chat Modes** | Chat modes provided by extensions or by VS Code itself. Appear automatically when the extension is installed. | Any workspace with the extension enabled | Bundled within the extension (read-only) | ✅ Defined by the extension developer | Offer specialized modes (e.g. debugging, documentation) that integrate with language or tool extensions |

---

## Summary of GitHub Copilot Chat Functionality

These three layers work together in every Copilot Chat interaction. When you ask Copilot something in chat, the system takes into account:

1. **Your prompt** (the immediate question or command)
2. **Any active chat mode** (the role/persona Copilot is using)
3. **Your persistent instructions** (background preferences)

### Example in Action

Imagine you have:
- A **Copilot Instruction** set to "Be very brief in responses"
- A **"Fix code" chat mode** turned on
- A **prompt**: "Improve the efficiency of this algorithm"

The answer you get will likely be:
- **Concise** (due to the instruction)
- **Focused on refactoring the code** (due to Fix mode)

Without those settings, you might have gotten a longer, more exploratory answer.

### When to Use Which

| Scenario | What to Use |
| -------- | ----------- |
| **One-time answer or action** | Just type a prompt in plain language. This is your go-to for ad hoc questions or commands. |
| **Series of questions with a certain style** | Select a **chat mode** to align with your current phase of work (reviewing vs coding, brainstorming vs editing). Saves you from re-explaining your intent in every prompt. |
| **Overarching preference that should always apply** | Set it in **Copilot instructions**. For example: your project's name/domain, or "use UK English spelling" so you don't have to correct American spellings each time. |

### Combining the Layers

By combining these, Copilot Chat becomes a very flexible assistant.

**Example workflow:**
1. **Instruct** Copilot globally to "Answer any questions with a business-friendly tone"
2. **Switch** to a Project Management mode when working on task lists
3. **Prompt**: "Draft an update email for the client about project X status"

The result would:
- Respect your tone instruction
- Use the mode's knowledge to highlight tasks
- Directly answer your prompt by generating the email text

If the result isn't what you want, you can tweak one of the layers: maybe instruct it to be more detailed, or switch to a different mode, and ask again. This ability to fine-tune how the AI behaves is what makes Copilot Chat more powerful than a generic Q&A bot.

> [!NOTE]
> Copilot Chat is evolving. The exact modes available or how you set instructions may change as the product develops, but the concept of these layers will likely remain. Also, **always double-check Copilot's outputs**, especially when it's acting on your code or important documents – you remain the ultimate decision maker.

---

[← Back to GitHub Copilot](README.md) | [Next: MCP Server →](mcp-server.md)
