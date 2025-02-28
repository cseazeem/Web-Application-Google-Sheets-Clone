# Google Sheets-Like Web Application (Spring Boot + Thymeleaf + MySQL)

## **Project Overview**
This project is a web-based application designed to mimic the core functionalities of Google Sheets. It allows users to create, view, and edit spreadsheets with real-time updates. The system supports **formula evaluation**, **cell updates**, and **dynamic data handling** to ensure a smooth user experience. The backend is built using **Spring Boot**, with **MySQL** as the database, and **Thymeleaf** for frontend rendering.

---

## **Features Implemented**
### **1. Spreadsheet Management**
- Users can **create new spreadsheets**.
- List all available spreadsheets.
- Delete spreadsheets while maintaining database integrity.

### **2. Spreadsheet UI (Grid-Based Data Handling)**
- View and edit spreadsheet data in a structured grid format.
- Supports **dynamic cell updates**.
- Uses **Thymeleaf** for server-side rendering.

### **3. Formula Evaluation and Cell Updates**
- Users can enter **values or formulas** into cells.
- The system supports **basic mathematical functions** such as `SUM`, `AVERAGE`, `MAX`, `MIN`, and `COUNT`.
- Cells update dynamically when referenced by formulas.

### **4. Backend Implementation (Spring Boot + MySQL)**
- **Spring Boot** handles all CRUD operations efficiently.
- **Spring Data JPA & Hibernate** ensure seamless interaction with MySQL.
- Implemented proper database relationships to **link spreadsheets with individual cells**.

### **5. Frontend with Thymeleaf**
- **HTML + CSS + Thymeleaf** templates provide an interactive UI.
- Users can **edit cell values, apply formulas, and save changes**.
- Ensures proper **data binding** between the frontend and backend.

---

## **Technologies Used**
- **Spring Boot (Java)**: Backend framework for handling business logic.
- **Thymeleaf**: Template engine for rendering UI components.
- **MySQL**: Relational database for storing spreadsheets and cell data.
- **Hibernate / JPA**: ORM framework for efficient database interaction.
- **HTML, CSS, JavaScript**: Frontend technologies for UI and styling.
- **Apache Tomcat**: Embedded server for application deployment.

---

## **Challenges Faced & Solutions**
### **1. Thymeleaf Template Rendering Error Due to Null Values**
- **Issue**: When rendering the UI, some templates displayed errors due to missing data.
- **Solution**: Ensured proper **data binding** and initialized default values for empty cells.

### **2. Foreign Key Constraint Preventing Deletion of Spreadsheets**
- **Issue**: Attempting to delete a spreadsheet resulted in foreign key constraint errors.
- **Solution**: Implemented **cascade delete** for related cells when a spreadsheet is removed.

### **3. Efficient Formula Evaluation**
- **Issue**: Handling formulas dynamically while maintaining performance.
- **Solution**: Used **recursive dependency resolution** to evaluate formulas and update related cells accordingly.

### **4. Database Relationships Between Spreadsheets and Cells**
- **Issue**: Ensuring proper linking and retrieval of cell data.
- **Solution**: Used **One-to-Many** relationships in Hibernate to associate spreadsheets with cells.

---

## **Future Enhancements**
- Implement **AJAX** for real-time updates without page refresh.
- Add **support for complex formulas and absolute cell referencing**.
- Enable **file import/export functionality** (CSV, Excel compatibility).
- Implement **user authentication and multi-user collaboration**.

---

## **Installation & Setup**
### **1. Prerequisites**
- Java 17 or later
- MySQL installed and running
- Maven

### **2. Clone the Repository**
```sh
git clone https://github.com/cseazeem/Web-Application-Google-Sheets-Clone.git
cd google-sheets-clone
