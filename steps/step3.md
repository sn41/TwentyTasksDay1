# Задача 3. Функция загрузки файла

#### Задание:
Нужен инструмент, позволяющий загрузить текст из файла в наш текстовый буфер TextBuffer

#### Реализация:
Создайте класс `FileHandler` со статическим методом` loadFile(String filename, TextBuffer buffer)`, который считывает содержимое файла и загружает его в объект TextBuffer.

#### Описание решения:
Метод `loadFile` считывает содержимое файла, объединяет его в строку и передаёт в `TextBuffer`. Использование `try-catch` позволяет обеспечить стабильную работу даже при ошибках чтения файла.

#### Подсказка1:
- Получите путь к файлу, используя java.nio.file.Paths.get(filename)
- Используйте java.nio.file.Files.readAllLines(java.nio.file.Path) для чтения всех строк из файла.
- Используйте метод уже написанного класса TextBuffer.setText для того, чтобы поместить текст в буфер.
- Обработайте возможные исключения (например, IOException). 


#### Базовый каркас решения:

```java
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;

public class FileHandler {
    public static void loadFile(String filename, TextBuffer buffer) {
        try {
            Path filePath = Paths.get(filename);
            // Прочитайте все строки из файла
            List<String> lines = Files.readAllLines(TODO);
            String text = String.join("\n", lines);
            // Поместите текст в буфер
            TODO();
            System.out.println("Файл успешно загружен.");
        } catch (Exception e) {
            System.out.println("Ошибка при загрузке файла '" + filename + "': " + e.getMessage());
        }
    }
}
```