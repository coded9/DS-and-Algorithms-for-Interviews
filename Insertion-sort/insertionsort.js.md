```
function insertionSort(arr){
		var i,hole,value;
	  console.log("### Before sorting ###");
		for(i=0;i<arr.length;i++){
			console.log(arr[i]+" ");  //Print the array before sorting
		}
		
		for(i=1;i<arr.length;i++){
			value = arr[i];
			hole = i;
			while(hole>0 && arr[hole-1]>value){
				arr[hole] = arr[hole-1];   //Hole is the element which we insert in the sorted subarray from  unsorted 
				hole = hole-1;
			}
			arr[hole] = value;   //if the left side of the hole element is sorted,then loop will not execute
		}
	
		console.log("### After Sorting ###");
		for(i=0;i<arr.length;i++){      //Print the array after sorting
			console.log(arr[i]+" ");
		}
}
var A = [24,13,25,11,36,22,45,3,44,23];
insertionSort(A);
```
