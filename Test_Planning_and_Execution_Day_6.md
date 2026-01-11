# Software Testing Notes

---

## 1. Test Data Management (TDM)

### What is Test Data?

Test data is the information used to execute test cases and verify whether the application works as expected.

**Examples:**

* Usernames and passwords
* Bank account numbers
* Transaction amounts
* OTPs, dates, files

---

### What is Test Data Management?

Test Data Management is the process of **planning, creating, maintaining, and using test data** effectively so that testing reflects real-world scenarios.

**Analogy**
Test data management is like organizing ingredients before cooking so that nothing is missing during preparation.

---

### Importance of Test Data Management

* Ensures realistic testing similar to real users
* Helps detect edge cases and boundary defects early
* Supports automation, regression, and CI/CD pipelines
* Reduces test execution failures caused by bad data
* Improves test coverage and confidence in quality
* Ensures compliance with data privacy laws (masking/mocking)
* Saves time and cost by avoiding repeated data creation

**Real-life Example:**
Testing an ATM without real account balance data may pass tests but fail in real usage.

* Ensures realistic testing
* Helps find edge and boundary defects
* Supports automation and regression testing
* Avoids data-related test failures
* Protects sensitive customer data

---

### Data Requirement vs Data Gathering

**Data Requirement (WHAT is needed):**

* Identifying the type of data needed for testing
* Done during test planning and test case design

**Examples:**

* Valid user
* Invalid password
* Locked account

**Data Gathering (HOW & FROM WHERE):**

* Collecting or creating the actual test data
* Sources include database, UI, APIs, Excel, SQL

---

### Types of Test Data

#### Based on Nature of Data

* **Valid Data** – Expected inputs (correct username/password)
* **Invalid Data** – Wrong or unexpected inputs
* **Negative Data** – Used to break the system intentionally
* **Edge / Boundary Data** – Minimum & maximum limits

#### Based on Creation Method

#### Static Test Data

* Fixed, predefined, and reusable
* Same data used every execution

**Advantages:**

* Easy to maintain
* Ideal for automation
* Useful for regression testing

**Disadvantages:**

* Risk of data exhaustion
* Less realistic if overused

**Used for:**

* Regression testing
* Automation scripts
* Bug reproduction
* Fixed and reusable
* Same data used every time

**Used for:**

* Regression testing
* Automation testing
* Bug reproduction

#### Dynamic Test Data

* Generated or modified during execution
* Unique data each run

**Advantages:**

* Mimics real-world usage
* Avoids data conflicts
* Ideal for parallel testing

**Disadvantages:**

* Harder to debug failures
* Requires scripting/logic

**Used for:**

* OTP and transaction testing
* Load & performance testing
* Security testing
* Changes for every execution
* Generated at runtime


---

### Boundary Value Data Perspective

Boundary Value Analysis focuses on testing limits of input values.

**Example:**
Password length allowed: 8–16

* 7 ❌
* 8 ✅
* 16 ✅
* 17 ❌

---

### Test Data Challenges

* Test data not available on time
* Dependency between test cases (data collision)
* Handling sensitive production data
* Frequent data reset in environments
* Dynamic data like OTPs and tokens
* Limited DB or backend access
* Environment mismatch (QA vs UAT)

**How testers handle this:**

* Data masking
* Mock services
* Reset scripts
* Data creation APIs
* Data unavailability
* Data dependency between tests
* Sensitive production data
* Dynamic data like OTPs
* Environment mismatch
* Limited database access

---

### Test Data Management Tools

**Common Project Tools:**

* Excel / CSV files
* SQL scripts
* Mockaroo

---

### Data Subsetting

**Definition:**
Data subsetting is extracting a **small but meaningful portion of production data** for testing.

**Benefits:**

* Faster testing
* Reduced storage
* Better performance
* Data privacy compliance

---

## 2. Test Metrics and Reporting

### What are Test Metrics?

Test metrics are **quantitative measurements** used to evaluate the progress, quality, and effectiveness of testing activities.

