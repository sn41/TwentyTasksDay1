
## Задача 7. Командный интерфейс (CLI) для управления редактором

**Задание:**  
Создайте класс командной строки `CLI`, который организует цикл ввода команд пользователем и выполняет операции (загрузка, сохранение, вставка, удаление, поиск) посредством вызова соответствующих методов.
Командная строка - это строка, которая содержит имя команды, которое может быть дополнено агрументом. Команда и аргумент разделены пробелом.
Необходимо:
1. Выделить команды, агрумент.
2. Для каждой определённой команды вызвать соответствующую функцию, 

**Подробное описание решения:**  
Класс `CLI` реализует цикл ввода команд. После разбивки строки на команду и аргументы осуществляется вызов соответствующего метода – загрузки, сохранения, вставки, удаления или поиска. Это позволяет пользователю взаимодействовать с редактором через консоль.


**Базовый каркас решения:**
```java
import java.util.Scanner;

public class CLI {
    public static void run() {
        Scanner scanner = new Scanner(System.in);
        TextBuffer buffer = new TextBuffer();
        // Вывод сообщения приветствия "MiniTextEditor (CLI) запущен. Введите 'help' для списка команд."
        // Бесконечный цикл обработки команд
        while (true) {
            //Вывод приглашения   ">> "
            
            // Получение строки, выделение команды и аргумента
            //Получить новую строку используя scanner.nextLine()
            String input = scanner.nextLine().trim();
            //Убрать начальные и конечные пробелы, используя .trim()
            TODO.trim();
            //если строка пуста - выйти из цикла используя continue
            if(TODO.isEmpty()) continue;
            //Разбить строку на две части по пробельным символам, используя команду split("\\s+", 2)
            String[] parts = input.split("\\s+", 2);
            //Перевести первый элемент строки в нижний регистр
            String command = parts[0].toLowerCase();
            // Поместить в переменную args строку аргумента.
            String args = parts.length > 1 ? parts[1] : "";
            
            //Сравниваем строку команды и шаблон
            // например проверяем, является ли команда словом "exit"
            // command.equals("exit")
            
            //Выполнение команды
            if (TODO проверить, что это слово "exit") {
                System.out.println("Выход из редактора.");
                break;
            } else if (TODO проверить, что это слово "help") {
                System.out.println("Доступные команды: load <filename>, save <filename>, insert <index> <text>, delete <index>, search <query>, help, exit");
            } else if (command.equals("load")) {
                FileHandler.loadFile(args, buffer);
            } else if (TODO проверить, что это слово "save") {
                FileHandler.saveFile(args, buffer);
            } else if (TODO проверить, что это слово "insert") {
                // ситаксис вставки insert <номер строки> <вставляемая строка>
                // разделить теперь строку аргументов на две части
                String[] insertArgs = args.TODO;
                if (insertArgs.length < 2) {
                    System.out.println("Некорректный формат. Пример: insert 0 \"Новая строка\"");
                    continue;
                }
                try {
                    // превратить в число первую часть аргументов вставки, 
                    // получить номер строки, куда необходимо вставить подстроку 
                    int index = Integer.parseInt(insertArgs[0]);
                    // использовать ранее написанный вами метод insertLine для TextBuffer
                    buffer.insertLine(index, insertArgs[1]);
                } catch (NumberFormatException e) {
                    // Если преобразоавние строки в число невозможно
                    System.out.println("Ошибка: индекс должен быть числом.");
                }
            } else if (TODO проверить, что это слово "delete") {
                // синтаксис строки удаления:  delete <номер удаляемой строки>
                try {
                    // Пребразуем аргумент в число, получим номер удаляемой строки
                    int index = Integer.parseInt(args);
                    // Удаляем строку
                    buffer.deleteLine(index);
                } catch (NumberFormatException e) {
                    // Если строку в число преобразовать нельзя
                    System.out.println("Ошибка: индекс должен быть числом.");
                }
            } else if (TODO проверить, что это слово "search") {
                // запустить поиска 
                TextSearch.searchText(buffer, args);
            } else {
                System.out.println("Неизвестная команда. Введите 'help' для списка команд.");
            }
            
            
            
        }
        scanner.close();
    }

    // Для тестирования CLI можно добавить метод main в этом же классе.
    public static void main(String[] args) {
        run();
    }
}
```
