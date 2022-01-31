# BMI-Calculator
This is a code for calculating BMI (Body Mass Index) in JAVA.

import java.util.Scanner;
public class BMICalculate {
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);

        //Prompts the user to enter weight in pounds
        System.out.print("Enter weight in pounds: ");
        double weight = input.nextDouble();

        //Prompts the user to enter height in inches
        System.out.print("Enter height in inches: ");
        double height = input.nextDouble();

        final double KILOGRAMS_PER_POUND = 0.45359237;  //Constant
        final double METERS_PER_INCH = 0.0254; //constant

        //Compute the BMI
        double weightInKilogram = weight * KILOGRAMS_PER_POUND;
        double heightInMeters = height * METERS_PER_INCH;
        double bmi = weightInKilogram / (heightInMeters * heightInMeters);

        //Displaying the results
        System.out.println(" BMI is " + bmi);
        if (bmi < 18.5)
            System.out.println("Underweight");
        else if (bmi < 25)
            System.out.println("Normal");
        else if (bmi < 30)
            System.out.println("Overweight");
        else
            System.out.println("Obese");


    }
}
