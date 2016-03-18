```
/* package whatever; // don't place package name! */

import java.util.*;
import java.lang.*;
import java.io.*;

/* Name of the class has to be "Main" only if the class is public. */
class Ideone
{
	static void selectionSort(int arr1[],int n){
		int i=0,j=0;
			for(i=0;i<arr1.length-1;i++){
				int min = i;
				for(j=i+1;j<arr1.length;j++){
					if(arr1[j]<arr1[min]){
						min = j;
					}
					
				}
				    //System.out.print(min);
					int temp = arr1[i];
					arr1[i] = arr1[min];
					arr1[min] = temp;
				//	System.out.print(min);
				
			}
				for( i=0;i<arr1.length;i++){
			System.out.print(arr1[i]+" ");
		}
		}
	public static void main (String[] args) throws java.lang.Exception
	{
		int arr2[] = {24,13,25,11,36,22,45,3,44,23};
		System.out.println("###### Before Sorting #####");
		for(int k=0;k<arr2.length;k++){
			System.out.print(arr2[k]+" ");
		}
		
		System.out.println();
		System.out.println("### After sorting ###");
		selectionSort(arr2,arr2.length);
		```
	}
}
