import java.util.Scanner;


public class Main {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Enter number of students: ");
        int students = input.nextInt();
        //store marks in an array
        int[] marksArr = new int[students];

        for (int i = 0; i < students; i++) {
            System.out.print("Enter marks " + (i + 1)+": ");
            marksArr[i] = input.nextInt();


        }
        //print results
        System.out.print("Original marks entered: ");
        for (int i =0; i < students; i++) {
            System.out.print(marksArr[i] + " ");
        }

       //Ascending order
        // for desc you just change sign in if statement to >
        int oder = 0;
        for (int i = 0; i < students; i++) {
            for (int j = i + 1; j < students; j++) {
               if (marksArr[j] < marksArr[i]) {
                   oder = marksArr[i];
                   marksArr[i] = marksArr[j];
                   marksArr[j] = oder;

              }

            }
        }
        //print
        System.out.println(" ");
        System.out.print("marks in ascending: ");
        for (int i = 0; i < students; i++) {
            System.out.print(marksArr[i] + " ");
        }
    }
}
