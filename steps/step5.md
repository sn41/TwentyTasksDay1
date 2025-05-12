Задача 5. Операции вставки и удаления строк
#### Задание:
Расширьте класс `TextBuffer`, добавив методы` insertLine(int index, String line)` и `deleteLine(int index)` для вставки и удаления строки по индексу.

#### Описание решения:
Методы `insertLine` и `deleteLine` позволяют динамически изменять содержимое буфера. 
Корректность индексов проверяется перед выполнением операции, что помогает избегать ошибок во время выполнения.

#### Подсказка1:
- Проверьте корректность индекса.
- Используйте методы ArrayList.add(index, element) и ArrayList.remove(index).

#### Подсказка2:
- Добавьте к классу `TextBuffer` метод `void insertLine(int index, String line){}`.
- Добавьте к классу `TextBuffer` void `deleteLine(int index){}`.
- В методе `insertLine` проверьте условие index >= 0 && index <= lines.size(), если оно истинно, 
добавьте строку к ArrayList lines, используя метод add(index, line).
- В методе `deleteLine` проверьте условие index >= 0 && index <= lines.size(), если оно истинно,
удалите строку в ArrayList lines, используя метод remove(index).
- Выведите сообщения об успешности и не успешности операций

#### Базовый каркас решения:

```java
public void insertLine(int index, String line) {
    if(TODO) {
        TODO();
        System.out.println("Строка вставлена на позицию " + index);
    } else {
        System.out.println("Некорректный индекс для вставки.");
    }
}

public void deleteLine(int index) {
    if(TODO) {
        TODO();
        System.out.println("Строка на позиции " + index + " удалена.");
    } else {
        System.out.println("Некорректный индекс для удаления.");
    }
}
```