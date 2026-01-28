# 🏥 Hospital Management System – Backend (Spring Boot)

## 📌 Project Overview

The **Hospital Management System Backend** is a comprehensive Spring Boot–based RESTful application designed to streamline hospital operations by managing patients, medical staff, clinical records, and facilities in a unified platform.

The system focuses on modular design, scalable architecture, and clean data relationships to support real-world healthcare workflows such as diagnosis tracking, diet management, room allocation, and patient mobility monitoring.

---

## 🚀 Key Features

### 👩‍⚕️ Nurse Management

* Secure authentication
* CRUD operations
* Specialization tracking

### 🧑‍🤝‍🧑 Auxiliary Staff Management

* Staff authentication
* Profile management

### 🧍 Patient Management

* Personal details & emergency contacts
* Medical history storage
* Observation records

### 📋 Medical Records

* Diagnoses & detailed diagnosis levels
* Vital signs monitoring
* Observations and clinical notes

### 🏨 Facility Management

* Room creation and allocation
* Patient–room mapping

### 🥗 Diet Tracking

* Diet plans with texture types
* Dietary requirements
* Many-to-many diet relationships

### 🚶 Mobilization Management

* Sedestation tracking
* Walking assistance monitoring

### 🩺 Drain Management

* Drain types
* Output tracking

### 🚿 Hygiene Management

* Hygiene procedures and types

---

## 🛠 Technology Stack

* **Java 17**
* **Spring Boot**
* **Spring Data JPA**
* **Jakarta Persistence (Hibernate)**
* **RESTful APIs**
* **MySQL**

---

## 🧩 Core Entities

* **Patient** – Central patient profile and history
* **Register** – Main medical record hub
* **Nurse** – Nursing staff
* **Auxiliary** – Supporting medical staff
* **Diagnosis** – Patient diagnosis records
* **DetailDiagnosis** – Dependency levels & equipment
* **VitalSign** – Patient vitals
* **Diet** – Nutrition tracking
* **Room** – Hospital facilities
* **Observation** – Additional notes
* **Mobilization** – Patient mobility
* **Drain** – Drainage monitoring

---

## 🔗 Entity Relationships

* **One-to-Many**

  * Diagnosis → DetailDiagnosis
  * Patient → Observation

* **Many-to-Many**

  * Diet ↔ DietType

* **One-to-One**

  * Register ↔ VitalSign
  * Register ↔ Diet
  * Patient ↔ Room

---

## 🌐 REST API Endpoints

### Nurse Management

* `POST /nurse/login`
* `GET /nurse`
* `GET /nurse/name/{name}`
* `GET /nurse/{id}`
* `POST /nurse`
* `PUT /nurse/{id}`
* `DELETE /nurse/{id}`

### Auxiliary Management

* `POST /auxiliary/login`
* `POST /auxiliary`
* `GET /auxiliary/{id}`

### Patient Management

* `POST /patient/list`
* `POST /patient`
* `GET /patient/{id}`
* `PUT /patient/{id}`

### Register Management

* `POST /register`
* `GET /register/{id}`
* `GET /register/vitalSign/{id}`
* `GET /register/diagnosis/{id}`

### Room Management

* `POST /room`
* `POST /room/list`
* `GET /room`

---

## 🗄 Database Design

Relational schema implemented using JPA/Hibernate with:

* Normalized tables
* Foreign key constraints
* Bidirectional mappings
* Cascade operations where appropriate

Designed for scalability and data integrity.

---

## ⚙️ Setup & Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/nsaladie/MP13-Final-Proyect-BackEnd.git
```

### 2️⃣ Build Project

```bash
mvn clean install
```

### 3️⃣ Configure Database

Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/hospital
spring.datasource.username=your_username
spring.datasource.password=your_password
```

### 4️⃣ Run Application

```bash
mvn spring-boot:run
```

---

## 📁 Project Structure

```
src/main/java/com/example/Hospital/Hospital/
├── controller/    # REST Controllers
├── entity/        # JPA Entities
├── repository/   # Spring Data Repositories
├── service/      # Business Logic
```

## Author
Nakul Kapre

