## Mobile (React-Native)

### 1. Регистрация на Cryptorank
Вам нужно зарегистрироваться на [Cryptorank](https://cryptorank.io/)  
После регистрации [сгенерируйте](https://cryptorank.io/public-api/keys) себе API ключ для запросов

API для запроса списка криптовалют  
https://api.cryptorank.io/v1/currencies?api_key=YOUR_API_KEY&limit=10&offset=0
**YOUR_API_KEY** - это ключ который вы [сгенерировали](https://cryptorank.io/profile/api)

---

### 2. Напишите небольшое мобильное приложение
Приложение должно состоять из двух экранов:

1. Конвертер. Где пользователь может конвертировать из одной валюты в другую.

Пример: Мобильное приложение CryptoRank [iOS](https://apps.apple.com/ru/app/cryptorank-tracker-portfolio/id1609951971), [Android](https://play.google.com/store/apps/details?id=com.cryptorank&hl=en_US) > монета Bitcoin > таб Overview
![telegram-cloud-photo-size-2-5224592016824980684-y](https://github.com/novev9/cr-test-tast/assets/20814827/a7b17a42-85e1-4638-b3f7-a62d0424cee8)


2. Список криптовалют для выбора конвертера.
![telegram-cloud-photo-size-2-5224592016824980690-x](https://github.com/novev9/cr-test-tast/assets/20814827/6c034561-cbf7-4866-8dcb-c80b8dbe3389)


Добавить дополнительно:
  - пагинацию с помощью limit и offset
  - поиск с помощью symbol (в symbol передается значение из input)
  - сортировку по rank, -rank, price, -price

Итоговый запрос может быть таким https://api.cryptorank.io/v1/currencies?api_key=YOUR_API_KEY&limit=10&offset=0&sort=price&symbol=btc

---

В первую очередь мы смотрим на код и реализацию, а не на UI. Дизайнеры у нас есть =)       

**Для реализации используйте:**
* [TypeScript](https://www.typescriptlang.org/)
* [React Native](https://reactnative.dev/)
* [React Navigation](https://reactnavigation.org/)

**В результате необходимо прислать .apk файл и ссылку на репозиторий**
