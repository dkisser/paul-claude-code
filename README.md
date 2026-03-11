# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Claude Code custom skills repository containing skill definitions that extend Claude's capabilities.

## Structure

- `frontend-mvp-design/SKILL.md` - Skill for MVP/frontend demo design preparation workflow
- `image-analyzer/SKILL.md` - Skill for image analysis using vision-capable models

## Skill Format

Skills are defined in YAML frontmatter format:

```yaml
---
name: skill-name
description: Description of what this skill does
---

Content here...
```

## Development Workflow

This repository has no build system, package manager, or tests. Skills are plain Markdown files with YAML frontmatter.

To add a new skill:
1. Create a new directory for the skill
2. Add a `SKILL.md` file with proper YAML frontmatter
3. Commit the changes

## File Locations

| Skill | Path |
|-------|------|
| frontend-mvp-design | `frontend-mvp-design/SKILL.md` |
| image-analyzer | `image-analyzer/SKILL.md` |
