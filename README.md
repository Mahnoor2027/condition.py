# condition.py
# ==============================================
#        CONDITIONAL ASSIGNMENT - PYTHON
#              Student: Your Name
# ==============================================

print("=" * 50)
print("        CONDITIONAL ASSIGNMENT")
print("=" * 50)

# ==================================================
# Question 1 - ATM Machine System
# ==================================================

print("\n========== Question 1 ==========")

balance = 50000
withdraw = 1000

if withdraw > balance:
    print("Insufficient Balance")

elif withdraw < 500:
    print("Minimum withdrawal is 500")

else:
    balance -= withdraw
    print("Withdrawal Successful")
    print("Remaining Balance:", balance)

    if balance > 10000:
        print("Premium User")
    else:
        print("Normal User")


# ==================================================
# Question 2 - Smart Username Validator
# ==================================================

print("\n========== Question 2 ==========")

username = input("Enter Username: ")

if len(username) < 8:
    print("Username must be at least 8 characters.")

elif " " in username:
    print("Username should not contain spaces.")

elif not username[0].isupper():
    print("Username must start with a capital letter.")

elif not any(char.isdigit() for char in username):
    print("Username must contain at least one number.")

else:
    print("Username is Valid.")


# ==================================================
# Question 3 - Exam Eligibility Checker
# ==================================================

print("\n========== Question 3 ==========")

name = input("Enter Student Name: ")
attendance = float(input("Enter Attendance Percentage: "))
fees = input("Enter Fees Status (paid/unpaid): ")

if attendance >= 75 and fees.lower() == "paid":
    print("Eligible For Exam")

elif attendance < 75 and fees.lower() != "paid":
    print("Not Eligible: Attendance is below 75% and Fees are Unpaid")

elif attendance < 75:
    print("Not Eligible: Attendance is below 75%")

else:
    print("Not Eligible: Fees are Unpaid")


# ==================================================
# Question 4 - Password Security Checker
# ==================================================

print("\n========== Question 4 ==========")

password = input("Enter Password: ")

if len(password) < 8:
    print("Weak Password")

elif " " in password:
    print("Weak Password")

elif not password[0].isupper():
    print("Weak Password")

elif "@" not in password and "#" not in password:
    print("Weak Password")

else:
    print("Strong Password")


# ==================================================
# Question 5 - Online Shopping Discount System
# ==================================================

print("\n========== Question 5 ==========")

name = input("Enter Customer Name: ")
bill = float(input("Enter Total Bill: "))
member = input("Membership Status (yes/no): ")

if bill > 5000 and member.lower() == "yes":
    discount = bill * 0.20

elif bill > 3000:
    discount = bill * 0.10

else:
    discount = 0

final_bill = bill - discount

print("Customer Name :", name)
print("Discount      :", discount)
print("Final Bill    :", final_bill)


# ==================================================
# Question 6 - Email Verification System
# ==================================================

print("\n========== Question 6 ==========")

email = input("Enter Email: ")

if len(email) <= 12:
    print("Invalid Email")

elif " " in email:
    print("Invalid Email")

elif not email.endswith("@gmail.com"):
    print("Invalid Email")

else:
    print("Email Verified")


# ==================================================
# Question 7 - Smart Number Analyzer
# ==================================================

print("\n========== Question 7 ==========")

num = int(input("Enter a Number: "))

if num >= 0:
    print("Positive Number")
else:
    print("Negative Number")

if num % 2 == 0:
    print("Even Number")
else:
    print("Odd Number")

if num % 5 == 0:
    print("Divisible by 5")
else:
    print("Not Divisible by 5")

if num > 100:
    print("Large Number")


# ==================================================
# Question 8 - Truthy Falsy Login System
# ==================================================

print("\n========== Question 8 ==========")

username = input("Enter Username: ")
password = input("Enter Password: ")

if username and password:
    print("Login Attempted")
else:
    print("Fields Cannot Be Empty")

print("Lowercase Username :", username.lower())
print("Reversed Username  :", username[::-1])


# ==================================================
# Question 9 - Word Analyzer System
# ==================================================

print("\n========== Question 9 ==========")

sentence = input("Enter a Sentence: ")

if "Python" in sentence:
    print("Python Found")

if len(sentence) > 20:
    print("Long Sentence")
else:
    print("Short Sentence")

print("Updated Sentence :", sentence.replace("Python", "JavaScript"))
print("Reversed Sentence:", sentence[::-1])


# ==================================================
# Question 10 - Nested Login & Role Checker
# ==================================================

print("\n========== Question 10 ==========")

username = input("Enter Username: ")
password = input("Enter Password: ")
role = input("Enter Role: ")

if username == "admin" and password == "12345":

    if role.lower() == "admin":
        print("Welcome Admin")

    elif role.lower() == "student":
        print("Welcome Student")

    else:
        print("Invalid Role")

else:
    print("Invalid Username or Password")

print("\n==============================================")
print("      Assignment Completed Successfully")
print("==============================================")
