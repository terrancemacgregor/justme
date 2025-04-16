# Website Personas

This directory contains the definitions of all user personas for the website. Personas are divided into two main categories:

## Administrative Personas
Located in [`./admin/`](./admin/):
- [ADMIN-AUTHOR-001](./admin/ADMIN-AUTHOR-001.md) - Content Author
- [ADMIN-EDITOR-001](./admin/ADMIN-EDITOR-001.md) - Content Editor
- [ADMIN-ADMIN-001](./admin/ADMIN-ADMIN-001.md) - Site Administrator
- [ADMIN-DEV-001](./admin/ADMIN-DEV-001.md) - Technical Developer
- [ADMIN-MOD-001](./admin/ADMIN-MOD-001.md) - Content Moderator
- [ADMIN-SUPPORT-001](./admin/ADMIN-SUPPORT-001.md) - Customer Support
- [ADMIN-ANALYST-001](./admin/ADMIN-ANALYST-001.md) - Data Analyst

## Reader Personas
Located in [`./reader/`](./reader/):
- [READER-DEV-001](./reader/READER-DEV-001.md) - Personal Development Seeker
- [READER-INSP-001](./reader/READER-INSP-001.md) - Inspiration and Motivation Seeker
- [READER-EVAL-001](./reader/READER-EVAL-001.md) - Reputation Evaluator

## Adding New Personas

1. Choose the appropriate category (admin or reader)
2. Create a new file in the corresponding directory
3. Use the template format from [_template.md](./_template.md)
4. Update this README with the new persona reference

## Persona IDs
- Administrative personas use prefix: `ADMIN-ROLE-XXX`
  - ROLE can be: AUTHOR, EDITOR, ADMIN, DEV, MOD, SUPPORT, ANALYST
- Reader personas use prefix: `READER-PURPOSE-XXX`
  - PURPOSE can be: DEV (development), INSP (inspiration), EVAL (evaluation)
- Always increment the highest existing number in each category 

## Repository Notes
- All commits are automatically pushed to the remote repository via git hooks 