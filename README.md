# node-basics
Основы работы с node/npm.

Для работы с node.js прежде всего необходимо скачать и установить node.js. В комплекте с node.js будет установлен пакетный менеджер - npm.

#### 1. Создать пустую папку под проект. Инициализировать в ней npm проект.
```
npm init -y
```

#### 2. Создать файл HelloWorld.js, который будет выводить в консоль текст Hello, World! и выполнить при помощи node.
```
touch index.js
```

Содержимое index.js
```javascript
console.log('Hello, World!');
```

Выполнить в консоли 
```
node index.js
```

#### 3. Превратить эту команду в скрипт для npm в файле package.json.

```
"scripts": {
    "start": "node main.js"
},
```

Теперь для запуска этой команды достаточно выполнить в консоли
```
npm start
```

#### 4. Создать папку src и в ней файл src/utils.js.
```
mkdir src
cd src
touch utils.js
```

#### 5. В файле src/utils.js написать функцию и экспортировать её. Содержимое src/utils.js:
```javascript
var sum = function (x, y) {
    return x + y;
}

module.exports.sum = sum;
```

#### 6. В файле index.js импортировать функцию из src/utils.js и воспользоваться ей. Содержимое index.js:
```javascript
var utils = require('./src/utils.js');

console.log(utils.sum(2, 2));
```

#### 7. Установить пакет локально.
```
npm install --save console-log-hello-world
```

C ключом `--save` пакет устанавливается в секцию `dependencies`.

С ключом `--save--dev` пакет устанавливается в секцию `devDependencies`.

Локально установленные пакеты хранятся в папке `node_modules`.

Деинсталировать пакет можно выполнив команду
```
npm uninstall console-log-hello-world 
```

Посмотреть список всех локально установленных паетов можно выполнив команду
```
npm list
```

#### 8. Создать файл helloWorld.js и импортировать установленный пакет. Содержимое файла:
```javascript
require("console-log-hello-world");
```

Выполнить команду 
```
node helloWorld.js
```

В консоли должен появиться текст `Hello, World`.
