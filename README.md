# Smart-Coders-Programs

Smart Coders - 112 Practice Problems: Python Solutions

Section 1: Operators

Arithmetic Operators

1. Read two numbers and print their sum, difference, product, quotient, and remainder


a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
print("Sum:", a + b)
print("Difference:", a - b)
print("Product:", a * b)
print("Quotient:", a / b)
print("Remainder:", a % b)

2. Calculate the area of a circle given radius (A = πr²)


import math
r = float(input("Enter radius: "))
area = math.pi * r ** 2
print(f"Area: {area:.2f}")

3. Calculate simple interest given P, R, T → (P × R × T) / 100


p = float(input("Enter principal: "))
r = float(input("Enter rate: "))
t = float(input("Enter time: "))
si = (p * r * t) / 100
print(f"Simple Interest: {si:.2f}")

4. Convert temperature from Celsius to Fahrenheit and vice versa


c = float(input("Enter temperature in Celsius: "))
f = (c * 9/5) + 32
print(f"{c}°C = {f}°F")

f2 = float(input("Enter temperature in Fahrenheit: "))
c2 = (f2 - 32) * 5/9
print(f"{f2}°F = {c2:.2f}°C")

5. Divisibility Check: Check whether a number is divisible by 3, 5, both, or neither


n = int(input("Enter a number: "))
if n % 3 == 0 and n % 5 == 0:
    print("Divisible by both 3 and 5")
elif n % 3 == 0:
    print("Divisible by 3 only")
elif n % 5 == 0:
    print("Divisible by 5 only")
else:
    print("Not divisible by 3 or 5")

Relational & Logical Operators

6. Read two numbers and print which is greater (use relational operators)


a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
if a > b:
    print(a, "is greater")
elif b > a:
    print(b, "is greater")
else:
    print("Both are equal")

7. Check if a number is positive, negative, or zero


n = float(input("Enter a number: "))
if n > 0:
    print("Positive")
elif n < 0:
    print("Negative")
else:
    print("Zero")

8. Read three numbers and check if all three are equal


a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
c = float(input("Enter third number: "))
if a == b and b == c:
    print("All three are equal")
else:
    print("Not all equal")

9. Read age and check eligibility to vote (age ≥ 18)


age = int(input("Enter age: "))
if age >= 18:
    print("Eligible to vote")
else:
    print("Not eligible to vote")

10. Check if a character is uppercase, lowercase, digit, or special character


ch = input("Enter a character: ")
if ch.isupper():
    print("Uppercase letter")
elif ch.islower():
    print("Lowercase letter")
elif ch.isdigit():
    print("Digit")
else:
    print("Special character")

Bitwise Operators

11. Check if a number is even or odd using bitwise AND (n & 1)


n = int(input("Enter a number: "))
if n & 1 == 0:
    print("Even")
else:
    print("Odd")

12. Swap two numbers using XOR


a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print(f"Before swap: a={a}, b={b}")
a = a ^ b
b = a ^ b
a = a ^ b
print(f"After swap: a={a}, b={b}")

13. Find the value of n << 1 and n >> 1 — relate to multiply/divide by 2


n = int(input("Enter a number: "))
print(f"{n} << 1 = {n << 1}  (equivalent to {n} * 2)")
print(f"{n} >> 1 = {n >> 1}  (equivalent to {n} // 2)")

14. Check if the Kth bit of a number is set or not


n = int(input("Enter a number: "))
k = int(input("Enter bit position (0-indexed): "))
if n & (1 << k):
    print(f"Bit {k} is SET")
else:
    print(f"Bit {k} is NOT set")

15. Count the number of set bits in a number


n = int(input("Enter a number: "))
count = 0
temp = n
while temp:
    count += temp & 1
    temp >>= 1
print(f"Number of set bits in {n}: {count}")
# Alternative one-liner: bin(n).count('1')

Section 2: Conditional Statements

if / if-else

16. Check if a number is even or odd


n = int(input("Enter a number: "))
if n % 2 == 0:
    print("Even")
