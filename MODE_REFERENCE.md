# Implementation Mode Reference Guide

> **Quick reference for using each specialized implementation mode effectively.**

## 🎯 Mode Selection Decision Tree

```
Start Here: Do you have completed context-engineering/ specifications?
├─ No → Use Context Engineering Framework first
└─ Yes → Continue with Implementation Framework

What are you implementing?
├─ Starting new implementation project → ⚙️ Implementation Orchestrator
├─ Setting up infrastructure → 🗄️ Database Implementation + 🚀 DevOps Implementation  
├─ Building backend APIs → 🔧 Backend Implementation + 🔌 API Endpoint Builder
├─ Building frontend UI → 🎨 Frontend Implementation + 🧩 UI Component Builder
├─ Connecting external services → 🔗 Integration Implementation
├─ Creating comprehensive tests → 🧪 Testing Implementation
├─ Validating implementation quality → ✅ QA Validator + ⚡ Performance + 🔒 Security
```

## 🤖 Mode Descriptions & Use Cases

### ⚙️ Implementation Orchestrator
**Purpose**: Master coordinator of the entire implementation process  
**When to Use**: Always start here when beginning implementation  
**Context Requirements**: Complete context-engineering/ folder with all phases  
**Key Responsibilities**:
- Reads all context engineering specifications
- Creates execution plan from task-breakdown.md
- Delegates to appropriate specialist modes in correct order
- Validates quality gates between phases
- Coordinates dependencies and ensures proper sequencing

**Example Prompts**:
```
"Begin implementation execution following context-engineering specifications. Start with infrastructure phase."

"Read the implementation guide and coordinate Phase 2 backend development with the appropriate specialist modes."

"Validate current implementation phase against quality gates and determine next steps."
```

### 🎨 Frontend Implementation Specialist
**Purpose**: Builds complete frontend applications and user interfaces  
**When to Use**: For pages, routing, state management, and complex UI workflows  
**Context Requirements**: component-specifications.md, user-stories-exhaustive.md  
**Key Responsibilities**:
- Implements pages and routing per specifications
- Sets up state management per architecture
- Connects to backend APIs per contracts
- Implements responsive design and accessibility
- Handles user interactions and workflows

**Example Prompts**:
```
"Implement the user dashboard page following the user stories and component specifications."

"Create the application routing structure per system-architecture.md specifications."

"Implement the user authentication flow following the specified user journey."
```

### 🧩 UI Component Builder  
**Purpose**: Creates individual reusable UI components  
**When to Use**: For buttons, inputs, modals, forms, and other reusable elements  
**Context Requirements**: component-specifications.md with detailed interfaces  
**Key Responsibilities**:
- Builds components with exact interfaces specified
- Implements all variants, states, and behaviors
- Adds accessibility features per requirements
- Creates component tests and documentation
- Ensures reusability and consistency

**Example Prompts**:
```
"Build the Button component following the exact interface specification in component-specifications.md."

"Create the Modal component with all variants and accessibility features specified."

"Implement the Form Input components with validation and error handling per specs."
```

### 🔧 Backend Implementation Specialist
**Purpose**: Builds complete backend services and business logic  
**When to Use**: For service architecture, business logic, and complex backend workflows  
**Context Requirements**: system-architecture.md, technical-requirements.md  
**Key Responsibilities**:
- Implements service layer architecture
- Builds business logic per technical requirements
- Sets up authentication and authorization systems
- Implements middleware and request processing
- Handles complex data operations and transactions

**Example Prompts**:
```
"Implement the user management service following the system architecture specifications."

"Build the business logic for order processing per technical requirements."

"Create the authentication and authorization system per security specifications."
```

### 🔌 API Endpoint Builder
**Purpose**: Creates individual API endpoints with precise contracts  
**When to Use**: For specific endpoints with defined request/response contracts  
**Context Requirements**: api-contracts-complete.md with exact specifications  
**Key Responsibilities**:
- Implements endpoints matching API contracts exactly
- Adds request validation and response formatting
- Implements error handling per specifications
- Adds authentication and rate limiting
- Creates endpoint tests and documentation

