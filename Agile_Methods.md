# Agile Methodology, Agile Testing & JIRA Kanban – Notes

## 1. Introduction to Agile

Agile is a way of working that focuses on delivering value to customers early and continuously. Instead of building everything at once and delivering at the end, Agile teams deliver small pieces of working software regularly and improve them based on feedback.

**Key idea:** Flexibility, collaboration, and continuous improvement.

---

## 2. Agile Principles (Simplified)

### 1. Early and Continuous Delivery

* Deliver small usable features frequently.
* Customers see progress early.
* Reduces risk and rework.

**Example:** Showing a login screen in the first sprint instead of waiting for the full application.

---

### 2. Welcoming Change

* Changes are accepted even late in development.
* Agile adapts instead of resisting change.

**Example:** Client asks to change a button position after development has started → added to backlog and handled in next sprint.

---

### 3. Customer Collaboration

* Customer is involved throughout the project.
* Regular feedback ensures correct development.

**Example:** Sprint reviews where customers see demos and give suggestions.

---

### 4. Sustainable Development

* Teams work at a steady pace.
* Avoids burnout and improves quality.

**Example:** Working consistently 8 hours daily instead of overtime every sprint.

---

## 3. Agile Workflow (Scrum Ceremonies)

### 1. Sprint Planning

* Decide what work will be done in the sprint.
* Break stories into tasks.
* Estimate using story points.

**Output:** Sprint Backlog

---

### 2. Daily Stand-up

* Short 15-minute meeting.
* Three questions:

  1. What did I do yesterday?
  2. What will I do today?
  3. Any blockers?

---

### 3. Sprint Review

* Demo completed work to stakeholders.
* Collect feedback.

---

### 4. Retrospective

* Discuss what went well.
* Discuss what didn’t go well.
* Identify improvements for next sprint.

---

## 4. Agile Roles

### Product Owner (PO)

* Owns product vision and backlog.
* Clarifies requirements.
* Accepts or rejects completed work.

### Scrum Master (SM)

* Ensures Agile process is followed.
* Removes blockers.
* Facilitates meetings.

### Developers

* Build the product.
* Estimate and complete tasks.

### Testers / QA Engineers

* Ensure product quality.
* Perform manual and automation testing.
* Raise bugs in JIRA.

### Stakeholders (Optional)

* Business users, management, or clients.
* Provide feedback and expectations.

---

## 5. Agile Testing

Agile testing starts from day one and continues throughout the project.

### 1. Continuous Testing

* Testing happens with every change.
* Prevents defects from accumulating.

**Analogy:** Tasting food while cooking.

---

### 2. Exploratory Testing

* Tester explores the application freely.
* Focus on finding unexpected issues.

**Example:** Entering invalid data, emojis, or random inputs.

---

### 3. Automation Testing

* Repetitive tests are automated.
* Saves time and supports CI/CD.

**Example:** Automated login tests running after every code commit.

---

## 6. JIRA – Basics

JIRA is a project management tool used to track work in Agile projects.

### What is an Issue?

An issue is any work item such as:

* Story
* Task
* Bug
* Epic

---

### Bug Management in JIRA

* Bugs are created as issues with type = Bug.
* Includes summary, steps to reproduce, expected vs actual result, priority, and attachments.

---

### Priority Levels

* Blocker – Work cannot continue
* High – Major functionality broken
* Medium – Important but not urgent
* Low – Minor issue

---

## 7. Kanban Board

Kanban is a visual way to track work status.

### Typical Columns

* To Do
* In Progress
* Review / Testing
* Done

**Benefit:** Clear visibility of work and continuous delivery.

---
##  Summary

* Agile focuses on flexibility and customer value.
* Work is done in small iterations.
* Testing is continuous and collaborative.
* JIRA and Kanban help track and visualize work.
* Clear roles and regular feedback ensure success.
