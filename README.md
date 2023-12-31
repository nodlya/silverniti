## Начало работы

Далее в инструкции описан порядок дейсвий для развертывания проекта на вашем локальном компьютере
для разработки.

Для работы в [VSCode](https://code.visualstudio.com/) рекомендуется установить расширение
[Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (и проверить, что отключено
расширение Vetur)

### Установка

Для установки зависимостей используйте команду

```sh
npm install
```
//нужная команда



Для запуска приложения в браузере с горячей перезагрузкой введите команду

```sh
npm run dev
```

Для сборки приложения введите команду

```sh
npm run build
```
//нужная команда для деплоя + порт 5173



Для линтинга введите команду

```sh
npm run lint
```

## Code style

В целях соблюдения договоренностей, а также поддержания однообразия и чистоты кода, в проекте
используется модифицированный пресет eslint'а
[plugin:vue/vue3-recommended](https://eslint.vuejs.org/rules/).

### Интеграция с IDE

Для автоматического исправления замечаний линтера в **VSCode** необходимо в settings.json указать
настройки:

```sh
  ...

  "eslint.format.enable": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  }

  ...
```
