---
# 📘 **SOFTWARE TESTING – DETAILED NOTES**

---

# 🧪 **STLC – Software Testing Life Cycle (Full Explanation)**

STLC is a **step-by-step process** followed during testing.
It ensures that testing is planned, systematic, and produces high-quality results.

---

## **1️⃣ Requirement Analysis (Understanding what to test)**

In this phase, testers study and analyze project requirements from documents such as:

* BRD (Business Requirement Document)
* SRS (Software Requirement Specification)
* User Stories
* Acceptance Criteria

**Goal:** Understand *what needs to be tested*.

### **Activities:**

* Identify testable vs non-testable requirements
* Clarify doubts with BA / client / developer
* Identify missing, incomplete, or ambiguous requirements
* Prepare Requirement Traceability Matrix (RTM)
* Identify automation feasibility
* Identify testing tools required

### **Example:**

If the requirement says:
“System should validate login with correct username and password”
→ Testable.

If the requirement says:
“System should be user-friendly”
→ Not testable without more details.

### **Deliverables:**

* Requirement Review Report
* Requirements Clarification List
* Draft RTM

---

## **2️⃣ Test Planning (How to test)**

This is the **brain of STLC**.
Here the Test Manager / Lead prepares a strategy for the entire testing process.

### **Activities:**

* Define testing scope (what will be tested + what will NOT be tested)
* Identify testing types (functional, non-functional, regression)
* Choose testing tools (Selenium, JMeter, etc.)
* Estimate time & cost
* Identify resources (testers, tools, hardware)
* Define entry & exit criteria
* Identify risks and mitigation plans
* Set up communication plan (daily standup, weekly report)

### **Example Entry Criteria:**

* Requirements are signed off
* Test environment ready

### **Deliverables:**

* Test Plan Document
* Test Strategy
* Effort & Time Estimation
* Risk Plan

---

## **3️⃣ Test Case Design (What exact tests will be executed)**

In this phase, testers write detailed test cases.

### **Activities:**

* Write test scenarios
* Write detailed test cases with steps & expected results
* Prepare test data
* Review test cases
* Prioritize test cases (High / Medium / Low)

### **Types of Test Case Techniques:**

* Equivalence Partitioning
* Boundary Value Analysis
* Decision Table Testing
* State Transition Testing

### **Example:**

For login:

* Valid username/password
* Invalid username
* Invalid password
* Blank fields

### **Deliverables:**

* Test Cases
* Test Scenarios
* Test Data Sheet
* Updated RTM

---

## **4️⃣ Test Environment Setup (Where testing will happen)**

A test environment simulates the production environment.

### **Activities:**

* Set up servers, databases, and networks
* Configure browsers, devices, OS
* Install required tools/frameworks
* Get test URLs, API keys, credentials
* Validate if environment works properly

### **Example:**

* QA environment
* UAT environment
* Staging environment

### **Deliverables:**

* Environment Setup Document
* Smoke test report

---

## **5️⃣ Test Execution (Executing test cases)**

This is where actual testing happens.

### **Activities:**

* Execute test cases
* Mark test cases as Pass/Fail
* Log defects with screenshots, logs
* Re-test defects after fix
* Perform Regression testing
* Update RTM

### **Example:**

If login fails with valid credentials → log bug.

### **Deliverables:**

* Test Execution Report
* Defect Report
* Daily/Weekly Status Reports

---

## **6️⃣ Test Cycle Closure (Ending the testing formally)**

This is the final phase where testing is completed.

### **Activities:**

* Ensure all test cases are executed
* Check if major defects are closed
* Prepare Test Summary Report
* Collect metrics (defect density, test coverage)
* Identify lessons learned
* Conduct test closure meeting

### **Deliverables:**

* Test Summary Report (TSR)
* Metrics
* Lessons Learned Document

---

# ---------------------------------------------

# 🛡️ **QA vs QC (Detailed Notes)**

## ⭐ **Quality Assurance (QA)** – *Process-Oriented, Proactive*

**Definition:** QA ensures the **process** used to create the product is good.
It prevents defects before they occur.

### **Key Points:**

* Focus on **improving software development processes**
* Ensures standards are followed
* Involves reviews, audits, meetings
* Mainly *prevention*

### **Activities (Static Testing):**

* Requirement review
* Test plan review
* Code review
* Walkthroughs
* Inspection
* Risk analysis
* Test strategy creation
* Automation planning

---

## ⭐ **Quality Control (QC)** – *Product-Oriented, Reactive*

**Definition:** QC ensures the product **meets requirements and is defect-free**.

### **Key Points:**

* Focus on identifying defects in the final product
* Involves executing tests
* Mainly *detection*

### **QC Activities Include:**

### ✔ Functional Testing

