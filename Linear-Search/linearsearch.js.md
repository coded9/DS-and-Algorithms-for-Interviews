```
function linearSearch(arr){
  var ele = prompt("Enter the element you want to search"); //Prompting the user for input
  flag = false;
  var i;
  for(i=0;i<arr.length;i++){
    if(arr[i]==ele){
      flag = true;
      break;
    }
  }
  if(flag){
    console.log("The Element "+ele+" found at "+(i+1)+" position");
  }
  else
    console.log("Element not found");
  
}
 A = [20,33,44,24,45,36,29];

linearSearch(A);
```
