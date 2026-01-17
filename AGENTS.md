# Agent Definitions

## Concurrent Agents for Module Development

This project uses 5 specialized agents working in parallel to build different modules.

### Agent 1: AuthAgent
- **Role**: Authentication module developer
- **Directory**: `/src/auth/`
- **Files to create**:
  - `index.ts` - Main authentication exports
  - `jwt.ts` - JWT token handling
  - `middleware.ts` - Auth middleware

### Agent 2: APIAgent
- **Role**: API endpoint developer
- **Directory**: `/src/api/`
- **Files to create**:
  - `index.ts` - API router setup
  - `users.ts` - User endpoints
  - `health.ts` - Health check endpoint

### Agent 3: DBAgent
- **Role**: Database layer developer
- **Directory**: `/src/db/`
- **Files to create**:
  - `index.ts` - Database connection
  - `models.ts` - Data models
  - `migrations.ts` - Migration helpers

### Agent 4: UtilsAgent
- **Role**: Utility functions developer
- **Directory**: `/src/utils/`
- **Files to create**:
  - `index.ts` - Utility exports
  - `logger.ts` - Logging utility
  - `validators.ts` - Input validators

### Agent 5: ConfigAgent
- **Role**: Configuration management developer
- **Directory**: `/src/config/`
- **Files to create**:
  - `index.ts` - Config exports
  - `env.ts` - Environment handling
  - `constants.ts` - Application constants

## Coordination

All agents should:
1. Work only in their assigned directories
2. Create all listed files
3. Include proper TypeScript types
4. Add file header comments with agent name
