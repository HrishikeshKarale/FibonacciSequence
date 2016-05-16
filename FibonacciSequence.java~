/**
Fibonacci Sequence
(http://blog.smartbear.com/programming/7-silly-programming-challenges-to-do-for-fun/)

The Fibonacci sequence is constructed by adding the last two numbers of the sequence so far to get the next number in the sequence. The first and second numbers of the sequence are defined as 0 and 1. We get:

0, 1, 1, 2, 3, 5, 8, 13, 21…

Write a function that returns the nth number of the sequence. This should be pretty easy. Your solution here may well be suitable for one of the next mini-challenges.

Note that for this, I mention a single function, but you may choose to have a “setup function” and a “processing function,” as you see fit.

Write the same function, but you may not use a loop; and if you use variables, treat them as constants (within the scope of the function). You may not reassign them.

Write the same function, but you may not use local variables at all.

Write the same function, but the last statement must be a recursive function call. The result of the recursion is returned as-is; it is not transformed in any way, or added to anything. This is a concept called tail recursion, and can be used to optimize processing in languages and compilers that support it.

Write the same function, but this time, you’re not allowed to use recursion.
 */

import java.util.Scanner;

class FibonacciSequence {
	private static int count= 0;
	private int sum= 1;
	private int lastSum= 0;
	private int counter= 0;
	private int temp= 0;
	
	private void initialize() {
		sum= 1;
		lastSum= 0;
		counter= 0;
		temp= 0;
	}
	
	private void iterativeFibonacci() {
		if(count>= 1) {
			System.out.print(lastSum);
		}
		if(count>= 2) {
			System.out.print(", "+sum);
		}
		for(int i= 3; i<= count; i++){
			temp= 0;
			temp= sum;
			sum= sum+lastSum;
			System.out.print(", "+sum);
			lastSum= temp;
		}
	}
	
	private void recursiveFibonacci() {
		if(counter<count) {
			if(counter== 0) {
				System.out.print(lastSum);
				counter++;
			}
			else if(counter== 1) {
				System.out.print(", "+sum);
				counter++;
			}
			else {
				temp= 0;
				temp= sum;
				sum= sum+lastSum;
				System.out.print(", "+sum);
				lastSum= temp;
				counter++;
			}
			recursiveFibonacci();
		}
	}
	
	
	public static void main(String args[]) {
		FibonacciSequence fibSeqObject= new FibonacciSequence();
		Scanner scrObject= new Scanner(System.in);
		System.out.println("\n\n**********FIbonacci Series**********");
		System.out.print("Please Enter no of fibonacci sequence numbers you want to print: ");
		try {
			count= scrObject.nextInt();
		}
		catch (Exception e) {
			System.out.println("Wrong Input\n");
			System.exit(0);
		}
		System.out.print("\nIterative Fibonaci sequence: ");
		fibSeqObject.iterativeFibonacci();
		System.out.println();
		fibSeqObject.initialize();
		System.out.print("Recursive Fibonaci sequence: ");
		fibSeqObject.recursiveFibonacci();
		System.out.println();
		fibSeqObject.initialize();
		System.out.println("\n");
	}
}
