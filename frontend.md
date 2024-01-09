## Frontend

### 1. Регистрация на Cryptorank
Вам нужно зарегистрироваться на [Cryptorank](https://cryptorank.io/)  
После регистрации [сгенерируйте](https://cryptorank.io/public-api/keys) себе API ключ для запросов

### 2. Высчитать историческую стоимость

Даны значения percentChange24h, percentChange7d и прочие в процентах и текущая цена в USD. Необходимо вычислить сколько стоила монета в эти периоды historicalPrice24h, historicalPrice7d и тд. 
Функцию расчета покрыть тестами.    

---

### 3. Напишите небольшое SPA
Приложение должно состоять из двух страниц:

1. Конвертер. Где пользователь может конвертировать из одной валюты в другую.  
Пример: https://cryptorank.io/converter

3. Текущие курсы криптовалют.  
На странице пользователь видит таблицу с колонками Name, Price USD, Circulating Supply, Market Cap, Category   
Пример: https://cryptorank.io/watchlist/9a31a11dfe4b    
**Добавить дополнительные колонки percentChange используя функцию из п.2**
**Использовать пагинацию с помощью limit и offset**


API для запроса списка криптовалют  
https://api.cryptorank.io/v1/currencies/1?api_key=YOUR_API_KEY&limit=10&offset=0
**YOUR_API_KEY** - это ключ который вы [сгенерировали](https://cryptorank.io/profile/api)

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
