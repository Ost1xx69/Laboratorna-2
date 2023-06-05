while True:

    file_path = input("Введіть шлях до файлу: ")

    try:

        with open(file_path, 'r') as file:

            lines = file.readlines()


            num_lines = len(lines)


            num_empty_lines = len([line for line in lines if line.strip() == ""])


            num_lines_with_z = len([line for line in lines if "z" in line])


            num_z_chars = sum([line.count("z") for line in lines])


            num_and_lines = len([line for line in lines if "and" in line])

            print(f"Кількість рядків: {num_lines}")
            print(f"Кількість порожніх рядків: {num_empty_lines}")
            print(f"Кількість рядків з літерою 'z': {num_lines_with_z}")
            print(f"Кількість літер 'z' у файлі: {num_z_chars}")
            print(f"Кількість рядків з групою символів 'and': {num_and_lines}")

    except FileNotFoundError:
        print("Файл не знайдено.")


    choice = input("Бажаєте проаналізувати ще один файл? (y/n) ")

    if choice.lower() != "y":
        break
