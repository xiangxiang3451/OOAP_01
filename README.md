## Проект: Pizza Ordering System

Документация:

#### 1.Введение: 

Pizza Ordering System - это простая система для заказа пиццы, которая предоставляет пользователю возможность выбрать стиль пиццы (сырная или с перцем) и регион (Китай или Россия), а затем разместить заказ.

#### 2.Описание классов:

- **CheesePizza:** Абстрактный класс, представляющий собой пиццу с сыром. Он содержит методы для подготовки, выпечки, нарезки и упаковки пиццы.
- **PepperPizza:** Абстрактный класс, представляющий пиццу с перцем. Он также содержит методы для подготовки, выпечки, нарезки и упаковки пиццы.
- **AbstractFactory:** Абстрактный класс, представляющий собой абстрактную фабрику, которая отвечает за создание семейства связанных продуктов (пицц).
- **ChinaPizzaFactory и RussiaPizzaFactory:** Конкретные фабрики, реализующие абстрактную фабрику. Они создают семейства продуктов для Китая и России соответственно.
- **OrderPizza:** Класс, отвечающий за организацию заказа пиццы. Он взаимодействует с фабрикой для создания соответствующих объектов пиццы и управляет процессом приготовления заказа.
- **PizzaOrderUI:** Класс для пользовательского интерфейса. Он предоставляет пользователю возможность выбрать стиль пиццы и регион, а затем разместить заказ через графический интерфейс.

#### 3.Применение паттернов:

- **Абстрактная фабрика (Abstract Factory):** Этот паттерн используется для создания семейства связанных или зависимых объектов без указания их конкретных классов. В данном случае, абстрактная фабрика (`AbstractFactory`) определяет методы для создания различных видов пиццы (с сыром и с перцем), а конкретные фабрики (`ChinaPizzaFactory` и `RussiaPizzaFactory`) реализуют эти методы для создания пиццы, характерной для конкретных регионов.
- **Фабричный метод (Factory Method):** В данном проекте фабричный метод применяется в методах `createCheesePizza` и `createPepperPizza` каждой конкретной фабрики для создания соответствующих видов пиццы.

#### 4.Преимущества применения паттернов:

- **Разделение ответственностей:** Паттерны позволяют разделить различные аспекты функциональности программы, что делает код более чистым и поддерживаемым.
- **Гибкость и расширяемость:** Использование абстрактной фабрики позволяет легко добавлять новые типы продуктов (пицц) или новые фабрики для других регионов без изменения существующего кода.
- **Упрощение тестирования:** Паттерны способствуют созданию более тестируемого кода за счет лучшего управления зависимостями и разделения функциональности.