# AI Ecoverse: Tools for AI-Assisted Development

A comprehensive ecosystem of tools designed to enhance the AI-assisted development experience, improve transparency, and ensure proper attribution in AI-human collaborative coding.

## 🤖 Core AI Agent Tools

### [YOLO](https://github.com/trieloff/yolo)

![YOLO - AI CLI Wrapper with Worktree Isolation](https://raw.githubusercontent.com/trieloff/yolo/main/hero-banner.jpg)

AI CLI tool wrapper with worktree support. Launches AI coding assistants (Claude, Codex, Cursor, Gemini, etc.) with appropriate bypass flags and optional isolated git worktrees for safe experimentation. Supports multi-agent mode with parallel execution and automatic cleanup.

### [ai-aligned-git](https://github.com/trieloff/ai-aligned-git)

![AI-Aligned-Git](https://github.com/user-attachments/assets/38110bb1-c1d2-4e3d-ae58-2bebb18fe64c)

Git wrapper that enforces safe practices for AI coding agents. Prevents dangerous operations like `git add .`, ensures proper AI attribution, enforces commit hooks, and maintains human sign-off on all AI-generated commits.

### [ai-aligned-gh](https://github.com/trieloff/ai-aligned-gh)

![AI-Aligned-GH](https://github.com/user-attachments/assets/969463fc-4276-4ed1-8e20-6fee8aafeb3c)

Transparent GitHub CLI wrapper that automatically detects AI tool usage and ensures proper bot attribution. Uses device flow to exchange user tokens for bot tokens, so actions appear as "as-a-bot[bot] on behalf of @user" rather than appearing to come directly from the user.

### [as-a-bot](https://github.com/trieloff/as-a-bot)

GitHub App token broker running on Cloudflare Workers. Provides user-to-server GitHub tokens via device flow for ai-aligned-gh, ensuring actions show proper user attribution with app badges rather than appearing as bot-only actions.

## 🛠️ Developer Productivity Tools

### [gh-workflow-peek](https://github.com/trieloff/gh-workflow-peek)

![GH Workflow Peek](https://github.com/user-attachments/assets/451a28c1-ccb5-4bae-bb16-b94b45f9cebf)

GitHub CLI extension that intelligently filters and highlights errors in GitHub Actions workflow logs by severity. Auto-detects failed PR checks, prioritizes errors (fatal → error → warn → fail), and shows context around matches. Perfect for developers and AI agents working with limited context windows.

### [upskill](https://github.com/trieloff/upskill)

![Upskill – Install Agent Skills](https://raw.githubusercontent.com/trieloff/upskill/main/hero-banner.jpeg)

Quickly install Claude/Agent skills from other repositories. Works standalone or as a GitHub CLI extension. Copies skills, creates discovery scripts, and updates AGENTS.md with clear markers for idempotent updates.

## 📊 Transparency & Analytics

### [vibe-coded-badge-action](https://github.com/trieloff/vibe-coded-badge-action)

![Vibe Coded Badge Action](https://github.com/user-attachments/assets/0350cfe6-7631-4613-aa3e-74e2bd53eda4)

GitHub Action that analyzes repository git history to determine what percentage of commits were made by AI tools. Generates dynamic badges showing AI contribution levels with smart logo selection based on the dominant AI tool (Claude, Cursor, Gemini, Copilot, etc.).

## 📚 Libraries

### [am-i-ai](https://github.com/trieloff/am-i-ai)

![am-i-ai](https://raw.githubusercontent.com/trieloff/am-i-ai/main/hero.png)

Lightweight shell library for detecting AI coding agents. Provides robust two-phase detection (environment variables + process tree) to identify when code is running under AI control. Powers the AI detection in ai-aligned-git and ai-aligned-gh.

## 🎯 Use Cases

- **Safe Experimentation**: Use YOLO with worktree mode to test AI-generated changes in isolation
- **Proper Attribution**: Ensure all AI contributions are clearly marked in git history and GitHub
- **Efficient Debugging**: Quickly find critical errors in CI/CD logs with gh-workflow-peek
- **Skill Sharing**: Share and install AI agent skills across projects with upskill
- **Transparency**: Track and visualize AI contributions with vibe-coded-badge-action

## 🚀 Getting Started

Each tool can be installed independently. Visit the individual repository links above for detailed installation instructions and usage examples.

Most tools offer one-line installation:

```bash
# YOLO
curl -fsSL https://raw.githubusercontent.com/trieloff/yolo/main/install.sh | sh

# ai-aligned-git
curl -fsSL https://raw.githubusercontent.com/trieloff/ai-aligned-git/main/install.sh | sh

# ai-aligned-gh
curl -fsSL https://raw.githubusercontent.com/trieloff/ai-aligned-gh/main/install.sh | sh

# upskill
curl -fsSL https://raw.githubusercontent.com/trieloff/upskill/main/install.sh | bash

# gh extensions
gh extension install trieloff/gh-workflow-peek
gh extension install trieloff/upskill

# am-i-ai (detection library, used by ai-aligned-git/gh)
curl -fsSL https://raw.githubusercontent.com/trieloff/am-i-ai/main/install.sh | sh
```

## 🌟 Philosophy

These tools embrace **vibe coding** - a new AI-assisted software development paradigm where developers guide AI tools through natural language to build software. The ecosystem ensures:

1. **Transparency**: All AI contributions are clearly attributed
2. **Safety**: Dangerous operations are prevented or clearly flagged
3. **Accountability**: Human developers maintain oversight and sign-off
4. **Efficiency**: Tools reduce friction in AI-human collaboration
5. **Visibility**: Analytics show the real impact of AI on codebases

## 📄 License

All projects are open source under Apache 2.0 or MIT licenses. See individual repositories for details.

## 🤝 Contributing

Contributions are welcome across all projects! Please visit individual repositories to submit issues or pull requests.
