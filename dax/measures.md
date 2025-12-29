## Key DAX Measures

### Overall Satisfaction Score (Respondents Only)
```DAX
Overall Satisfaction Score :=
CALCULATE(
    AVERAGE('Hospital Emergency Room Data'[Patient Satisfaction Score]),
    'Hospital Emergency Room Data'[Patient Satisfaction Score] <> BLANK(),
    ALL('Hospital Emergency Room Data')
)
```

### Feedback Response Rate
Feedback Response Rate :=
DIVIDE(
    COUNT('Hospital Emergency Room Data'[Patient Satisfaction Score]),
    COUNT('Hospital Emergency Room Data'[Patient ID])
)
