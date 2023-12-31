**Задача: Система учета товаров в интернет-магазине**

Вы разрабатываете систему учета товаров для интернет-магазина. Вам необходимо создать JavaScript-приложение, которое будет обрабатывать заказы покупателей и подсчитывать общую стоимость заказа, учитывая различные акции и скидки.

У вас есть следующие данные:

1. Объект `товары`, содержащий информацию о доступных товарах. Каждый товар имеет следующие свойства:
   - `название` (строка) - название товара.
   - `цена` (число) - цена товара.
   - `акционнаяСкидка` (число) - скидка, которая применяется к товару (если есть акция).
   - `количество` (число) - количество единиц товара на складе.

```javascript
const товары = [
  { название: "Футболка", цена: 20, акционнаяСкидка: 0, количество: 50 },
  { название: "Джинсы", цена: 50, акционнаяСкидка: 10, количество: 30 },
  { название: "Кроссовки", цена: 80, акционнаяСкидка: 20, количество: 20 },
];
```

2. Массив `корзина`, в котором хранятся товары, выбранные покупателем. Каждый элемент массива - это объект, содержащий информацию о товаре и его количестве.

3. Система скидок:
   - Если покупатель добавляет в корзину 3 и более товара, он получает дополнительную скидку 15% на всю корзину.
   - Если покупатель добавляет товар, у которого установлена акционная скидка, скидка применяется к этому товару.

Задачи:

a. Напишите функцию `добавитьВКорзину(товар, количество)`, которая добавляет товар в корзину с указанным количеством. Учтите, что товар должен быть доступным на складе, и уменьшите количество товара на складе после добавления в корзину.

b. Напишите функцию `подсчитатьОбщуюСумму()`, которая вычисляет общую стоимость товаров в корзине, учитывая все скидки.

c. Напишите функцию `применитьСкидку15Процентов()`, которая применяет 15% скидку, если в корзине есть 3 и более товара.

d. Напишите функцию `оформитьЗаказ()`, которая выводит информацию о заказе и общей стоимости, после чего очищает корзину и обновляет данные о товарах на складе.

Помимо этого, учтите проверки на наличие товара на складе и корректность ввода данных при добавлении в корзину.


**Усложнение: Учет пользовательских аккаунтов и истории заказов**

Вам необходимо расширить вашу систему учета товаров, добавив учет пользовательских аккаунтов и истории их заказов.

Для этого добавьте следующее:

1. Объект `пользователи`, содержащий информацию о пользователях. Каждый пользователь имеет следующие свойства:
   - `имя` (строка) - имя пользователя.
   - `email` (строка) - адрес электронной почты пользователя.
   - `пароль` (строка) - пароль для входа в систему.
   - `историяЗаказов` (массив) - массив объектов, представляющих историю заказов пользователя.

```javascript
const пользователи = [
  { имя: "Иван", email: "ivan@example.com", пароль: "ivan123", историяЗаказов: [] },
  { имя: "Мария", email: "maria@example.com", пароль: "maria456", историяЗаказов: [] },
];
```

2. Функцию `авторизация(email, пароль)`, которая будет проверять существующих пользователей и авторизовывать их в системе.

3. Функцию `создатьЗаказ(пользователь)`, которая будет добавлять текущую корзину в историю заказов указанного пользователя.

4. Функцию `получитьИсториюЗаказов(пользователь)`, которая будет возвращать историю заказов для указанного пользователя.

5. Функцию `очиститьИсториюЗаказов(пользователь)`, которая будет очищать историю заказов для указанного пользователя.

Убедитесь, что только авторизованные пользователи могут создавать заказы и просматривать историю заказов.