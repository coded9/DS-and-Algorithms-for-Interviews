Problem link ->[here](https://www.hackerearth.com/problem/algorithm/roy-and-cipher-disk/)
```
import java.io.BufferedReader;
import java.io.InputStreamReader;


class TestClass {
    public static void main(String args[] ) throws Exception {
       

         BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int T = Integer.parseInt(line),diff=-1,j;
        char ch ;
        boolean flag ;
        for (int i = 0; i < T; i++) {
        	ch = 'a';
        	flag = true;
         line = br.readLine();
         for(j=0;j<line.length();j++){
         	
         		diff = line.charAt(j)-ch;
         	
         		if(diff>13){
         			diff = -26+Math.abs((line.charAt(j)-ch));
         		}
         		if(diff<-12){
         		    diff = 26 - Math.abs((line.charAt(j)-ch));
         		}
         			//System.out.println(diff+" "+line.charAt(j));
         	
    
         	System.out.print(diff+" ");
         	ch = line.charAt(j);
         }
         System.out.println();
        }

       
    }
}
```