* Unit Testing
* Integration Testing
* System Testing
* Smoke Testing
* Sanity Testing

### ✔ Non-Functional Testing

* Performance (Load, Stress, Scalability)
* Usability
* Security

### ✔ Regression Testing

After bug fixes, ensure old features still work.

### ✔ Acceptance Testing

* Alpha: In company
* Beta: In client environment

### ✔ Exploratory & Ad-hoc Testing

Unscripted testing based on tester’s intuition.

---

# ---------------------------------------------

# 🧾 **Detailed Test Cases**

### **Test Case: TC001 — Successful Login**

**Objective:** Check if user can log in with valid credentials
**Steps:**

1. Open saucedemo.com
2. Enter username: `standard_user`
3. Enter password: `secret_sauce`
4. Click Login

**Expected Result:**
User is redirected to the **Inventory Page**.

---

### **TC002 — Invalid Username**

**Expected Result:**
Error message: **"Invalid User"** or default website error.

---

### **TC003 — Invalid Password**

**Expected Result:**
"Wrong Password"

---

### **TC004 — Blank Credentials**

**Expected Result:**
"Missing credentials. Enter to login."

---

### **Actual SauceDemo Error Message Example:**

**“Epic sadface: Username and password do not match any user in this service”**

This is used when username OR password is wrong.

---

# ---------------------------------------------

# 🔁 **State Transition Testing (Detailed)**

State Transition Testing is used when:

* Output depends on **current state** AND **input**
* The system changes states based on user actions

### **Why Important?**

Useful for testing:

* Login/logout
* Banking applications
* ATM machines
* e-Commerce workflows
* Session timeout

---

## 🔄 **SauceDemo State Diagram**

| Current State | Input                     | Next State     |
| ------------- | ------------------------- | -------------- |
| Idle          | Correct credentials       | Logged In      |
| Idle          | Wrong credentials         | Error Message  |
| Idle          | Wrong credentials 3 times | Account Locked |
| Logged In     | Click Logout              | Logged Out     |
| Logged In     | Session Timeout           | Logged Out     |

---

## **State Transition Test Cases (Explained)**

### **STT001 — Valid Login**

**Checks:** Idle → Logged In transition.

---

### **ST001 — Account Locked**

**Checks:** Idle → Account Locked

User enters wrong credentials 3 times.

---

### **ST002 — Wrong Credentials Once**

**Checks:** Idle → Error Message

---

### **ST003 — Logout**

**Checks:** Logged In → Logged Out

---

### **STT005 — Session Time Out**

**Checks:** Logged In → Logged Out after inactivity.

---

# ---------------------------------------------

# 🪲 **Error Guessing (Detailed Notes)**

Error Guessing is a technique where tester uses **experience and intuition** to find potential defects.

### **Examples:**

* Typos: teh, thier, ther
* Special characters in username/password: @#$%^&*
* SQL injection risks: `' OR 1=1 --`
* Very long input values
* Invalid formats (emails, phone numbers)
* Not closing pop-ups
* Refreshing pages during transaction

This technique often finds defects missed by regular testing.

---

# ---------------------------------------------

# 🔍 **Types of Testing (Fully Explained)**

## ⭐ **Functional Testing (QC)**

Checks if each function of the application works as expected.

### 1. **Unit Testing**

* Performed by developers
* Test smallest components (functions, methods)

### 2. **Integration Testing**

* Test modules when combined
* Check data flow between modules

### 3. **System Testing**

* Test complete system end-to-end

### 4. **Smoke Testing**

* Basic checks → Is build stable?
  Example: app opens, login works.

### 5. **Sanity Testing**

* Quick checks after minor changes.
  Example: developer fixes login → tester checks just login.

---

## ⭐ **Non-Functional Testing (QC)**

### 1. **Performance Testing**

Checks speed, stability, scalability.

#### **Load Testing:**

Normal load → expected users
Example: Can site handle 500 users?

#### **Stress Testing:**

Beyond normal → break point
Example: Push 5000 users to see when app crashes.

#### **Scalability Testing:**

Can the system scale up when needed?

---

### 2. **Usability Testing**

Checks if UI is simple, clean, easy to use.

---

### 3. **Security Testing**

Checks:

* Authentication
* Authorization
* Data protection
* Vulnerability scanning

---

## ⭐ **Regression Testing**

After bug fixes or enhancements, ensure existing features still work.

---

## ⭐ **Acceptance Testing**

Final testing before release.

### **Alpha Testing:**

* Internal environment
* Performed by internal users

### **Beta Testing:**

* Performed by end users
* Real-world environment

---

## ⭐ **Exploratory Testing**

Tester explores without pre-defined test cases.

---

## ⭐ **Ad-hoc Testing**

Unstructured, random testing based on intuition.

---