**Example Prompts**:
```
"Build the POST /api/users endpoint following the exact API contract specification."

"Implement the GET /api/orders/{id} endpoint with all error handling scenarios."

"Create the authentication endpoints (login/logout/refresh) per API contracts."
```

### 🗄️ Database Implementation Specialist
**Purpose**: Creates database schemas, migrations, and data access layers  
**When to Use**: For database setup, schema creation, and data access patterns  
**Context Requirements**: database-schema-detailed.md, system-architecture.md  
**Key Responsibilities**:
- Creates database tables, relationships, and constraints
- Builds migration scripts and seed data
- Implements data access repositories and patterns
- Sets up database connections and pooling
- Optimizes queries and indexes per specifications

**Example Prompts**:
```
"Create the complete database schema following database-schema-detailed.md specifications."

"Implement the data access layer with repository pattern per system architecture."

"Build database migrations and seed data per implementation guide."
```

### 🔗 Integration Implementation Specialist
**Purpose**: Connects application with external services and APIs  
**When to Use**: For payment gateways, email services, file storage, and third-party APIs  
**Context Requirements**: integration-specs.md, error-handling-specs.md  
**Key Responsibilities**:
- Implements external service connections
- Handles authentication and API communication
- Adds error handling and retry logic
- Implements data transformation and mapping
- Creates integration tests and monitoring

**Example Prompts**:
```
"Implement Stripe payment integration following the integration specifications."

"Connect to SendGrid email service per integration-specs.md requirements."

"Build the file upload integration with AWS S3 per specifications."
```

### 🚀 DevOps Implementation Specialist
**Purpose**: Sets up deployment, CI/CD, and infrastructure  
**When to Use**: For deployment pipelines, containerization, and operational setup  
**Context Requirements**: deployment-architecture.md, technical-requirements.md  
**Key Responsibilities**:
- Creates CI/CD pipelines and deployment scripts
- Sets up containerization and orchestration
- Configures monitoring, logging, and alerting
- Implements infrastructure as code
- Sets up environments and deployment strategies

**Example Prompts**:
```
"Setup CI/CD pipeline following deployment-architecture.md specifications."

"Create Docker containers and Kubernetes configurations per deployment specs."

"Implement monitoring and logging infrastructure per technical requirements."
```

### 🧪 Testing Implementation Specialist
**Purpose**: Creates comprehensive test suites validating all requirements  
**When to Use**: For unit, integration, e2e, and performance testing  
**Context Requirements**: testing-procedures.md, acceptance-criteria-detailed.md  
**Key Responsibilities**:
- Creates unit tests for all business logic
- Builds integration tests for APIs and services
- Implements e2e tests for user journeys
- Adds performance and security testing
- Ensures test coverage meets requirements

**Example Prompts**:
```
"Create comprehensive test suite validating all acceptance criteria from the requirements."

"Build integration tests for all API endpoints per testing procedures."

"Implement e2e tests covering all user stories from user-stories-exhaustive.md."
```

### ✅ QA Validator
**Purpose**: Validates implementation against all context specifications  
**When to Use**: For systematic validation of completed implementation phases  
**Context Requirements**: All context-engineering documents, validation-criteria.md  
**Key Responsibilities**:
- Validates implementation against acceptance criteria
- Checks compliance with technical requirements
- Verifies error handling and edge cases work correctly
- Confirms coding standards compliance
- Validates accessibility and security requirements

**Example Prompts**:
```
"Validate the current implementation against all acceptance criteria in the context engineering documents."

"Check implementation compliance with technical requirements and coding standards."

"Verify all edge cases from edge-cases-catalog.md are properly handled."
```

### ⚡ Performance Validator
**Purpose**: Validates performance requirements and benchmarks  
**When to Use**: For performance testing and optimization validation  
**Context Requirements**: technical-requirements.md with performance benchmarks  
**Key Responsibilities**:
- Runs performance tests against specified benchmarks
- Validates response times and throughput requirements
- Checks memory usage and resource consumption
- Tests scalability and concurrent user capacity
- Verifies caching and optimization strategies work

