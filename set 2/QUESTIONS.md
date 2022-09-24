# Questions

The following program checks if the personal identification number (PIN) entered for a locker is correct. There are 10 lockers available and the correct PIN for each locker is stored in an array. **A PIN cannot start with the digit 0.**

The program allows the user to enter the number of the locker array they want to open, and a PIN. It checks if the PIN is correct for that locker.

```python
arraypins = [1234, 1654, 1936, 3957, 2058, 7689, 2749, 2265, 1010, 9966]
locker = int(input("Please enter the locker you would like to open: "))
pin = float(input("Please enter the PIN for the locker: "))

if (pin == arraypins[locker - 1]):
    print("The locker is open.")
else:
    print("Incorrect PIN for that locker.")
```

## Question 1
Edit the program so that it converts the PIN input by the user to an integer.

## Question 2
Edit the program to only accept a locker number between 1 and 10 (inclusive) to be input. A suitable error message must be displayed if the locker number input is not in this range. The program must loop until a valid locker number is input.

## Question 3
Edit the program to only accept a PIN of 4 digits to be entered by the user. A suitable error message must be displayed if an incorrect input is given. The program must loop until the PIN input is 4 digits.

## Question 4
Edit the program to loop until the user inputs both a correct locker number and the matching PIN for that locker.