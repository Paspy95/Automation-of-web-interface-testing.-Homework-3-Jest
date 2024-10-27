## Задача 1. Jest. Unit-тесты и отчёты

1. Сделайте форк [проекта с лекции](https://github.com/netology-code/jsaqa-code/tree/main/7.3/jest).
2. Добавьте отчёты о покрытии.

Ваши отчёты должны создаваться во время прогона тестов с помощью скрипта. Его нужно добавить в блок со скриптами в файле `package.json`.
    
Скрипт для запуска оценки покрытия должен запускать команду `"jest --collectCoverage"`. Создайте нужный скрипт по аналогии с существующим скриптом `"test"`.

Для корректной работы, нужно задать критерии, где будут работать отчёты, а также параметры, которые исключают проверку в определённых местах проекта.

В нашем случае мы хотим:

- проверять покрытие кода во всех файлах с расширениями `.js` и `.jsx`;
- исключать из проверки директорию `"/node_modules/"`;
- исключать из проверки директорию `"/coverage/"`, в которой будут создаваться отчёты.

Документация, которая вам поможет, есть [по ссылке](https://jestjs.io/ru/docs/configuration#collectcoveragefrom-array).

3. Добавьте желаемые параметры покрытия:
```
"coverageThreshold": {
        "branches": 100,
        "functions": 100,
        "lines": 100
  }
```

4. Запустите тесты с проверкой покрытия при помощи нового скрипта: 

<details>
  <summary>Подсказка.</summary>
  
  Примерно так должны выглядеть скрипт и команда для его запуска: 

  ```"coverage": "jest --collectCoverage"``` 

  ```npm run coverage```
</details>


5. Допишите недостающие тесты для покрытия 100% по всем параметрам.
Рекомендуем использовать отчёт из папки `/coverage` и дебагер, чтобы понять, какой код недостаточно покрыт тестами.

6. Запушьте репозиторий и сдайте ссылку на проверку.
