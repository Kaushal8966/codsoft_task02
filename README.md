# codsoft_task02
#student grade calculator
import java.util.Scanner;

class StudentGrade {
    public String grade(int avg) {
        switch (avg / 10) {
            case 10:
            case 9:
                return "A+";
            case 8:
                return "A";
            case 7:
                return "B+";
            case 6:
                return "B";
            case 5:
                return "C";
            default:
                return "F";
        }
    }


//public class Main {
    public static void main(String[] args) {
        StudentGrade G = new StudentGrade();
        Scanner sc = new Scanner(System.in);

        // Taking input
        System.out.println("Enter the amount of Subjects:");
        int totalSubject = sc.nextInt();
        int totalmarks = 0;

        for (int i = 0; i < totalSubject; i++) {
            System.out.println("Enter the marks obtained in subject " + (i + 1) + ":");
            int marks = sc.nextInt();
            totalmarks += marks;
        }

        // Calculating Percentage
        int avg = totalmarks / totalSubject;

        // Calculating Grade
        String studentGrade = G.grade(avg);

        // Displaying all the data
        System.out.println("Total marks obtained: " + totalmarks);
        System.out.println("Percentage obtained: " + avg + "%");
        System.out.println("Grade obtained: " + studentGrade);

        sc.close();
    }
}
