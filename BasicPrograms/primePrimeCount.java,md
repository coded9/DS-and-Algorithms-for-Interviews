Problem link -->[here](https://www.hackerearth.com/problem/algorithm/micro-and-prime-prime-1/)
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
 
 
class TestClass {
    public static void main(String args[] ) throws Exception {
       
 
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int T = Integer.parseInt(line);
        String input[];
        int i,j,x,y,k;
        boolean arr[] = new boolean[1000001];
        int primeCount[] = new int[1000001];
         int primePrime[] = new int[1000001];
          for(j=2;j<=1000000;j++){
              arr[j] = true;
          }
          for(j=2;j<=(int)Math.sqrt(1000000);j++){
              if(arr[j]){
                  for(k=j;k*j<=1000000;k++){    //Sieve of Eratosthenes
                      arr[k*j] = false;
                  }
              }
          }
          primeCount[0] = 0;
          for(j=1;j<=1000000;j++){
              primeCount[j] = primeCount[j-1]; //preCompute the primeCount
           	if(arr[j]){
           		primeCount[j]++;
           	}
          }
           for(j=1;j<=1000000;j++){
              primePrime[j] = primePrime[j-1];
           	if(arr[primeCount[j]]){       //preCompute the primePrimeCount
           		primePrime[j]++;
           	}
          }
        for ( i = 0; i < T; i++) {
        	input = br.readLine().split(" ");
           x = Integer.parseInt(input[0]);
           y = Integer.parseInt(input[1]);
           
           System.out.println(primePrime[y]-primePrime[x-1]);
        }
    }
}
```
