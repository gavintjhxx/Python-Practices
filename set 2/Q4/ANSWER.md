# O Level 2020 Paper 2 Question 4
The following consists of both the code from Q3 as a continuation and the solution to the second question.

## Original Code
```python
arraypins = [1234, 1654, 1936, 3957, 2058, 7689, 2749, 2265, 1010, 9966]
locker = int(input("Please enter the locker you would like to open: "))

while locker > 10 or locker < 1:
    print("Please enter a locker number from 1 to 10")
    locker = int(input("Please enter the locker you would like to open: "))

pin = int(input("Please enter the PIN for the locker: "))

while pin < 1000 or pin > 9999:
    print("Please input a 4 digit number.")
    pin = int(input("Please enter the PIN for the locker: "))

if (pin == arraypins[locker - 1]):
    print("The locker is open.")
else:
    print("Incorrect PIN for that locker.")
```

## Solution Code
```python
arraypins = [1234, 1654, 1936, 3957, 2058, 7689, 2749, 2265, 1010, 9966]

while True:
    locker = int(input("Please enter the locker you would like to open: "))

    while locker > 10 or locker < 1:
        print("Please enter a locker number from 1 to 10")
        locker = int(input("Please enter the locker you would like to open: "))

    pin = int(input("Please enter the PIN for the locker: "))

    while pin < 1000 or pin > 9999:
        print("Please input a 4 digit number.")
        pin = int(input("Please enter the PIN for the locker: "))

    if (pin == arraypins[locker - 1]):
        print("The locker is open.")
        break
    else:
        print("Incorrect PIN for that locker.")
```

## Additional Comments by Marker
- `while True` (line 3) initiates a forever loop so a `break` statement at the correct point in the program will end the program.
- `break` (line 18) statement is placed when both locker X and pin for the corresponding locker matches. This ends the program.