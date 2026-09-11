# Simple-Calculator
it's an simple java code for a calculator to solve mathematical calculations easily. 

```java
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        int choice;

        System.out.println("===== SIMPLE CALCULATOR =====");

        do {
            System.out.println("\n1. Addition");
            System.out.println("2. Subtraction");
            System.out.println("3. Multiplication");
            System.out.println("4. Division");
            System.out.println("5. Exit");

            System.out.print("Enter your choice: ");
            choice = sc.nextInt();

            if (choice >= 1 && choice <= 4) {

                System.out.print("Enter first number: ");
                double num1 = sc.nextDouble();

                System.out.print("Enter second number: ");
                double num2 = sc.nextDouble();

                double result = 0;

                switch (choice) {
                    case 1:
                        result = num1 + num2;
                        break;

                    case 2:
                        result = num1 - num2;
                        break;

                    case 3:
                        result = num1 * num2;
                        break;

                    case 4:
                        if (num2 == 0) {
                            System.out.println("Error: Cannot divide by zero.");
                            continue;
                        }
                        result = num1 / num2;
                        break;
                }

                System.out.println("Result = " + result);

            } else if (choice == 5) {
                System.out.println("Thank you for using the calculator!");

            } else {
                System.out.println("Invalid choice. Please try again.");
            }

        } while (choice != 5);

        sc.close();
    }
}
```

### What's better in this version?

* **Menu system** makes it easier to use.
* **Loop** lets you perform calculations repeatedly.
* **Exit option** allows the user to stop the program.
* **Division-by-zero protection** prevents errors.
* Still uses basic Java concepts like `Scanner`, `switch`, `if`, and `do-while`, so it's good for a beginner.
