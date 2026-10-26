# OpenCode Toolkit

**English** | [Español](README.es.md)

A practical guide to commands, context management, and productivity for AI-assisted software development.

## Introduction

OpenCode Toolkit is a reference guide for understanding commands, organizing work sessions, and improving development workflows with AI coding agents.

Its goal is to explain what each command is intended to do, identify its limitations, and promote practices that help protect development work.

## Commands

### 1. `/init`

Initializes a project's context and, in compatible environments, helps generate instructions that describe its structure and conventions.

```text
/init
```

**Limitations**
- It does not guarantee that the agent understands every file, dependency, or architectural decision.
- Generated instructions may be incomplete or become outdated.
- It does not replace code review or test execution.
- It does not guarantee that context will persist automatically across sessions.

**Best practice:** Review the generated instructions and update them as the project evolves.

### 2. `/models`

Allows users to inspect or select models when the environment implements this command.

```text
/models
```

**Limitations**
- Available models depend on the provider, configuration, and environment capabilities.
- Models may differ in quality, speed, context limits, and cost.
- A cheaper model does not always reduce total costs if it requires more attempts.
- Switching models does not guarantee that all previous context will be preserved.

**Best practice:** Use lightweight models for straightforward tasks and more capable models for complex problems, after checking their costs and limitations.

### 3. `/sessions`

Provides access to previous sessions when the tool supports session history and recovery.

```text
/sessions
```

**Limitations**
- Only sessions that have been retained and remain accessible can be recovered.
- Reopening a session does not guarantee restoration of processes, variables, temporary files, or external state.
- Available history depends on the tool and its configuration.
- A recovered session may not contain all the context needed to continue working.

**Best practice:** Record progress, decisions, and pending tasks in persistent project files.

### 4. `/compact`

Reduces or summarizes conversation context when the environment supports this functionality.

```text
/compact
```

**Limitations**
- Summaries may omit details, examples, secondary decisions, or code snippets.
- It does not guarantee literal preservation of the entire conversation.
- It does not necessarily increase the model's maximum context window.
- It does not replace backups or persistent storage for important information.

**Best practice:** Preserve critical requirements, relevant commands, and the current project state in files such as `README.md`, `AGENTS.md`, or project notes.

### 5. `/undo`

Requests the reversal of a previous action or change when the tool provides this functionality.

```text
/undo
```

**Limitations**
- The scope of a reversal depends on the implementation.
- It does not guarantee that every change made during a session can be undone.
- Changes to external systems and irreversible actions may not be recoverable.
- It should not be treated as a replacement for version control.

**Best practice:** Use Git to track changes and review or restore previous versions of the project.

## General recommendations

1. Initialize the project's context before starting work.
2. Choose a model based on task complexity and expected cost.
3. Save progress in persistent files to make work easier to resume across sessions.
4. Summarize long conversations only after identifying critical information.
5. Use Git and review changes before performing destructive operations.

## Compatibility

The commands described in this guide should not be considered universal commands. Their availability and behavior depend on the OpenCode version, installed extensions, configuration, and external tools in use.

Check the official documentation for your environment before assuming that a command is available or behaves in a particular way.

---

[Back to the main page](README.md)
