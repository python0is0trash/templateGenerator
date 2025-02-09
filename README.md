## Использование
```
Use: ./tg -t TEMPLATE -a FILE [-o OUT_FILE_PREFIX]

Основное:
  -t, --template TEMPLATE                Шаблон команды. В качестве места подстановки используйте знак #
  -a, --arguments FILE                   Файл со списком нужных аргументов, которые будут подставлены в шаблон на место знака #
Опционально:
  -o, --output-template OUT_FILE_PREFIX  Шаблон имен файлов, в которые будут выведены результаты работы каждой команды.
```

## Пример
### Входные данные
1. Шаблон: `echo #`
2. Файл: `args.txt`, содержащий
```args.txt
1
2
3
```
3. Шаблонное название выходных файлов: `test1`, `test2`, `test3`

### Вывод
Тогда команда
```
tg -t 'echo #' -a args.txt -o test
```
выведет результат работы команд `echo 1`, `echo 2` и `echo 3` в соответствующие файлы `test1`, `test2` и `test3`.

Для работы скачайте файл tg и введите в командной строке `chmod +x tg`
