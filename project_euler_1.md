### **Problem Statement**

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000.

### **Solution**

The sum of numbers from 0 to a positive number N is N(N + 1)//2.

The multiples of 3 below 1000 are 0, 3, 6...993, 996, 999. Their sum is 3\*sum(0, 1, 2,...331, 332, 333) = 3\*333\*(333 + 1)/2 = 166833.
The multiples of 5 below 1000 are 0, 5, 10...985, 990, 995. Their sum is 5\*sum(0, 1, 2...197, 198, 199) = 5\*199\*(199 + 1)/2 = 99500.

If we simply add the two summations, we will get a wrong answer because all multiples of 15 will be counted twice. To fix this, we must subtract the sum of multiples of 15 below 1000.

The multiples of 15 below 1000 are 0, 15, 30...960, 975, 990 = 15\*sum(0, 1, 2...64, 65, 66) = 15*66*(66 + 1)/2 = 33165.

Therefore our answer is 166833 + 99500 - 33165 = 233168.
