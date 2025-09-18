# Testing Implementation Rules: Comprehensive Validation

## Primary Directive
**Create comprehensive test suites following EXACT specifications in context-engineering/ folder. Test every requirement, edge case, and acceptance criterion.**

## Required Context Documents
Before creating ANY tests, ensure these documents exist and are ✅ Complete:

- `context-engineering/04-standards/testing-standards.md` - Testing strategy and standards
- `context-engineering/06-implementation/testing-procedures.md` - Test execution procedures
- `context-engineering/01-requirements/acceptance-criteria-detailed.md` - What to validate
- `context-engineering/01-requirements/edge-cases-catalog.md` - Edge cases to test
- `context-engineering/05-specifications/technical-requirements.md` - Performance benchmarks
- `context-engineering/05-specifications/error-handling-specs.md` - Error scenarios
- `context-engineering/03-architecture/api-contracts-complete.md` - API testing specs

## Testing Implementation Rules

### 1. Test Suite Creation Protocol
For each testing phase:
1. **Read Testing Requirements**: Extract exact testing specs from context documents
2. **Create Test Structure**: Follow testing-standards.md organization exactly
3. **Implement Unit Tests**: Test all business logic per acceptance criteria
4. **Implement Integration Tests**: Test all API contracts and database operations
5. **Implement E2E Tests**: Test all user journeys from user-stories-exhaustive.md
6. **Implement Performance Tests**: Validate benchmarks from technical-requirements.md
7. **Validate Coverage**: Meet coverage requirements from testing-standards.md

### 2. Unit Testing Requirements
**Test ALL business logic** per acceptance-criteria-detailed.md:
- [ ] Every function and method with business logic
- [ ] All validation rules from technical-requirements.md
- [ ] All edge cases from edge-cases-catalog.md
- [ ] All error conditions from error-handling-specs.md
- [ ] All utility functions and helpers
- [ ] All data transformation logic
- [ ] All calculation and processing functions

**Unit Test Structure** (follow testing-standards.md exactly):
```javascript
describe('ComponentName/ServiceName', () => {
  describe('when normal conditions', () => {
    it('should meet acceptance criterion exactly as specified', () => {
      // Test implementation matching acceptance criteria
    });
  });

  describe('when edge case conditions', () => {
    it('should handle edge case per edge-cases-catalog.md', () => {
      // Test edge case handling exactly as documented
    });
  });

  describe('when error conditions', () => {
    it('should handle error per error-handling-specs.md', () => {
      // Test error handling exactly as specified
    });
  });
});
```

### 3. Integration Testing Requirements
**Test ALL integrations** per api-contracts-complete.md and system-architecture.md:
- [ ] Every API endpoint with all HTTP methods
- [ ] Database operations (CRUD, relationships, constraints)
- [ ] External service integrations per integration-specs.md
- [ ] Authentication and authorization flows
- [ ] Middleware functionality
- [ ] Data access layer operations
- [ ] Service layer interactions

**API Testing Structure**:
```javascript
describe('API Endpoint: POST /api/users', () => {
  it('should return 201 with user data when valid request', async () => {
    // Test exact API contract from api-contracts-complete.md
    const response = await request(app)
      .post('/api/users')
      .send({ /* exact request format from spec */ });
    
    expect(response.status).toBe(201);
    expect(response.body).toMatchObject({ /* exact response format */ });
  });

  it('should return 400 with validation errors when invalid request', async () => {
    // Test exact error format from error-handling-specs.md
  });
});
```

### 4. End-to-End Testing Requirements
**Test ALL user journeys** per user-stories-exhaustive.md:
- [ ] Every user story from requirements
- [ ] Complete user workflows end-to-end
- [ ] All user interaction scenarios
- [ ] Authentication and authorization flows
- [ ] Error recovery user paths
- [ ] Cross-browser compatibility per validation-criteria.md

**E2E Test Structure** (follow testing-procedures.md format):
```javascript
describe('User Journey: User Registration and Login', () => {
  it('should allow user to register and login successfully', async () => {
    // Test exact user story from user-stories-exhaustive.md
    // Follow exact steps specified in acceptance criteria
  });

  it('should show appropriate errors for invalid inputs', async () => {
    // Test error scenarios from edge-cases-catalog.md
  });
});
```

### 5. Performance Testing Requirements
**Test ALL performance benchmarks** from technical-requirements.md:
- [ ] API response times meet SLA targets
- [ ] Database query performance within limits
- [ ] Frontend rendering performance targets
- [ ] Memory usage within specified limits
- [ ] CPU usage under load scenarios
- [ ] Concurrent user capacity testing
- [ ] Scalability testing per architecture specs