else:
    print("Odd")

17. Check if a year is a leap year


year = int(input("Enter a year: "))
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print("Leap year")
else:
    print("Not a leap year")

18. Find the largest of two numbers


a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
print("Largest:", a if a > b else b)

19. Find the largest of three numbers


a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
c = float(input("Enter third number: "))
if a >= b and a >= c:
    largest = a
elif b >= a and b >= c:
    largest = b
else:
    largest = c
print("Largest:", largest)

20. Check if a character is a vowel or consonant


ch = input("Enter a character: ").lower()
if ch in 'aeiou':
    print("Vowel")
else:
    print("Consonant")

21. Ticket Pricing: Calculate ticket price based on the customer's age


age = int(input("Enter age: "))
if age < 5:
    price = 0
elif age < 12:
    price = 50
elif age < 60:
    price = 100
else:
    price = 60
print("Ticket price:", price)

22. Age Category: Classify a person as a child, teenager, adult, or senior based on age


age = int(input("Enter age: "))
if age < 13:
    print("Child")
elif age < 20:
    print("Teenager")
elif age < 60:
    print("Adult")
else:
    print("Senior")

23. Time Greeting: Given an hour, print Morning, Afternoon, Evening, or Night


hour = int(input("Enter hour (0-23): "))
if 5 <= hour < 12:
    print("Good Morning")
elif 12 <= hour < 17:
    print("Good Afternoon")
elif 17 <= hour < 21:
    print("Good Evening")
else:
    print("Good Night")

24. Login Validator: Check whether a username and password combination is valid


username = input("Enter username: ")
password = input("Enter password: ")
if username == "admin" and password == "admin123":
    print("Login successful")
else:
    print("Invalid username or password")

if-else if-else (Ladder)

25. Given marks (0-100), print grade: A (>=90), B (>=80), C (>=70), D (>=60), F (<60)


marks = float(input("Enter marks: "))
if marks >= 90:
    grade = 'A'
elif marks >= 80:
    grade = 'B'
elif marks >= 70:
    grade = 'C'
elif marks >= 60:
    grade = 'D'
else:
    grade = 'F'
print("Grade:", grade)

26. Read a number (1-7) and print the corresponding day of the week


day = int(input("Enter day number (1-7): "))
days = {1: "Monday", 2: "Tuesday", 3: "Wednesday", 4: "Thursday",
        5: "Friday", 6: "Saturday", 7: "Sunday"}
print(days.get(day, "Invalid day number"))

27. Calculate electricity bill based on slab rates


units = float(input("Enter units consumed: "))
if units <= 100:
    bill = units * 1.5
elif units <= 300:
    bill = 100 * 1.5 + (units - 100) * 3
else:
    bill = 100 * 1.5 + 200 * 3 + (units - 300) * 5
print(f"Electricity bill: {bill:.2f}")

28. Check if a triangle is equilateral, isosceles, or scalene given 3 sides


a = float(input("Enter side a: "))
b = float(input("Enter side b: "))
c = float(input("Enter side c: "))
if a == b == c:
    print("Equilateral triangle")
elif a == b or b == c or a == c:
    print("Isosceles triangle")
else:
    print("Scalene triangle")

29. Given 3 sides, check if a valid triangle can be formed


a = float(input("Enter side a: "))
b = float(input("Enter side b: "))
c = float(input("Enter side c: "))
if a + b > c and b + c > a and a + c > b:
    print("Valid triangle")
else:
    print("Not a valid triangle")

Nested if & switch-case

30. Build a simple calculator (+, -, x, /) using switch-case (match-case in Python)


a = float(input("Enter first number: "))
op = input("Enter operator (+, -, *, /): ")
b = float(input("Enter second number: "))

match op:
    case '+':
        print("Result:", a + b)
    case '-':
        print("Result:", a - b)
    case '*':
        print("Result:", a * b)
    case '/':
        print("Result:", a / b if b != 0 else "Error: division by zero")
    case _:
        print("Invalid operator")

