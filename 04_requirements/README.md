# Functional and Non-Functional Requirements: Overview and Guide

## What Are Functional and Non-Functional Requirements?

In software development, requirements are formal specifications of what a system must do and how it must behave. Requirements bridge the gap between high-level product concepts (like user stories) and detailed technical designs. They provide a common language for product managers, designers, developers, and QA engineers.

Requirements are typically divided into two categories: **functional** and **non-functional**.

### Functional Requirements

A **functional requirement** specifies a capability or behavior that the system must provide. Functional requirements describe *what* the system does—the features, functions, and interactions users will experience. They articulate concrete, observable behaviors that can be tested and verified.

**Examples of Functional Requirements:**
- "The system shall allow users to search for products by name, category, and price range."
- "The system shall display search results within 2 seconds."
- "The system shall calculate tax based on shipping address."
- "The system shall prevent duplicate user registrations using the same email address."
- "The system shall send an order confirmation email immediately after payment is processed."

### Non-Functional Requirements

A **non-functional requirement** specifies a quality attribute, performance characteristic, or operational constraint of the system. Non-functional requirements describe *how well* the system must perform or behave—its speed, reliability, security, scalability, and other quality characteristics. They are constraints or service level expectations that apply across the entire system or multiple features.

**Examples of Non-Functional Requirements:**
- "The system shall support 10,000 concurrent users without performance degradation."
- "All passwords shall be hashed using bcrypt with a minimum cost factor of 12."
- "The system shall maintain 99.9% uptime."
- "The system shall comply with WCAG 2.1 Level AA accessibility standards."
- "The system shall be available in English, Spanish, and French."

### The Relationship Between Requirements and User Stories

User stories and requirements complement each other but serve different purposes:

**User Stories** (from user_stories.md):
- Focus on *who* and *why*: "As a customer, I want to search for products so I can find what I'm looking for."
- Are written from the user's perspective
- Are relatively brief and serve as conversation starters
- Emphasize user value and outcomes

**Functional Requirements**:
- Focus on *what* and *how specifically*: "The system shall support product search by name, category, price range, and rating."
- Are written from a technical perspective
- Are detailed and specific
- Emphasize implementation details and testable behaviors

**Non-Functional Requirements**:
- Focus on quality attributes: "Search results must return within 2 seconds for catalogs up to 100,000 items."
- Apply across multiple user stories or features
- Are measurable and verifiable
- Emphasize performance, quality, and constraints

In practice, you create user stories first (to capture user needs), then derive functional and non-functional requirements from those stories (to specify how to build them).

---

## Categories of Functional Requirements

Functional requirements typically fall into several categories:

### User Interaction & Interface

Requirements for how users interact with the system:
- "The system shall display a login form with fields for email and password."
- "The system shall validate email format before accepting registration."
- "The system shall display an error message if login fails with an appropriate explanation."

### Data & Processing

Requirements for how the system processes data:
- "The system shall store all user passwords using bcrypt hashing."
- "The system shall calculate order totals including tax and shipping."
- "The system shall remove expired sessions after 30 minutes of inactivity."

### Business Logic

Requirements for how the system enforces business rules:
- "The system shall prevent orders with zero items."
- "The system shall apply promotional discounts only to eligible customers."
- "The system shall update inventory immediately after a purchase."

### Integration & External Systems

Requirements for how the system interacts with external systems:
- "The system shall integrate with Stripe API for payment processing."
- "The system shall send email notifications via SendGrid."
- "The system shall log all activities to a centralized logging service."

### Data Storage & Retrieval

Requirements for data persistence and access:
- "The system shall store all user profiles in a relational database."
- "The system shall retain order history for at least 7 years for audit purposes."
- "The system shall support efficient retrieval of product information."

---

## Categories of Non-Functional Requirements

Non-functional requirements typically fall into several categories:

### Performance

How fast and efficient the system must be:
- Response times: "Search results must load within 2 seconds."
- Throughput: "The system must process 1,000 requests per second."
- Resource utilization: "The system must not exceed 80% CPU usage during normal operation."

### Security

How the system must protect data and enforce access control:
- Authentication: "Users must authenticate with email and password."
- Authorization: "Users can only view their own order history."
- Encryption: "All data in transit must use TLS 1.2 or higher."
- Data Protection: "Sensitive data must be encrypted at rest."

### Scalability

