# Задача 2. Создание класса TextBuffer для хранения текста

#### Задание:
Создайте класс TextBuffer, который будет представлять текст как список строк. 
Реализуйте методы для получения всего текста как строки и для установки нового текста.

#### Описание решения:
Класс TextBuffer инкапсулирует данные редактора в виде списка строк. Методы getText() и setText(String text) позволяют получить всё содержимое и загрузить новый текст соответственно. Это фундамент для дальнейших операций над текстом.

#### Подсказка1:
- Используйте ArrayList<String> для хранения всех строк текста.
- Метод String getText() должен возвращать строку, объединяющую все строки текста через разделитель \n.
- Метод setText(String) должен разбивать передаваемый в параметре текст на строки по строке "\\R".
#### Подсказка1:
- Создайте класс TextBuffer, 
- Создайте свойство ArrayList<String> lines,
- Создайте метод String getText(), для объединения строк используйте метод String.join
- Создайте метод void setText(String text), который очистит ArrayList, разобьёт text на строки, добавит текст в ArrayList. Для разбиения строк используйте метод String.split
#### Базовый каркас решения:
```java
import java.util.ArrayList;

public class TextBuffer {
    private ArrayList<String> lines;

    public TextBuffer() {
        lines = new ArrayList<>();
    }

    public String getText() {
        // Объединяем строки 
        String text = String.join("\n", lines);
        return TODO ;
    }
    
    public void setText(String text) {
        // Разбиваем входной текст на строки
        lines.clear();
        String[] textLines = text.split("\n");
        for(String line : TODO ) {
            lines.add(line);
        }
    }
}
```



