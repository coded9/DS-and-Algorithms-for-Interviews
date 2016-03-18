```
function selectionSort(A){
  console.log("Before sorting");
  for(var i=0;i<A.length;i++){
    console.log(A[i]); //Print the array before sorting
  }
  for(i=0;i<A.length;i++){
    var min =i;        //Assume the first element in the array is minimum
    for(var j=i+1;j<A.length;j++){
      if(A[j]<A[min]){
        min = j;        //Looping through the array from i+1 postion to find the minimum element in the array 
                        //Store the position of minimum element in min
      }
    }
    var temp = A[i];
    A[i] = A[min];     //Swap the elements (ith element of the array from the beginning with the minimum element in the whole array)
    A[min] = temp;     //So that there will be two subarrays,sorted(from the beginning to the ith element),unsorted(i+1 to last)
    
  }
  console.log("After Sorting");
  for(i=0;i<A.length;i++){
    console.log(A[i]);  //Printing the array after sorting
  }
  
}
var A = [24,13,25,11,36,22,45,3,44,23];
selectionSort(A);
```
