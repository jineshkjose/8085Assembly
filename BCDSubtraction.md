## BCD Subtraction
Aim : To subtract two digit bcd nos

Algorithm: 
To subtract two BCD numbers, we are going to use the 10s complement method. Taking the first number and storing into B, Load 99 into A then subtract the number to get the 9’s complement. After that add 1 with the result to get 10’s complement. We cannot increase using INR instruction. This does not effect on CY flag. So we have to use ADI 01. Then DAA instruction will be used to adjust the decimal.

The below example is to subtarct 35 from 74.


74+ 10's complement of 35.


74+[(9's complement of 35)+1]


74+[(99h - 35)+1]


~~~

	   MVI A,35
	   MOV C,A
	   MVI A,99
	   SUB C
	   ADI 01
	   MOV B,A
	   MVI A,74
	   ADD B
	   DAA
~~~
