//MODULAR CALCULATOR
//Assignment for Comprog2, Mrs. Grachel Greta

import java.util.Scanner;

public class CalcComp22 {

    public static double add(double a, double b) {
        return a + b;
    }

    public static double subtract(double a, double b) {
        return a - b;
    }

    public static double multiply(double a, double b) {
        return a * b;
    }

    public static double divide(double a, double b) {
        return a / b;
    }

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        int choice;
        double num1, num2, result;

        do {
            System.out.println("\n===CALCULATOR===");
            System.out.println("1. Addition");
            System.out.println("2. Subtraction");
            System.out.println("3. Multiplication");
            System.out.println("4. Division");
            System.out.println("5. EXIT");
            System.out.print("CHOOSE AN OPTION: ");

            choice = input.nextInt();

            if (choice >= 1 && choice <= 4) {

                System.out.print("Enter first Number: ");
                num1 = input.nextDouble();

                System.out.print("Enter Second Number: ");
                num2 = input.nextDouble();

                switch (choice) {
                    case 1:
                        result = add(num1, num2);
                        System.out.println("Result: " + result);
                        break;
                    case 2:
                        result = subtract(num1, num2);
                        System.out.println("Result: " + result);
                        break;
                    case 3:
                        result = multiply(num1, num2);
                        System.out.println("Result: " + result);
                        break;
                    case 4:
                        if (num2 == 0) {
                            System.out.println("Error! Cannot be divided by Zero.");
                        } else {
                            result = divide(num1, num2);
                            System.out.println("Result: " + result);
                        }   break;
                    default:
                        break;
                }
            }

        } while (choice != 5);

        System.out.println("Calc closed!");
    }
}
