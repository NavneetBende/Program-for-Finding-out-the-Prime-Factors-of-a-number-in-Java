# Program-for-Finding-out-the-Prime-Factors-of-a-number-in-Java

Program for Finding out the Prime Factors of a number in Java
Prime Factors of a number in Java
 

Here, in this page we will discuss the program to print all the prime factors of a number in java. Prime factorization is a way of expressing a number as a product of its prime factors. A prime number is a number that has exactly two factors, 1 and the number itself.

Example :

Input : 12
Output : 2 2 3
Prime Factors of a number in Java
Method  :
Create a function say isprime(int n), that will return 1 if a number is prime, otherwise return 0.
primeFactors(int n), will print the prime factors of the number.
Run a loop from 2 to n,
Check if it is prime, then
Create a variable x to hold n,
Run a while loop that will terminate when ( x is not divisible by i)
Inside that loop print i and decrement as, x = x/2
Prime Factors of a number
Code to print prime factors of a number in java
Run
import java.io.*;
import java.lang.Math;

class Main {

   public static int isprime(int n){

      for(int i = 2; i<=Math.sqrt(n); i++){
        if(n%i==0)
          return 0;
      }

      return 1;
   }

   public static void primeFactors(int n)
   {

      for(int i = 2; i<= n; i++){
          if(isprime(i)==1){
             int x = n;
             while(x%i==0){
                System.out.print(i + " ");
                x /= i;
             }
          }
       }

   }

   public static void main(String[] args)
   {
       int n = 90;
       primeFactors(n);
   }
}
Output :

2 3 3 5
Related Pages
Power of a number

Factor of a number

Finding Prime Factors of a number

Strong number

Perfect number

Perfect Square

Method  2 :
Run a while loop that will terminate when the number is not divisible by two,
So, inside that loop print(“2”), and divide the number by 2 in each iteration.
After this, n will be odd number. Now start a loop from i = 3 to square root of n.
Run a while loop that terminate when  i is not divisible by n,
Inside loop print i and divide n by i, increment i by 2 and continue.
If n is a prime number and is greater than 2, then n will not become 1 by above two steps.
So print n if it is greater than 2.
Code to print prime factors of a number in java
Run
import java.io.*;
import java.lang.Math;

class Main {

  public static void primeFactors(int n)
  {

    while (n % 2 == 0) {
        System.out.print(2 + " ");
        n /= 2;
    }

    for (int i = 3; i <= Math.sqrt(n); i += 2) { while (n % i == 0) { System.out.print(i + " "); n /= i; } } if (n > 2)
     System.out.print(n);
  }

  public static void main(String[] args)
  {
    int n = 90;
    primeFactors(n);
  }
}
Output :

2 3 3 5
