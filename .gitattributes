import os

while True:
    file_path = input("Введіть шлях до файлу: ")

    if not os.path.isfile(file_path):
        print("Файл не існує!")
        continue

    num_lines = 0
    num_empty_lines = 0
    num_lines_with_z = 0
    num_z_characters = 0
    num_lines_with_and = 0

    with open(file_path, "r") as file:
        for line in file:
            num_lines += 1
            if line.strip() == "":
                num_empty_lines += 1
            if "z" in line:
                num_lines_with_z += 1
                num_z_characters += line.count("z")
            if "and" in line:
                num_lines_with_and += 1

    print(f"Кількість рядків: {num_lines}")
    print(f"Кількість порожніх рядків: {num_empty_lines}")
    print(f"Кількість рядків з літерою 'z': {num_lines_with_z}")
    print(f"Кількість літер 'z' у файлі: {num_z_characters}")
    print(f"Кількість рядків з групою символів 'and': {num_lines_with_and}")

    choice = input("Бажаєте проаналізувати ще один файл? (так/ні): ")
    if choice.lower() != "так":
        break
