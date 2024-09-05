# hm_java_2708
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        /*Task #1
        Введите 2 слова, воспользуйтесь сканером, состоящие из четного количества букв
        (проверьте количество букв в слове).
        Нужно получить слово, состоящее из первой половины первого слова
        и второй половины второго слова. распечатать на консоль.*/

        Scanner scan = new Scanner(System.in);
        System.out.println("Type first word: ");
        String wordOne = scan.nextLine();
        System.out.println("Type second word: ");
        String wordTwo = scan.nextLine();
        int wordOneFirstHalf = wordOne.length() / 2;
        int wordTwoSecondHalf = wordTwo.length() / 2;
        String firstHalf = wordOne.substring(0, wordOneFirstHalf);
        String secondHalf = wordTwo.substring(wordTwoSecondHalf);
        String newWord = firstHalf + secondHalf;
        System.out.println(newWord);

        /*Task #2
        Реализовать программу, выводящую на экран результаты:
        Сложения двух чисел
        Вычитания двух чисел
        Умножения двух чисел
        Деления двух чисел
        Каждая из арифметических операций должна быть реализована как отдельный метод.
        */
        System.out.println("Type first number: ");
        int num1 = scan.nextInt();
        System.out.println("Type second number: ");
        int num2 = scan.nextInt();

        int sum = add(num1, num2);
        int dif = substract(num1, num2);
        int mul = multiply(num1, num2);
        double div = divide(num1, num2);

        System.out.println("Сложение: " + num1 + " + " + num2 + " = " + sum);
        System.out.println("Вычитание: " + num1 + " - " + num2 + " = " + dif);
        System.out.println("Умножение: " + num1 + " * " + num2 + " = " + mul);
        System.out.println("Деление: " + num1 + " / " + num2 + " = " + div);

        /*Task #3
        Программа запрашивает у пользователя сумму в Евро для конвертации
        Реализовать метод, который конвертирует полученную сумму в сумму в долларах США
         */
        System.out.println("How many EUR to convert to USD?");
        int usd = scan.nextInt();
        double conv = convert(usd);
        System.out.println("In USD it will be " + conv + "€");

    }
    public static double convert(int a){
        return a * 0.9;
    }
    public static int add(int a, int b) {
        return a + b;
    }

    public static int substract(int a, int b) {
        return a - b;
    }

    public static int multiply(int a, int b) {
        return a * b;
    }

    public static int divide(int a, int b) {
        if (b != 0) {
            return a / b;
        } else {
            System.out.println("На ноль делить нелья");
            return 0;
        }
    }
}
