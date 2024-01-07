2024/01/06 JAVA

# Method overloading converting cemtimeters


public class Main {
    
    public static void main(String[] args) {
        //
        System.out.println("5ft, 8in = " + convertToCentimeters(5, 8) + "cm");
        System.out.println("68in = " + convertToCentimeters(68) + "cm");
    }
    // 두개의 똑같은 method를 쓸수있음
    public static double convertToCentimeters(int inches) {

        return inches * 2.54;
    }

    public static double convertToCentimeters(int feet, int inches) {
        // return ((feet * 12) + inches) * 2.54;
        // return convertToCentimeters((feet * 12) + inches); // 이렇게 써도된다
        int feetToInches = feet * 12; 
        int totalInches = feetToInches + inches;
        double result = convertToCentimeters(totalInches);
        return result;
    }
}
