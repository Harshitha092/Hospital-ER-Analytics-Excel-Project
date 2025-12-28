## Calculated Columns (DAX)

### Age Group
```DAX
Age Group =
IF([Patient Age] > 70, "70-79",
IF([Patient Age] > 60, "60-69",
IF([Patient Age] > 50, "50-59",
IF([Patient Age] > 40, "40-49",
IF([Patient Age] > 30, "30-39",
IF([Patient Age] > 20, "20-29",
IF([Patient Age] > 10, "10-19",
"0-09")))))))

---
### Patient Attend Status
Patient Attend Status =
IF([Wait Time] > 30, "Delayed", "On Time")

---
