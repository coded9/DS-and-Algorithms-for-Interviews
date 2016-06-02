```
package basic;

import java.io.BufferedReader;
import java.io.InputStreamReader;

class TestClass {
	  public static int maxSubArray(int[] A) {
	       int current_max=A[0];
	       int max_so_far=A[0];
	       for(int i=1;i<A.length;i++){
	           current_max=Math.max(current_max+A[i],0);
	           max_so_far= Math.max(max_so_far, current_max);
	       }
	       return max_so_far;
	    }
    public static void main(String args[] ) throws Exception {
        /*
         * Read input from stdin and provide input before running      */

        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int N = Integer.parseInt(line);
        int arr[] = new int[N];
        int i;
        String str[] = br.readLine().split(" ");
        for (i = 0; i < N; i++) {
        	if(str[i].length()>0)
          arr[i] = Integer.parseInt(str[i]);
        }
       //System.out.println(maxSubArray(arr));
  System.out.println(maxSubArray(arr)>0?maxSubArray(arr):0);

      
    }
}

```