**Layman Analogy:**
Like a car dashboard that shows speed and fuel level.

---

### Purpose of Test Metrics

* Measure testing progress
* Identify gaps and risks
* Support release decisions
* Improve testing efficiency

---

### Types of Test Metrics

#### Process Metrics

Measure how testing is performed.

**Examples:**

* Test case preparation rate
* Test execution rate
* Defect removal efficiency

#### Product Metrics

Measure quality of the product.

**Examples:**

* Defect density
* Customer-found defects

---

### Key Test Metrics

#### Test Case Execution Rate

Measures testing progress.

**Why it matters:**
Shows how much testing is completed vs pending.

---

#### Defect Leakage

Measures quality of testing effectiveness.

**Interpretation:**

* Low leakage = good test coverage
* High leakage = gaps in testing

---

#### Defect Density

Defects per size of application.

**Formula:**
Defects / Size (modules, stories, lines of code)

---

#### Defect Rejection Rate

Shows quality of bug reporting.

**High value means:**
Poor bug understanding or reporting issues.

#### Test Case Execution Rate

Measures how many test cases have been executed.

**Formula:**
(Executed Test Cases / Total Test Cases) × 100

**Example:**
80 executed out of 100 → 80%

---

#### Defect Leakage

Measures defects that escaped testing and were found after release.

**Formula:**
(Defects found after release / Total defects) × 100

**Note:**
Total defects = Defects found during testing + defects found after release

---

### Test Reporting

Test reporting communicates the **overall testing status** to stakeholders.

**Test Report Includes:**

* Total test cases
* Passed, Failed, Blocked cases
* Defect summary (Critical, Major, Minor)
* Risks and issues
* Recommendation for release

---

## 3. Bug Life Cycle (Defect Life Cycle)

### What is a Bug?

A bug is a deviation between the **expected result** and the **actual result** of the application.

---

### Bug Life Cycle Stages (Detailed)

1. **New** – Tester reports the bug
2. **Open** – Bug accepted for analysis
3. **Assigned** – Assigned to developer
4. **In Progress** – Developer working on fix
5. **Fixed** – Code fix completed
6. **Retest** – Tester verifies the fix
7. **Closed** – Bug resolved successfully

**Optional flows:**

* Reopened
* Deferred
* Rejected
* Duplicate

1. New
2. Open
3. Assigned
4. Fixed
5. Retest
6. Closed

---

### Important Bug Statuses Testers Must Know

**Deferred:**
Valid bug but postponed to a future release.

**Duplicate:**
Bug already reported earlier.

**Rejected / Invalid:**
Reported issue is not a bug.

**Need More Info:**
Bug lacks sufficient details.

**Cannot Reproduce:**
Developer unable to reproduce the issue.

**On Hold:**
Fix blocked due to dependency.

**Reopened:**
Bug still exists after fix.

**Won’t Fix:**
Business decision not to fix the bug.

---

### Severity vs Priority (Detailed Explanation)

**Severity:**

* Impact on application functionality
* Types: Blocker, Critical, Major, Minor, Trivial
* Suggested by Tester

**Priority:**

* Urgency of fixing the bug
* Types: High, Medium, Low
* Decided by Product Owner / Business

**Key Point:**
A bug can be low severity but high priority and vice versa.

**Severity:**
Impact of the bug on system functionality (decided by Tester).

**Priority:**
Urgency to fix based on business needs (decided by PM/PO).

---

### Severity vs Priority Table

| Severity | Priority | Example                      |
| -------- | -------- | ---------------------------- |
| High     | High     | Payment failure              |
| High     | Low      | Admin feature issue          |
| Low      | High     | Logo missing during campaign |
| Low      | Low      | Typo in footer               |

---

### Bug Triage Meeting

**Definition:**
A meeting where bugs are reviewed, prioritized, and assigned.

**Participants:**

* Tester
* Developer
* Product Owner
* Test Lead / Project Manager

**Outcome:**

* Priority and severity confirmation
* Bug ownership
* Fix timelines

---

