# task1
import java.util.Random;
import java.util.Scanner;

public class numberGame1 {
        static int userInput;
	int Number=0;
	static int attempts = 0;
         void myMethod(){
            
           Random chance = new Random();
           Number = chance.nextInt(100);
        
            Scanner scanner = new Scanner(System.in);

            System.out.println("Welcome to the Number Guessing Game!");
            System.out.println(" Guess a number between 1 to 100: ");

            do {
                System.out.print("Enter your guess: ");
                 userInput = scanner.nextInt();
                 attempts++;
	           if(attempts == 5){
		        System.out.println("your turn is over");
		        System.out.println("you want play again! for yes type 121:");
		        break;
               }	

                if (userInput == Number) {
                System.out.println("Guessed is correct"+" " + attempts + " attempts.");
              } else if (userInput < Number) {
                System.out.println("Too low! Try again.");
              } else {
                System.out.println("Too high! Try again.");
              }

           } while(userInput != Number);
        } public static void main(String[] args) {
          numberGame1 obj=new numberGame1();
          obj.myMethod();
	  Scanner scanner = new Scanner(System.in);
	  userInput=scanner.nextInt();
            boolean isCondition=(userInput==121);
           if(isCondition){
               obj.myMethod();
           }
    }
}
