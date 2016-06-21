Problem link-->[here](https://www.hackerearth.com/problem/algorithm/password-1/)
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.*;

class TestClass {
	static String palingen(String input){
		String str ="";
		char chars[] = input.toCharArray();
		for(int i=chars.length-1;i>=0;i--){
			str += chars[i];
		}
		return str;
	}
    public static void main(String args[] ) throws Exception {
        /*
         * Read input from stdin and provide input before running  */

        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
       // boolean flag = false;
        int N = Integer.parseInt(line);
        ArrayList<String> arr = new ArrayList<String>();
        for (int i = 0; i < N; i++) {
            arr.add(br.readLine());
        }
        for(String str:arr){
        	if(arr.contains(palingen(str))){
        	//	flag = true;
        		line = str;
        		break;
        	}
        }
      
    System.out.println(line.length()+" "+line.charAt(line.length()/2));
        
    }
}
```
