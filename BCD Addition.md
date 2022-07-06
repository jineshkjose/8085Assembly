## BCD ADDITION
Aim : To find sum of two bcd no

Example : 25+ 26 , result of above sum is 4B in hexa decimal . To convert it into desimal ie 51 use DAA instruction after addition. DAA istruction is valid only after addition.

~~~
	   MVI A,25
	   MVI B,26
	   ADD B
	   DAA
~~~


