# Day 2 – Testing Foundations

## Objective

Understand SDLC, STLC, test case design, equivalence partitioning, and boundary value analysis. Apply these concepts to login testing and prepare for future test automation.

## 1. Software Development Life Cycle (SDLC)

SDLC describes the process of developing, releasing, and maintaining software.

Main phases:
1. Requirements
2. Planning and design
3. Development
4. Testing
5. Deployment
6. Maintenance

### Role of QA in SDLC

QA reviews requirements, identifies risks, designs test cases, tests the application, reports defects, and verifies fixes. QA can be involved throughout development, not only after coding is finished.

## 2. Software Testing Life Cycle (STLC)

STLC describes the main activities involved in testing software.

1. Requirement analysis
2. Test planning
3. Test case design
4. Test environment setup
5. Test execution
6. Defect reporting and retesting
7. Test closure

### How automation fits into STLC

- Test design: Identify suitable automation candidates.
- Environment setup: Configure Node.js, Playwright, and other required tools.
- Execution: Run automated tests.
- Defect reporting: Investigate failures and report confirmed product defects.
- Test closure: Review results, coverage, and remaining risks.

## 3. SDLC vs STLC

| SDLC | STLC |
|---|---|
| Covers the overall software lifecycle | Covers testing activities |
| Includes development and deployment | Includes test design and execution |
| Involves multiple project roles | Focuses on testing activities and collaboration |

## 4. Test Case Design

A test case defines the steps, test data, and expected outcome used to verify a particular behavior.

A good test case includes:
- Test Case ID
- Title
- Preconditions
- Test data
- Steps to reproduce
- Expected result
- Actual result
- Status

## 5. Equivalence Partitioning

Equivalence partitioning divides input data into groups expected to behave similarly.

Example: An age field accepts values from 18 to 60 inclusive.

| Partition | Example | Expected result |
|---|---:|---|
| Below minimum | 17 | Reject |
| Valid range | 30 | Accept |
| Above maximum | 61 | Reject |

## 6. Boundary Value Analysis

Boundary value analysis focuses on values at and around the limits of an allowed range.

For an age field accepting 18–60:

| Input | Expected result |
|---:|---|
| 17 | Reject |
| 18 | Accept |
| 19 | Accept |
| 59 | Accept |
| 60 | Accept |
| 61 | Reject |

## 7. Login Test Case Exercise

Assumed requirements:
- Email is required and must have a valid format.
- Password is required.
- Valid credentials allow login.
- Invalid credentials display an appropriate error.

Create test cases for:
1. Valid credentials.
2. Incorrect password.
3. Unregistered email.
4. Both fields empty.
5. Empty email.
6. Empty password.
7. Invalid email format.
8. Email with leading or trailing spaces.
9. Incorrect password casing.
10. Password masking.

For every test case, document the ID, preconditions, test data, steps, and expected result.

### My test cases

Add your completed login test cases here.

| Test Case ID | Scenario | Expected Result |
|---|---|---|
| TC_LOGIN_001 | Valid credentials | User reaches dashboard |
| TC_LOGIN_002 | Incorrect password | Appropriate error is displayed |
| TC_LOGIN_003 | Unregistered email | Appropriate error is displayed |
| TC_LOGIN_004 | Both fields empty | Required-field validations appear |
| TC_LOGIN_005 | Empty email | Email validation appears |
| TC_LOGIN_006 | Empty password | Password validation appears |
| TC_LOGIN_007 | Invalid email format | Email format validation appears |
| TC_LOGIN_008 | Email with surrounding spaces | Behavior matches requirements |
| TC_LOGIN_009 | Incorrect password casing | Login fails unless password rules specify otherwise |
| TC_LOGIN_010 | Password masking | Password is masked while typing |

## 8. Connection to Test Automation

A manual test case can later become an automated test.

- Manual steps become browser actions.
- Test data becomes input to the script.
- Expected results become assertions.
- Test execution produces a pass or fail result.

Example: An automated login test can open a page, enter credentials, click Login, and assert that the dashboard is visible.

## 9. Key Takeaways

1. SDLC covers the broader software development lifecycle.
2. STLC covers testing activities.
3. Clear test cases make manual and automated testing more reliable.
4. Equivalence partitioning reduces redundant test data.
5. Boundary value analysis focuses on input limits.
6. Expected results are essential for determining whether a test passes.
7. Good test design is the foundation of reliable automation.

## Day 2 Completion Checklist

- [ ] Understand SDLC.
- [ ] Understand STLC.
- [ ] Explain the difference between SDLC and STLC.
- [ ] Understand test case structure.
- [ ] Practice equivalence partitioning.
- [ ] Practice boundary value analysis.
- [ ] Complete 10 login test cases.
- [ ] Review which cases are suitable for automation.
- [ ] Save and commit this file to GitHub.
