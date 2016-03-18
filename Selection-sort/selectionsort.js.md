```
function selectionSort(A){
  console.log("Before sorting");
  for(var i=0;i<A.length;i++){
    console.log(A[i]);
  }
  for(i=0;i<A.length;i++){
    var min =i;
    for(var j=i+1;j<A.length;j++){
      if(A[j]<A[min]){
        min = j;
      }
    }
    var temp = A[i];
    A[i] = A[min];
    A[min] = temp;
    
  }
  console.log("After Sorting");
  for(i=0;i<A.length;i++){
    console.log(A[i]);
  }
  
}
var A = [24,13,25,11,36,22,45,3,44,23];
selectionSort(A);
```
