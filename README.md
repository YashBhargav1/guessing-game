import java.util.Scanner;

public class guessingGame {
    int random;
    guessingGame(){
        random = (int) Math.ceil(Math.random()*100);
    }

    int guess(int guessNumber){
        return guessNumber-random;
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        guessingGame game = new guessingGame();
        int guess;
        int result;
        System.out.println("guess the number between the 1 - 100");
        do{
            System.out.println("guess the number:");
            guess = input.nextInt();
            result = game.guess(guess);
            if (result==0){
                System.out.println("congrats, your guess is correct");
            } else if (result<0) {
                System.out.println("please guess higher");
            }else System.out.println("please guess lower");
        }while(result!=0);
    }


}