31. Read month number (1-12) and print number of days in that month


month = int(input("Enter month number (1-12): "))
days_in_month = {1:31, 2:28, 3:31, 4:30, 5:31, 6:30,
                  7:31, 8:31, 9:30, 10:31, 11:30, 12:31}
if month in days_in_month:
    print(f"Days: {days_in_month[month]}")
else:
    print("Invalid month")

32. Check if a number is positive, negative, or zero -- then if positive check even/odd


n = int(input("Enter a number: "))
if n > 0:
    if n % 2 == 0:
        print("Positive and Even")
    else:
        print("Positive and Odd")
elif n < 0:
    print("Negative")
else:
    print("Zero")

33. Given 3 numbers, print them in ascending order using only if-else


a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
c = float(input("Enter third number: "))

if a <= b and a <= c:
    first = a
    second, third = (b, c) if b <= c else (c, b)
elif b <= a and b <= c:
    first = b
    second, third = (a, c) if a <= c else (c, a)
else:
    first = c
    second, third = (a, b) if a <= b else (b, a)

print(f"Ascending order: {first}, {second}, {third}")

34. Find the roots of a quadratic equation (check discriminant: real, equal, imaginary)


import math
a = float(input("Enter a: "))
b = float(input("Enter b: "))
c = float(input("Enter c: "))

discriminant = b**2 - 4*a*c

if discriminant > 0:
    root1 = (-b + math.sqrt(discriminant)) / (2*a)
    root2 = (-b - math.sqrt(discriminant)) / (2*a)
    print(f"Two real roots: {root1:.2f}, {root2:.2f}")
elif discriminant == 0:
    root = -b / (2*a)
    print(f"One repeated real root: {root:.2f}")
else:
    real = -b / (2*a)
    imag = math.sqrt(-discriminant) / (2*a)
    print(f"Complex roots: {real:.2f} + {imag:.2f}i, {real:.2f} - {imag:.2f}i")

Mixed / Applied

35. Check if a given character is an alphabet, digit, or special character


ch = input("Enter a character: ")
if ch.isalpha():
    print("Alphabet")
elif ch.isdigit():
    print("Digit")
else:
    print("Special character")

36. Read the cost price and selling price -- print profit, loss, or no profit no loss


cp = float(input("Enter cost price: "))
sp = float(input("Enter selling price: "))
if sp > cp:
    print(f"Profit: {sp - cp:.2f}")
elif cp > sp:
    print(f"Loss: {cp - sp:.2f}")
else:
    print("No profit, no loss")

37. Given coordinates (x, y), determine which quadrant the point lies in


x = float(input("Enter x: "))
y = float(input("Enter y: "))
if x == 0 and y == 0:
    print("Point is at the origin")
elif x == 0:
    print("Point is on the Y-axis")
elif y == 0:
    print("Point is on the X-axis")
elif x > 0 and y > 0:
    print("Quadrant I")
elif x < 0 and y > 0:
    print("Quadrant II")
elif x < 0 and y < 0:
    print("Quadrant III")
else:
    print("Quadrant IV")

38. Check if a 3-digit number is an Armstrong number (e.g., 153)


n = int(input("Enter a 3-digit number: "))
s = str(n)
total = sum(int(d) ** 3 for d in s)
if total == n:
    print(f"{n} is an Armstrong number")
else:
    print(f"{n} is not an Armstrong number")

39. Given hours worked and rate, compute salary with overtime (>40 hrs at 1.5x rate)


hours = float(input("Enter hours worked: "))
rate = float(input("Enter hourly rate: "))
if hours > 40:
    salary = 40 * rate + (hours - 40) * rate * 1.5
else:
    salary = hours * rate
print(f"Salary: {salary:.2f}")

40. ATM Withdrawal: Approve or reject based on amount, balance, and minimum-balance rules


balance = float(input("Enter current balance: "))
amount = float(input("Enter withdrawal amount: "))
MIN_BALANCE = 500

if amount <= 0:
    print("Invalid amount")
