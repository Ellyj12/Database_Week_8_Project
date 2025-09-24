# Database_Week_8_Project

# Clinic Booking System – Relational Database

A relational database schema for managing a **clinic’s operations**: patients, doctors, appointments, billing, and long-term doctor–patient associations.

---

## Features

- Manage **patients** with unique contact details  
- Store **doctor details** with specializations  
- Track **appointments** between patients and doctors  
- Handle **billing** linked to appointments  
- Manage **doctor–patient relations** (many-to-many)  
- Enforce data integrity with **primary keys, foreign keys, and constraints**  

---

## Database Schema

### Tables

| Table Name       | Purpose                                            |
|------------------|----------------------------------------------------|
| `Patients`       | Stores patient details                             |
| `Specializations`| Lists medical specializations                      |
| `Doctors`        | Stores doctor details (linked to specialization)   |
| `Appointments`   | Schedules patient ↔ doctor meetings                |
| `Billing`        | Tracks payments per appointment                    |
| `DoctorPatient`  | Junction table for many-to-many (Doctors ↔ Patients) |

### Relationships

- **Patients ↔ Appointments** → One-to-Many  
- **Doctors ↔ Appointments** → One-to-Many  
- **Appointments ↔ Billing** → One-to-One  
- **Specializations ↔ Doctors** → One-to-Many  
- **Doctors ↔ Patients** → Many-to-Many 

---

##  Run Instructions

```sql
-- Create the database
CREATE DATABASE Clinic_Database;
USE Clinic_Database;

--Verify tables are created
SHOW TABLES;
SELECT * FROM Patients;
SELECT * FROM Doctors;
SELECT * FROM Appointments;
SELECT * FROM Billing;
SELECT * FROM DoctorPatient;

-- Populate tables with your data (run yourData.sql file)
SOURCE yourData.sql;





