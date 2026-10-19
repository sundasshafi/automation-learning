# Day 1 – Automation Foundations

## Objective

Understand the fundamentals of test automation before starting automation coding.

---

## 1. What is Test Automation?

Test automation is the use of software tools and scripts to automatically execute test cases, perform actions, and verify expected results.

Instead of manually performing the same test repeatedly, an automated test can perform the steps and report whether the test passed or failed.

### Example

Manual test:

1. Open the application.
2. Enter a valid username.
3. Enter a valid password.
4. Click Login.
5. Verify that the dashboard is displayed.

Automated test:

```text
Automation Script
       ↓
Open application
       ↓
Enter username
       ↓
Enter password
       ↓
Click Login
       ↓
Verify dashboard
       ↓
PASS / FAIL
```

---

## 2. Why Do We Use Test Automation?

Test automation can help with:

- Repetitive testing
- Regression testing
- Smoke testing
- Faster test execution
- Running tests frequently
- Reducing repetitive manual effort
- Running tests with different data
- Supporting CI/CD pipelines
- Producing consistent test results

Automation does not replace QA knowledge. A tester still needs to understand requirements, risks, test scenarios, expected behavior, and defects.

---

## 3. When Should a Test Be Automated?

A test is a good candidate for automation when:

- It is executed frequently.
- It is part of regression testing.
- It is repetitive.
- It has stable expected results.
- It takes a long time to execute manually.
- It needs to be executed against multiple sets of data.
- It is important to the application.
- It is likely to be executed many times in the future.

### Example

Login with valid credentials is a good automation candidate because it is usually executed frequently during regression testing.

---

## 4. When Should a Test NOT Be Automated?

A test may not be a good automation candidate when:

- It will only be executed once.
- The functionality is changing constantly.
- The test requires human judgment.
- The automation effort is greater than the testing benefit.
- The feature is highly unstable.
- Exploratory testing is required.

### Example

Checking whether a newly designed page looks visually appealing may require human judgment and may not be suitable for a basic functional automation test.

---

## 5. Manual Testing vs Automation Testing

| Manual Testing | Automation Testing |
|---|---|
| Tester performs steps manually | Script performs steps automatically |
| Usually slower for repetitive tests | Faster for repetitive tests |
| Good for exploratory testing | Good for repetitive regression testing |
| Requires manual execution every time | Can be executed repeatedly |
| Human judgment is useful | Best for predictable checks |
| Results may depend on manual execution | Results can be consistent |

Automation and manual testing are not competitors. They complement each other.

---

# 6. Automation Candidates from Manual Testing

I selected the following manual test scenarios to evaluate whether they should be automated.

### Test 1 – Login with Valid Credentials

**Automation:** YES

**Reason:** Login is frequently tested and is usually part of smoke and regression testing.

---

### Test 2 – Login with Invalid Password

**Automation:** YES

**Reason:** This is a repeatable validation and can easily be executed automatically during regression testing.

---

### Test 3 – Forgot Password with Invalid Email

**Automation:** YES

**Reason:** Email validation is a repeatable functional check and can be automated.

---

### Test 4 – Check Whether the UI Looks Visually Appealing

**Automation:** NO

**Reason:** Visual and aesthetic judgment may require human evaluation.

---

### Test 5 – Logout

**Automation:** YES

**Reason:** Logout is a stable and repeatable functional scenario that can be included in regression testing.

---

# 7. My Automation Decision

| Test Scenario | Automate? | Reason |
|---|---|---|
| Valid login | Yes | Frequently executed |
| Invalid password | Yes | Repeatable validation |
| Invalid email | Yes | Stable functional validation |
| Visual appearance | No | Requires human judgment |
| Logout | Yes | Stable regression scenario |

---

# 8. Key Takeaways

Today I learned that:

1. Test automation uses scripts and tools to execute tests automatically.
2. Automation is especially useful for repetitive and frequently executed tests.
3. Not every manual test should be automated.
4. Regression testing is an important area for automation.
5. Human judgment and exploratory testing still require manual testing.
6. Good automation starts with good testing knowledge.
7. Automation should reduce repetitive effort rather than simply automate everything.

---

## Day 1 Status

- [x] Understand what test automation is
- [x] Understand why automation is useful
- [x] Identify good automation candidates
- [x] Identify poor automation candidates
- [x] Evaluate manual test scenarios
- [x] Document Day 1 learning
