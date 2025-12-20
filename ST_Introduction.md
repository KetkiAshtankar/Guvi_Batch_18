---

# 📘 **SDLC MODELS**
---
# ## ⭐ **1. Software Development Life Cycle (SDLC)**

SDLC is the process used by software teams to **plan, build, test, and deliver** software in a systematic way.

### **Phases of SDLC**

1. **Planning**
2. **Requirement Analysis**
3. **Design**
4. **Development (Coding)**
5. **Testing**
6. **Deployment**
7. **Maintenance**

### **Example:**

Building software = Building a **car**

* Planning → What type of car?
* Requirements → What features?
* Design → Engineering blueprints
* Development → Assemble parts
* Testing → Crash tests
* Deployment → Launch car in market
* Maintenance → Servicing the car

---

# ## ⭐ **2. SDLC MODELS**

---

# ### **2.1 Waterfall Model**

### **Concept**

A **linear and sequential** development model.
Each phase must finish before the next begins.

### **Diagram (imagine Like a Waterfall)**

```
Planning 
   ↓
Requirement Analysis
   ↓
Design
   ↓
Development
   ↓
Testing
   ↓
Deployment
   ↓
Maintenance
```

### ** Explanation**

Like constructing a **house**—you cannot redo the foundation after completing the roof.

### **Technical**

Phases follow strict order with heavy documentation.

### **Best Use Case**

* Fixed requirements
* No frequent changes
* Example: Simple company website

---

# ### **2.2 Agile Model**

### **Concept**

Agile is **iterative**, **flexible**, and **customer feedback–driven**.
Work is divided into **Sprints** (1–4 weeks).

### **Diagram**

```
[ Sprint Cycle ]
Planning → Development → Testing → Review → Feedback → Improvement
              ↺ repeated every sprint
```

### ** Explanation**

Like making **cupcakes**:
You bake one → taste → adjust → bake again → improve.

### **Technical**

* Continuous integration
* Shippable product every sprint
* High collaboration

### **Use Case**

* Apps that change often
* Continuous updates (ex: Swiggy, Instagram)

---

# ### **2.3 Iterative Model**

### **Concept**

Software is built **version by version**, improving each time.

### **Diagram**

```
Iteration 1 → Basic Version
Iteration 2 → Improved Version
Iteration 3 → More Features
Iteration 4 → Refined System
```

### ** Explanation**

Like sculpting a **statue**:
Start with a rough shape → refine → refine → refine → final statue.

### **Technical**

* Each iteration includes:

  * Planning
  * Design
  * Development
  * Testing
  * Feedback

### **Real Example**

E-commerce platform:

* V1: Product list
* V2: Cart
* V3: Payment
* V4: Reviews

---

# ### **Difference Between Agile and Iterative (Important)**

| Feature            | Agile                      | Iterative                             |
| ------------------ | -------------------------- | ------------------------------------- |
| Delivery           | Small features each sprint | Improved versions of the same product |
| Customer Feedback  | Every sprint               | After major versions                  |
| Flexibility        | Very high                  | Medium                                |
| Team Collaboration | Very high                  | Moderate                              |
| Build Style        | Build different parts      | Improve the same part                 |

### **Analogy:**

* **Iterative** → Perfecting the **same statue** bit by bit
* **Agile** → Building **different statue parts separately**, assembling later

---

# ### **2.4 V-Model (Verification & Validation Model)**

### **Concept**

An extension of Waterfall where **testing activities run parallel** to each development phase.

### **Diagram**

```
            Requirements   →   Acceptance Testing
         System Design     →   System Testing
     High-Level Design     →   Integration Testing
      Low-Level Design     →   Unit Testing
                 Coding (Bottom of V)
```

### ** Explanation**

Like building a **bridge**:
While designing, engineers also design **tests** for each stage.

### **Technical**

* Verification = Are we building the product right?
* Validation = Are we building the right product?
* Testing planned early

### **Use Case**

* Medical software
* Avionics software
* Safety-critical systems

---

# ### **2.5 Spiral Model**

### **Concept**

A **risk-driven**, iterative development process.
Each loop of the spiral adds more detail and features.

### **Four Activities per Loop**

1. Planning
2. Risk Analysis
3. Engineering
4. Evaluation

### **Diagram**

```
      (Spiral expanding outward)
   Loop 1 → Loop 2 → Loop 3 → Loop 4
Each loop: Planning → Risk → Build → Review
```

### ** Explanation**

Like building a **custom house**:
You plan, check risks, build a part, review—repeat.

### **Technical**

