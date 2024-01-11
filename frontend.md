## Frontend

### 1. Регистрация на Cryptorank
Вам нужно зарегистрироваться на [Cryptorank](https://cryptorank.io/)  
После регистрации [сгенерируйте](https://cryptorank.io/public-api/keys) себе API ключ для запросов

API для запроса списка криптовалют  
https://api.cryptorank.io/v1/currencies/1?api_key=YOUR_API_KEY&limit=10&offset=0
**YOUR_API_KEY** - это ключ который вы [сгенерировали](https://cryptorank.io/profile/api)

### 2. Высчитать историческую стоимость

В ответе на запрос присутствуют значения: 
1) price - это текущая цена монеты;
2) percentChange24h, percentChange7d, percentChange30d, percentChange3m, percentChange6m - эти значение отображают, насколько процентов изменилась цена монеты за соответствующий промежуток.
Необходимо вычислить сколько стоила монета в эти периоды. 
Функцию расчета покрыть тестами.

---

### 3. Напишите небольшое SPA
Приложение должно состоять из двух страниц:

1. Конвертер. Где пользователь может конвертировать из одной валюты в другую.  
Пример: https://cryptorank.io/converter

3. Текущие курсы криптовалют.  
На странице пользователь видит таблицу с колонками Name, Price USD, Circulating Supply, Market Cap, Category   
Пример: https://cryptorank.io/watchlist/9a31a11dfe4b

**Добавить дополнительные колонки percentChange, используя функцию из п.2**

**Внедрить пагинацию с помощью limit и offset**

---

**Плюсом будет:**
* Правильное использование SSR, можно запросить данные для первой страницы монет в таблице
* Тесты ([Jest](https://jestjs.io/ru/))
* Грамотная настройка конфигов проекта

В первую очередь мы смотрим на код и реализацию, а не на UI. Дизайнеры у нас есть =)    
Например нам интересно, как вы реализуете функцию из п.2 и обработаете момент с потерей точности    

**Для реализации используйте:**
* [TypeScript](https://www.typescriptlang.org/)
* [React](https://ru.reactjs.org/)
* [Next.js](https://nextjs.org/)
* [styled-components](https://styled-components.com/)
* [SWR](https://swr.vercel.app/)
