# node-basics
Основы работы с node/npm.

Для работы с node.js прежде всего необходимо скачать и установить node.js. В комплекте с node.js будет установлен пакетный менеджер - npm.

1. Создать пустую папку под проект. Инициализировать в ней npm проект.
```
npm init -y
```

2. Создать файл HelloWorld.js, который будет выводить в консоль текст Hello, World! и выполнить при помощи node.
```
touch index.js
```

Содержимое index.js
```
console.log('Hello, World!');
```

Запускаем node
```
node index.js
```
