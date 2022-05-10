# Write-a-program-to-list-the-first-n-prime-numbers-in-Python.-The-positive-integer-n-is-entered-from-
Write a program to list the first n prime numbers in Python. The positive integer n is entered from the keyboard
import math
 
"""
  * check the original
  *
  * @author viettuts.vn
  * @param n: so nguyen duong
  * @return true is so nguyen so,
  * false is not original
"""
def isPrimeNumber(n):
     # n < 2 does not have to be a prime
     if (n < 2):
         return False;
 
     # check so nguyen to when n >= 2
     squareRoot = int(math.sqrt(n));
     for i in range(2, squareRoot + 1):
         if (n % i == 0):
             return False;
     return True;
 
n = int(input("Enter a positive integer n = "));
print(n, "First prime is:");
dem = 0; # count prime numbers
i = 2; # find prime numbers starting from 2
sb = "";
while (dem < n):
     if (isPrimeNumber(i)):
         sb = sb + str(i) + " ";
         dem = dem + 1;
     i = i + 1;
print(sb);
