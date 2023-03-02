# kata.academy-Java


## 1.         
### Java для начинающих. Урок 2: Переменные. Примитивные типы данных.

```
public class Main {
    public static void main(String[] args) {
        //целые числа (byte, short, int, long)
        int myInt;
        myInt = 1347;
        System.out.println(myInt);
        short myShort = 3266;
        long myLong = 26246246;
        byte myByte = 100;

        //числа с плавающей точкой (float, double);
        double myDouble = 235.35;
        float myFloat = 2362.4f;
        //логический (boolean);
        boolean b = true;
        //символьный (char).
        char c = 'a';
    }
}
```
### Java для начинающих. Методы в Java            



```
public class Main {
    public static void main(String[] args) {
        Person person1 = new Person();
        person1.name = "валера";
        person1.age = 50;
        person1.speak();
        Person person2 = new Person();
        person2.name = "vova";
        person2.age = 20;
        person1.sayHello();
    }
}
class Person {
    String name;
    int age;
    void speak() {
        for (int i = 0; i < 3; i++) {
            System.out.println("Меня зовут " + name + " Мне " + age + " лет");
        }
    }
    void sayHello() {
        System.out.println("Привет! ");
    }
}
//Меня зовут валера Мне 50 лет
//Меня зовут валера Мне 50 лет
//Меня зовут валера Мне 50 лет
//Привет! 
```

### Java для начинающих. Тип возвращаемого значения метода

Void - пустота.
После return нет смысла ничего писать.

```
public class Main {
    public static void main(String[] args) {
        Person person1 = new Person();
        person1.name = "валера";
        person1.age = 50;
        Person person2 = new Person();
        person2.name = "vova";
        person2.age = 20;
        int year1 = person1.calculateYearsToRetirement();
        int year2 = person2.calculateYearsToRetirement();
        System.out.println("первому челу до пенсии "+year1+" лет");
        System.out.println("первому челу до пенсии "+year2+" лет");
    }
}
class Person {
    String name;
    int age;
    int calculateYearsToRetirement(){
        int years = 65-age;
        return years;
    }
    void speak() {
        for (int i = 0; i < 3; i++) {
            System.out.println("Меня зовут " + name + " Мне " + age + " лет");
        }
    }
    void sayHello() {
        System.out.println("Привет! ");
    }
}
//первому челу до пенсии 15 лет
//первому челу до пенсии 45 лет
```

## 2. Арифметические операции в Java
### Java для начинающих. Арифметические операции

![alt!](/src/8888.jpg)
Пример
```
package com.company;

public  class Main {
    public static void main(String[] args) {
        int a=5, b=7;
        int c=a+b;
System.out.println(c);

    }
}
//12
```
Ещё пример       
```
package com.company;

public  class Main {
    public static void main(String[] args) {
        int a=5, b=7;
        int c=a+b;

        short d = (short)(c+5+a+7);
System.out.println(d);

    }
}
//29
```
пример с мусором float      
```
package com.company;

public  class Main {
    public static void main(String[] args) {
        float a=5.8f, b=7.6f;
        double c=a-b;

        short d = (short)(c+5+a+7);
System.out.println(c);

    }
}
//-1.799999713897705
```
и целочисленный       
```
package com.company;

public  class Main {
    public static void main(String[] args) {
        float a=5.8f, b=7.6f;
        double c=a-b;
        int d = (int)a-(int)b;
System.out.println(d);

    }
}
//-2
```
пример
```
package com.company;

public  class Main {
    public static void main(String[] args) {
        float a=5.8f, b=7.6f;
        double c=a-b;
        int d = (int)(a-b);
System.out.println(d);

    }
}
//-1
```
(int) может отбросить дробную часть 
```
package com.company;

public  class Main {
    public static void main(String[] args) {
        float a=5.8f, b=7.6f;
        double c=3*a;
        int d = (int)(3*a);
System.out.println(d);

    }
}
//17
```
Программа для вычисления сторон прямоугольника.
```
package com.company;

import java.util.Scanner;

public  class Main {
    public static void main(String[] args) {
        double a, b;
        Scanner in = new Scanner(System.in);
System.out.print("a = "); a = in.nextDouble();
System.out.print("b = "); b = in.nextDouble();

double p = 2*(a+b);

System.out.println(p);
in.close();

    }
}
//a = 5,4
//b = 6,7
//24.200000000000003
```
Деление
```
public  class Main {
    public static void main(String[] args) {
        int a = 7;
        int b = 2;

        double c = a / b;

        System.out.println(c);
    }
}
//3.0
```
Деление с дробью
```
package com.company;

import java.util.Scanner;

public  class Main {
    public static void main(String[] args) {
        int a = 7;
        int b = 2;

        double c = (double) a / b;

        System.out.println(c);
    }
}
//3.5
```
ещё пример деления
```package com.company;

import java.util.Scanner;

public  class Main {
    public static void main(String[] args) {

        float d = 7/2;

        System.out.println(d);
    }
}
//3.0
```
```
package com.company;

import java.util.Scanner;

public  class Main {
    public static void main(String[] args) {

        float d = 7.0f/2;

        System.out.println(d);
    }
}
//3.5
```
```
package com.company;

import java.util.Scanner;

public  class Main {
    public static void main(String[] args) {

        float d = (float) 7/2;

        System.out.println(d);
    }
}
//3.5
```
![alt!](/src/777.jpg)

