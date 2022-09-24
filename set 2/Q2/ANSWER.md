# O Level 2020 Paper 2 Question 2
The following consists of both the code from Q1 as a continuation and the solution to the second question.

## Original Code
```python
arraypins = [1234, 1654, 1936, 3957, 2058, 7689, 2749, 2265, 1010, 9966]
locker = int(input("Please enter the locker you would like to open: "))
pin = float(input("Please enter the PIN for the locker: "))

if (pin == arraypins[locker - 1]):
    print("The locker is open.")
else:
    print("Incorrect PIN for that locker.")
```

## Solution Code
```python
arraypins = [1234, 1654, 1936, 3957, 2058, 7689, 2749, 2265, 1010, 9966]
locker = int(input("Please enter the locker you would like to open: "))

while locker > 10 or locker < 1:
    print("Please enter a locker number from 1 to 10")
    locker = int(input("Please enter the locker you would like to open: "))

pin = int(input("Please enter the PIN for the locker: "))

if (pin == arraypins[locker - 1]):
    print("The locker is open.")
else:
    print("Incorrect PIN for that locker.")
```

## Additional Comments by Marker
- Keywords in the question: "The program must loop until..." hints to a while loop.
- While-loop checks for invalid input to run error code and ask user for another input.
- If input is valid, while-loop is skipped and the rest of the program runs.