import java.util.Scanner;

public class MinElementFinder {

    public static int[] readIntegers(int count) {
        int[] array = new int[count];
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter " + count + " integers:");

        for (int i = 0; i < count; i++) {
            array[i] = scanner.nextInt();
        }

        return array;
    }

    public static int findMin(int[] array) {
        int min = Integer.MAX_VALUE;
        for (int value : array) {
            if (value < min) {
                min = value;
            }
        }
        return min;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the number of integers: ");
        int count = scanner.nextInt();

        int[] integers = readIntegers(count);
        int min = findMin(integers);

        System.out.println("Minimum value in the array is: " + min);
    }
}# Ch2
