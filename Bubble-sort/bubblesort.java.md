````

/* package whatever; // don't place package name! */

import java.util.*;
import java.lang.*;
import java.io.*;

/* Name of the class has to be "Main" only if the class is public. */
class Ideone
{
	
	static void bubbleSort(int arr2[]){
		int n = arr2.length,i;
		for(int k=1;k<n;k++){
			int flag =0;
			for(i=0;i<n-k;i++){
				if(arr2[i]>arr2[i+1]){
					int temp = arr2[i];
					arr2[i] = arr2[i+1];
					arr2[i+1] = temp;
					flag = 1;
				}
			}
			if(flag==0){
				
				break;
			}
		}

		for(i=0;i<n;i++){
			System.out.print(arr2[i]+" ");
		}
		
	}
	public static void main (String[] args) throws java.lang.Exception
	{
		// your code goes here
		int arr[] = {24,13,25,11,36,22,45,3,44,23};
		System.out.println("#### Before Sorting ####");
		for(int j=0;j<arr.length;j++){
			System.out.print(arr[j]+" ");
		}
		System.out.println();
		System.out.println("### After Sorting ###");
		bubbleSort(arr);
	}
}

```
