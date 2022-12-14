# Застосунок для моніторингу погоди
## Завдання
Задання полягає в реалізації моніторингу погоди з використанням OpenWeatherMap API і компонентів бібліотеки Boost.

Програма поділяється на 3 блоки:
- network       - повинен відповідати за підключення до серверу, відправки запиту і отримання відповіді;
- client        - повинен відповідати за відправлення необхідних даних в network, обробку відповіді від network і виводу її на екран в обробленому вигляді;
- application   - повинен отримувати аргументи з командного рядка, відправляти певні дані в client.

Програма повина мати наступні функції:
- введення міста з консолі;
- введення токену з консолі (Якщо не було введено - перевірити файл 'token.txt' в директорії виконуваного файлу). Пам'ятайте, токен - це ваші приватні дані;
- виведення допомоги (Яка показана 'application.hpp'), якщо не було введено аргументів, або був аргумент help або h;
- виведення наступної інформації про погоду по шуканому місту (Приклад виводу в 'application.hpp'):
    - назва міста;
    - температура (в градусах Цельсія);
    - швидкість повітря (метрів/секунду);
    - напрямок повітря (в градусах);
- підключення до серверу (host = 'api.openweathermap.org', port = '80'), відправка запиту і отримування відповіді;
- програма повина коректно відпрацьовувати при відсутності з'єднання з сервером.

Хедери можна тільки доповнювати. main.cpp заборонено редагувати. Обов'язково потрібно використовувати для роботи з мережею Boost.Asio і Boost.Beast, а для роботи з аргументами командного рядка - Boost.Program options. Обов'язково використовувати CMake.

Для збірки проекту потрібно використовувати `CMake`. Напишите инструкцию how to build и how to run.

## Отримання токену
Послідовність дій для отримання токену:
1. Open the following site: https://home.openweathermap.org/users/sign_up
2. Sing up there
3. In purpose field select "Education/science"
4. Check your email, open letter and press "Verify"
5. Your API will be here: https://home.openweathermap.org/api_keys
6. Read the API doc: https://openweathermap.org/current
