# 🐾 Animal Shelter Database System (QUELIFE)

##  Project Overview
This project is a relational database design for QUELIFE, an animal shelter organization with branches across Wisconsin, Illinois, Missouri, Montana, California, Texas, and Nevada. The goal is to streamline data management related to shelters, animals, employees, sponsors, medical history, and adoptions using a well-normalized schema.

##  Objectives
- Design an efficient, normalized database schema
- Capture relationships among shelter branches, animals, sponsors, and employees
- Track animal transfers, medical and grooming history
- Implement payroll and employee roles
- Ensure lossless join and dependency preservation using BCNF

##  Core Features
- Support for animal adoptions, surrenders, transfers
- Detailed grooming, training, medical, and vaccination records
- Sponsor and shelter relationships
- Hourly employee payroll with gross/net calculations
- BCNF normalization and data integrity
- Functional dependencies clearly defined and preserved

##  Entities (Partial List)
- shelter_branch
- animal_info & animal_breed_info
- animal_features
- adoption_details & surrender_details
- medical_history, vaccination, disease_mitigation
- employees_staff_details, employee_pay, employee_payroll
- sponsor, payment_details
- grooming_history, training_history
- shelter_loc_details, facilities

##  Technologies Used
- SQL (PostgreSQL / MySQL)
- ERD tools (e.g., dbdiagram.io, draw.io)
- Microsoft Access (optional prototyping)
- Excel for test data generation

##  Normalization
The database has been fully normalized up to **BCNF** ensuring:
- No redundancy
- Dependency preservation
- Lossless join decomposition
- Efficient relational design

##  Sample Functional Dependencies
- `shelter_id -> shelter_name, shelter_loc`
- `animal_id -> a_breed, a_dob, a_vaccine_status`
- `emp_id -> hourly_pay`
- `transfer_id -> transfer_from, transfer_to, transfer_date`
- `disease -> vaccination_id` (split into disease_mitigation table)

##  Future Improvements
- Integrate a front-end interface for CRUD operations
- Add role-based access control
- Connect to a Streamlit or Flask-based web dashboard
- Enable analytics and reporting dashboards
- Enable REST API integration for mobile/IoT adoption kiosks


