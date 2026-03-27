> ⚠️ **Login Note:** Before starting, ensure you are logged into **IBM OpenPages** using the **Use case owner** role.
> This access is required to create and manage **Business Entities**, **Model Use Cases**, and perform associated governance tasks.

---

# 📊 Business Entity Creation in watsonx.governance

## 📌 Overview

This guide walks you through creating a **Primary Business Entity** and a **Child Business Entity** in watsonx.governance for the **AskHR Project**, under the **Techcorp** organization.

---

## 🏢 Business Entity Creation

In **IBM OpenPages**, a **Business Entity**:

* Represents a logical division or unit within an organization.
* Serves as a container for managing risks, controls, issues, and processes.
* Supports parent/child hierarchy to enable structured governance.

---

## 🎯 Structure to Be Created

| Entity Level   | Entity Name   | Description                                                        |
| -------------- | ------------- | ------------------------------------------------------------------ |
| Primary Entity | Techcorp      | Main entity representing the organization.                         |
| Child Entity   | AskHR - GenAI | GenAI use case entity under the AskHR project, linked to Techcorp. |

---

## 🛠️ Step-by-Step Creation Process

### 1️⃣ Step 1: Create Primary Business Entity — Techcorp

1. **Log in as:**
   `Use case owner`

2. **Navigate to the Business Entity Section:**

   * Click the **Hamburger Menu (☰)**.
   * Go to **Organization**.
   * Select **Business Entity**.

   <img width="800" alt="image" src="https://github.com/user-attachments/assets/e5562f7d-9a18-4225-8d03-c5172d813ee4" />


3. **Create a New Entity:**

   * Click **Create New**.
   * Fill in the following fields:

   | Field             | Value                                |
   | ----------------- | ------------------------------------ |
   | **Entity Name**   | `Techcorp`                           |
   | **Description**   | Parent entity representing Techcorp. |
   | **Owner**         | Use case owner     |
   | **Business Unit** | As applicable                        |

4. **Click Save.**

   <img width="800" alt="image" src="https://github.com/user-attachments/assets/10ff298c-7055-4f36-a8e0-ceb1eec4c874" />


---

### 2️⃣ Step 2: Create Child Business Entity — AskHR - GenAI

1. After **Techcorp** is created, click **Create New** again to add the child entity.

2. Fill in the following fields:

   | Field                       | Value                                                    |
   | --------------------------- | -------------------------------------------------------- |
   | **Entity Name**             | `AskHR - GenAI`                                          |
   | **Description**             | Child entity for the GenAI use case under AskHR project. |
   | **Owner**                   | Use case owner / Governance Lead                            |
   | **Business Unit**           | As applicable                                            |
   | **Primary Business Entity** | Select `Techcorp` from the dropdown or lookup list.      |

   <img width="800" alt="image" src="https://github.com/user-attachments/assets/15fde0c3-3362-480e-a02d-4564f69b438b" />


3. ✅ **Ensure `Techcorp` is selected** as the **Primary Business Entity**.

4. **Click Save.**

---

## ✅ Example Child Entity Summary

* **Entity Name:** `AskHR - GenAI`
* **Description:** Child entity for the GenAI use case in the AskHR project.
* **Primary Business Entity:** `Techcorp`
* **Owner:** Use case owner

---

## 📊 Summary

By setting up:

* **Techcorp** as the **Primary Business Entity**, and
* **AskHR - GenAI** as a **Child Entity** linked to it,

You enable:

* Clear governance hierarchy
* Focused compliance tracking
* Organized risk and issue management within your AI initiatives

<img width="800" alt="image" src="https://github.com/user-attachments/assets/f6e44d46-8a4f-4834-a6ce-097516cd99b0" />


---

👏 **Well Done!**
Creating structured Business Entities in OpenPages sets a strong foundation for scalable, transparent, and well-governed AI initiatives.
