Problem link -->here[https://www.hackerearth.com/practice/data-structures-1/string-manipulation-1/basics-2/tutorial/]
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.*;
 


class TestClass {
    public static void main(String args[] ) throws Exception {
        /*
         * Read input from stdin and provide input before running*/

        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int N = Integer.parseInt(line);
        String input[],word;
        char subs[];
        int l,u;
        
        for (int i = 0; i < N; i++) {
           input = br.readLine().split(" ");
           word = input[0];
           l = Integer.parseInt(input[1]);
           u = Integer.parseInt(input[2]);
           subs = word.substring(l,u+1).toCharArray();
           Character subs1[] = new Character[subs.length];
           for(int j=0;j<subs.length;j++){
           	subs1[j] = subs[j];
           }
           Arrays.sort(subs1,new Comparator<Character>(){
 
        @Override
        public int compare(Character o1, Character o2) {
            // TODO Auto-generated method stub
            return o2.compareTo(o1);
        }
           });
            for(int j=0;j<subs.length;j++){
           	subs[j] = subs1[j].charValue();
           }
           
         //  System.out.println(subs1[1]);
           System.out.println(word.substring(0,l)+new String(subs)+word.substring(u+1,word.length()));
        }
        

       
    }
}
```
