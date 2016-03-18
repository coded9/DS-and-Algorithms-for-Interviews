#Code:
```

/* package whatever; // don't place package name! */

import java.util.*;
import java.lang.*;
import java.io.*;

/* Name of the class has to be "Main" only if the class is public. */
class Ideone
{
	static void insertionSort(int arr[]){
		int i,hole,value;
		System.out.println("### Before sorting ###");
		for(i=0;i<arr.length;i++){
			System.out.print(arr[i]+" ");
		}
		
		for(i=1;i<arr.length;i++){
			value = arr[i];
			hole = i;
			while(hole>0 && arr[hole-1]>value){
				arr[hole] = arr[hole-1];
				hole = hole-1;
			}
			arr[hole] = value;
		}
		System.out.println();
		System.out.println("### After Sorting ###");
		for(i=0;i<arr.length;i++){
			System.out.print(arr[i]+" ");
		}
	}
	public static void main (String[] args) throws java.lang.Exception
	{
		// your code goes here
		int arr1[] = {24,13,25,11,36,22,45,3,44,23};
		insertionSort(arr1);
		
	}
}
```
#Explanation:
-->Here we set values for value and hole using first element 
-->we insert elements into sorted subarray from unsorted subarray
-->Inner while loop is for inserting the value into the sorted array.
