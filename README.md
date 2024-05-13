import random

def generate_random_numbers(lower, upper, count):
    random_numbers = []
    for _ in range(count):
        random_numbers.append(random.randint(lower, upper))
    return random_numbers

lower_limit = 1
upper_limit = 46
numbers_count = 6

random_numbers = generate_random_numbers(lower_limit, upper_limit, numbers_count)
print(random_numbers)
