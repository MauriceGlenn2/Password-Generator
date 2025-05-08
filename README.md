# 🔐 Password Generator Project

## 🧠 What I Learned

In this project, I learned how to:
- Create and manipulate lists in Python
- Use `for` loops to iterate over ranges
- Use the `random` module to select random items
- Combine different types of characters (letters, numbers, symbols) into a single list
- Shuffle and join elements in a list to build a randomized password
- Take user input and use it to control how many elements are added to the list

This project helped me understand how powerful and flexible lists can be, especially when used with loops and modules like `random`.

 ```python
import random

# letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
# numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
# symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']
# new_password = []
#
# #my code
# print("Welcome to the PyPassword Generator!")
# nr_letters = int(input("How many letters would you like in your password?\n"))
# if 1 < nr_letters <= len(letters):
#     new_password += random.sample(letters, nr_letters)
#
# nr_symbols = int(input(f"How many symbols would you like?\n"))
# if 1 < nr_symbols <= len(symbols):
#     new_password += random.sample(symbols, nr_symbols)
#
# nr_numbers = int(input(f"How many numbers would you like?\n"))
# if 1 <= nr_numbers <= len(numbers):
#     new_password += random.sample(numbers, nr_numbers)
#
# random.shuffle(new_password)
# print("Your password is:","".join(new_password))

#instructor code 
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']


nr_letters = int(input("How many letters would you like in your password?\n"))
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

password = []
#user chose 4
for char in range(0, nr_letters):
    # 1 - 4
    password += random.choice(letters)
for char in range(0, nr_symbols):
    password += random.choice(symbols)
for char in range(0, nr_numbers):
    password += random.choice(numbers)
random.shuffle(password)
print("".join(password))
