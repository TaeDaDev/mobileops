MobileOps — Product Requirements Document
Product direction selected
Version 1.0
November 9, 2026

1. Product overview
Product name: MobileOps

Product category: SaaS / Operations Management

Product vision: Build a centralized operations platform that helps mobile service businesses manage their daily operations, customers, jobs, employees, and business performance.

MobileOps aims to eliminate disconnected spreadsheets, manual processes, and inefficient communication by bringing essential business operations into one platform.

The long-term ambition is to develop MobileOps into a scalable business operations platform.
2. Problem statement
Mobile service businesses often manage their operations through disconnected systems.

Examples include:
- Customer information stored in spreadsheets.
- Jobs assigned through text messages.
- Scheduling handled manually.
- Invoices managed separately.
- Employees communicating through different applications.
- Business owners lacking visibility into daily performance.
Our opportunity: Provide a centralized system that makes running a mobile service business easier, more organized, and more efficient.

These problems are initial product hypotheses that require customer interviews and validation.
3. Target customers
Initial customer segments:
Segment	Potential use case
Mobile mechanics	Job scheduling and customer management
Cleaning businesses	Employee and appointment management
Landscaping companies	Job assignments and scheduling
Mobile detailing	Customer and service management
Other field services	Daily operations management

Initial market hypothesis: Small and growing mobile service businesses that need operational software without enterprise-level complexity.

We will validate the first customer segment before committing to a narrow market.
4. Product objectives
Primary objectives
1. Centralize customer information.
2. Make job creation and management straightforward.
3. Improve scheduling and assignment workflows.
4. Provide visibility into business operations.
5. Reduce repetitive administrative work.
6. Build an architecture that supports future growth.
Non-goals for the initial MVP
- Building a complete accounting platform.
- Replacing enterprise ERP software.
- Developing a sophisticated AI assistant.
- Supporting every possible industry-specific workflow.
- Building native iOS and Android applications immediately.
5. MVP feature requirements
Core MVP scope
Feature	Priority	Description
Authentication	P0	Secure user registration and login
Dashboard	P0	Overview of business operations
Customer management	P0	Create, view, edit, and manage customers
Job management	P0	Create and manage service jobs
Scheduling	P0	View and organize upcoming jobs
Employee management	P1	Manage employees and assignments
Job status tracking	P0	Track job progress
Notifications	P1	Notify users about important events
Reporting	P1	Basic operational metrics
Payments	P2	Payment processing integration

P0 means necessary for the initial usable product. P1 and P2 features can follow.
6. User stories
Business owner
- As a business owner, I want to see all upcoming jobs so I can understand daily operations.
- As a business owner, I want to create customer records so customer information stays organized.
- As a business owner, I want to assign jobs to employees so responsibilities are clear.
- As a business owner, I want to monitor job statuses so I know which jobs are completed or outstanding.
Employee
- As an employee, I want to see my assigned jobs so I know what work needs to be completed.
- As an employee, I want to update job statuses so management can track progress.
- As an employee, I want access to relevant customer and job information.
7. Technical direction
The architecture should support a professional full-stack development workflow without making the first release unnecessarily complicated.
Layer	Proposed technology
Frontend	React + TypeScript
Backend	Node.js + TypeScript
API	REST API
Database	PostgreSQL
ORM	Prisma
Authentication	Secure session-based authentication
Cloud	AWS
Version control	Git + GitHub
CI/CD	GitHub Actions
Testing	Vitest + Playwright
Deployment	AWS-based deployment

These are proposed technical choices, not irreversible decisions.
AWS direction
We should learn AWS through implementation rather than attempting to master every service before building.

Initial services to investigate:
- AWS IAM
- AWS RDS
- AWS S3
- AWS CloudWatch
- AWS ECS or another suitable application hosting option
- AWS Secrets Manager
8. CI/CD requirements
Every change should follow a professional development workflow.

Proposed pipeline:
1. Developer creates a feature branch.
2. Developer implements the feature.
3. Code is pushed to GitHub.
4. GitHub Actions runs linting.
5. Automated tests execute.
6. Build verification runs.
7. Pull request is reviewed.
8. Approved changes merge into the main branch.
9. Deployment pipeline releases the application.
No untested changes should automatically reach production.
9. Security requirements
- Passwords must never be stored in plaintext.
- Authentication must use secure practices.
- API endpoints must enforce authorization.
- Users must only access data belonging to their organization.
- Secrets must not be committed to Git.
- Validate and sanitize incoming data.
- Protect against common web application vulnerabilities.
- Maintain appropriate backups and logging.
Multi-tenant data isolation is particularly important because MobileOps is intended to support multiple businesses.
10. Success metrics
We need to measure whether the product actually solves a problem.
Metric	What it measures
Customer activation	Businesses successfully setting up MobileOps
Weekly active users	Actual product usage
Jobs created	Operational activity
Job completion rate	Workflow effectiveness
Customer retention	Whether customers continue using the platform
Administrative time saved	Product value to customers

We should establish numerical targets after initial customer discovery.
11. Development roadmap
1. Phase 1 — Product foundation
   - Finalize requirements.
   - Define initial customer segment.
   - Design database schema.
   - Establish GitHub repository.
   - Configure development environment.
   - Establish coding standards.
2. Phase 2 — Core backend
   - Authentication.
   - Organization management.
   - Customer CRUD operations.
   - Job management.
   - API validation and authorization.
3. Phase 3 — Frontend
   - Dashboard.
   - Customer management interface.
   - Job management interface.
   - Scheduling interface.
   - Employee workflows.
4. Phase 4 — Infrastructure
   - AWS environment.
   - Database deployment.
   - CI/CD implementation.
   - Logging and monitoring.
   - Production deployment.
5. Phase 5 — Testing and validation
   - Automated testing.
   - Security review.
   - User acceptance testing.
   - Customer interviews.
   - Initial pilot release.
12. Open product decisions
These are decisions we must resolve before committing to the complete architecture.
Decision	Current status
Initial customer segment	Needs validation
Multi-tenant architecture	Proposed
Subscription pricing	Undecided
Employee permissions	Needs specification
Payment integration	Future consideration
Scheduling complexity	MVP requirements need refinement
Mobile experience	Responsive web initially

13. Definition of MVP completion
The MVP is considered ready for initial customer testing when:
- [ ] A business can register and create an organization.
- [ ] A business owner can securely log in.
- [ ] Customers can be created and managed.
- [ ] Jobs can be created and assigned.
- [ ] Job statuses can be updated.
- [ ] Upcoming jobs can be viewed.
- [ ] Organization data is properly isolated.
- [ ] Automated tests cover critical workflows.
- [ ] CI/CD successfully builds and deploys the application.
- [ ] The application is deployed to AWS.
- [ ] At least one real business has tested the product.

14. Product management rules
Going forward, we'll operate under these rules:
1. No unnecessary features. Every feature needs a reason to exist.
2. No coding ahead of requirements. Understand the task before implementing it.
3. Use Git professionally. Feature branches, commits, pull requests, and reviews.
4. Document decisions. Important technical and product decisions should be recorded.
5. Test everything important. Passing a visual inspection isn't enough.
6. Validate with customers. Don't assume we understand the market.
7. Prioritize shipping. Avoid overengineering the MVP.