How the system must grow with demand:
- User capacity: "System must support 10,000 concurrent users."
- Data volume: "Database must handle 1 million product records."
- Geographic distribution: "System must serve users from multiple geographic regions."

### Reliability and Availability

How often and how well the system must operate:
- Uptime: "System must maintain 99.9% availability."
- Fault tolerance: "System must recover from component failures without data loss."
- Backup and recovery: "Backups must occur hourly with recovery time < 1 hour."

### Usability

How easy and intuitive the system must be:
- Accessibility: "All pages must comply with WCAG 2.1 Level AA."
- Internationalization: "System must support English, Spanish, and French."
- Browser support: "System must work on Chrome, Firefox, Safari, and Edge (latest 2 versions)."

### Maintainability

How easy it must be to maintain and evolve the system:
- Code quality: "All code must follow PEP 8 style guide."
- Documentation: "All functions must include docstrings."
- Logging: "All errors must be logged with full context for debugging."
- Monitorability: "System must expose health check and metrics endpoints."

### Compliance and Legal

Regulatory and legal requirements:
- Data protection: "System must comply with GDPR."
- Industry standards: "System must comply with PCI-DSS for payment data."
- Audit trails: "All user actions must be logged for compliance audits."

---

## How to Write Effective Requirements

### Make Requirements Specific and Measurable

Requirements must be concrete and unambiguous. Developers should know exactly what to build, and QA engineers should know exactly what to test.

**Poor:** "The system should be fast."
**Better:** "The system shall return search results within 2 seconds for databases with up to 100,000 records."

**Poor:** "The system should be secure."
**Better:** "All passwords shall be hashed using bcrypt with a minimum cost factor of 12."

### Use Precise Language

Use requirement language conventions to be clear about whether something is mandatory, optional, or conditional:
- **"Shall"** = Mandatory requirement that must be implemented
- **"Should"** = Strong recommendation that should be implemented unless there is a good reason not to
- **"May"** = Optional feature that can be implemented if resources permit
- **"Must not"** = Prohibited behavior

Example: "The system shall prevent duplicate user registrations" (mandatory)
Example: "The system should send reminder emails 24 hours before an event" (recommended but not mandatory)
Example: "The system may support voice commands" (optional)

### Tie Requirements to User Stories

Every functional requirement should be traceable to one or more user stories. Include the user story identifier (US-XXX) in your requirement. This maintains traceability from user need to implementation.

Example:
- US-003: "As a customer, I want to search for products by category"
- FR-012: "The system shall allow users to filter products by category (Related to US-003)"

### Make Non-Functional Requirements Quantifiable

Non-functional requirements must be measurable so you can verify compliance. Avoid vague language.

**Poor:** "The system shall be reliable."
**Better:** "The system shall maintain 99.9% uptime, with a maximum of 43 minutes of unplanned downtime per month."

**Poor:** "The system shall be secure."
**Better:** "All authentication credentials shall be encrypted in transit using TLS 1.2 or higher, and at rest using AES-256."

### Avoid Implementation Details in Requirements

Requirements should specify *what* the system must do and *how well*, but not necessarily *how* to build it. Implementation details belong in design documents, not requirements.

**Poor:** "The system shall use the bcrypt library to hash passwords."
**Better:** "All passwords shall be hashed using a strong cryptographic algorithm (bcrypt or equivalent) with a minimum cost factor of 12."

(This leaves room for developers to choose bcrypt, scrypt, or other suitable algorithms.)

### Consider the User's Perspective

Write functional requirements with the user in mind. What is the user trying to accomplish, and what does the system need to do to enable that?

**Poor:** "The system shall query the products table and filter by category."
**Better:** "The system shall display only products in the selected category when a user applies the category filter."

### Write Requirements Collaboratively

Requirements should be written by a team, not in isolation. Involve:
- **Product managers** — to ensure requirements capture user needs and business value
- **Developers** — to ensure requirements are implementable and technically sound
- **QA engineers** — to ensure requirements are testable
- **Designers** — to ensure requirements support the intended user experience

---

## Deriving Requirements from User Stories

Once you have completed your User Stories Document, you can derive functional and non-functional requirements.

### Step 1: Review User Stories

For each user story, ask: "What specific behaviors or capabilities does the system need to provide to make this story work?"

**Example User Story:**
- US-005: "As a customer, I want to add items to my cart, so I can purchase multiple products at once."

