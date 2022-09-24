# O Level 2020 Paper 2 Question 1
The following consists of both the original code given by the paper and the solution to the first question.

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
pin = int(input("Please enter the PIN for the locker: "))

if (pin == arraypins[locker - 1]):
    print("The locker is open.")
else:
    print("Incorrect PIN for that locker.")
```

## Additional Comments by Marker
- Change typecasting (line 3)