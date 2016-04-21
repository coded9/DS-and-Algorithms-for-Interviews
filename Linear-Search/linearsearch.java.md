```
/* package whatever; // don't place package name! */

import java.util.*;
import java.lang.*;
import java.io.*;

/* Name of the class has to be "Main" only if the class is public. */
class Ideone
{
	static void linearSearch(int arr[],int ele){ //static method since we dont require any object instance to cal it.
				boolean flag = false;
				int i=0;
			for(i=0;i<arr.length;i++){
				if(arr[i]==ele){ //loop through each and every element to find the match
				  flag = true; //if element is found,we can exit out of loop and flag does the rest.
				  break;
			}
		}
		if(flag){ //flag is true,then we found a match
			System.out.print(ele +" found at "+(i+1)+" position ");
		}
		else{
			System.out.print("Element not found");
		}
	}
	public static void main (String[] args) throws java.lang.Exception
	{
		// your code goes here
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter the element you want to search");
		int x = sc.nextInt();
		int A[] = {20,33,44,24,45,36,29};
		
	          linearSearch(A,x);
}
}
```
