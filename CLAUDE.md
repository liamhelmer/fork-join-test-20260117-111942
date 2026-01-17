# Test Project - Agent Fork-Join E2E Test

This is a test project for validating the agent-fork-join plugin.

## IMPORTANT: E2E Test Requirements

This project tests the agent-fork-join plugin. The following MUST be true:

1. **Branch creation is automatic**: The plugin's UserPromptSubmit hook MUST automatically
   create and push a feature branch when work begins. You do NOT need to create branches manually.

2. **Commits are automatic**: The plugin's AgentComplete hook MUST automatically commit
   changes when agents complete their work. You do NOT need to commit manually.

3. **PR creation is automatic**: The plugin MUST create the PR automatically.
   You do NOT need to create a PR manually.

Just focus on creating the requested files. The plugin handles all git operations.

## Project Structure

This project will be built by multiple concurrent agents, each creating a separate module.

## Plugin Configuration

The agent-fork-join plugin is configured with:
- Max concurrent agents: 8
- Merge strategy: rebase
- Branch naming: Angular commit types (feat/, fix/, refactor/, etc.)
- Agent branch prefix: agent/

## Development Rules

1. Each agent creates files in its assigned directory only
2. All code must include a file header comment
3. No agent should modify another agent's files
4. Tests should be created alongside implementation files

## Agent Assignment

When spawning agents for this project:
- Agent 1: Creates `/src/auth/` module (authentication)
- Agent 2: Creates `/src/api/` module (API endpoints)
- Agent 3: Creates `/src/db/` module (database layer)
- Agent 4: Creates `/src/utils/` module (utility functions)
- Agent 5: Creates `/src/config/` module (configuration management)
