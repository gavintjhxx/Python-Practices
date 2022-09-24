# Questions

Blood pressure (BP) readings are expressed as a ratio of the systolic pressure over the diastolic pressure. The program below takes in the patient's systolic and diastolic pressure and outputs the diagnosed outcome of the patient.

```python
systolic = int(input("Enter your systolic pressure (mmHg): "))
diastolic = int(input("Enter your diastolic pressure (mmHg): "))

cat = None

result = ["Normal BP", "High-normal BP"]

if systolic < 120 and diastolic < 80:
    cat  = 0
if (systolic >= 120 and systolic <= 139) or (diastolic >= 80 and diastolic <= 89):
    cat = 1

print("Diagnosis:", result[cat])
```

## Question 1
**Edit the program so that it prints the patient's blood pressure reading** in the following form after the patient's data has been entered:
```
Enter your systolic pressure (mmHg): 120
Enter your diastolic pressure (mmHg): 75
Your BP is 120 / 75 mmHg.
```

## Question 2
A more complete organisation is shown in the table below.
![NAS 2020 P2 Fig 1](/set%201/NAS%20P2%202020%20Fig%201.jpg)
When systolic and diastolic blood pressures fall into different categories, the higher category should be used to classify blood pressure level. For example, 160/95 mmHg would be classified stage 2 hypertension.

**Edit the program so that it can also correctly output the additional 3 cases of hypertension**.

## Question 3
**Edit the program so that it will request the user to enter the number of sets of data to be entered and perform the categorisation for the entered number of times**.

Your program should prompt the user with the following message:
```
Enter the number of sets of data to be categorised: 
```