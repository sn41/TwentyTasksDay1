
## Задача 6. Реализация поиска текста в буфере

**Задание:**  
Создайте класс `TextSearch` с методом `searchText(TextBuffer buffer, String query)`, который ищет подстроку во всех строках буфера и выводит номера строк, где она найдена.

**Описание решения:**  
Метод `searchText` проходит по всем строкам текстового буфера, используя метод `contains` для поиска подстроки. При нахождении совпадения выводится номер строки и её содержимое.


**Подсказка1:**
- Переберите строки из буфера с помощью цикла.
- Используйте метод `contains` для проверки вхождения подстроки.

**Базовый каркас решения:**
```java
public class TextSearch {
    public static void searchText(TextBuffer buffer, String query) {
        // Перебираем строки буфера
    }
}
```

**Подсказка2:**
```
- Переберите строки из буфера с помощью цикла.
  - Разбейте текст на строки.
  - Объявите переменную флага поиска, инициируйте её значением `false`.
  - Создайте цикл с переменной цикла, чтобы можно было вы видеть номер обрабатываемой строки.
    - В цикле, проверьте условие, что текущая строка содержит искомую подстроку `query`
      - если да, выведите сообщение с номером текущей строки, и установите флаг поиска в true
  - После цикла, если флаг не равен true, выведите сообщение, что ничего не найдено. 
- Используйте метод `contains` для проверки вхождения подстроки.
```

**Базовый каркас решения:**
```java
public class TextSearch {
    public static void searchText(TextBuffer buffer, String query) {
        // Перебираем строки буфера
        String[] lines = TODO;
        boolean found = TODO;
        for (int i = 0; i < lines.length; i++) {
            if(lines[i].contains(query)) {
                TODO("Найдено в строке " + i + ": " + lines[i]);
                found = TODO;
            }
        }
        if(TODO) {
            TODO("По запросу '" + query + "' ничего не найдено.");
        }
    }
}
```

