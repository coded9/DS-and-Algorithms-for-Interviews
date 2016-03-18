```
function bubbleSort(A){
  var i,k,flag=0;     //Flag for tracking the swaps
  console.log("Before sorting");
  for(i=0;i<A.length;i++){
    console.log(A[i]);  //Printing the array before sorting
  }
  console.log("After Sorting");
  for(k=1;k<A.length;k++){      //Number of passes
    for(i=0;i<A.length-k;i++){
      if(A[i]>A[i+1]){     
        var temp = A[i];
        A[i] = A[i+1];      //Swapping the elements to make the highest element bubble up in each pass
        A[i+1] = temp;
        flag =1;
      }
    }
    if(flag===0){      //If there are no swaps in the pass,then the array is sorted
      break;
    }
  }
  for(i=0;i<A.length;i++){
    console.log(A[i]);   //Printing the array after sorting
  }
}

var A = [24,13,25,11,36,22,45,3,44,23];
bubbleSort(A);

```
