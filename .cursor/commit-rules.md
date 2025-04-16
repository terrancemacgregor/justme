# Commit Message Rules

## Format
```
<type>: <description> [<prefix>-XXX]
```

## Types
- `feat:` - New features
- `fix:` - Bug fixes
- `doc:` - Documentation updates
- `improve:` - Improvements to existing code
- `refactor:` - Code refactoring without changing functionality
- `test:` - Adding or modifying tests
- `chore:` - Maintenance tasks, dependencies, etc.

## Prefix Types
- `FEAT` - Feature related changes
- `INFRA` - Infrastructure and project setup
- Multiple prefixes allowed: `[FEAT-001] [INFRA-002]`

## Feature Reference
- Each commit should reference appropriate ID in square brackets
- Feature IDs are defined in `documentation/features/README.md`
- Infrastructure IDs are tracked in `documentation/infrastructure/README.md`

## Examples
- `feat: add user authentication [FEAT-001]`
- `fix: resolve login redirect issue [FEAT-001]`
- `doc: update architecture documentation [INFRA-001]`
- `improve: optimize image loading performance [FEAT-002]`
- `refactor: restructure admin components [FEAT-003]`
- `test: add unit tests for email service [FEAT-004]`
- `chore: update project dependencies [INFRA-002]`

## Rules
- Type should be lowercase
- Description should be in present tense
- Keep descriptions concise but descriptive
- Always include appropriate ID(s) in square brackets
- Use body for additional context when needed
- Use footer for breaking changes or issue references 