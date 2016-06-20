Prime number or composite number ?
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
class TestClass {
    public static void main(String args[] ) throws Exception {
        /*
         * Read input from stdin and provide input before running */

        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int T = Integer.parseInt(line),i,j;
        long P;
        boolean flag;
        for (i = 0; i < T; i++) {
            P = Long.parseLong(br.readLine()); 
          flag = false;
           for(j=2;j<=(long)Math.sqrt(P);j++){
           	if(P%j==0){
           	flag = true;
           		break;
           	}
           }
           System.out.println(flag?"composite":"prime");
        }
       
    }
}
```
