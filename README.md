# Password-Generator
 ```python
import random

letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']
new_password = []

print("Welcome to the PyPassword Generator!")
nr_letters = int(input("How many letters would you like in your password?\n"))
if 1 < nr_letters <= len(letters):
    new_password += random.sample(letters, nr_letters)

nr_symbols = int(input(f"How many symbols would you like?\n"))
if 1 < nr_symbols <= len(symbols):
    new_password += random.sample(symbols, nr_symbols)

nr_numbers = int(input(f"How many numbers would you like?\n"))
if 1 <= nr_numbers <= len(numbers):
    new_password += random.sample(numbers, nr_numbers)

random.shuffle(new_password)
print("Your password is:","".join(new_password))



# letters = list("abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ")
# symbols = list("!@#$%^&*()")
# numbers = list("0123456789")
#
# nr_letters = int(input("How many letters would you like in your password?\n"))
# nr_symbols = int(input("How many symbols would you like?\n"))
# nr_numbers = int(input("How many numbers would you like?\n"))
#
# # Validation (optional)
# if (
#     1 <= nr_letters <= len(letters)
#     and 1 <= nr_symbols <= len(symbols)
#     and 1 <= nr_numbers <= len(numbers)
# ):
#     password_letters = random.sample(letters, nr_letters)
#     password_symbols = random.sample(symbols, nr_symbols)
#     password_numbers = random.sample(numbers, nr_numbers)
#
#     # Combine all parts and shuffle
#     new_password_list = password_letters + password_symbols + password_numbers
#     random.shuffle(new_password_list)
#
#     # Join into a final string
#     new_password = ''.join(new_password_list)
#     print("Your password is:", new_password)
# else:
#     print("One of your requested amounts is invalid.")
