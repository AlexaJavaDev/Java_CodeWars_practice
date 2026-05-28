# Find the smallest and biggest integer in the array

**Уровень:** 8 kyu

## Условие

В этом небольшом задании вам дана последовательность чисел, разделенных пробелами, и вы должны найти наибольшее и наименьшее из них.

Примеры
highAndLow("1 2 3 4 5") // return "5 1"
highAndLow("1 2 -3 4 5") // return "5 -3"
highAndLow("1 9 3 4 -5") // return "9 -5"
Примечания
Все числа действительны Int32, подтверждать их не нужно .
Во входной строке всегда будет как минимум одно число.
Выходная строка должна состоять из двух чисел, разделенных одним пробелом, причем наибольшее число должно быть первым.

## Моё решение
```java
public static String highAndLow(String numbers) {
  
    String[] str = numbers.split(" ");
    
    int max = Integer.parseInt(str[0]);
    int min = Integer.parseInt(str[0]);
    
    for (int i = 0; i < str.length; i++) {
      int num = Integer.parseInt(str[i]);
    if (num > max) {
      max = num;
    }
      if (num < min) {
        min = num;
      }
    }
    return max + " " + min;
  }
```
