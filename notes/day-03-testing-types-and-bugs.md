# Day 3 – Testing Types and Bug Lifecycle

## Objective

Understand functional and non-functional testing, smoke, sanity and regression testing, severity vs priority, and the defect lifecycle. Practice writing professional bug reports and identifying automation candidates.

## 1. Functional Testing

Functional testing verifies whether application features work according to requirements.

Examples:
- Login with valid credentials
- Password reset
- User registration
- Add to cart
- Payment processing

## 2. Non-Functional Testing

Non-functional testing evaluates quality characteristics of the application.

Examples:
- Performance
- Security
- Usability
- Accessibility
- Compatibility
- Reliability

### Functional vs Non-Functional

| Functional Testing | Non-Functional Testing |
|---|---|
| Checks what the system does | Checks quality characteristics |
| Validates expected functionality | Evaluates performance, security, usability, etc. |
| Example: Login succeeds | Example: Login responds within an agreed time limit |

## 3. Smoke Testing

Smoke testing checks critical functionality to determine whether a build is stable enough for further testing.

Example:
1. Verify application loads.
2. Verify login works.
3. Verify dashboard loads.
4. Verify critical navigation works.

## 4. Sanity Testing

Sanity testing focuses on verifying a particular change or bug fix.

Example:
After fixing a Forgot Password issue, verify the affected password-reset workflow.

## 5. Regression Testing

Regression testing verifies that existing functionality continues working after changes.

Example:
After adding a new login feature, verify that registration, password reset, and existing login functionality still work.

### Smoke vs Sanity vs Regression

| Type | Purpose | Example |
|---|---|---|
| Smoke | Check critical build functionality | Login and dashboard |
| Sanity | Verify a specific change or fix | Password-reset fix |
| Regression | Detect unintended side effects | Existing features after release |

## 6. Severity vs Priority

Severity describes the impact of a defect.

Priority describes the urgency of fixing the defect.

| Severity | Priority | Example |
|---|---|---|
| High | High | Login completely broken |
| High | Low | Serious failure in rarely used functionality |
| Low | High | Incorrect homepage text before launch |
| Low | Low | Minor alignment issue |

## 7. Bug Lifecycle

Typical stages:

1. New
2. Assigned / Open
3. In Progress
4. Fixed
5. Ready for Retest
6. Verified
7. Closed

Additional statuses:
- Reopened
- Duplicate
- Rejected
- Cannot Reproduce
- Deferred

Actual statuses depend on the team's workflow.

## 8. Practical Bug Reporting Exercise

### BUG-001: Login button does not respond

**Module:** Authentication

**Severity:** High

**Priority:** High

**Preconditions:** An active user account exists.

**Steps to Reproduce:**
1. Open the login page.
2. Enter a valid email.
3. Enter a valid password.
4. Click Login.

**Expected Result:**
The user should be redirected to the dashboard.

**Actual Result:**
The login button does not respond.

**Status:** New

### BUG-002: Forgot Password email validation issue

**Module:** Forgot Password

**Severity:** Medium

**Priority:** Medium

**Steps to Reproduce:**
1. Open the Forgot Password page.
2. Enter an invalid email format.
3. Click Submit.

**Expected Result:**
An appropriate email-format validation message should appear.

**Actual Result:**
The invalid email is accepted without validation.

**Status:** New

### BUG-003: Notification count mismatch

**Module:** Admin – Notifications

**Severity:** Medium

**Priority:** Medium

**Steps to Reproduce:**
1. Log in to the Admin panel.
2. Navigate to Notifications.
3. Observe the total count at the top.
4. Compare it with the pagination total.

**Expected Result:**
Both counts should be consistent when they represent the same notification set and filters.

**Actual Result:**
The displayed total differs from the pagination total.

**Status:** New

**Note:** These three bug reports are hypothetical practice examples. Actual severity, priority, and results should be verified against requirements.

## 9. Connection to Automation Testing

### Good automation candidates

- Valid login
- Invalid login
- Password validation
- Logout
- Critical smoke tests
- Repeatable regression tests
- API response validation

### Tests requiring human evaluation or additional tools

- Exploratory testing
- Subjective visual appearance checks
- Usability evaluation
- Performance and load testing using specialized tools

### My Learning

Automation is particularly useful for repetitive functional checks, especially smoke and regression tests. However, automation results still require investigation, and not every failure represents a product defect.

## 10. Key Takeaways

1. Functional testing verifies application behavior.
2. Non-functional testing evaluates quality characteristics.
3. Smoke testing checks critical build functionality.
4. Sanity testing focuses on specific changes.
5. Regression testing checks existing behavior after changes.
6. Severity describes impact; priority describes urgency.
7. A defect moves through different lifecycle stages.
8. Clear bug reports make defects easier to reproduce and fix.
9. Automation supports testing but does not replace human judgment.

## Day 3 Completion Checklist

- [ ] Understand functional testing.
- [ ] Understand non-functional testing.
- [ ] Differentiate smoke, sanity and regression testing.
- [ ] Understand severity vs priority.
- [ ] Understand the bug lifecycle.
- [ ] Write three sample bug reports.
- [ ] Identify suitable automation candidates.
- [ ] Commit Day 3 notes to GitHub.
