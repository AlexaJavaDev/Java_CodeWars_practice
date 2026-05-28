# Exes and Ohs

**Уровень:** 8 kyu

## Условие

Проверьте, совпадает ли количество символов «x» и «o» в строке.  
Метод должен возвращать логическое значение и быть нечувствительным к регистру.  
Строка может содержать любые символы.  
Примеры ввода/вывода:

XO("xoxoxo") => true - равное количество Х и О  
XO("xooxx") => false - неравное количество Х и О  
XO("ooxXm") => true - равное  
XO("zpzpzpp") => true - если нету ни Х ни О тоже возвращает true  
XO("zzoo") => false - не равное  

## Моё решение
```java
  public static boolean getXO (String str) {

    String s = str.toLowerCase();
    int countX = 0;
    int countO = 0;
    
    for (int i = 0; i < s.length(); i++) {
    if (s.charAt(i) == 'x') {
      countX++;
    }
    if (s.charAt(i) == 'o') {
      countO++;
    }
  }
    return countX == countO;
 }
```

## Решения других пользователей
```java
public static boolean getXO (String str) {

    str = str.toLowerCase();
    return str.replace("o","").length() == str.replace("x","").length();
  }
```
или
```java
public static boolean getXO (String str) {

    String xValues = str.replaceAll("[^xX]", "");
    String oValues = str.replaceAll("[^oO]", "");
    
    return xValues.length() == oValues.length();
  }
```
