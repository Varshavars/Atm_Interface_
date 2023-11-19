import java.util.*;
public class numgame
{
    public static void main(String [] args)
    {
        Random rd = new Random();
        int compnum = rd.nextInt(100);
        Scanner sc = new Scanner(System.in);
        int i=0;
        System.out.println("NUMBER GAME (GUESS THE NUMBER BETWEEN (1-100)-YOU HAVE 10 CHANCES)");
        while(true)
        {
            System.out.print("Guess the number:");
            int usernum=sc.nextInt();
            if(compnum==usernum)
            {
                System.out.println("Awesome! You guessed it correctly");
                System.out.println("Do you want to play again? (0/1)");
                int n = sc.nextInt();
                if(n==1)
                {
                    compnum = rd.nextInt(100);
                    i=0;
                }
                else
                {
                    System.out.println("Game Exited.");
                    break;
                }
            }
            else if (compnum>usernum)
            {
                System.out.println("Think of a bigger number");
                System.out.println("You have "+(10-i-1)+" more chances left.");
            }
            else
            {
                System.out.println("Think of a smaller number.");
                System.out.println("You have "+(10-i-1)+" more chances left.");
            }
            i++;
            if(i==10)
            {
                System.out.println("You lost! The number is "+compnum);
                System.out.println("Do you want to play again? (0/1)");
                int n = sc.nextInt();
                if(n==1)
                {
                    compnum = rd.nextInt(100);
                    i=0;
                }
                else
                {
                System.out.println("Game Exited.");
                break;
            }
        }
    }

    }
}
