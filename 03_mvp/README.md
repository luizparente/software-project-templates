# MVP Definition: Overview and Guide

## What Is an MVP?

An **MVP (Minimum Viable Product)** is the smallest, most focused version of your product that is capable of delivering core value to users and solving the primary problem your product is designed to address. The term was popularized by entrepreneur Eric Ries and the Lean Startup methodology, and it has become a foundational concept in software development.

The key word in MVP is *minimum*. The goal is not to build everything you can imagine, but to build *only* what is necessary to validate your product concept, learn from users, and iterate. By launching with an MVP, you can:

1. **Get to market faster** — Launch with less time, cost, and resource investment
2. **Validate assumptions** — Test whether users actually want your product before investing heavily
3. **Gather real feedback** — Learn from real users in real conditions, not from hypothetical scenarios
4. **Reduce risk** — Minimize the cost of being wrong; if the MVP fails, you have not invested years
5. **Iterate based on data** — Use user feedback to guide future development rather than guessing

An MVP is not a beta version or a "half-baked" product. It is a fully functional, polished product that addresses a well-defined problem for a specific user base, even if it lacks some features that would be nice to have.

### MVP vs. Full Feature Set

Consider an e-commerce platform:

**Full Feature Set Might Include:**
- User registration and login
- Product browsing, filtering, and search
- Shopping cart and checkout
- Payment processing (with 5+ payment methods)
- Order tracking and history
- User reviews and ratings
- Wish lists and saved items
- Admin dashboard with analytics
- Email notifications
- Mobile app (iOS and Android)
- Advanced personalization engine
- Live chat support
- API for third-party integrations

**MVP Might Include:**
- User registration and login
- Product browsing and basic search
- Shopping cart and checkout
- Payment processing (1–2 payment methods)
- Email order confirmation

Notice the difference: the MVP has ~10% of the features but delivers ~80% of the core value. Users can register, browse products, and make purchases—the essential functions. Features like reviews, wish lists, advanced analytics, and mobile apps are deferred.

---

## The Five Categories

When planning an MVP, categorize all user stories into five categories that reflect their timing and importance:

### 1. Must-Haves

**Definition:** Absolutely essential features without which the product cannot fulfill its core purpose.

**Characteristics:**
- Directly solve the primary problem identified in your Project Proposal
- Are referenced explicitly in your Value Proposition
- Without them, the product is fundamentally broken or unusable
- All users will encounter or need these features
- They represent the core product experience

**Examples:**
- In an e-commerce platform: user registration, product listing, shopping cart, checkout, payment processing
- In a task management tool: task creation, task assignment, task status tracking
- In a video streaming service: video playback, video library browsing, user accounts

**Timeline:** All Must-Haves are implemented for the MVP launch.

**How Many?** Typically 5–15 Must-Have stories for a well-scoped MVP. If you have more than 20 Must-Haves, your MVP scope may be too broad.

### 2. Should-Haves

**Definition:** Important features that significantly enhance the user experience but are not critical for launch.

**Characteristics:**
- Improve usability, performance, or user satisfaction
- Address common use cases or workflows, but not all
- Add polish or sophistication to the core experience
- Are needed soon after launch but not on day one
- Often emerge from user feedback on the MVP

**Examples:**
- In an e-commerce platform: email notifications, order history, user ratings and reviews
- In a task management tool: task templates, task analytics, bulk operations
- In a video streaming service: watch history, recommendations, playlist creation

**Timeline:** Should-Haves are typically implemented in the first or second post-launch update (v1.1, v1.2, etc.)

**How Many?** Typically 5–15 Should-Haves. This represents your near-term roadmap after launch.

### 3. Nice-To-Haves

**Definition:** Desirable features that add delight or differentiation but are not essential.

**Characteristics:**
- Enhance the product but are not necessary for core functionality
- May appeal to a subset of users, not all
- Can be implemented if time and resources permit
- Often represent opportunities for product differentiation
- May depend on mature core features to be implemented

**Examples:**
- In an e-commerce platform: advanced filtering, personalization, gamification (badges, achievements), wish lists
- In a task management tool: advanced reporting, Gantt charts, time tracking
- In a video streaming service: custom playlists, social features, offline download

**Timeline:** Nice-to-Haves are candidates for later releases after Should-Haves are complete, or they may be implemented incrementally if there is available capacity.

**How Many?** Typically 5–20 Nice-to-Haves. These represent longer-term ideas that make the product more compelling.

### 4. May-Haves

**Definition:** Speculative or exploratory features that may or may not be implemented.

