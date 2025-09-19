// Program to calculate Total Marks, Average Percentage and Grade

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Step 1: Take marks input from user
        System.out.print("Enter number of subjects: ");
        int numSubjects = sc.nextInt();

        double[] marks = new double[numSubjects];

        for (int i = 0; i < numSubjects; i++) {
            System.out.print("Enter marks obtained in subject " + (i + 1) + " (out of 100): ");
            marks[i] = sc.nextDouble();
        }

        // Step 2: Calculate Total Marks
        double totalMarks = 0;
        for (double mark : marks) {
            totalMarks += mark;
        }

        // Step 3: Calculate Average Percentage
        double averagePercentage = totalMarks / numSubjects;

        // Step 4: Grade Calculation
        String grade;
        if (averagePercentage >= 90) {
            grade = "A+";
        } else if (averagePercentage >= 80) {
            grade = "A";
        } else if (averagePercentage >= 70) {
            grade = "B";
        } else if (averagePercentage >= 60) {
            grade = "C";
        } else if (averagePercentage >= 50) {
            grade = "D";
        } else {
            grade = "F";
        }

        // Step 5: Display Results
        System.out.println("\n--- Result ---");
        System.out.println("Total Marks: " + totalMarks);
        System.out.printf("Average Percentage: %.2f%%\n", averagePercentage);
        System.out.println("Grade: " + grade);

        sc.close();
    }
}
