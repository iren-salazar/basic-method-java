# basic-method-java
Write a program that contains 4 methods: namely add(), subtract(), multiply(), average(). The function of each method is to accept two integer values as input from the user and perform computation based on its name. Then display the result. Allow the user to select to select which computation to execute.


import java.io.*;

public class ReturnType {
	public static void main(String args[]) throws IOException {
	
		BufferedReader br = new BufferedReader (new InputStreamReader(System.in));
		
		//declare
		int num1, num2;
		
		//assignment
		System.out.print("Input First number: ");
		num1 = Integer.parseInt(br.readLine());
		System.out.print("Input Second number: ");
		num2 = Integer.parseInt(br.readLine());
		
		// print options
		System.out.println("\r======= Options =======");
		System.out.println("\radd\rmultiply\rsubtract\raverage");
		System.out.print("\rChoice: ");

		String choice = br.readLine();
		
		switch (choice) {
		
		case "add":
			add (num1,num2);
			break;
		case "multiply":
			multiply (num1,num2);
			break;
		case "subtract":
			subtract (num1,num2);
			break;
		case "average":
			average (num1,num2);
			break;
		default:
			System.out.println("You have input a non existing option, Please try again. ");

		}
	}
		static void add (int num1, int num2) {
			System.out.println("\rAdding " + num1 + " and " +num2);
			System.out.print("\rsum : ");
			System.out.print(num1+num2);
			
		}
		static void multiply (int num1, int num2) {
			System.out.println("\rmultiplying " + num1 +" and " +num2);
			System.out.print("\rproduct: ");
			System.out.print(num1*num2);
		}
		static void subtract (int num1, int num2) {
			System.out.println("\rsubtracting " + num1 +" and " +num2);
			System.out.print("\rdifference: ");
			System.out.print(num1-num2);
		}
		static void average (int num1, int num2) {
			System.out.println("\rcalculating " + num1 +" and " +num2);
			System.out.print("\raverage: ");
			System.out.print((num1+num2)/2);
		}
}


