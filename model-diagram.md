
# Healthcare Semantic Model — Star Schema Diagram

This semantic model represents a simplified healthcare encounter analytics dataset.  
All data is synthetic and for demonstration purposes only.

---

## ⭐ Fact Table

### **FactEncounter**
FactEncounter
   ├── EncounterID (PK)
   ├── PatientID (FK)
   ├── ProviderID (FK)
   ├── DepartmentID (FK)
   ├── EncounterDateKey (FK)
   ├── LengthOfStay
   ├── EncounterType
   ├── EncounterStatus
   └── VisitCost

---

## ⭐ Dimension Tables

### **DimPatient**
DimPatient
   ├── PatientID (PK)
   ├── Gender
   ├── AgeGroup
   ├── Race
   ├── Ethnicity
   └── ZipCode

### **DimProvider**
DimProvider
   ├── ProviderID (PK)
   ├── ProviderName
   ├── Specialty
   ├── ProviderType
   └── DepartmentID (FK)

### **DimDepartment**
DimDepartment
   ├── DepartmentID (PK)
   ├── DepartmentName
   ├── ServiceLine
   └── Location

### **DimDate**
DimDate
   ├── DateKey (PK)
   ├── Date
   ├── Month
   ├── Quarter
   └── Year

---

## ⭐ Relationship Overview

- **FactEncounter** links to:
  - **DimPatient** via `PatientID`
  - **DimProvider** via `ProviderID`
  - **DimDepartment** via `DepartmentID`
  - **DimDate** via `EncounterDateKey`

This creates a classic **star schema** optimized for:
- Healthcare KPIs  
- Time intelligence  
- Provider performance analysis  
- Encounter volume trends  
- Operational reporting  

---

## ⭐ Notes

- All data represented is **synthetic** and safe for public demonstration.  
- This model is intentionally simplified to highlight architecture concepts.  
- The structure mirrors common patterns found in healthcare analytics environments.