## 3. Класс String, работа со строками. Преобразование строки в число
### Строки(String). Ссылочные типы данных
```
package com.company;

import java.util.Scanner;

public  class Main {
    public static void main(String[] args) {

        int x =5;
        String s = "hello";
        String space = " ";
        String name = "Bob ";
        System.out.println(s+space+name);
        System.out.println("HeLLO"+space+"John");
        System.out.println(s+space+" 1347 "+name+x);
    }
}
//hello Bob 
//HeLLO John
//hello  1347 Bob 5
```
### Класс String и его методы

Основные операции со строками раскрывается через методы класса String, среди которых можно выделить следующие:   
  
concat(): объединяет строки   

valueOf(): преобразует объект в строковый вид   

join(): соединяет строки с учетом разделителя   
 
сompareTo(): сравнивает две строки   

charAt(): возвращает символ строки по индексу  

getChars(): возвращает группу символов   

equals(): сравнивает строки с учетом регистра   

equalsIgnoreCase(): сравнивает строки без учета регистра   

regionMatches(): сравнивает подстроки в строках   

indexOf(): находит индекс первого вхождения подстроки в строку   

lastIndexOf(): находит индекс последнего вхождения подстроки в строку   

startsWith(): определяет, начинается ли строка с подстроки   

endsWith(): определяет, заканчивается ли строка на определенную подстроку   

replace(): заменяет в строке одну подстроку на другую   

trim(): удаляет начальные и конечные пробелы    

substring(): возвращает подстроку, начиная с определенного индекса до конца или до определенного индекса   

toLowerCase(): переводит все символы строки в нижний регистр   

toUpperCase(): переводит все символы строки в верхний регистр    