* Very good for large, high-risk projects
* Heavy risk analysis
* Expensive but safe

### **Use Case**

* Banking System
* Government systems
* Aerospace projects

---

# ### **2.6 Big Bang Model**

### **Concept**

No planning, no documentation — just **start building**.

### **Diagram**

```
Requirements? → Code  
Design?       → Code  
Testing?      → At end  
```

### ** Explanation**

Like a **science experiment**:
Just mix ingredients and see what happens.

### **Technical**

* High uncertainty
* Not suitable for large projects
* Fast for small prototypes

### **Use Case**

* College projects
* Hackathon prototypes
* Tiny tools or scripts

---

# ## ⭐ **3. Comparison of All Models**

| Model     | Best For                | Flexibility | Cost   | Documentation | Examples            |
| --------- | ----------------------- | ----------- | ------ | ------------- | ------------------- |
| Waterfall | Fixed requirements      | Low         | Low    | High          | Simple website      |
| Agile     | Changing needs          | Very high   | Medium | Low           | Food delivery app   |
| Iterative | Gradual improvements    | Medium      | Medium | Medium        | E-learning platform |
| V-Model   | Safety-critical systems | Low         | High   | High          | Medical software    |
| Spiral    | High-risk projects      | High        | High   | High          | Banking software    |
| Big Bang  | Small experiments       | Very high   | Low    | None          | Hackathon chatbot   |

---

# ## ⭐ **4. Real-Life Software Examples**

### **Waterfall** → Flight control system, payroll systems

### **Agile** → Swiggy, Zomato, Instagram

### **Iterative** → Amazon-like e-commerce store

### **V-Model** → Pacemaker device software

### **Spiral** → Banking security system

### **Big Bang** → Hackathon prototype chatbot, startup experiment tools

---

# ## ⭐ **5. Statue Analogy (Best Teaching Example)**

### **Iterative Model**

Refine the **same statue** slowly → shape → detail → polish.

### **Agile Model**

Build **head, hands, torso, legs separately** in sprints → assemble.

---

# ## ⭐ **End Summary (One-Line Definitions)**

* **Waterfall:** One-way flow, no changes
* **Agile:** Small features delivered fast
* **Iterative:** Improve the same product gradually
* **V-Model:** Testing planned early, parallel to development
* **Spiral:** Iterative + heavy risk analysis
* **Big Bang:** No plan, just code

---




# ## ⭐ **Reference**

* **Waterfall:** [One-way flow, no changes](https://www.geeksforgeeks.org/software-engineering/waterfall-model/)
  
* **Agile:** [Small features delivered fast](https://asana.com/resources/agile-methodology)
  
* **Iterative:** [Improve the same product gradually](https://medium.com/@nld.anuradha/the-iterative-model-in-sdlc-a-practical-approach-to-software-development-a8eebf87fda7)
  
* **V-Model:** [Testing planned early, parallel to development](https://www.geeksforgeeks.org/software-engineering/software-engineering-sdlc-v-model/)
  
* **Spiral:** [Iterative + heavy risk analysis](https://www.geeksforgeeks.org/software-engineering/software-engineering-spiral-model/)
  


---

# ## ⭐ **Test - Reporting**

1. What was tested?
2. How it was tested?
3. Test Results ( Passed, Failed, Blocked, Skipped)
4. Defects Found
5. Status of requirements
6. Risks, blockers and recommendations.



Types of Test Reports:
1. Daily / Execution report
2. TSR Test Summary Report
3. Defect Report
4. Metric Report / Dashboard

   what test report should contain:
   1. objective: purpose
   2. scope: what is included, what is excluded
   3. test summary : no. of test cases executed
   4. defects: all the defects found with its severity
   5. metrics: pass% , fail %, execution%, defect density% etc.
   6. risk : issue that may impact release
   7. recommendations: whether to release or not?

Examples:
      Test Report
      module: Login Test- Daily report
      date: 6-12-2025
      executed test cases: 10
         passed: 8
         failed: 2
         blocked: 0
      defects found: 
      1. wrong error message displayed
         severity: medium
      2. Login button clickable without password.
         serverity : high

      status : testing in progress


      TSR Test Summary report:
      Total test cases: 120 
      passed: 100
      failed: 10 
      blocked: 5
      skipped: 5     110/120  * 100

      defects: 
      critcal: 2
      high:    3
      medium:   10
      low:    5

      Coverage : 91.6% tested 
      recommendation: release with known low-severity issues.

      Tools :
      Jira
      excel/ google sheet
      jenkins reports
      allure-report
      pytest-html 

      









      







---