elif amount % 100 != 0:
    print("Amount must be in multiples of 100")
elif balance - amount < MIN_BALANCE:
    print("Transaction declined: insufficient balance (minimum balance rule)")
else:
    balance -= amount
    print(f"Withdrawal successful. New balance: {balance:.2f}")

41. Clock Angle: Given hour and minute, calculate the smaller angle between the two hands


hour = int(input("Enter hour (0-12): "))
minute = int(input("Enter minute (0-59): "))

hour = hour % 12
hour_angle = 0.5 * (hour * 60 + minute)
minute_angle = 6 * minute
angle = abs(hour_angle - minute_angle)
angle = min(angle, 360 - angle)
print(f"Angle between hands: {angle:.2f} degrees")

42. Scholarship Eligibility: Determine eligibility based on marks, attendance, and family income


marks = float(input("Enter marks percentage: "))
attendance = float(input("Enter attendance percentage: "))
income = float(input("Enter annual family income: "))

if marks >= 75 and attendance >= 80 and income <= 200000:
    print("Eligible for scholarship")
else:
    print("Not eligible for scholarship")

Section 3: Loops

Basic Counting & Iteration

43. Print numbers from 1 to N


n = int(input("Enter N: "))
for i in range(1, n + 1):
    print(i)

44. Print numbers from N to 1


n = int(input("Enter N: "))
for i in range(n, 0, -1):
    print(i)

45. Print all even numbers from 1 to N


n = int(input("Enter N: "))
for i in range(2, n + 1, 2):
    print(i)

46. Print all odd numbers from 1 to N


n = int(input("Enter N: "))
for i in range(1, n + 1, 2):
    print(i)

47. Calculate the sum of first N natural numbers


n = int(input("Enter N: "))
total = 0
for i in range(1, n + 1):
    total += i
print("Sum:", total)
# Alternative: print(n * (n + 1) // 2)

Digit-Based Problems

48. Count the number of digits in a number


n = int(input("Enter a number: "))
count = 0
temp = abs(n)
if temp == 0:
    count = 1
while temp > 0:
    count += 1
    temp //= 10
print("Number of digits:", count)

49. Find the sum of digits of a number


n = int(input("Enter a number: "))
temp = abs(n)
total = 0
while temp > 0:
    total += temp % 10
    temp //= 10
print("Sum of digits:", total)

50. Reverse a number


n = int(input("Enter a number: "))
temp = abs(n)
reversed_num = 0
while temp > 0:
    digit = temp % 10
    reversed_num = reversed_num * 10 + digit
    temp //= 10
if n < 0:
    reversed_num = -reversed_num
print("Reversed number:", reversed_num)

51. Check if a number is a palindrome


n = int(input("Enter a number: "))
temp = n
reversed_num = 0
while temp > 0:
    reversed_num = reversed_num * 10 + temp % 10
    temp //= 10
if n == reversed_num:
    print(f"{n} is a palindrome")
else:
    print(f"{n} is not a palindrome")

52. Happy Number: Repeatedly replace with sum of squares of digits; check if it reaches 1


def is_happy(n):
    seen = set()
    while n != 1 and n not in seen:
        seen.add(n)
        n = sum(int(d) ** 2 for d in str(n))
    return n == 1

n = int(input("Enter a number: "))
print(f"{n} is {'a happy' if is_happy(n) else 'not a happy'} number")

53. Product of Digits: Find the product of all digits of a number using recursion


def product_of_digits(n):
    if n < 10:
        return n
    return (n % 10) * product_of_digits(n // 10)

n = int(input("Enter a number: "))
print("Product of digits:", product_of_digits(abs(n)))

54. Extract and print each digit of a number from left to right


n = int(input("Enter a number: "))
digits = str(abs(n))
for d in digits:
    print(d)

Math / Number Theory

55. Find factorial of N


n = int(input("Enter N: "))
factorial = 1
for i in range(1, n + 1):
    factorial *= i
print(f"{n}! = {factorial}")

