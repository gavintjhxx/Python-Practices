# NAS 2020 Paper 2 Task 2 Question 3
The following consists of both the code from Question 2 as a continuation and the solution to the third question.

## Original Code
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

## Solution Code
```python
num_inputs = int(input("Enter the number of sets of data to be categorised: "))

for i in range(num_inputs):
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
- User-defined number of inputs: ask user for number of inputs and use a for-loop.
- Unknown number of inputs with a terminating condition: ask user for data, use while-loop to check for terminating condition and ask for data again at the end of while-loop.