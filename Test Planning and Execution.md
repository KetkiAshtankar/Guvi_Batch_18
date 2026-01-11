---

# 📘 PROJECT MANAGEMENT TOOL

## 📌 HANDS-ON WITH JIRA – DETAILED NOTES

---

## 1. WHAT IS A PROJECT MANAGEMENT TOOL?

A **Project Management Tool** is software used to:

* Plan work
* Track progress
* Assign responsibilities
* Monitor timelines
* Ensure timely delivery of a project

### Why it is needed in software projects:

* Multiple teams work together (Dev, QA, Product)
* Many tasks run in parallel
* Progress must be visible to everyone

### Common Tools:

* Jira (Most widely used)
* Azure DevOps
* Trello
* Asana

📌 **Industry fact:**
Jira is used in most Agile projects across IT companies.

---

## 2. WHY TESTERS NEED JIRA

Testers use Jira to:

* Understand requirements (User Stories)
* Track testing tasks
* Log bugs
* Follow bug lifecycle
* Provide test reports
* Support release decisions

### Tester’s daily Jira usage:

```
Story → Test Case → Test Execution → Bug → Retest → Closure
```

📌 **Key point:**
Jira is not just for developers – QA uses it extensively.

---

## 3. JIRA & AGILE CONNECTION

* **Agile** = Process / Methodology
* **Jira** = Tool that supports Agile

### Agile concepts in Jira:

* Backlog
* Sprint
* User Stories
* Scrum Board
* Reports

---

## 4. JIRA PROJECT SETUP (HANDS-ON)

### Step 1: Create Jira Account

1. Go to [https://www.atlassian.com/software/jira](https://www.atlassian.com/software/jira)
2. Sign up using email
3. Choose **Free Plan**

---

### Step 2: Create a Jira Project

1. Click **Create Project**
2. Select **Scrum Software Project**
3. Choose **Company-managed project**
4. Project Name: *Sauce Demo Testing Project*
5. Click **Create**

---

## 5. JIRA DASHBOARD OVERVIEW

### Important Sections:

* **Backlog** – All pending work
* **Board** – Sprint execution view
* **Issues** – All created items
* **Reports** – Charts & metrics
* **Project Settings** – Configuration

---

## 6. JIRA ISSUE TYPES (CORE CONCEPT)

| Issue Type | Meaning       | Example                     |
| ---------- | ------------- | --------------------------- |
| Epic       | Large feature | Checkout Module             |
| Story      | Requirement   | User Login                  |
| Task       | Work item     | Write test cases            |
| Bug        | Defect        | Login error message missing |

📌 **QA mostly works with:** Story, Task, Bug

---

## 7. CREATING ISSUES IN JIRA (HANDS-ON)

### A. Create an Epic

1. Click **Create**
2. Issue Type: **Epic**
3. Epic Name: *Sauce Demo E-Commerce Flow*
4. Save

---

### B. Create User Story

1. Click **Create**
2. Issue Type: **Story**
3. Summary: *User should be able to login*
4. Description: Functional requirement
5. Add **Acceptance Criteria**
6. Link to Epic
7. Save

---

### C. Create Task

Example:

* Prepare test cases for login
* Execute regression testing

---

### D. Create Bug

1. Issue Type: **Bug**
2. Summary: *Login error message not displayed*
3. Description: Bug details
4. Steps to Reproduce
5. Expected Result
6. Actual Result
7. Priority
8. Save

---

## 8. SCRUM WORKFLOW & STATUS

### Common Workflow:

```
To Do → In Progress → In Review → Done
```

### Bug Lifecycle:

```
Open → Assigned → Fixed → Retest → Closed / Reopen
```

📌 **Tester responsibilities:**

* Move bug to Retest
* Verify fix
* Close or Reopen

---

## 9. SPRINT MANAGEMENT

### What is a Sprint?

* Fixed duration (1–2 weeks)
* Contains selected stories/tasks

### Steps to Create & Start Sprint:

1. Go to **Backlog**
2. Click **Create Sprint**
3. Drag stories into sprint
4. Click **Start Sprint**
5. Set sprint duration
6. Start

---

## 10. JIRA REPORTS & CHARTS (VERY IMPORTANT)

---

## A. VELOCITY CHART

### What it Shows:

* Work completed per sprint
* Measured in **Story Points**

### Why Velocity is Important:

* Helps in sprint planning
* Shows team efficiency

---

### Steps to View Velocity Chart:

1. Open Project
2. Click **Reports**
3. Select **Velocity Chart**

---

### Conditions to Show Velocity:

✔ Multiple completed sprints
✔ Story points added to stories
✔ Stories moved to **Done**

📌 **Important Note:**
Velocity cannot be edited manually.

---

## B. BURNDOWN CHART

### What it Shows:

* Remaining work vs time
* Sprint progress

---

### Steps to View Burndown Chart:

1. Open Project
2. Go to **Reports**
3. Click **Sprint Burndown**

---

### How to Interpret:

* Downward line → On track
* Flat line → No progress
* Upward spike → Scope increase

---

## C. SPRINT REPORT

### What it Shows:

* Completed issues
* Incomplete issues
* Removed issues

### Steps:

1. Go to **Reports**
2. Select **Sprint Report**
3. Choose Sprint

---

## D. CUMULATIVE FLOW DIAGRAM (Optional)

Shows:

* Status-wise issue distribution
* Bottlenecks

---

## 11. CUSTOMIZING FIELDS IN JIRA (SEVERITY)

---

## WHY SEVERITY IS NOT VISIBLE BY DEFAULT

* Jira provides **Priority** by default
* Severity must be **custom-created**

---

## STEPS TO CREATE SEVERITY FIELD

### Step 1: Create Custom Field

1. Go to **⚙️ Settings**
2. Click **Issues**
3. Select **Custom Fields**
4. Click **Create Custom Field**
5. Choose **Select List (Single Choice)**
6. Field Name: **Severity**
7. Add values:

   * Blocker
   * Critical
   * Major
   * Minor
   * Trivial
8. Click **Create**

---

### Step 2: Add Severity to Bug Screen

1. Go to **⚙️ Settings → Issues**
2. Click **Screens**
3. Identify Bug Screen
4. Click **Configure**
5. Click **Add Field**
6. Select **Severity**
7. Save

---

### Step 3: Display Severity Column on Board

1. Open Board
2. Click **••• → Configure**
3. Go to **Card Layout**
4. Add **Severity**

OR

In Issue List:

1. Click **Columns**
2. Select **Severity**

---

## 12. PRIORITY vs SEVERITY (INTERVIEW MUST)

| Severity         | Priority       |
| ---------------- | -------------- |
| Impact on system | Urgency of fix |
| Decided by QA    | Decided by PM  |
| Custom field     | Default field  |

---

## 13. TESTER REPORTING IN JIRA

### Test Report Contains:

* Total test cases
* Passed
* Failed
* Blocked
* Bugs logged
* Release recommendation

---

## 14. END-TO-END REAL PROJECT FLOW

```
Requirement → Story → Sprint → Test Case → Execution → Bug → Retest → Report → Release
```

📌 Jira supports every step above.

---
