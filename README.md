# EmployeeWebSite
# 👩‍💼 Employee Project Management Web API

This is a **Spring Boot-based RESTful Web API** for managing employees, projects, and their assignments. The project implements standard **CRUD (Create, Read, Update, Delete)** operations for three main modules:

1. **Employee Management**
2. **Project Management**
3. **Employee-to-Project Assignment**

Developed as part of the **FELECE Java Backend Training**.

---

## 📌 Project Features

- ✅ Add, update, delete, and list employees
- ✅ Add, update, delete, and list projects
- ✅ Assign employees to projects
- ✅ Structured using layered architecture (`Controller`, `Service`, `Repository`)
- ✅ Includes nested entities such as `PersonalInformation` and `OtherInformation`
- ✅ Enum usage for fields like `WorkType`, `ContractType`, and `EmployeeLevel`

---

## 🧱 Technologies Used

- **Java 17**
- **Spring Boot**
- **Spring Data JPA**
- **Maven**
- **Lombok**
- **MapStruct** (optional for DTO mapping)
- **Validation API**
- **Swagger** (for API documentation)
- **Postman** (for endpoint testing)

---

## 🧩 Entity Structure Overview

### 🧑 Employee

- `id` (auto-generated)
- `firstName`, `lastName`
- `manager` (self-referencing employee)
- `level` (`L0`–`L5`)
- `phoneNumber` (unique, required)
- `email` (unique, required)
- `birthDate`
- `workType` (Remote, Office, Hybrid)
- `contractType` (Temporary, Permanent)
- `team` (Java, Angular, DevOps, etc.)
- `startDate`, `endDate`
- `personalInformation` (1-1 relation)
- `otherInformation` (1-1 relation)
- `project` (many-to-one)

---

### 📂 PersonalInformation

- `birthDate`
- `nationalID`
- `militaryStatus` (Deferred, Exempt, Completed, On Duty)
- `gender`
- `maritalStatus`

---

### 📁 OtherInformation

- `address`
- `bankName`
- `iban`
- `emergencyContactName`
- `emergencyContactPhone`

---

### 🧪 Project

- `id`
- `projectName`
- `projectType` (Support, Internal, HR, Sales, Product)
- `department`
- `vpnUsername`
- `vpnPassword` (should be encrypted)
- `environmentDetails`
- `employees` (one-to-many)

---

## 📦 How to Run

```bash
# Clone the repository
git clone https://github.com/SudeNurErturk/EmployeeProjectWebSite.git
cd EmployeeProjectWebSite

# Run the project with Maven
mvn spring-boot:run
