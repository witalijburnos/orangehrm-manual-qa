# Project Charter

## Project Information

| Field | Value |
|---|---|
| Project name | OrangeHRM Manual QA |
| System under test | OrangeHRM Starter |
| Application version | 5.9 |
| Project type | Manual Web Application Testing |
| Test environment | Local Docker environment |
| Database | MySQL 8.4 |
| Tester | Witalij |
| Project status | In Progress |
| Start date | 2026-09-14 |

## Project Objective

The objective of this project is to perform structured manual testing
of selected OrangeHRM functionality and prepare a professional set of
QA artifacts suitable for a Junior QA Engineer portfolio.

The project demonstrates requirements analysis, risk-based testing,
test design, test documentation, defect reporting, exploratory testing,
cross-browser testing, responsive testing, and technical investigation
using browser developer tools.

## System Under Test

OrangeHRM Starter is an open-source human resource management system.
The tested instance is deployed locally using Docker and connected to
a dedicated MySQL database.

A local environment was selected to provide stable test data,
reproducible test results, and control over the application version.

## Test Scope

The following modules are included in the project:

### Authentication

- Login with valid and invalid credentials
- Required-field validation
- Logout
- Session behavior
- Access to protected pages
- Disabled-user authentication

### PIM and Employee Management

- Creating an employee
- Viewing employee information
- Editing employee information
- Searching and filtering employees
- Employee list behavior
- Uploading an employee photograph
- Deleting an employee
- Field validation

### User Management

- Creating a system user
- Assigning a user role
- Linking a user to an employee
- Enabling and disabling a user
- Searching and filtering users
- Editing a system user
- Deleting a system user
- Verifying relationships between employees and users

## Primary Business Flow

1. An administrator creates a new employee.
2. The administrator creates a system user linked to that employee.
3. The system user logs in using valid credentials.
4. The administrator changes the user's status or employee data.
5. The administrator deletes or disables the user.
6. The system enforces the expected access restrictions.

## Out of Scope

The following areas are excluded from this project:

- Test automation
- Direct API testing
- Direct database testing
- Performance and load testing
- Penetration and security testing
- Mobile application testing
- Accessibility audit beyond basic observations
- Modules other than Authentication, PIM, and User Management
- Modification of the OrangeHRM source code


## Test Types

The project includes:

- Functional testing
- Positive and negative testing
- Smoke testing
- Sanity testing
- Regression testing
- Retesting
- Exploratory testing
- Cross-browser testing
- Responsive testing
- Basic usability testing

## Test Design Techniques

The following techniques will be applied where appropriate:

- Equivalence partitioning
- Boundary value analysis
- Decision table testing
- State transition testing
- Use-case testing
- Pairwise testing
- Error guessing

## Test Environment

| Component | Configuration |
|---|---|
| Operating system | Windows 11 |
| Deployment | Docker Desktop and Docker Compose |
| Application container | OrangeHRM Starter 5.9 |
| Web server | Apache |
| Application runtime | PHP 8.3 |
| Database | MySQL 8.4 |
| Application URL | http://localhost:8080 |
| Primary browser | To be recorded |
| Additional browsers | To be recorded |
| Screen resolutions | To be recorded |

Exact browser versions will be recorded when test execution begins.

## Test Data Policy

Only fictional test data will be used.

The project will not contain:

- Real employee information
- Real email addresses
- Authentication passwords
- Session identifiers
- Access tokens
- Unredacted network files containing sensitive information

Test entities will use identifiable prefixes such as `QA_` to simplify
searching and cleanup.

## Assumptions

- The local OrangeHRM 5.9 installation is treated as the test baseline.
- The Docker environment remains unchanged during a test cycle.
- Official OrangeHRM documentation is used as a source of expected behavior.
- Undocumented behavior is recorded as an assumption or question before
  being classified as a defect.
- Test data can be created, modified, and deleted without business impact.

## Constraints

- The project is performed by one tester.
- No product owner, developer, or business analyst is directly available.
- Some expected results must be derived from official documentation,
  interface behavior, and business logic.
- Testing is limited to a local environment.
- Email delivery and external integrations may not be available.

## Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Missing detailed requirements | Incorrect expected results | Record assumptions and use official documentation |
| Local environment differs from production | Environment-specific results | Document the exact configuration |
| Test data affects later test cases | Unreliable execution results | Use unique data and perform cleanup |
| Browser-specific behavior | Defects may remain undetected | Execute critical tests in multiple browsers |
| Scope becomes too large | Superficial testing | Limit testing to three related modules |
| Sensitive data appears in evidence | Unsafe public repository | Review and sanitize all attachments |

## Planned Deliverables

- Product overview
- Requirements analysis
- Test plan
- Risk assessment
- Test-design documentation
- Checklists
- Test cases
- Smoke and regression suites
- Exploratory testing reports
- Bug reports
- DevTools investigation report
- Requirements traceability matrix
- Test execution results
- Jira/Xray evidence
- Test summary report
- Portfolio README

## Entry Criteria

Testing may begin when:

- OrangeHRM 5.9 is installed and accessible.
- The MySQL database is connected.
- The administrator can log in.
- Authentication, PIM, and User Management are available.
- The test environment configuration is documented.

## Exit Criteria

The project may be completed when:

- All planned high-priority tests have been executed.
- All critical business flows have been tested.
- Failed tests are linked to defects or explained.
- Confirmed defects contain sufficient evidence.
- Retesting and the planned regression cycle are completed.
- Remaining risks and limitations are documented.
- The final test summary report is prepared.