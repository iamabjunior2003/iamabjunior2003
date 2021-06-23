import java.util.Scanner;
public class ATM_Transaction
{
    public static void main(String args[] )
    { 
        int balance = 5000, withdraw, deposit;
        Scanner s = new Scanner(System.in);
        while(true)
        {
         
            System.out.println(" Withdraw your money ");
            System.out.println(" Deposit your money ");
            System.out.println(" Check your  Balance");
            System.out.println(" EXIT ");
            System.out.print("Choose the operation you want to perform:");
            int ch = s.nextInt();
            switch(ch)
            {
                case 1:
                System.out.print("Enter money to be withdrawn:");
                withdraw = s.nextInt();
                if(balance >= withdraw)
                {
                    balance = balance - withdraw;
                    System.out.println(" collect your amount ");
                }
                else
                {
                    System.out.println("Insufficient Balance");
                }
                System.out.println("");
                break;
 
                case 2:
                System.out.print("Enter money to be deposited:");
                deposit = s.nextInt();
                balance = balance + deposit;
                System.out.println("Your Money has been successfully depsited");
                System.out.println("");
                break;
 
                case 3:
                System.out.println("Balance : "+balance);
                System.out.println("");
                break;
 
                case 4:
                System.exit(0);
            }
        }
    }
}
