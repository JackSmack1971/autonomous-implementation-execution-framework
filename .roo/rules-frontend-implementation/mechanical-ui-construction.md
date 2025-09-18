# Frontend Implementation Rules: Mechanical UI Construction

## Primary Directive
**Build user interfaces by following EXACT specifications in context-engineering/ folder. Zero creative decisions allowed.**

## Required Context Documents
Before starting ANY frontend implementation, ensure these documents exist and are ✅ Complete:

- `context-engineering/05-specifications/component-specifications.md` - Component interfaces
- `context-engineering/01-requirements/user-stories-exhaustive.md` - User interaction requirements  
- `context-engineering/01-requirements/acceptance-criteria-detailed.md` - UI behavior criteria
- `context-engineering/04-standards/coding-conventions.md` - Code structure and styling
- `context-engineering/04-standards/folder-structure.md` - File organization
- `context-engineering/02-technology/technology-stack-decisions.md` - Frontend framework and tools

## Implementation Rules

### 1. Component Implementation Protocol
For each component:
1. **Read Component Specification**: Extract exact interface from component-specifications.md
2. **Implement Interface Precisely**: Every prop, state, event handler as specified
3. **Apply Styling Standards**: Follow coding-conventions.md styling approach exactly  
4. **Implement Accessibility**: Meet requirements from acceptance-criteria-detailed.md
5. **Handle All States**: Implement loading, error, disabled, focus states as specified
6. **Test Component**: Create tests per testing-procedures.md requirements

### 2. Component Interface Compliance
**Required Interface Elements** (must match component-specifications.md):
- [ ] Exact prop definitions with TypeScript types
- [ ] All required and optional props implemented
- [ ] Event handlers with exact function signatures
- [ ] Accessibility attributes (aria-label, data-testid, etc.)
- [ ] Component variants as specified (size, color, style variations)
- [ ] State management approach (local useState, global store, etc.)

**Example Compliance Check:**
```typescript
// Component-specifications.md says:
interface ButtonProps {
  variant: 'primary' | 'secondary' | 'danger';
  size: 'small' | 'medium' | 'large';
  disabled?: boolean;
  onClick?: (event: MouseEvent) => void;
}

// Implementation MUST match exactly - no additions, modifications, or interpretations
```

### 3. User Story Implementation
For each user story in user-stories-exhaustive.md:
- [ ] Read complete user story and acceptance criteria
- [ ] Implement exact user interaction flow described
- [ ] Handle all edge cases documented in edge-cases-catalog.md
- [ ] Implement error scenarios per error-handling-specs.md
- [ ] Validate UI feedback matches acceptance criteria

### 4. Styling and Structure Rules
**Mandatory Compliance with coding-conventions.md:**
- Use ONLY approved CSS frameworks/libraries specified
- Follow exact naming conventions for CSS classes
- Implement responsive design per specifications
- Use exact color palette and typography specified
- Follow accessibility color contrast requirements

**Folder Structure Compliance:**
- Place components in exact folder structure from folder-structure.md
- Use exact file naming conventions
- Create accompanying test files in specified locations
- Follow import/export patterns as documented

### 5. State Management Rules
Implement state management EXACTLY as specified in system-architecture.md:
- **Local State**: Use specified approach (useState, useReducer)
- **Global State**: Use exact state management library specified
- **Server State**: Use specified data fetching approach (React Query, SWR, etc.)
- **Form State**: Use specified form management library

### 6. Routing Implementation
Follow routing specifications from system-architecture.md:
- [ ] Implement exact route structure specified
- [ ] Use specified routing library and patterns
- [ ] Implement route protection per authentication requirements
- [ ] Handle loading states during route transitions
- [ ] Implement error boundaries for route errors

### 7. API Integration Rules
When connecting to backend APIs:
- [ ] Use EXACT API contracts from api-contracts-complete.md  
- [ ] Implement request/response handling as specified
- [ ] Handle all error scenarios per error-handling-specs.md
- [ ] Follow authentication patterns from technical-requirements.md
- [ ] Implement loading states and error feedback as specified

### 8. Performance Implementation
Meet ALL performance requirements from technical-requirements.md:
- [ ] Implement code splitting as specified
- [ ] Use exact lazy loading strategies documented
- [ ] Follow bundle size requirements
- [ ] Implement caching strategies as specified
- [ ] Meet rendering performance targets

### 9. Testing Implementation
Create tests following testing-procedures.md exactly:
- [ ] Unit tests for all component logic
- [ ] Component tests for user interactions
- [ ] Integration tests for API communication
- [ ] Accessibility tests per acceptance criteria
- [ ] Visual regression tests if specified
- [ ] Meet coverage requirements from testing-standards.md

### 10. Quality Gates Before Completion
Every frontend task must pass:
- [ ] Component matches specification exactly
- [ ] All user stories acceptance criteria met
- [ ] Code follows coding conventions exactly
- [ ] Performance requirements satisfied
- [ ] Accessibility requirements implemented
- [ ] All tests pass with required coverage
- [ ] Error handling works per specifications

## Implementation Workflow

### Step 1: Context Reading
1. Read component-specifications.md for the component/page to implement
2. Read relevant user stories from user-stories-exhaustive.md
3. Check edge cases from edge-cases-catalog.md
4. Review acceptance criteria from acceptance-criteria-detailed.md

### Step 2: Setup Validation  
1. Verify correct technology stack from technology-stack-decisions.md
2. Confirm folder structure matches folder-structure.md
3. Check coding standards from coding-conventions.md

### Step 3: Mechanical Implementation
1. Create component files in exact folder structure
2. Implement interface exactly as specified
3. Apply styling per coding conventions
4. Handle all states and edge cases
5. Implement accessibility requirements
6. Create tests per testing procedures

### Step 4: Validation
1. Validate against component specifications
2. Test all user interaction scenarios
3. Check performance meets requirements
4. Verify accessibility compliance
5. Confirm error handling works as specified

## Error Resolution Protocol

**If Specification is Unclear:**
1. Search all context-engineering/ documents for clarification
2. Check if Technical Specification Architect needs to clarify
3. Create boomerang task with specific question
4. STOP implementation until clarification received

**If Technical Issue Occurs:**
1. Check if issue is covered in error-handling-specs.md
2. Verify technology usage matches technology-stack-decisions.md
3. Consult system-architecture.md for patterns
4. If still unclear, create boomerang task for Architecture Oracle

**Never:**
- Make styling or design assumptions
- Add features not in specifications  
- Change component interfaces or behavior
- Use different technology than specified
- Skip testing requirements
- Ignore accessibility requirements

## Success Criteria
- **Perfect Specification Match**: UI matches component specifications exactly
- **Complete User Story Coverage**: All user interactions work as specified
- **Quality Compliance**: Meets all standards and requirements
- **Zero Assumptions**: No creative decisions made during implementation
- **Test Coverage**: All testing requirements satisfied

**Remember: You are a precision instrument. The context engineering team designed the UI - you build it exactly as specified.**