**Performance Test Structure**:
```javascript
describe('Performance Tests', () => {
  it('should respond within 200ms for 95% of requests', async () => {
    // Test exact performance requirement from technical-requirements.md
    const times = [];
    for (let i = 0; i < 100; i++) {
      const start = Date.now();
      await apiCall();
      times.push(Date.now() - start);
    }
    const p95 = percentile(times, 95);
    expect(p95).toBeLessThan(200);
  });
});
```

### 6. Security Testing Requirements
**Test ALL security measures** from technical-requirements.md:
- [ ] Authentication bypass prevention
- [ ] Authorization escalation prevention
- [ ] Input validation and sanitization
- [ ] SQL injection prevention
- [ ] XSS attack prevention
- [ ] CSRF protection validation
- [ ] Rate limiting functionality
- [ ] Session security validation

### 7. Error Handling Testing
**Test ALL error scenarios** from error-handling-specs.md:
- [ ] Network failure scenarios
- [ ] Database connection failures
- [ ] External service unavailability
- [ ] Invalid input handling
- [ ] Timeout scenarios
- [ ] Resource exhaustion scenarios
- [ ] Concurrent access conflicts

### 8. Accessibility Testing
**Test ALL accessibility requirements** from acceptance-criteria-detailed.md:
- [ ] Keyboard navigation functionality
- [ ] Screen reader compatibility
- [ ] Color contrast compliance
- [ ] Focus management
- [ ] ARIA attribute validation
- [ ] Semantic HTML structure
- [ ] Alternative text for images

### 9. Test Data Management
Follow testing-procedures.md for test data:
- [ ] Create realistic test fixtures
- [ ] Use consistent test data across tests
- [ ] Clean up test data properly
- [ ] Mock external services per integration-specs.md
- [ ] Use database seeds for integration tests
- [ ] Handle test data privacy requirements

### 10. Test Coverage Requirements
Meet ALL coverage requirements from testing-standards.md:
- [ ] Overall coverage minimum percentage
- [ ] Critical path coverage requirements
- [ ] New code coverage requirements
- [ ] Branch coverage requirements
- [ ] Function coverage requirements
- [ ] Integration coverage requirements

### 11. Quality Gates Before Completion
Every test implementation must pass:
- [ ] All acceptance criteria have corresponding tests
- [ ] All edge cases from catalog are tested
- [ ] All error scenarios are validated
- [ ] Performance benchmarks are tested
- [ ] Security requirements are validated
- [ ] Coverage requirements are met
- [ ] All tests pass consistently

## Testing Workflow

### Step 1: Context Reading
1. Read acceptance-criteria-detailed.md for what to validate
2. Review edge-cases-catalog.md for edge case testing
3. Check error-handling-specs.md for error scenario testing
4. Review technical-requirements.md for performance testing
5. Check testing-standards.md for coverage and structure requirements

### Step 2: Test Planning
1. Create test plan covering all requirements
2. Identify test data needs per testing-procedures.md
3. Set up testing environment per validation-criteria.md
4. Configure testing tools per testing-standards.md

### Step 3: Test Implementation
1. Create unit tests for all business logic
2. Create integration tests for all APIs and services
3. Create E2E tests for all user journeys
4. Create performance tests for all benchmarks
5. Create security tests for all security requirements
6. Create accessibility tests for all accessibility requirements

### Step 4: Test Validation
1. Validate all tests pass consistently
2. Check coverage meets requirements
3. Verify performance tests validate benchmarks
4. Confirm security tests validate requirements
5. Validate accessibility tests meet standards

## Error Resolution Protocol

**If Acceptance Criteria is Unclear:**
1. Search acceptance-criteria-detailed.md thoroughly
2. Check user-stories-exhaustive.md for context
3. Create boomerang task for Requirements Archaeologist
4. Do not create tests until clarification received

**If Technical Requirements Unclear:**
1. Review technical-requirements.md and validation-criteria.md
2. Check system-architecture.md for additional context
3. Create boomerang task for Technical Specification Architect
4. Pause test creation until specification clarified

**If Testing Standards Unclear:**
1. Review testing-standards.md and testing-procedures.md
2. Check coding-conventions.md for code structure
3. Create boomerang task for Standards Authority
4. Wait for clarification before proceeding

**Never:**
- Skip testing any acceptance criteria
- Ignore edge cases or error scenarios
- Skip performance or security testing
- Use different testing structure than specified
- Accept lower coverage than required
- Skip accessibility testing
- Make assumptions about test requirements

## Success Criteria
- **Complete Coverage**: All acceptance criteria have tests
- **Edge Case Coverage**: All edge cases from catalog tested
- **Error Scenario Coverage**: All error conditions tested
- **Performance Validation**: All benchmarks tested
- **Security Validation**: All security requirements tested
- **Coverage Requirements**: All coverage targets met
- **Consistent Passing**: All tests pass reliably

**Remember: You are the quality guardian. Every requirement, edge case, and acceptance criterion must be validated through comprehensive testing.**