**Example Prompts**:
```
"Run performance tests to validate all benchmarks in technical-requirements.md are met."

"Test application performance under load per validation criteria specifications."

"Validate caching strategies and optimization implementations are working correctly."
```

### 🔒 Security Validator
**Purpose**: Validates security implementation and requirements  
**When to Use**: For security testing and vulnerability validation  
**Context Requirements**: technical-requirements.md security specs, error-handling-specs.md  
**Key Responsibilities**:
- Tests authentication and authorization systems
- Validates input sanitization and injection prevention
- Checks encryption and data protection measures
- Tests security headers and configurations
- Runs security scans and vulnerability assessments

**Example Prompts**:
```
"Validate all security requirements from technical-requirements.md are properly implemented."

"Test authentication and authorization systems for security vulnerabilities."

"Run security scan and validate protection against common attack vectors."
```

## 📋 Context Document Requirements by Mode

### All Modes Require:
- `context-engineering/04-standards/coding-conventions.md` - Code structure and style
- `context-engineering/05-specifications/technical-requirements.md` - Performance and security
- `context-engineering/06-implementation/validation-criteria.md` - Quality gates

### Frontend Modes Require:
- `context-engineering/05-specifications/component-specifications.md` - Component interfaces
- `context-engineering/01-requirements/user-stories-exhaustive.md` - User interactions
- `context-engineering/01-requirements/acceptance-criteria-detailed.md` - UI behavior validation

### Backend Modes Require:
- `context-engineering/03-architecture/api-contracts-complete.md` - API specifications
- `context-engineering/03-architecture/system-architecture.md` - Service patterns
- `context-engineering/05-specifications/error-handling-specs.md` - Error handling

### Database Mode Requires:
- `context-engineering/03-architecture/database-schema-detailed.md` - Schema design
- `context-engineering/03-architecture/system-architecture.md` - Data access patterns

### DevOps Mode Requires:
- `context-engineering/03-architecture/deployment-architecture.md` - Infrastructure specs
- `context-engineering/02-technology/technology-stack-decisions.md` - Technology choices

### Testing Mode Requires:
- `context-engineering/04-standards/testing-standards.md` - Testing strategy
- `context-engineering/06-implementation/testing-procedures.md` - Test execution
- `context-engineering/01-requirements/edge-cases-catalog.md` - Edge case testing

## 🚨 Common Mode Issues & Solutions

### Issue: Mode asks clarifying questions
**Cause**: Context specification is incomplete or unclear
**Solution**: 
1. Search context-engineering/ folder for more details
2. Create boomerang task for appropriate Context Engineering specialist
3. Do not proceed until clarification received

### Issue: Mode makes creative decisions
**Cause**: Mode not following context specifications strictly
**Solution**:
1. Remind mode to follow context-engineering specifications exactly
2. Reference specific context document containing the decision
3. Use phrase: "Follow the context specifications without interpretation"

### Issue: Quality gates failing
**Cause**: Implementation doesn't match context specifications
**Solution**:
1. Review validation-criteria.md for specific requirements
2. Compare implementation to context specifications
3. Fix compliance issues and re-validate

### Issue: Mode can't find context documents
**Cause**: Context engineering phase incomplete or context folder missing
**Solution**:
1. Verify context-engineering/ folder exists in project root
2. Check all context documents are marked ✅ Complete 
3. Return to Context Engineering Framework if needed

## ⚡ Quick Mode Commands

### Start Implementation
```
Mode: ⚙️ Implementation Orchestrator
"Begin implementation execution per context-engineering specifications."
```

### Build UI Component
```  
Mode: 🧩 UI Component Builder
"Create [ComponentName] following component-specifications.md interface."
```

### Build API Endpoint
```
Mode: 🔌 API Endpoint Builder  
"Implement [METHOD] /api/[path] following api-contracts-complete.md."
```

### Create Tests
```
Mode: 🧪 Testing Implementation Specialist
"Create comprehensive tests validating acceptance-criteria-detailed.md."
```

### Validate Quality
```
Mode: ✅ QA Validator
"Validate implementation against all context engineering specifications."
```

---

**Remember: Every mode follows the same principle - read the context specifications and implement exactly what's documented with zero creative interpretation.**
