# Input-Calculator
This program reads input (int) from the keyboard and returns the sum and average when an invalid number is received. 

import java.util.Scanner;

public class Exercises {

    public static void main(String[] args) {
       inputThenPrintSumAndAverage();
    }

    public static void inputThenPrintSumAndAverage(){
        Scanner scanner = new Scanner(System.in);
        double sum = 0;
        int count = 0;

        while(true){
            boolean hasAnInt = scanner.hasNextInt();
            if(hasAnInt) {
                int input = scanner.nextInt();
                sum += input;
                count += 1;
            } else{
                break;
            }
            scanner.nextLine(); // handle inputs
        }
        System.out.println("SUM = " + (long)sum + " AVG = "  + Math.round(sum / count));
        scanner.close();
    }
}

