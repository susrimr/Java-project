import java.util.Scanner;

public class SimpleMIS {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String information = "";
        float balance =0;
        while (true) {
            clearConsole();


            System.out.println("Welcome to Beginner MIS!");
            System.out.println("1. Add Information");
            System.out.println("2. View Information");
            System.out.println("3. Update Information");
            System.out.println("4. Delete Information");
            System.out.println("5. Transaction");
            System.out.println("6. Exit");




            System.out.print("Please enter your choice (1-6): ");
            int choice = scanner.nextInt();


            switch (choice) {
                case 1:

                    System.out.print("Enter new information: ");
                    scanner.nextLine();
                    information = scanner.nextLine();
                    System.out.println("Information added successfully!");
                    break;
                case 2:

                    System.out.println("Information: " + information);
                    break;
                case 3:

                    System.out.print("Enter updated information: ");
                    scanner.nextLine();
                    information = scanner.nextLine();
                    System.out.println("Information updated successfully!");
                    break;
                case 4:

                    information = "";
                    System.out.println("Information deleted.");
                    break;
                case 5:

                    System.out.print("Enter transaction amount (positive for deposit, negative for withdrawal): ");
                    double transactionAmount = scanner.nextDouble();
                    balance += transactionAmount;
                    System.out.println("Transaction completed. Current balance: " + balance);
                    break;
                case 6:

                    System.out.println("Exiting...");
                    scanner.close();
                    System.exit(0);
                default:
                    // Handle invalid choices
                    System.out.println("Invalid choice! Please enter number between (1-6");

            }
        }
    }

    private static void clearConsole() {
        for (int i = 0; i < 50; i++) {
            System.out.println();
        }
    }
}
