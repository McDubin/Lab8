# Lab8

package abdellmelkjlab7;

/*My words and actions will reflect Academic Integrity.
I will not cheat or lie or steal in academic matters.
I will promote integrity in the UNCG community.
John Abdellmelk 10/27/2021
 */
//Lab Seven

/*
    John Abdellmelk 
    CSC 130, Sec 1
 */
import java.util.Scanner;

public class AbdellmelkJLab7 {

    static final double PI = 3.14159;
    static Scanner input;

    public static void squareArea() {
        System.out.print("What is the length of one side of the square? ");

        int side = input.nextInt();
        double area = side * side;
        System.out.printf("The area of the square is %.2f\n", area);
    }

    public static void rectangleArea() {
        System.out.print("What is the length of the rectangle? ");
        double length = input.nextDouble();
        System.out.print("What is the width of the rectangle? ");
        double width = input.nextDouble();
        double area = width * length;
        System.out.printf("The area of the rectangle is %.2f\n ", area);

    }

    public static void circleArea() {
        System.out.print("What is the radius of the circle? ");
        int radius = input.nextInt();
        double area = radius * radius * PI;
        System.out.printf("The area of the circle is %.2f\n ", area);
    }

    public static void main(String[] args) {
        int choice = 0;

        input = new Scanner(System.in);

        System.out.println("Lab Seven\nJohn Abdellmelk\nCSC 130, Sec 1\n");

        System.out.println("This program will show the user a menu that allows him to have\n"
                + " the program calculate the area of a square, rectangle, or circle.");
        System.out.println("The menu is in a loop so the user may use it as often as he wishes.");
        System.out.println("The code for the calculations is in methods called by main.");
        System.out.println(" ");

        do {
            System.out.println("************************* Menu *************************");
            System.out.println("1. Square");
            System.out.println("2. Rectangle");
            System.out.println("3. Circle");
            System.out.println("4. Quit the program");
            System.out.println("********************************************************");
            System.out.println(" ");

            System.out.print("Please make your choice from the menu: ");

            do {
                choice = input.nextInt();

                switch (choice) {
                    case 1:
                        squareArea();
                        break;
                    case 2:
                        rectangleArea();
                        break;
                    case 3:
                        circleArea();
                        break;
                    case 4:
                        break;
                    default:
                        System.out.print("Invalid choice, Please select 1, 2, 3, or 4. ");

                }
            } while (choice < 1 || choice > 4);

        } while (choice != 4);
        System.out.printf("\nThank you for using my program!");
    }
}
