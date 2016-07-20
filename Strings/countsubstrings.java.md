Problem link -->[here](https://www.hackerearth.com/problem/algorithm/counting-strings/)
Editorial -->[here](https://learn.hackerearth.com/tutorial/string-manipulation/79/editorial-for-counting-strings/)
```
import java.io.BufferedReader;
import java.io.InputStreamReader;


class TestClass {
    public static void main(String args[] ) throws Exception {
       BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		  int N = Integer.parseInt(br.readLine());
		  String str;
		 
        for(int i=0;i<N;i++)
        {
          str = br.readLine();
          long c=0,l=0;
          for(int j=0;j<str.length();j++)
             {
    			if(str.charAt(j)=='a'||str.charAt(j)=='z'){
					l=j+1;
					}
				c+=l; 
				//System.out.println(l+" "+c+" "+j);

			}
		System.out.println(c);
		}

       
    }
}
```
