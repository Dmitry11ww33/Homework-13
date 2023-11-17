# Homework-13
------------------------------------------------------------------------------------------------
Ex.1

Дана строка с произвольная строка  

написать регулярное выражение для определения номера автомобиля. 
Допускается только такая запись номера автомобиля А000АА
А-любая буква(латиница)
0-любая цифра

Программа должны вывести кол-во валидных значений и показать их в консоле

import re

def find_car_numbers(text):
    pattern = r'\b[A-Z]\d{3}[A-Z]{2}\b'
    matches = re.findall(pattern, text)
    return matches

input_text = "Произвольные номера авто: A123BC, X456YZ, B789DE. Неверные записи: AB12CD, 123XYZ."

valid_numbers = find_car_numbers(input_text)

print(f"Кол-во валидных номеров авто: {len(valid_numbers)}")
print("Валидные номера авто:", valid_numbers)

------------------------------------------------------------------------------------------------

Ex.2

используя модуль turtle и создав функцию рисования шестиугольника, решите следующую задачу:

import turtle
ws = turtle.Screen()
Turtle = turtle.Turtle()
for i in range(6):
    Turtle.forward(90)
    Turtle.left(300)
for i in range(6):
    Turtle.backward(90)
    Turtle.left(300)
for i in range(6):
    Turtle.forward(90)
    Turtle.right(300)
