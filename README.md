# Claude Code Starter Guide

**A friendly, no-nonsense guide to getting started with Claude Code — built for real workflows, not just demos.**

Created by Michael Schenck, Sr. Product Manager, Digital — Jaipur Living (2026)

---

## What Is This?

This repo is a starter kit to help teammates (and anyone curious) get up and running with [Claude Code](https://docs.anthropic.com/en/docs/claude-code), Anthropic's CLI-based AI coding assistant. It includes:

- A **slide deck** walking through initial setup, adding context, reference materials, skills, and slash commands
- A **ready-to-use example setup** with templates and sample project files to jumpstart productive workflows

No prior AI tooling experience required. If you can open a terminal, you can do this.

---

## What's Inside

```
Claude Code Starter Guide - Public/
|
|-- Claude Code Starter Guide -public.pptx   # The main slide deck (start here!)
|-- Claude Code Setup Example (public).zip    # Zipped copy of the example setup below
|-- Claude Code Setup Example/                # Unzipped example files
    |
    |-- MASTER Claude Markdown File/
    |   |-- claude.md                         # Your "master prompt" — global config for Claude
    |
    |-- jaipur-living-style-guide.md          # Example: brand/design reference file
    |
    |-- Example Obsidian Vault for Claude Code/
        |-- LLM Context/                      # Business & personal profile templates
        |   |-- business-profile.md
        |   |-- personal-profile.md
        |   |-- Business (Jaipur Living)/     # Business-specific context files
        |
        |-- SAMPLE PROJECT 1/                 # A full sample project setup
        |   |-- Project Requirements Document.md
        |   |-- Reference Files for Project 1/  # Logos, screengrabs, HTML snippets
        |
        |-- Tasks/templates/                  # Obsidian task templates
```

---

## Getting Started (The Short Version)

1. **Install Claude Code** — Follow the [official install guide](https://docs.anthropic.com/en/docs/claude-code/getting-started). It's just a few lines in the terminal.
2. **Set up your `claude.md`** — Copy the master template from this repo into your `~/.claude/` folder. Customize it with your name, preferences, and reference file paths.
3. **Add your context files** — Drop in business profiles, style guides, and any reference docs Claude should know about. Use the included templates as a starting point.
4. **Create a project folder** — For each project, set up a dedicated directory with a requirements doc and relevant reference files. Open Claude Code from inside that folder.
5. **Explore skills & slash commands** — Add skills that match your workflow and create custom slash commands for repeatable tasks.

---

## Key Concepts

- **`claude.md`** — Think of this as Claude's "home base" instructions. It tells Claude who you are, how you like to work, and where to find reference materials. Lives in `~/.claude/` and applies across all projects.
- **LLM Context folder** — A directory of markdown files giving Claude persistent knowledge about your business, role, and preferences. The more relevant context Claude has, the less you have to repeat yourself.
- **Project folders** — Keep project-specific docs (requirements, reference images, code snippets) in their own directories. This keeps Claude's context tight and focused, which means better results.
- **Skills** — Modular capability files that give Claude specialized knowledge (UX design, code review, marketing, etc.). Add what's relevant to your work.
- **Slash commands** — Custom one-liner shortcuts for prompts you use often. Create a markdown file, drop it in `~/.claude/commands/`, and you're set.

---

## Tips for Getting the Most Out of Claude Code

- **Keep context tight** — Only give Claude what's relevant to the current task. Less noise = fewer hallucinations.
- **Use `/clear` between tasks** — Clears the context window so previous conversations don't bleed into new ones.
- **Ask Claude to save reference files** — At the end of a session, have Claude create a summary doc for next time. It builds up a personalized knowledge base over time.
- **Start simple, then layer on** — Get comfortable with the basics before adding skills and custom commands. There's no rush.

---

## Who Is This For?

Anyone on the team who wants to work faster, think bigger, and offload the tedious stuff. Whether you're writing code, drafting requirements, analyzing data, or just trying to get through your inbox — Claude Code can help. This guide is here to make the first step easy.

---

## Questions?

Reach out to Michael Schenck or open an issue in this repo.
