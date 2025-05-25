# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Chosen:
University / Hospital (choose one)

## ER Diagram:
![438267879-61922e0f-7513-4773-83c2-38753d629dae](https://github.com/user-attachments/assets/1250a730-10a6-432e-9d18-8e23cb36d47a)


## Entities and Attributes:
Patient:

Pat_id, PName, PDiagnosis, PAddress

Hospital:

H_id, H_name, Hcity, HAddress

Medical record:

PRecord, Date, Problem

Receptionist:

No direct attributes shown in the diagram

Medicine:

Date, Quantity, Price

Doctor:

D_id, D_name, Qualification, Salary

ISA Relationship:

Specialization into Permanent and Trainee (sub-entities). ...

## Relationships and Constraints:
- Relationship1 (Cardinality, Participation)

- Relationship2 (Cardinality, Participation)

- Admitted in: (between Patient and Hospital)

Cardinality: Many-to-One (many patients can be admitted to one hospital)

Participation: Partial for Patient, total for Hospital (assumption)

has: (between Patient and Medical record)

Cardinality: One-to-Many (a patient can have multiple medical records)

Participation: Total for Medical record (each record must belong to a patient)

maintains: (between Receptionist and Patient)

Cardinality: Many-to-Many (receptionists can maintain multiple patients, and patients can be handled by multiple receptionists)

Participation: Partial for both

bills: (between Medical record and Medicine)

Cardinality: Many-to-Many (a medical record can bill multiple medicines; a medicine can appear in multiple records)

Participation: Partial for both

has: (between Hospital and Doctor)

Cardinality: One-to-Many (one hospital has many doctors)

Participation: Total for Doctor (every doctor belongs to a hospital)

ISA (Inheritance between Doctor and Permanent/Trainee)

A Doctor can be either Permanent or Trainee (exclusive specialization).
...

## Extension (Prerequisite / Billing):

- Explain how you modeled prerequisites or billing.

- Billing is modeled through the relationship bills between Medical record and Medicine.

Each bill captures:

The Medicine prescribed

The Date of transaction

Quantity and Price information of medicines.

Billing logic assumes that medical records generate billing entries for the medicines used during treatment.

## Design Choices:

Brief explanation of why you chose certain entities, relationships, and assumptions

Separate entities for Patient, Hospital, Doctor, Medicine, and Receptionist to allow flexible scalability.

Specialization (ISA) for Doctors into Permanent and Trainee because their employment types have different attributes and potential behaviors.

Receptionist maintains patient data — included for administrative management without burdening the medical records directly.

Medicine entity is modeled separately, acknowledging that medicines are not unique to a patient but rather are standardized items billed during medical treatment.

Separate Medical Record entity — ensures patient history is preserved even if they switch hospitals or change doctors.

## RESULT
The entities in the ER diagram are Patient, Hospital, Doctor (specialized into Permanent and Trainee), Receptionist, Medicine, and Medical Record, each with their relevant attributes. Patients are admitted into hospitals, have medical records, and are maintained by receptionists; medical records bill medicines, and hospitals have doctors. Billing is managed by connecting medical records to medicines, recording date, quantity, and price to accurately capture treatment costs. The design separates entities for clarity, uses specialization for doctors to reflect different employment types, and models billing independently to allow flexible management of patient treatments and expenses.
