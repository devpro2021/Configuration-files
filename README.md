# Configuration-files

Устанавливаем пакеты
---
npm i -D eslint eslint-config-airbnb eslint-config-prettier eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks babel-eslint prettier husky lint-staged

Добавьте в ваш package.json скрипты
---

lint - проверяет все файлы на ошибки
"lint": "eslint ./src",

lint:fix - проверяет и исправляет те ошибки, которые может
"lint:fix": "eslint ./src --fix",

format - форматирует все файлы с помощью prettier
"format": "prettier --write ./src",

precommit - запускает lint-staged
"precommit": "lint-staged",

```
"lint-staged": {
    "*.{js, jsx}": [
      "npm run lint",
      "npm run lint:fix",
      "npm run format",
      "git add"
    ]
  }
```
