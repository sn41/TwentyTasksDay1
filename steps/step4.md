# Задача 4. Функция сохранения файла

#### Задание:
Дополните класс `FileHandler` методом `saveFile(String filename, TextBuffer buffer)`, который записывает содержимое текстового буфера в указанный файл.

#### Описание решения:
Метод saveFile получает текст из буфера с помощью метода getText() и записывает его в указанный файл. Обработка исключений защищает программу от сбоев при ошибках ввода-вывода.

#### Подсказка1:
- Используйте Files.write для записи текста в файл.
- Обработайте исключения для обеспечения отказоустойчивости.
#### Подсказка2:
- Добавьте статический метод saveFile(String filename, TextBuffer buffer) к классу FileHandler 
- Используйте метод Paths.get() для получения пути к файлу
- Используйте метод TextBuffer.getText() для получения полного текста из буфера
- Используйте метод String.getBytes() для преобразования строки в массив байт. 
- Используйте метод Files.write(Path, byte[]) для сохранения массива в файл. 
- Выведите сообщение об успешном выполнении
- Поместите предыдущие операции в блок try-catch
####  Базовый каркас решения:
```java
import java.nio.file.Files;
import java.nio.file.Paths;

public class FileHandler {
    public static void saveFile(String filename, TextBuffer buffer) {
        try {
            Path path = Paths.get(TODO);
            String bufferText = TODO();
            byte[] bytes = bufferText.getBytes();
            Files.write(path, TODO);
            System.out.println("Файл '" + filename + "' успешно сохранён.");
        } catch(Exception e) {
            System.out.println("Ошибка при сохранении файла '" + filename + "': " + e.getMessage());
        }
    }
}
```