# 15. Write a Python function to multiply all the numbers in a list.
def multiply_list(lst):
    result = 1
    for num in lst:
        result *= num
    return result

numbers = [2, 3, 4, 5]
print("Product of list:", multiply_list(numbers))


# 16. Check if a number is perfect.
def is_perfect_number(n):
    divisors = [i for i in range(1, n) if n % i == 0]
    return sum(divisors) == n

num = 28
print(f"Is {num} a perfect number?", is_perfect_number(num))


# 17. Create a function that checks if a passed string is a palindrome or not.
def is_palindrome(s):
    s = s.replace(" ", "").lower()
    return s == s[::-1]

text = "Madam"
print(f"Is '{text}' a palindrome?", is_palindrome(text))


# 18. Write a Python program to check if a passed string is a pangram or not.
import string

def is_pangram(s):
    alphabet = set(string.ascii_lowercase)
    return set(s.lower()) >= alphabet

sentence = "The quick brown fox jumps over the lazy dog"
print(f"Is the sentence a pangram?", is_pangram(sentence))


# 19. Calculate the sum of the digits of a number.
def sum_of_digits(n):
    return sum(int(digit) for digit in str(n))

num = 12345
print("Sum of digits:", sum_of_digits(num))


# 20. Generate a list of four random numbers.
import random

def generate_random_numbers(count=4):
    return [random.randint(1, 100) for _ in range(count)]

print("Random numbers:", generate_random_numbers())
