---

# ⭐ **TEST DATA MANAGEMENT (TDM)**

## ✅ **Definition**

Test Data Management (TDM) is the process of **creating, organizing, maintaining, securing, and refreshing** the data used for software testing.

Good test data ensures that tests run smoothly, accurately, and safely.

---

# ⭐ **1. Key Functions of TDM**

### **1. Creating Test Data**

Test data can be created:

* **Manually**
* **Using tools** (Mockaroo: [https://mockaroo.com/](https://mockaroo.com/))
* **By scripts or automation**

### ✔ Example Test Data:

* **Fake user account:**

  * Name
  * Email
  * Password

* **Dummy products:**

  * Shoes → size, color, stock, price

* **Sample transactions:**

  * ₹999 paid
  * ₹199 refund

---

### **2. Organizing Test Data**

* Keep data in proper folders
* Separate valid, invalid, boundary, bulk upload data
* Maintain naming conventions
* Maintain test data in Excel, JSON, CSV etc.

---

### **3. Maintaining Test Data**

* Update data when new modules/features come
* Remove outdated test data
* Reuse test data when possible
* Ensure accuracy after system changes

---

### **4. Securing Test Data**

Sensitive user information must be protected.

### ✔ Data Masking Examples:

* PAN Number → **XXXXX1234F**
* Credit Card → **1234 XXXX XXXX 3556**

Masking hides real information but keeps the format same.

---

### **5. Refreshing Test Data**

* Recreate data for every new test cycle
* Reset database to baseline
* Refill sample transactions
* Remove stale records

---

# ⭐ **Steps in TDM**

### **1️⃣ Data Generation**

* Fake accounts, dummy products, sample transactions
* Tools: **Mockaroo, CSV generators, scripts**

---

### **2️⃣ Data Masking**

Hide sensitive fields while keeping format intact.

Examples:

* **ABCDE1234F → XXXXX1234F**
* **1234 5678 9000 3556 → 1234 XXXX XXXX 3556**

---

### **3️⃣ Data Validation**

Ensure test data is **correct, usable, and relevant**.

Checklist:

1. Format is correct
2. Values make sense
3. No missing/corrupt data
4. Data matches test objective

---

### **4️⃣ Data Refreshing**

* Recreate or reload data
* Sync test environment
* Clear old records

---

### **5️⃣ Provide Data for Test Cases**

Use the generated data:

* Login tests
* Checkout tests
* API tests
* Bulk upload tests

---

---

# ⭐ **TEST METRICS & REPORTING**

**Duration: 25 minutes**

Test metrics help understand:

* Testing progress
* Quality of product
* Efficiency of testing
* How quickly defects are fixed

---

# ⭐ **1. Defect Density**

Formula:

### **Defect Density = (Defects Found / Size of Module) × 100**

### Example 1:

10 defects in 100 lines of code →
**(10/100) × 100 = 10%**

### Example 2:

Module test cases = 300
Failed = 50
Defect density = (50 / 300) × 100
= **16.66%**

---

# ⭐ **2. Test Execution Rate**

Formula:

### **Execution Rate = (Executed Test Cases / Total Test Cases) × 100**

Example:
Total = 50
Executed = 40
Execution rate = (40/50) × 100 = **80%**

Example 2:
Executed = 10 of 10
= **100%**

---

# ⭐ **3. Defect Resolution Time**

The time required to **fix a defect**.

Example:

* Bug raised on Monday
* Fixed on Wednesday
  Resolution time = **2 days**

---

---

# ⭐ **TEST CASE DESIGN TECHNIQUES**

**Duration: 30 minutes**

Three core techniques:

1. **BVA – Boundary Value Analysis**
2. **EP – Equivalence Partitioning**
3. **Decision Table Testing**

---

# ⭐ 1️⃣ **Boundary Value Analysis (BVA)**

Used when inputs have **ranges, limits, thresholds**.

---

## Example 1: Text box accepts **1 to 10**

| Value | Result |
| ----- | ------ |
| 0     | ❌ Fail |
| 1     | ✔ Pass |
| 2     | ✔ Pass |
| 9     | ✔ Pass |
| 10    | ✔ Pass |
| 11    | ❌ Fail |

---

## Example 2: Age must be **18–60**

| Value | Result |
| ----- | ------ |
| 17    | ❌ Fail |
| 18    | ✔ Pass |
| 19    | ✔ Pass |
| 59    | ✔ Pass |
| 60    | ✔ Pass |
| 61    | ❌ Fail |

---

## Example 3: ATM withdrawal **500–10000**

| Value | Result |
| ----- | ------ |
| 499   | ❌ Fail |
| 500   | ✔ Pass |
| 501   | ✔ Pass |
| 9999  | ✔ Pass |
| 10000 | ✔ Pass |
| 10001 | ❌ Fail |

---

---

# ⭐ 2️⃣ **Equivalence Partitioning (EP)**

Divides input data into **valid and invalid partitions**.

---

## Example 1: Range **100–1000**

* Below 100 → **invalid** → 50
* Between 100–1000 → **valid** → 500
* Above 1000 → **invalid** → 1500

---

## Example 2: ATM 500–10000

* 1–499 → invalid → 450
* 500–10000 → valid → 7499
* Above 10000 → invalid → 21000

---

## Example 3: Password length **6–12**

* <6 → invalid → 3
* 6–12 → valid → 9
* > 12 → invalid → 15

---

---

# ⭐ 3️⃣ **Decision Table Testing**

Used when the output depends on **multiple conditions**.

---

## Example 1: Loan Approval

Condition:

* Salary > 30000
* CIBIL > 700

| Salary | CIBIL | Result     |
| ------ | ----- | ---------- |
| Yes    | Yes   | ✔ Approved |
| Yes    | No    | ❌ Rejected |
| No     | Yes   | ❌ Rejected |
| No     | No    | ❌ Rejected |

---

## Example 2: Login

Condition:

1. Password correct?
2. User blocked?

| Password correct | User blocked | Login   |
| ---------------- | ------------ | ------- |
| No               | No           | Fail    |
| No               | Yes          | Fail    |
| Yes              | No           | ✔ Login |
| Yes              | Yes          | Fail    |

---

## Example 3: ATM

Conditions:

1. Sufficient balance?
2. Correct PIN?

| Sufficient Balance | Correct PIN | Withdraw  |
| ------------------ | ----------- | --------- |
| Yes                | Yes         | ✔ Valid   |
| Yes                | No          | ❌ Invalid |
| No                 | Yes         | ❌ Invalid |
| No                 | No          | ❌ Invalid |

---

# ⭐ SUMMARY TABLE

| Technique          | Purpose                 | Example                                |
| ------------------ | ----------------------- | -------------------------------------- |
| **TDM**            | Create/manage test data | Fake users, masked PAN, validated data |
| **Defect Density** | Measure defects vs size | 10%                                    |
| **Execution Rate** | Testing progress        | 80%, 100%                              |
| **BVA**            | Test boundaries         | 499, 500, 10000, 10001                 |
| **EP**             | Partition groups        | 450, 7499, 21000                       |
| **Decision Table** | Test combinations       | Balance + PIN                          |

---

