# Backend Implementation Rules: Precise API & Service Construction

## Primary Directive
**Build server-side functionality following EXACT specifications in context-engineering/ folder. Zero creative decisions allowed.**

## Required Context Documents
Before starting ANY backend implementation, ensure these documents exist and are ✅ Complete:

- `context-engineering/03-architecture/api-contracts-complete.md` - Exact API specifications
- `context-engineering/03-architecture/system-architecture.md` - Service structure and patterns
- `context-engineering/03-architecture/database-schema-detailed.md` - Database design
- `context-engineering/05-specifications/technical-requirements.md` - Performance & security specs
- `context-engineering/05-specifications/error-handling-specs.md` - Error handling patterns
- `context-engineering/05-specifications/integration-specs.md` - External service connections
- `context-engineering/04-standards/coding-conventions.md` - Code structure standards

## Implementation Rules

### 1. API Endpoint Implementation Protocol
For each API endpoint:
1. **Read API Contract**: Extract exact specification from api-contracts-complete.md
2. **Implement Request Validation**: Validate inputs per specification exactly
3. **Implement Business Logic**: Follow system-architecture.md patterns precisely
4. **Implement Response Format**: Return exact response structure specified
5. **Handle All Error Cases**: Implement error responses per error-handling-specs.md
6. **Add Authentication/Authorization**: Per technical-requirements.md security specs
7. **Test Endpoint**: Create tests per testing-procedures.md requirements

### 2. API Contract Compliance
**Required API Elements** (must match api-contracts-complete.md):
- [ ] Exact HTTP method (GET, POST, PUT, DELETE)
- [ ] Precise URL path and parameter structure
- [ ] Complete request schema validation
- [ ] Exact response format with all fields
- [ ] All specified HTTP status codes
- [ ] Error response formats per RFC 7807
- [ ] Authentication and authorization requirements
- [ ] Rate limiting specifications

**Example Compliance Check:**
```javascript
// api-contracts-complete.md specifies:
POST /api/users
Request: { email: string, password: string, firstName: string }
Response 201: { id: string, email: string, firstName: string, createdAt: string }
Response 400: { type: string, title: string, detail: string, errors: Array }

// Implementation MUST match exactly - no deviations allowed
```

### 3. Service Architecture Compliance
Follow system-architecture.md patterns exactly:
- [ ] Use specified service layer structure
- [ ] Implement exact data access patterns
- [ ] Follow dependency injection approach specified
- [ ] Use middleware stack as documented
- [ ] Implement logging per architecture specs
- [ ] Follow error handling architecture

### 4. Database Integration Rules
Connect to database following database-schema-detailed.md:
- [ ] Use exact table names and column names
- [ ] Implement relationships as specified
- [ ] Use indexes and constraints as documented
- [ ] Follow connection pooling specifications
- [ ] Implement transactions per technical requirements
- [ ] Use exact query patterns from architecture specs

### 5. Business Logic Implementation
For each business rule in technical-requirements.md:
- [ ] Read complete business rule specification
- [ ] Implement validation logic exactly as specified
- [ ] Handle edge cases from edge-cases-catalog.md
- [ ] Implement error scenarios per error-handling-specs.md
- [ ] Apply security rules from technical-requirements.md

### 6. Authentication & Authorization
Implement security per technical-requirements.md:
- [ ] Use exact authentication method specified (JWT, session, etc.)
- [ ] Implement token generation/validation as documented
- [ ] Apply authorization rules precisely as specified
- [ ] Implement password hashing per security requirements
- [ ] Follow session management specifications
- [ ] Implement rate limiting as specified

### 7. External Service Integration
For integrations specified in integration-specs.md:
- [ ] Use exact API credentials and configuration
- [ ] Implement authentication per integration specs
- [ ] Follow request/response transformation as specified
- [ ] Implement error handling and retry logic as documented
- [ ] Add monitoring and logging as specified
- [ ] Follow fallback strategies as documented

