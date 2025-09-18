---
trigger: always_on
---

# Global System Design Rules

## 1. Page Structure & Sitemap Design

### Routing Hierarchy
- Use clear hierarchical routing structure
- Implement protection levels for all routes:
  - `guestOnly`: Accessible only to non-authenticated users
  - `protected`: Requires authentication
  - `public`: Accessible to all users
- Root path (`/`) should redirect to appropriate landing page

### Page Organization
- Group related pages into logical sections (Auth, Profile, Payments, etc.)
- Use descriptive route names that reflect functionality
- Implement navigation bars between related views
- Include page descriptions in sitemap documentation

### Common Page Patterns
- **Auth Pages**: `/signup`, `/login`, `/confirm`, `/resetPass`
- **Profile Pages**: `/profile`, `/profile/transaction`, `/profile/subscription`
- **Payment Pages**: `/checkout`
- **List Views**: Display items with brief descriptions
- **Detail Views**: Full data representation of selected items

## 2. API Route Design Patterns

### RESTful Conventions
- Use standard HTTP methods:
  - `GET`: Retrieve data
  - `POST`: Create data
  - `PUT`: Update data
  - `DELETE`: Remove data
- Route naming: `/resource/:id` or `/resource/action`
- Pluralize resource names in routes

### Access Control
- Implement middleware for route protection
- Use JWT Bearer tokens for protected endpoints
- Structure: `Authorization: Bearer AccessToken`
- Validate client applications for external integrations

## 3. Data Model Design

### Field Structure
- Define clear field types for all data models
- Include validation rules and constraints
- Use descriptive field names
- Implement proper indexing for frequently queried fields

### Enum Standards
- Define enums for fixed value sets
- Use uppercase naming convention
- Document all possible values and their meanings
- Implement enum validation at API level


### Validation Rules
- Required field validation
- Type checking (string, number, boolean, etc.)
- Format validation (email, dates, etc.)
- Business rule validation

## 4. Component Grouping

### UI Component Organization
- Group related UI components together
- Create reusable component libraries
- Implement consistent styling and theming
- Use component composition for complex interfaces

### Backend Module Structure
- Organize by feature/domain
- Separate concerns: routes, controllers, models, services
- Implement dependency injection
- Use middleware for cross-cutting concerns

### Common Component Patterns
- **Navigation Components**: Bars, menus, breadcrumbs
- **Form Components**: Input fields, validation, submission
- **List Components**: Tables, cards, pagination
- **Detail Components**: Read-only views, edit modes

## 5. Sequence Diagram Standards

### Actor Definitions
- Define clear actors: User, UI, API, Database, External Services
- Use consistent lifeline representations
- Include actor descriptions and responsibilities

### Interaction Patterns
- Show clear message flow between components
- Include request/response pairs
- Use proper arrow types (synchronous, asynchronous, return)
- Implement alt/loop/opt blocks for conditional logic

### Diagram Organization
- Group related sequence diagrams
- Use descriptive titles and descriptions
- Include timing and concurrency considerations
- Document error handling paths

## 6. Authentication & Authorization

### JWT Token Management
- Implement access and refresh token pattern
- Set appropriate token expiration times
- Store tokens securely on client side
- Implement token refresh logic

### Authentication Flow
- User signup with email validation
- Email confirmation process
- Password reset functionality
- Two-factor authentication support

### Authorization Rules
- Role-based access control
- Resource-level permissions
- Route protection middleware
- Client application authorization

### Security Standards
- Password hashing and salting
- Token revocation mechanisms
- Rate limiting for auth endpoints
- Secure cookie handling

## 7. Error Handling

### Error Response Format
```javascript
{
  error: "descriptive_error_message",
  details: "additional_context_if_needed",
  code: "error_code_for_programmatic_handling"
}