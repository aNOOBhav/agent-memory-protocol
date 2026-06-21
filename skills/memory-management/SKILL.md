# Agent Memory Protocol (AMP)

> Persistent memory and session handover standards for AI coding agents.

Agent Memory Protocol (AMP) is an open collection of reusable skills, templates, and conventions that enable coding agents to preserve project context across sessions, transfer work between different agents, and maintain long-term knowledge about a codebase.

Rather than relying solely on an LLM's context window, AMP externalizes memory into structured Markdown and machine-readable artifacts that can be shared between humans and agents.

---

## Why?

Modern coding agents are excellent at solving individual tasks, but they still struggle with long-running projects.

Common problems include:

- Losing architectural context between sessions
- Repeating previous investigations
- Forgetting design decisions
- Poor collaboration between different agents
- Weak project handoffs
- Lack of persistent institutional knowledge

AMP aims to solve these problems with lightweight, repository-native memory.

---

# Goals

- Persistent project memory
- Reliable session handoffs
- Transferable context between agents
- Framework-agnostic design
- Human-readable documentation
- Machine-readable metadata
- Git-friendly workflow

---

# Vision

Instead of every coding agent maintaining its own proprietary memory, projects should own their own knowledge.

```
Project
     │
     ├── Memory
     ├── Handover
     ├── Decisions
     ├── Changelog
     └── Workspace
```

Any compatible agent can enter the project, understand its history, perform work, and leave behind an accurate handoff for the next agent.

---

# Repository Structure

```
skills/
    memory-management/
    handover-management/
    workspace-management/

templates/

examples/

docs/
```

---

# Components

## Memory Management

Long-term project knowledge.

Examples include:

- Project overview
- Architecture
- Coding standards
- Design decisions
- Known issues
- Technical debt
- Changelog
- Long-term TODOs

Memory changes infrequently and represents what the project "knows."

---

## Handover Management

Short-term working memory.

Captures:

- Current objective
- Completed work
- Remaining work
- Files modified
- Commands executed
- Risks
- Blockers
- Recommended next steps

Handover changes every working session.

---

## Workspace Management *(planned)*

Ephemeral execution context.

Examples:

- Active files
- Current branch
- Build status
- Open investigations
- Temporary notes

Workspace state is regenerated frequently and should never become permanent project knowledge.

---

# Supported Agents

The protocol is designed to work with any coding agent.

Current targets include:

- Claude Code
- OpenAI Codex
- Gemini CLI
- Omnigent
- Cursor
- Cline
- Roo Code
- OpenHands
- Aider
- Amp
- Continue
- Custom agents

---

# Design Principles

- Human-first documentation
- Machine-friendly structure
- Version control friendly
- Minimal overhead
- Portable across repositories
- No vendor lock-in

---

# Inspiration

The Session Handoff skill from the Softaworks Agent Toolkit provided valuable inspiration for the handover management concepts used in this repository.

https://github.com/softaworks/agent-toolkit

AMP extends these ideas with persistent project memory, architectural knowledge, changelogs, decision records, and standardized memory conventions.

---

# Roadmap

- Memory Management skill
- Session Handover skill
- Workspace Management
- JSON schemas
- Validation tools
- Automatic memory updates
- IDE integrations
- GitHub Actions
- Multi-agent compatibility layer

---

# Contributing

Contributions are welcome.

The long-term goal is to establish a common, open protocol for persistent memory across AI coding agents.