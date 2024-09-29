# ЗАДАНИЕ ПО ТЕМЕ "Цикл for. Элементы списка. Полезные функции в цикле"

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]
print(numbers)
primes = []  # Список для простых чисел
not_primes = []  # Список для составных чисел

for i in range(len(numbers)):
    number = numbers[i]
    is_prime = True
    if number == 1:
        continue
    elif number == 2:
        primes.append(number)
    else:
        for j in range(2, number):
            if number % j != 0:
                continue
            else:
                is_prime = False
                break
        if is_prime:
            primes.append(number)
        else:
            not_primes.append(number)

print(primes, '- Простые числа')
print(not_primes, '- Составные числа')
