# Finding-Roots-of-a-quadratic-equation-in-Java

Finding Roots of a Quadratic Equation in Java
In this Java program, we will find the roots of a quadratic equation [ax2 + bx + c]. We can solve a Quadratic Equation by finding its roots. Mainly roots of the quadratic equation are represented by a parabola in 3 different patterns like :

No Real Roots
One Real Root
Two Real Roots
Roots of a quadratic equation in java
Explanation
A quadratic equation is an equation of the second degree, meaning it contains at least one term that is squared.
The standard form is ax² + bx + c = 0 with a, b, and c being constants, or numerical coefficients, and x is an unknown variable.
One absolute rule is that the first constant "a" cannot be a zero.
Algorithm :
Calculate the determinant value (b*b)-(4*a*c).
If determinant is greater than 0 roots are [-b +squareroot(determinant)]/2*a and [-b -squareroot(determinant)]/2*a.
If determinant is equal to 0 root value is (-b+Math.sqrt(d))/(2*a)
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Power of a Number 

Prime Number

Largest element in an array

Code in Java
Run
/* Write a program to find roots of a quadratic equation in Java*/
import java.io.*;
import static java.lang.Math.*;
class Main{
 
    static void findRoots(int a, int b, int c)
    {
        if (a == 0) {
            System.out.println("Invalid");
            return;
        }
 
        int d = b * b - 4 * a * c;
        double sqrt_val = sqrt(abs(d));
 
        if (d > 0) {
            System.out.println("Roots are real and different");
            System.out.println((double)(-b + sqrt_val) / (2 * a) + "\n"+ (double)(-b - sqrt_val) / (2 * a));
        }
        else if (d == 0) {
            System.out.println("Roots are real and same ");
            System.out.println(-(double)b / (2 * a) + "\n" + -(double)b / (2 * a));
        }
        else // d < 0
        {
            System.out.println("Roots are complex");
 
            System.out.println(-(double)b / (2 * a) + " + i" + sqrt_val + "\n" + -(double)b / (2 * a) + " - i" + sqrt_val);
        }
    }
 
    // Driver code
    public static void main(String args[])
    {
 
        int a = 1, b = 4, c = 4;
       
        // Function call
        findRoots(a, b, c);
    }
}
Output :
Roots are real and same

-2.0
-2.0
