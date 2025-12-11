# CodSoft-Internship-Task-4
import java.util.Scanner;
public class CurrencyConverter {
    
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);

        // Simple fixed rates (example values)
        double usdToInr = 83.12;
        double eurToInr = 89.45;
        double gbpToInr = 104.50;
        double inrToUsd = 1 / usdToInr;
        double inrToEur = 1 / eurToInr;
        double inrToGbp = 1 / gbpToInr;

        System.out.println("====================================");
        System.out.println("        SIMPLE CURRENCY CONVERTER   ");
        System.out.println("====================================");
        System.out.println("1. USD → INR");
        System.out.println("2. EUR → INR");
        System.out.println("3. GBP → INR");
        System.out.println("4. INR → USD");
        System.out.println("5. INR → EUR");
        System.out.println("6. INR → GBP");
        System.out.println("------------------------------------");
        System.out.print("Choose an option (1-6): ");
        
        int choice = sc.nextInt();

        System.out.print("Enter amount: ");
        double amount = sc.nextDouble();

        double result = 0.0;
        String message = "";

        switch (choice) {
            case 1:
                result = amount * usdToInr;
                message = amount + " USD = " + result + " INR";
                break;

            case 2:
                result = amount * eurToInr;
                message = amount + " EUR = " + result + " INR";
                break;

            case 3:
                result = amount * gbpToInr;
                message = amount + " GBP = " + result + " INR";
                break;

            case 4:
                result = amount * inrToUsd;
                message = amount + " INR = " + result + " USD";
                break;

            case 5:
                result = amount * inrToEur;
                message = amount + " INR = " + result + " EUR";
                break;

            case 6:
                result = amount * inrToGbp;
                message = amount + " INR = " + result + " GBP";
                break;

            default:
                message = "Invalid choice. Please restart and try again.";
        }

        System.out.println("------------------------------------");
        System.out.println(message);
        System.out.println("====================================");

        sc.close();
    }
}
