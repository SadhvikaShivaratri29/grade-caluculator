# grade-caluculator
import java.util.Scanner;

public class StudentGradeCalculator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input marks for three subjects
        System.out.println("Enter marks for Subject 1: ");
        double subject1 = scanner.nextDouble();

        System.out.println("Enter marks for Subject 2: ");
        double subject2 = scanner.nextDouble();

        System.out.println("Enter marks for Subject 3: ");
        double subject3 = scanner.nextDouble();

        // Calculate total marks
        double totalMarks = subject1 + subject2 + subject3;

        // Calculate average percentage
        double averagePercentage = totalMarks / 3;

        // Determine grade based on average percentage
        char grade;
        if (averagePercentage >= 90) {
            grade = 'A';
        } else if (averagePercentage >= 80) {
            grade = 'B';
        } else if (averagePercentage >= 70) {
            grade = 'C';
        } else if (averagePercentage >= 60) {
            grade = 'D';
        } else if (averagePercentage >= 50) {
            grade = 'E';
        } else {
            grade = 'F'; // Fail
        }

        // Display results
        System.out.println("\nTotal Marks: " + totalMarks);
        System.out.println("Average Percentage: " + averagePercentage + "%");
        System.out.println("Grade: " + grade);

        scanner.close();
    }
}