**Derived Functional Requirements:**
- FR-015: "The system shall add the selected product to the user's shopping cart."
- FR-016: "The system shall update the cart item count displayed in the header."
- FR-017: "The system shall allow users to specify quantity when adding items to cart."
- FR-018: "The system shall display a confirmation message when an item is added to cart."

### Step 2: Identify Performance and Quality Needs

For each user story, ask: "What performance or quality attributes matter for this capability?"

**Example:**
- FR-015 (Add to cart): "FR-015 shall complete within 1 second so users do not experience delays."

### Step 3: Identify Cross-Cutting Requirements

Ask: "What non-functional requirements apply across multiple stories or the entire system?"

**Examples of Cross-Cutting Requirements:**
- All user data must be encrypted at rest
- All API responses must be logged for auditing
- All pages must comply with accessibility standards
- All operations must work on mobile browsers

---

## Requirements Traceability Matrix

A **requirements traceability matrix** (RTM) maps requirements to:
- **User stories** (upstream traceability): Which user story necessitates this requirement?
- **Design elements** (design traceability): How is this requirement addressed in the architecture/design?
- **Test cases** (test traceability): Which test cases verify this requirement?
- **Code** (implementation traceability): Which code modules implement this requirement?

Traceability ensures that:
1. Every requirement is grounded in a user story (no orphaned requirements)
2. Every requirement is implemented (no missed requirements)
3. Every requirement is tested (no unverified requirements)

In practice, maintain traceability by:
- Including user story identifiers (US-XXX) in your requirements
- Including requirement identifiers (FR-XXX, NR-XXX) in your design documents, test plans, and code comments

---

## Common Pitfalls to Avoid

**1. Confusing Requirements with User Stories:** User stories express user needs; requirements specify system behavior. Both are necessary, but they serve different purposes.

**2. Writing Vague Non-Functional Requirements:** "The system shall be fast" is not a requirement; it is not measurable. Write quantifiable targets: "response time < 2 seconds."

**3. Over-Specifying Implementation:** Requirements should specify *what* the system must do, not *how* to build it. Leave implementation decisions to architects and developers.

**4. Missing Non-Functional Requirements:** Many teams focus on functional requirements and neglect non-functional ones. Security, performance, and scalability requirements are just as important.

**5. Failing to Trace Requirements:** If you do not trace requirements to user stories, design, tests, and code, you lose accountability and may miss implementing or testing requirements.

**6. Writing Too Many Requirements:** A common trap is writing a separate requirement for every minor detail. Group related behaviors into single, coherent requirements.

**7. Ignoring Testability:** Every requirement must be testable. If you cannot verify a requirement with tests, it is not a good requirement.

---

## Using Requirements in Subsequent Project Phases

Your Functional and Non-Functional Requirements Document serves multiple purposes:

### In Design

Architects use requirements to design system architecture, data models, and API contracts. Each design element should be traced to requirements it satisfies.

### In Development

Developers use requirements as a specification of what to build. Each code module or feature should implement one or more requirements, and code comments should reference requirement identifiers.

### In Testing

QA engineers use requirements as the basis for test case creation. Each requirement generates one or more test cases. Test reports should show which requirements have been tested and verified.

### In Validation

Product managers and stakeholders use requirements to verify that the product meets expectations. Requirements provide a formal checklist of what should be implemented for the project.

---

## Next Steps

To create your Functional and Non-Functional Requirements Document:

1. Review your MVP Definition Document to confirm which user stories are Must-Haves (part of your MVP).

2. For each Must-Have user story, identify the functional requirements needed to implement it.

3. Group functional requirements by feature area for clarity.

4. Identify non-functional requirements that apply to your MVP (performance, security, scalability, reliability, usability, maintainability, compliance).

5. Ensure that each requirement is specific, measurable, and traceable to user stories.

6. Use consistent identifiers (FR-XXX for functional, NR-XXX for non-functional) to enable cross-referencing.

7. For each non-functional requirement, define quantifiable acceptance criteria so you can verify compliance.

8. Review with your team for completeness and clarity. Do developers understand what to build? Can QA engineers test everything?

9. Define an implementation plan for the user stories and requirements that will be implemented after the MVP.

10. Share with stakeholders to ensure alignment.

Your Functional and Non-Functional Requirements Document will be the detailed specification that guides all design, development, and testing work. Invest time in making it clear, complete, and measurable.
