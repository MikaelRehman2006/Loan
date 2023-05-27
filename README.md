# Loan
Finds the final amount one will have to pay back after receiving a loan 

    import java.util.Scanner;
    import java.lang.Math;

    public class Loan1
    {
      private static Scanner myScanner = new Scanner(System.in); 

      public static void main(String[] args)
      {
        System.out.println("Enter a loan amount.");
        double loan = myScanner.nextDouble(); 

        System.out.println("Enter the monthly interest rate.");
        double interestRate = myScanner.nextDouble(); 

        System.out.println("Enter the number of years for which payments will be made.");
        int years = myScanner.nextInt(); 

        double topEquation = loan * interestRate;

        int power = 12 * years;

        double bottomEquation = Math.pow((1 + interestRate), years);

        double monthlyPayment = topEquation / (1 - (1 / bottomEquation));

        double totalPayment = monthlyPayment * years * 12;

        System.out.println(totalPayment);





      }

    }
