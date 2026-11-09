# ЛР 2. Программа в отладчике

Отладчик LLDB в VS Code, macOS ARM64.

1. Без отладчика программа вывела `agent: total=6 area=12`.
2. Точка останова установлена на строке 15.
3. До присваивания отладчик показал `p.x = -16`, `p.y = -1`, `total = 1`. После присваивания `p.x = 3` и `p.y = 4`. Объявление массива на строке 16 не выполняет отдельную команду.
4. После `strcpy` в `name[0]` записан код 97 (буква a). Завершающий ноль находится в `name[5]`.
5. На втором проходе `i = 2` и `total = 1`. После прибавления `total = 3`.
6. В стеке три кадра. Сверху `area`, ниже `main` и системный `start`.
7. Команда умножения `mul w8, w8, w9`. Перед `printf` значения `a = 12` и `total = 6`.
8. Под отладчиком программа вывела `agent: total=6 area=12` и завершилась с кодом 0.

[Открыть PDF](Лабораторная%20работа%202.pdf)

## Снимки

![01](screenshots/01_build_run.png)

![02](screenshots/02_breakpoint.png)

![03](screenshots/03_paused.png)

![04](screenshots/04_array_name.png)

![05](screenshots/05_watch_loop.png)

![06](screenshots/06_call_stack.png)

![07](screenshots/07_disassembly.png)

![08](screenshots/08_finished.png)