**Characteristics:**
- Depend on external factors like user feedback, technical feasibility, or market developments
- Are ideas you are considering but have not committed to
- May become Must-Haves or Should-Haves after user feedback; may be abandoned
- Are candidates for re-evaluation after MVP launch
- Often represent experimental features or niche use cases

**Examples:**
- In an e-commerce platform: integration with third-party marketplaces, AI-powered recommendations, AR product previews
- In a task management tool: mobile app, voice commands, AI-assisted task creation
- In a video streaming service: live streaming capability, social gaming, virtual reality support

**Timeline:** May-Haves are not committed to any specific release. They are re-evaluated quarterly or after gathering sufficient user feedback.

**How Many?** Typically 3–10 May-Haves. These represent ideas you want to track but are not yet committed to.

### 5. Out of Scope

**Definition:** Features or capabilities that you have explicitly decided *not* to build.

**Characteristics:**
- Fall outside your product's core mission or domain
- Are better served by other products or integrations
- Require resources or expertise you do not have
- Are deferred indefinitely, not just to a future release
- Are explicitly listed to manage stakeholder expectations

**Examples:**
- In an e-commerce platform: marketplace seller features (if you are building a B2C platform, not a marketplace), hardware logistics, custom manufacturing
- In a task management tool: accounting and invoicing (unless you are a business suite), AI copilot (too speculative for MVP)
- In a video streaming service: video creation tools, social network features, gaming platform

**Timeline:** Out of scope features are not built as part of this product. If circumstances change, they can be re-evaluated and moved to May-Haves or lower categories.

**How Many?** Typically 2–5 Out of Scope items. These are usually things stakeholders or customers have requested that you have decided to pass on.

---

## How to Categorize User Stories

### Step 1: Understand Your Core Value Proposition

Before categorizing stories, revisit your Project Proposal Document, specifically:
- The Problem Statement: What is the primary problem you solve?
- The Proposed Solution: What is your core solution?
- The Value Proposition: What are the key benefits users realize?

Stories that directly enable these elements are Must-Haves. Stories that enhance or support them are Should-Haves or lower.

### Step 2: Categorize Defensibly

For each user story, ask:

**Is this a Must-Have?**
- Would the product be fundamentally broken without this story?
- Do all (or nearly all) users need this feature?
- Is this explicitly promised in my Value Proposition?
- If I launch without this, will users find the product unusable?

If you answer "yes" to all questions, it is a Must-Have. If you answer "no" to any, move to the next category.

**Is this a Should-Have?**
- Does this significantly improve the user experience?
- Will many users want this feature?
- Can I launch without it and still have a viable product?
- Is this something I plan to add within 3 months of launch?

If yes to all, it is a Should-Have.

**Is this a Nice-To-Have?**
- Does this delight users or add differentiation?
- Is this useful to some, but not all, users?
- Can I realistically build this after launch?
- Would removing this from the MVP hurt significantly?

If yes, it is a Nice-to-Have.

**Is this a May-Have?**
- Am I unsure about the value or feasibility of this?
- Do I need user feedback before committing to this?
- Might this depend on technical breakthroughs or partnerships?
- Is this worth tracking but not worth committing to?

If yes, it is a May-Have.

**Is this Out of Scope?**
- Does this fall outside my product's core mission?
- Would building this require me to become a different product?
- Is there a better way to address this need (e.g., integration, partnership)?
- Have I explicitly decided not to build this?

If yes, it is out of scope.

### Step 3: Validate Your Categorization

Review your categorization with your team and stakeholders. Ask:

1. **MVP Defensibility:** Can you justify why each Must-Have is essential? If any Must-Have is hard to justify, it might be a Should-Have.

2. **MVP Completeness:** Do your Must-Haves collectively deliver the value promised in your proposal? If not, you may be missing Must-Haves.

3. **Scope Reasonableness:** Do you have 5–15 Must-Haves? Significantly fewer suggests you might be missing critical features. Significantly more suggests you need to be more ruthless about what is truly essential.

4. **Alignment:** Do your Should-Haves align with user feedback and market expectations? Are there obvious features that users expect that you have placed in Should-Haves or lower?

---

## Creating the MVP Implementation Plan

Once you have identified your Must-Haves, the next step is to determine the order in which to implement them. This is where dependencies and parallelization become important.

### Understanding Dependencies

A **dependency** is when one user story cannot be implemented until another is complete. For example:

- "US-002: User Login" depends on "US-001: User Registration" because you cannot log in if users cannot create accounts.
- "US-005: View Cart Total" depends on "US-003: Add Item to Cart" because you cannot calculate a total without items in the cart.

