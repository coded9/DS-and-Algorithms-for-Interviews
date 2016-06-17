```
package basic;

import java.util.Stack;

public class Stacktest {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
      Stack<Integer> st = new Stack<Integer>();
      st.push(10);
      st.push(20);
      st.push(30);
      System.out.println(st);
      System.out.println(st.peek());
      st.push(50);
      System.out.println(st);
      st.push(60);
      st.pop();  //Removes element from the top of the stack
      System.out.println(st);
      System.out.println(st.search(10)); //Returns the offset from the top of stack,Here it prints 4 
	}

}

```