### 8. Error Handling Implementation
Handle ALL error scenarios per error-handling-specs.md:
- [ ] Implement exact error types and codes specified
- [ ] Return error responses in exact format documented
- [ ] Log errors per logging specifications
- [ ] Implement recovery strategies as specified
- [ ] Handle validation errors precisely as documented
- [ ] Implement timeout and retry logic as specified

### 9. Performance Implementation
Meet ALL performance requirements from technical-requirements.md:
- [ ] Implement caching strategies as specified
- [ ] Follow database optimization patterns
- [ ] Implement connection pooling as documented
- [ ] Meet response time targets specified
- [ ] Implement pagination as specified
- [ ] Follow memory and CPU usage limits

### 10. Testing Implementation
Create tests following testing-procedures.md exactly:
- [ ] Unit tests for all business logic
- [ ] Integration tests for database operations
- [ ] API endpoint tests for all contracts
- [ ] Authentication and authorization tests
- [ ] Error handling tests for all scenarios
- [ ] Performance tests meeting benchmarks
- [ ] Meet coverage requirements from testing-standards.md

### 11. Quality Gates Before Completion
Every backend task must pass:
- [ ] API endpoints match contracts exactly
- [ ] All business rules implemented correctly
- [ ] Security requirements fully implemented
- [ ] Performance requirements satisfied
- [ ] Error handling works per specifications
- [ ] All tests pass with required coverage
- [ ] Integration tests validate external services

## Implementation Workflow

### Step 1: Context Reading
1. Read api-contracts-complete.md for endpoints to implement
2. Review system-architecture.md for service patterns
3. Check database-schema-detailed.md for data access
4. Review technical-requirements.md for security/performance

### Step 2: Setup Validation
1. Verify correct technology stack from technology-stack-decisions.md
2. Confirm database schema matches specifications
3. Check coding standards from coding-conventions.md
4. Validate external service configurations

### Step 3: Mechanical Implementation
1. Create service files per folder structure specifications
2. Implement API endpoints exactly per contracts
3. Add business logic per technical requirements
4. Implement data access per architecture patterns
5. Add authentication/authorization per security specs
6. Implement error handling per error specifications
7. Create tests per testing procedures

### Step 4: Validation
1. Test all API endpoints against contracts
2. Verify business logic meets all requirements
3. Check security implementation completeness
4. Validate performance meets benchmarks
5. Confirm error handling works as specified
6. Run integration tests with database and external services

## Error Resolution Protocol

**If API Contract is Unclear:**
1. Search api-contracts-complete.md and system-architecture.md
2. Check technical-requirements.md for additional details
3. Create boomerang task for Technical Specification Architect
4. STOP implementation until clarification received

**If Business Logic is Ambiguous:**
1. Check technical-requirements.md and user-stories-exhaustive.md
2. Look for edge cases in edge-cases-catalog.md
3. Create boomerang task for Requirements Archaeologist
4. Do not implement until clarification provided

**If Integration Requirements Unclear:**
1. Review integration-specs.md thoroughly
2. Check system-architecture.md for patterns
3. Create boomerang task for Architecture Oracle
4. Pause integration until specification clarified

**Never:**
- Make API contract assumptions
- Add endpoints not specified
- Change request/response formats
- Skip authentication/authorization
- Ignore error handling requirements
- Use different database schema than specified
- Skip performance requirements
- Ignore testing requirements

## Success Criteria
- **Perfect API Contract Match**: All endpoints match specifications exactly
- **Complete Business Logic**: All rules implemented per requirements
- **Security Compliance**: All security requirements fully implemented
- **Performance Compliance**: All benchmarks met
- **Integration Success**: All external services work per specifications
- **Test Coverage**: All testing requirements satisfied
- **Zero Assumptions**: No creative decisions made during implementation

**Remember: You are building the exact backend system designed by the architecture team. Follow their blueprint precisely.**
