# Commit Message Rules

## Format
```
<type>: <description> [FEAT-XXX]
```

## Types
- `feat:` - New features
- `fix:` - Bug fixes
- `doc:` - Documentation updates
- `improve:` - Improvements to existing code
- `refactor:` - Code refactoring without changing functionality
- `test:` - Adding or modifying tests
- `chore:` - Maintenance tasks, dependencies, etc.

## Feature Reference
- Each commit should reference a feature ID in square brackets: `[FEAT-XXX]`
- Feature IDs are defined in `documentation/features/README.md`
- Multiple features can be referenced: `[FEAT-001] [FEAT-002]`

## Examples
- `feat: add user authentication [FEAT-002]`
- `fix: resolve login redirect issue [FEAT-002]`
- `doc: update README with setup instructions [FEAT-003]`
- `improve: optimize image loading performance [FEAT-001]`
- `refactor: restructure admin components [FEAT-004]`
- `test: add unit tests for email service [FEAT-005]`
- `chore: update dependencies to latest versions`

## Rules
- Type should be lowercase
- Description should be in present tense
- Keep descriptions concise but descriptive
- Always include feature ID(s) in square brackets
- Use body for additional context when needed
- Use footer for breaking changes or issue references 