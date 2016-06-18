Problem link -->[here](https://www.hackerearth.com/problem/algorithm/compiler-version-2/)
```
import java.io.BufferedReader;
import java.io.InputStreamReader;

class TestClass {
    public static void main(String args[] ) throws Exception {
        /*
         * Read input from stdin and provide input before running*/

       BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
	String line;
	String input[];
        while((line=br.readLine())!=null) {
            input = line.split("//",2);
            if(input.length>1){
                line = input[0].replace("->",".")+"//"+input[1];
            }
            else{
                line = input[0].replaceAll("->",".");
            }
          System.out.println(line);  
        }
        

        
    }
}
```
