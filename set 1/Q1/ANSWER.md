# NAS 2020 Paper 2 Task 2 Question 1
The following consists of both the original code given by the paper and the solution to the first question.

## Original Code
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

## Solution Code
```python
systolic = int(input("Enter your systolic pressure (mmHg): "))
diastolic = int(input("Enter your diastolic pressure (mmHg): "))
print("Your BP is", systolic, "/", diastolic, "mmHg.")

cat = None

result = ["Normal BP", "High-normal BP"]

if systolic < 120 and diastolic < 80:
    cat  = 0
if (systolic >= 120 and systolic <= 139) or (diastolic >= 80 and diastolic <= 89):
    cat = 1

print("Diagnosis:", result[cat])
```

## Additional Comments by Marker
- Output statement must match the sample given in question.
- Alternative answers:
  - `print("Your BP is " + str(systolic) + " / " + str(diastolic) + " mmHg.")`