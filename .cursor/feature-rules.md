# Feature Creation Rules

## Feature Lifecycle

### 1. Planning Phase
1. **Feature Request**
   - Create a new feature document in `documentation/features/`
   - Name format: `FEAT-XXX-feature-name.md`
   - Get next available FEAT-XXX number from `documentation/features/README.md`

2. **Documentation Requirements**
   ```markdown
   # Feature Name (FEAT-XXX)
   
   ## Description
   Clear description of the feature purpose and goals
   
   ## Components
   - List of main components
   - Required UI elements
   - Backend services needed
   
   ## Technical Details
   - Architecture decisions
   - Data models
   - API endpoints
   - Security considerations
   
   ## Dependencies
   - Required packages
   - External services
   - Internal dependencies
   
   ## Related Features
   - Links to dependent features
   - Links to related features
   
   ## Status
   - [ ] Planning
   - [ ] In Development
   - [ ] Testing
   - [ ] Deployed
   ```

### 2. Development Phase
1. **Branch Creation**
   - Create feature branch from main
   - Branch naming: `feature/FEAT-XXX-short-name`

2. **Development Steps**
   - Create/update necessary components
   - Follow architecture guidelines in `.cursor/architecture.md`
   - Add tests for new functionality
   - Update documentation as needed

3. **Commit Guidelines**
   - Follow commit rules in `.cursor/commit-rules.md`
   - Always include feature ID: `[FEAT-XXX]`
   - Keep commits focused and atomic

### 3. Testing Phase
1. **Required Tests**
   - Unit tests for all new components
   - Integration tests for feature workflows
   - E2E tests if UI is involved
   - Security testing if applicable

2. **Documentation Updates**
   - Update feature status in documentation
   - Add testing notes and coverage
   - Document any known limitations

### 4. Deployment Phase
1. **Pre-deployment Checklist**
   - [ ] All tests passing
   - [ ] Documentation complete
   - [ ] Security review done
   - [ ] Performance testing complete
   - [ ] Feature flags configured (if needed)

2. **Post-deployment**
   - Update feature status to "Deployed"
   - Add deployment notes to documentation
   - Create monitoring alerts if needed

## Example Workflow

```bash
# 1. Create feature documentation
cp documentation/features/template.md documentation/features/FEAT-XXX-new-feature.md

# 2. Create feature branch
git checkout -b feature/FEAT-XXX-new-feature

# 3. Development commits
git commit -m "feat: add initial structure [FEAT-XXX]"
git commit -m "feat: implement core functionality [FEAT-XXX]"
git commit -m "test: add unit tests [FEAT-XXX]"

# 4. Update documentation
git commit -m "doc: update feature status and notes [FEAT-XXX]"

# 5. Create PR
# - Use PR template
# - Reference feature documentation
# - Include testing notes
```

## Feature Template Location
- Template stored at: `documentation/features/template.md`
- Copy template when creating new feature
- Update README.md with new feature reference

## Review Requirements
1. **Code Review**
   - Architecture compliance
   - Test coverage
   - Security considerations
   - Performance impact

2. **Documentation Review**
   - Feature documentation complete
   - API documentation updated
   - Deployment notes added
   - Monitoring requirements specified 