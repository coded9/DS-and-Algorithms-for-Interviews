Problem link --> [here](https://www.hackerearth.com/problem/algorithm/emma-and-the-prime-sum/)
```
import java.io.BufferedReader;
import java.io.InputStreamReader;


class TestClass {
    public static void main(String args[] ) throws Exception {
        /*
         * Read input from stdin and provide input before running  */

      BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int T = Integer.parseInt(line),j,x,y,k;
         long sum[];
        boolean flag;
        String input[];
         boolean arr[] = new boolean[10000001];
         sum = new long[10000001];
          for(j=2;j<=1000000;j++){
              arr[j] = true;
          }
          for(j=2;j<=(int)Math.sqrt(1000000);j++){
              if(arr[j]){
                  for(k=j;k*j<=1000000;k++){
                      arr[k*j] = false;
                  }
              }
          }
          sum[0] = 0;
          for(j=1;j<=1000000;j++){
              if(arr[j]){
                  sum[j] = sum[j-1]+j; //Precomputing the sum of prime numbers
              }
              else{
                  sum[j] = sum[j-1];
              }
             // System.out.println(j+" "+sum[j]);
          }
    
        for (int i = 0; i < T; i++) {
           input = br.readLine().split(" ");
          // sum =0;
           x = Integer.parseInt(input[0]);
           y = Integer.parseInt(input[1]);
           
         System.out.println(sum[y]-sum[x-1]);
      
    
        }
  }
  }
  ```
    
        