When creating your implementation plan, identify all dependencies. This ensures that:
1. You do not assign work on dependent stories until their dependencies are complete
2. You sequence work efficiently to minimize blocking

### Understanding Relationships (Non-Blocking Connections)

A **relationship** is when one user story is related to or shares context with another, but does not strictly depend on it. For example:

- "US-003: Add Item to Cart" relates to "US-004: Remove Item from Cart" (both about cart management, but you can build remove before add)
- "US-010: View Order History" relates to "US-005: Complete Checkout" (both about orders, but history does not block checkout)

Related stories are good candidates for parallel implementation. Two developers can work on related stories simultaneously because neither blocks the other.

### Sequencing Your Implementation

Use these guidelines to sequence Must-Have stories:

1. **Start with stories that have no dependencies.** These establish a foundation and allow other developers to start working in parallel.

2. **Respect all dependencies.** A story should never be scheduled before its dependencies.

3. **Group related stories together.** If two stories are related and have similar dependencies, schedule them close together so the same developer or team can work on related context.

4. **Front-load foundational work.** Authentication, user management, and core data models often need to be done first so other features can build on them.

5. **Aim for a reasonable number of parallel work streams.** If you have 5 developers, aim for 3–5 distinct work streams (groups of stories being developed in parallel) so people can work efficiently.

### Example Implementation Plan

**Scenario:** E-commerce MVP with Must-Have stories:
- US-001: User Registration
- US-002: User Login
- US-003: View Product Catalog
- US-004: Search Products
- US-005: Add Item to Cart
- US-006: Remove Item from Cart
- US-007: View Cart Total
- US-008: Checkout
- US-009: Process Payment
- US-010: Confirm Order

**Implementation Plan:**

| Priority | User Story | Depends On | Relates To |
|----------|-----------|-----------|-----------|
| 1 | US-001: User Registration | None | US-002 |
| 2 | US-002: User Login | US-001 | None |
| 3 | US-003: View Product Catalog | None | US-004 |
| 4 | US-004: Search Products | US-003 | None |
| 5 | US-005: Add Item to Cart | US-003 | US-006, US-007 |
| 6 | US-006: Remove Item from Cart | US-005 | None |
| 7 | US-007: View Cart Total | US-005, US-006 | None |
| 8 | US-008: Checkout | US-002, US-007 | US-009 |
| 9 | US-009: Process Payment | US-008 | None |
| 10 | US-010: Confirm Order | US-009 | None |

Notice the sequencing:
- Priorities 1–2: Authentication (foundation)
- Priorities 3–4: Product discovery (can work in parallel with auth)
- Priorities 5–7: Cart management (depends on products, works in parallel with checkout logic)
- Priorities 8–10: Checkout and payment (depends on cart and authentication)

---

## Common Pitfalls to Avoid

**1. MVP Scope Creep:** What starts as 10 Must-Haves gradually becomes 30. Ruthlessly defend Must-Have status. If you are unsure, it is probably a Should-Have.

**2. Confusing Nice-to-Haves with Must-Haves:** Features that would be "nice to have" at launch are not Must-Haves. No matter how cool they sound, if they are not essential to core functionality, they belong in a lower category.

**3. Depending on Assumptions About User Feedback:** You might think "users will want this feature in v1.1," but you do not know until you launch and gather feedback. Be humble about Should-Haves and May-Haves.

**4. Ignoring Dependencies:** Missing dependencies leads to sequencing problems—you schedule a story before its blocking dependency is done. Review dependencies carefully.

**5. Failing to Recognize When Scope Is Too Broad:** If your MVP has more than 20 Must-Haves or requires more than 6 months to build, your scope is probably too broad. Consider whether some Must-Haves should be Should-Haves.

---

## Next Steps

To create your MVP Definition Document:

1. Review your User Stories Document and your Project Proposal Document.

2. For each user story, categorize it into one of the five categories (Must-Have, Should-Have, Nice-to-Have, May-Have, Out of Scope).

3. Defend your Must-Have categorization. Ask: Is this truly essential, or would we still have a viable product without it?

4. Count stories in each category and ensure your MVP is reasonably scoped (typically 5–15 Must-Haves).

5. Create an MVP Implementation Plan that sequences Must-Haves respecting all dependencies.

6. Share with your team and stakeholders for feedback. Are they comfortable with the MVP scope? Do they see obvious features that are mislabeled?

7. Use the MVP Implementation Plan as the basis for sprint planning and task assignment.

Your MVP Definition Document will be your team's guide for the initial development phase. Invest time in getting the scope right—an MVP that is too broad will take too long and delay feedback; an MVP that is too narrow will fail to deliver enough value to validate your concept.