Пример
```
    public static void main(String[] args) {


        String str1 = new String("hello ");
        String str2 = "hello";
        System.out.println(str1.concat(str2));
    }
}
//hello hello
```
[Подробнее..](https://metanit.com/java/tutorial/7.1.php).
## 4. Циклы в Java, работа с массивами

## Массивы в Java
```
package com.company;

import java.util.Scanner;

public  class Main {
    public static void main(String[] args) {

        int number = 10; // примитивынй тип данных //[10]
        int[] numbers = new int[5];
        for(int i = 0; i<numbers.length; i++){
            numbers[i]=i*10;
            System.out.println(numbers[i]);
        }
        System.out.println();
        int[] numbers1 = {1,2,3};
        for (int i = 0; i<numbers1.length; i++){
            System.out.println(numbers1[i]);
        }
    }
}
//0
//10
//20
//30
//40
//
//1
//2
//3
```

## Цикл for each, Массивы строк
```
package com.company;

import java.util.Scanner;

public  class Main {
    public static void main(String[] args) {

        int number = 10; // примитивынй тип данных //[10]
        int[] numbers = new int[5];
        String[] strings = new String[3];
        strings[0] = " privet1 ";
        strings[1] = " privet2 ";
        strings[2] = " privet3 ";
        for(int i = 0; i<strings.length; i++){
            System.out.println(numbers[i]);
        }
        System.out.println();

        for (String string:strings){
            System.out.println(string);
        }
        int[] numbers1 = {1,2,3};
        int sum = 0;
        for (int x:numbers1){
            sum = sum+x;
        }
        System.out.println();
        System.out.println(sum);

        int value = 0;
        String s = null;
        System.out.println(s);
    }
}
//0
//0
//0
//
// privet1 
// privet2 
// privet3 
//
//6
//null
//
//Process finished with exit code 0

```
## Методы в Java
```
public class Main {
    public static void main(String[] args) {
        Person person1 = new Person();
        person1.name = "валера";
        person1.age = 50;
        person1.speak();
        Person person2 = new Person();
        person2.name = "vova";
        person2.age = 20;
        person1.sayHello();
    }
}
class Person {
    String name;
    int age;
    void speak() {
        for (int i = 0; i < 3; i++) {
            System.out.println("Меня зовут " + name + " Мне " + age + " лет");
        }
    }
    void sayHello() {
        System.out.println("Привет! ");
    }
}
//Меня зовут валера Мне 50 лет
//Меня зовут валера Мне 50 лет
//Меня зовут валера Мне 50 лет
//Привет! 
```


## Тип возвращаемого значения метода


Void - пустота.
После return нет смысла ничего писать.

public class Main {
    public static void main(String[] args) {
        Person person1 = new Person();
        person1.name = "валера";
        person1.age = 50;
        Person person2 = new Person();
        person2.name = "vova";
        person2.age = 20;
        int year1 = person1.calculateYearsToRetirement();
        int year2 = person2.calculateYearsToRetirement();
        System.out.println("первому челу до пенсии "+year1+" лет");
        System.out.println("первому челу до пенсии "+year2+" лет");
    }
}
class Person {
    String name;
    int age;
    int calculateYearsToRetirement(){
        int years = 65-age;
        return years;
    }
    void speak() {
        for (int i = 0; i < 3; i++) {
            System.out.println("Меня зовут " + name + " Мне " + age + " лет");
        }
    }
    void sayHello() {
        System.out.println("Привет! ");
    }
}
//первому челу до пенсии 15 лет
//первому челу до пенсии 45 лет



## Параметры метода
```
public class Main {
    public static void main(String[] args) {
        Person person1 = new Person();
        person1.setNameAndAge("Roman",20);
        String s1 = "vova";
        Person person2 = new Person();
        person2.setNameAndAge(s1,30);

        person1.speak();
        person2.speak();
    }
}
class Person {
    String name;
    int age;

    void setNameAndAge(String username, int userage){
        name = username;
        age = userage;
    }
    
    void speak() {
        for (int i = 0; i < 3; i++) {
            System.out.println("Меня зовут " + name + " Мне " + age + " лет");
        }
    }
}
//Меня зовут Roman Мне 20 лет
//Меня зовут Roman Мне 20 лет
//Меня зовут Roman Мне 20 лет
//Меня зовут vova Мне 30 лет
//Меня зовут vova Мне 30 лет
//Меня зовут vova Мне 30 лет
```

## 5. Логические операторы       

### Логическое И, ИЛИ, НЕТ   

```
public class Main {
    public static void main(String[] args) {

        int a = 5;
        int b = 9;
        boolean bool = false;
        if (!(a == b) || bool) {
            System.out.println("yru bro!");

        }
    }
}
//yru bro!
```
## 6. Условные операторы, сравнение, switch case   
### Условный оператор if     
 ```
 public class Main {
    public static void main(String[] args) {

        int a = 11;
        if(a<10){
            System.out.println("yes bro!");
        }else if (a<20) {
            System.out.println("no bro!");

        }
    }
}
//no bro!
```
### Оператор switch    
Тоже самое можно записать и со String,
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("скок лет ?");
        int age = scanner.nextInt();
        switch (age){
            case 0 :
                System.out.println("c dr");
                break;
            case 7 :
                System.out.println("scool");
                break;
            case 18:
                System.out.println("nah");
                break;
            default:
                System.out.println("ti lox");
        }
    }
}
//скок лет ?
//7
//scool
```

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("скок лет ?");
        String age = scanner.nextLine();
        switch (age){
            case "v" :
                System.out.println("c dr");
                break;
            case "l" :
                System.out.println("scool");
                break;
            case "a":
                System.out.println("nah");
                break;
            default:
                System.out.println("ti lox");
        }
    }
}
//скок лет ?
//a
//nah
```

## 7. Класс Enum    
### Enum (Перечисления)    
Main.java
```
public class Main {
    public static void main(String[] args) {
        Animal animal = Animal.CAT;

        switch (animal) {
            case CAT :
                System.out.println("it's a cat");
                break;
            case DOG :
                System.out.println("it's a dog");
                break;
            case FROG :
                System.out.println("it's a frog");
                break;
        }
    }
}
//it's a cat
```
enum Animal.java
```
public enum Animal {
    DOG, CAT, FROG
}

```

Пример
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Animal animal = Animal.CAT;
        System.out.println(animal.toString());

