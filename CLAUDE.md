# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository tracks AI agent capabilities across different task types to measure and compare performance over time. It's a **benchmark and documentation repository**, not a code project with builds or tests.

## Repository Structure

The repository is organized by task category, with each task containing:
- `README.md` - Task description, prompt, results table, responses, and evaluation criteria
- Response artifacts (images, markdown files with full responses, etc.)

### Categories

- **chats/** - Conversational tasks testing reasoning, logical thinking, and practical advice
- **image-generation/** - Tasks evaluating image generation capabilities against specific requirements
- **sheet-music/** - Tasks testing musical notation generation and transcription
- **coding/** - Tasks evaluating code writing, refactoring, and transformation abilities

### Task Structure Pattern

Each task follows this structure:
```
category/
└── task-name/
    ├── README.md          # Task definition and results
    ├── [agent-name].md    # Full response (for lengthy outputs)
    └── [images]           # Generated images or input materials
```

## Working with This Repository

### Adding a New Task

1. Choose the appropriate category directory (or create a new one if needed)
2. Create a subdirectory with a kebab-case name describing the task
3. Create a `README.md` following the established template:
   - Task title and category
   - Description
   - Prompt (exact prompt given to agents)
   - Results table (Agent | Score | Notes)
   - Responses section (one per agent tested)
   - Evaluation Criteria section

### Adding Test Results

1. Navigate to the task's `README.md`
2. Add a row to the Results table with: agent name, score, and brief notes
3. Add a full response section under "Responses" with:
   - Agent name and score as heading
   - Full response text or reference to separate markdown file
   - Analysis of the response quality
   - Specific failures or successes noted

### Updating the Top-Level README

When adding tasks or results, update `/README.md`:
- Add new tasks to the summary table
- Update "Best result" column when a better result is achieved
- Keep category descriptions current

## Evaluation Philosophy

**Focus on specific, measurable failures**: When documenting results, identify concrete errors (e.g., "Measure 3, bass note: Clearly F, transcribed as G") rather than vague assessments.

**Score honestly**: Use descriptive scores like "fail", "pass", "fail, almost passes", or "correct, but weird" that capture nuance better than numeric scales.

**Document both capability and failure modes**: The goal is to understand what current agents can and cannot do, not to advocate for any particular agent.

## Git Workflow

This is a documentation repository. Standard git practices apply:
- Commit message format: Describe what was added/updated (e.g., "Add ChatGPT Auto result for music-theory-homework")
- Keep commits focused on a single task or update
- Branch names can follow `claude/description` or similar patterns for agent-assisted additions
