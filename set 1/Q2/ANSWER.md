# NAS 2020 Paper 2 Task 2 Question 2
The following consists of both the code from Question 1 as a continuation and the solution to the second question.

## Original Code
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

## Solution Code
```python
systolic = int(input("Enter your systolic pressure (mmHg): "))
diastolic = int(input("Enter your diastolic pressure (mmHg): "))
print("Your BP is", systolic, "/", diastolic, "mmHg.")

cat = None

result = ["Normal BP", "High-normal BP", "Stage 1 Hypertension", "Stage 2 Hypertension", "Isolated Systolic Hypertension"]

if systolic < 120 and diastolic < 80:
    cat  = 0
if (systolic >= 120 and systolic <= 139) or (diastolic >= 80 and diastolic <= 89):
    cat = 1

if (systolic >= 140 and systolic <= 159) or (diastolic >= 90 and diastolic <= 99):
    cat = 2
if (systolic >= 160 or diastolic >= 100):
    cat = 3
if (systolic > 140 and diastolic < 90):
    cat = 4

print("Diagnosis:", result[cat])
```

## Additional Comments by Marker
- Diagnosis comes from the list `result[]` which contains the categories.
- The variable `cat` determines which position of the list to access based on the inputs.
- The variable `cat` is assigned a value depending on the range that the inputs fall in. (e.g. cat = 1 refers to the 2nd element in `result`, i.e. `result[1]`, resulting in "High Normal BP")
- Since there is an additional 3 cases of hypertension, `result[]` is updated to hole 5 elements.
- Another 3 if-statements are added to check for the cases and assign the variable `cat` a value based on the position of the new cases in `result[]`.