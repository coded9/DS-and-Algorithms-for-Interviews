Problem link -->[here](https://www.hackerearth.com/problem/algorithm/remove-duplicates-3)
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.*;


class TestClass {
    public static void main(String args[] ) throws Exception {
      

        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int i;
       Set<Character> set = new LinkedHashSet<Character>(); //LinkedHashSet preserves the insertion order.
       for(i=0;i<line.length();i++){
       	set.add((Character)line.charAt(i));
       }
     
       for(Character c:set){
           System.out.print(c+"");
       }
  }
}
```