//        switch (animal) {
//            case CAT :
//                System.out.println("it's a cat");
//                break;
//            case DOG :
//                System.out.println("it's a dog");
//                break;
//            case FROG :
//                System.out.println("it's a frog");
//                break;
//        }
    }
}
//CAT

public enum Animal {
    DOG("собака"), CAT("кошк"), FROG("ляга");

    private String translation;

    Animal(String translation) {
        this.translation = translation;
    }
    public String getTranslation() {
        return translation;
    }
//    public String toString() {
//        return "Перевод "+ translation;
//    }
}
```

вызов с переводом
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Animal animal = Animal.CAT;
        System.out.println(animal);

//        switch (animal) {
//            case CAT :
//                System.out.println("it's a cat");
//                break;
//            case DOG :
//                System.out.println("it's a dog");
//                break;
//            case FROG :
//                System.out.println("it's a frog");
//                break;
//        }
    }
}
//Перевод кошк

public enum Animal {
    DOG("собака"), CAT("кошк"), FROG("ляга");

    private String translation;

    Animal(String translation) {
        this.translation = translation;
    }
    public String getTranslation() {
        return translation;
    }
   public String toString() {
        return "Перевод "+ translation;
    }
}
```
Метод Name

```
public class Main {
    public static void main(String[] args) {
        Seasons seasons = Seasons.SUMMER;
        System.out.println(seasons.name());

    }
}
//SUMMER

public enum Seasons {
    SUMMER(35),WINTER(-20), AUTUMN(10);
    private int temperature;

    Seasons(int temperature) {
        this.temperature = temperature;
    }

    public int getTemperature() {
        return temperature;
    }
}
```
![alt!](/src/1347.png)

## 8. Работа с исключениями в Java
### Исключения (часть 1). Обработка исключений
1 метод обработки исключений.
```
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) throws FileNotFoundException {
       File file =new File("asdf");

       Scanner scanner = new Scanner(file);

    }
}
//at Main.main(Main.java:9)
```
2 метод 
```
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) throws FileNotFoundException {
       File file =new File("asdf");

        try {
            Scanner scanner = new Scanner(file);
        } catch (FileNotFoundException e) {
            System.out.println("Файл не найден");
        }
    }
}
//Файл не найден
```
А теперь создадим asdf и запустим обработку исключений
```
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) throws FileNotFoundException {
       File file = new File("asdf");

        try {
            Scanner scanner = new Scanner(file);

            System.out.println("posle scanera");
        } catch (FileNotFoundException e) {
            System.out.println("Файл не найден");
        }
        System.out.println("Kek");
    }
}
//posle scanera
//Kek
```
Обработка существуещего файла ничего не выведет а вот не существуещего 
```
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        try {
            readFile();
        } catch (FileNotFoundException e) {
            System.out.println("нету");
        }
    }
        public static void readFile() throws FileNotFoundException {
            File file = new File("qwer");
            Scanner scanner = new Scanner(file);
        }
    }

//нету
```


### Исключения (часть 2). Выбрасывание исключений

[Всё исключения Exception](https://docs.oracle.com/en/java/javase/16/docs/api/java.base/java/lang/Exception.html).

IOException
```

import java.io.IOException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) throws IOException {
    Scanner scanner = new Scanner(System.in);
    while (true){
        int x = Integer.parseInt(scanner.nextLine());

        if(x != 0) {
            throw new IOException();
        }
    }
        }
    }

//0
//0
//5
//Exception in thread "main" java.io.IOException
//	at Main.main(Main.java:13)
```
0 всё норм а при вводе 5 выводит ошибку.  



Создадим своё исключение, создаём класс ScannerException.
Вводим туда
```
public class ScannerException extends Exception {
    public  ScannerException(String description) {
        super(description);
    }
}
```
```
import java.io.IOException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) throws ScannerException {
    Scanner scanner = new Scanner(System.in);
    while (true){
        int x = Integer.parseInt(scanner.nextLine());

        if(x != 0) {
            throw new ScannerException("dasdasd");
        }
    }
        }
    }

//0  
//0
//1
//Exception in thread "main" ScannerException: dasdasd
//	at Main.main(Main.java:12)
```


### Исключения (часть 3). Checked и Unchecked исключения

Checked Exception(Compile time exception) = Исключительные случаи в работе программы(как в прошлых уроках).     

Unchecked (Runtime exception) = ошибка в работе программы      
например
```
int[] arr = new int[2]
  System.out.println(arr[3]);
```
или деление на ноль.
---
### Исключения (часть 4)

Можем работать с разными исключениеми и разными catch блоками.
