# Exes and Ohs

**Уровень:** 8 kyu

## Условие

Проверьте, совпадает ли количество символов «x» и «o» в строке. Метод должен возвращать логическое значение и быть нечувствительным к регистру. Строка может содержать любые символы.
Примеры ввода/вывода:

XO("ooxx") => true
XO("xooxx") => false
XO("ooxXm") => true
XO("zpzpzpp") => true // when no 'x' and 'o' is present should return true
XO("zzoo") => false

## Моё решение

public class XO {
  
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
}

## Решения других пользователей

public class XO {
  
  public static boolean getXO (String str) {

    str = str.toLowerCase();
    return str.replace("o","").length() == str.replace("x","").length();
  }
}

public class XO {
  
  public static boolean getXO (String str) {

    String xValues = str.replaceAll("[^xX]", "");
    String oValues = str.replaceAll("[^oO]", "");
    
    return xValues.length() == oValues.length();
  }
}
