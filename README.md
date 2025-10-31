## Warehouse Management System - Angular & Spring Boot (2-Visit Warehouse System)


### 1. Preorder Creation (First Visit by Agent)
- The **agent** fills out a preorder form with the **items** and their **quantities**.  
- The agent **submits the preorder**.

### 2. Admin Review
- The **admin** opens the preorder and can **modify quantities** if needed.  
- The admin can either **approve** or **reject** the preorder.  
- Once approved, the system **immediately deducts the approved quantities from inventory**, ensuring preorders are fulfilled on a **first-come, first-served** basis.

### 3. Order Delivery (Second Visit by Agent)
- During the second visit, the **agent delivers the final order**.  
- The system records the **final quantities delivered** and the **payment**.

### 4. Payment Cycle
- The agent collects **payment**, which can be **full** or **partial**.  
- **Full Payment:**  
  - Payment is marked as **completed**, with **no due date**.  
- **Partial Payment:**  
  - A **payment schedule** is used to track remaining payments.  
- Payment **status** can be:  
  - **Pending:** Not yet fully paid.  
  - **Completed:** Fully paid (even if partial payments were made in installments).  
  - **Canceled:** Payment was canceled.

### 5. Returns Management
- If items are returned, the agent must **open a return request**, including:  
  - Reason for return  
  - Quantities returned  
- If the return is **approved**, the returned quantities are **added back to inventory**.

---

**Note:**  
This system is a **2-visit warehouse system**, where:
1. **First visit** = preorder creation.  
2. **Second visit** = order delivery and payment collection.

---

### Here is an ERD

<img src="https://github.com/user-attachments/assets/3af15a92-dd87-414c-b8b9-63afcf5b4d68" width="800" height="600" />

---
### User Roles

- **Agent**
  - Limited to creating **preorders**.
  - Delivering **orders**.
  - Collecting **payments**.
  - Submitting **return requests**.

- **Admin**
  - Can **review and edit preorders**.
  - Can **approve or reject preorders**.
  - Manages **inventory** and **payment statuses**.

- **Manager**
  - Has **full control** over all actions in the system.
 
---

## Frontend (Angular)

**Purpose:** Provides the UI for Agents, Admins, and Managers.

**Responsibilities:**
- Fill and submit **preorders, deliveries, payments, and returns**.
- Display **dashboards** for inventory, payments, and order status.
- Handle **user authentication** and **role-based access**.
- Communicate with backend via **REST APIs**.

**Technologies:** Angular, HTML, CSS, TypeScript, HTTP client, Routing.

---

### Frontend (Angular)

- Fill and submit **preorders, payments,etc**.
- Display **dashboards** for inventory, payments, and order status.
- Handle **user authentication** and **role-based access**.
- Communicate with backend via **REST APIs**.

**Technologies:** Angular, HTML, CSS, TypeScript, HTTP client, Routing.

---

### Backend (Spring Boot)

- Manage **preorders, orders, payments, etc**.
- Implement **role-based access control**.
- Update **inventory** automatically.
- Provide **REST APIs** for the frontend.
- Handle database operations.

**Technologies:** Spring Boot, JPA/Hibernate, Spring Security, JWT, PostgreSQL.

---
### Some Figues from the website:
<img width="2874" height="1724" alt="image" src="https://github.com/user-attachments/assets/e58682ea-8a90-4c0a-bf35-8769c5b02a28" />
<img width="2878" height="1626" alt="image" src="https://github.com/user-attachments/assets/fe0e7439-95b3-49c9-bd0f-f788bda0b27b" />
<img width="2880" height="1630" alt="image" src="https://github.com/user-attachments/assets/b1a547f7-3a69-461f-93fa-1b51de507999" />
<img width="2876" height="1636" alt="image" src="https://github.com/user-attachments/assets/b48931cd-8bcc-4c3e-ac50-435babc24d41" />
<img width="2878" height="1626" alt="image" src="https://github.com/user-attachments/assets/ac233e1c-00e4-4cdc-930a-2beb2d5c1dbf" />
<img width="2880" height="1630" alt="image" src="https://github.com/user-attachments/assets/f5892861-266f-458f-92eb-312f98a8afa2" />
<img width="2880" height="1622" alt="image" src="https://github.com/user-attachments/assets/6fbf90fb-5071-4dc1-bd2b-b0f7440ef74e" />
















 
  




