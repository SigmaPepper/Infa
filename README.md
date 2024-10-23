# Infa
Зиновьев Павел, Кузьмин Семён, 9кс-134, Компьютрные комплексы и систмы программирования
# Список категорий и товаров с ценами
categories = {
    "Электроника": {
        "Смартфон": 30000,
        "Ноутбук": 60000,
        "Наушники": 5000
    },
    "Одежда": {
        "Футболка": 1500,
        "Джинсы": 3000,
        "Куртка": 5000
    },
    "Продукты": {
        "Хлеб": 50,
        "Молоко": 80,
        "Яблоки": 100
    }
}

# Ввод имени пользователя
user_name = input("Введите ваше имя: ")

# Выбор категории
print("Выберите категорию:")
for category in categories.keys():
    print(category)

selected_category = input("Введите категорию: ")

# Проверка существования категории
if selected_category in categories:
    # Выбор товаров
    print("Доступные товары:")
    products = categories[selected_category]
    for product, price in products.items():
        print(f"{product}: {price} руб.")
    
    selected_products = []
    while True:
        product_name = input("Введите товар для добавления в чек (или 'стоп' для завершения): ")
        if product_name.lower() == 'стоп':
            break
        if product_name in products:
            selected_products.append(product_name)
        else:
            print("Товар не найден. Попробуйте снова.")
else:
    print("Категория не найдена.")

# Формирование чека
if selected_products:
    total_price = sum(products[product] for product in selected_products)
    print("\nЧек:")
    print(f"Имя покупателя: {user_name}")
    print(f"Категория: {selected_category}")
    print("Выбранные товары:")
    for product in selected_products:
        print(f"{product}: {products[product]} руб.")
    print(f"Итого: {total_price} руб.")
else:
    print("Вы не выбрали ни одного товара.")



# Список категорий и товаров с ценами
categories = {
    "электроника": {
        "Смартфон": 30000,
        "Ноутбук": 60000,
        "Наушники": 5000
    },
    "одежда": {
        "Футболка": 1500,
        "Джинсы": 3000,
        "Куртка": 5000
    },
    "продукты": {
        "Хлеб": 50,
        "Молоко": 80,
        "Яблоки": 100
    }
}

# Ввод имени пользователя
user_name = input("Введите ваше имя: ")

# Выбор категории
print("Выберите категорию:")
for category in categories.keys():
    print(category.capitalize())

selected_category = input("Введите категорию: ").lower()

# Проверка существования категории
if selected_category in categories:
    # Выбор товаров
    print("Доступные товары:")
    products = categories[selected_category]
    for product, price in products.items():
        print(f"{product}: {price} руб.")
    
    selected_products = []
    while True:
        product_name = input("Введите товар для добавления в чек (или 'стоп' для завершения): ")
        if product_name.lower() == 'стоп':
            break
        if product_name in products:
            selected_products.append(product_name)
        else:
            print("Товар не найден. Попробуйте снова.")
else:
    print("Категория не найдена.")

# Формирование чека
if selected_products:
    total_price = sum(products[product] for product in selected_products)
    print("\nЧек:")
    print(f"Имя покупателя: {user_name}")
    print(f"Категория: {selected_category.capitalize()}")
    print("Выбранные товары:")
    for product in selected_products:
        print(f"{product}: {products[product]} руб.")
    print(f"Итого: {total_price} руб.")
else:
    print("Вы не выбрали ни одного товара.")
