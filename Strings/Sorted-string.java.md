Problem Link -->[here](https://www.hackerearth.com/problem/algorithm/sorted-string)
#Approach 1
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.*;


class TestClass {
    public static void main(String args[] ) throws Exception {
     
    	String str, output;
    	String alphaStr[] = new String[26];
    	int i,j,k,len,count;
    	char ch = 'a';
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int T = Integer.parseInt(line);
        for (i = 0; i<T; i++) {
        	str = br.readLine();
        	Arrays.fill(alphaStr,"");  
			
			for(j=0; j<str.length(); j++){
				char c = str.charAt(j);
				alphaStr[c-ch] += c+"" ;
			}
	
			output = "";
        	len=1;
        	for(j=0; j<str.length(); j++)
			{
			    count =0;
				for(k=0; k<26; k++){
				    count++;
					if(alphaStr[k].length() == len){
						output += alphaStr[k];
						
						//	System.out.println(output+" "+len+" "+k+" "+count);
							}
							
				}
				//	System.out.println(count);
				if(output.length()==str.length())
				{
				    break;
				}
				len++;
			}
        	System.out.println(output);
        }
    }
}
```

#Approach 2
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Comparator;
import java.util.HashMap;
import java.util.Map;
import java.util.TreeMap;
 
public class Temp {
 
	public static <Character, Integer extends Comparable<Integer>> Map<Character, Integer> sortByValues(final Map<Character, Integer> map) {
		Comparator<Character> valueComparator = new Comparator<Character>() {
			public int compare(Character k1, Character k2) {
				int compare = map.get(k2).compareTo(map.get(k1));
				if (compare == 0) {
					Integer int1 = (Integer) k1;
					Integer int2 = (Integer) k2;
					return  int2.compareTo(int1);
				} else
					return compare;
			}
		};
		Map<Character, Integer> sortedByValues = new TreeMap<Character, Integer>(valueComparator);
		sortedByValues.putAll(map);
		return sortedByValues;
	}
 
	public static void main(String[] args) throws IOException {
		BufferedReader bf = new BufferedReader(new InputStreamReader(System.in));
 
		int N = Integer.parseInt(bf.readLine());
		while (N-- > 0) {
			String name = bf.readLine();
			int length = name.length();
			Map<Character, Integer> map = new HashMap<>();
			for (int i = 0; i < length; i++) {
				char ch = name.charAt(i);
				if (map.containsKey(ch)) {
					map.put(ch, map.get(ch) + 1);
				} else {
					map.put(ch, 1);
				}
			}
			Map<Character, Integer> resultMap = sortByValues(map);
			StringBuilder result = new StringBuilder();
			for (Character ch : resultMap.keySet()) {
				int value = resultMap.get(ch);
				while (value-- > 0) {
					result.append(ch);
				}
			}
			System.out.println(result.reverse().toString());
		}
 
	}
}
```
#Approach 3
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.*;
 
 
class TestClass {
     static Map<Character, Integer> sortByComparator(Map<Character, Integer> unsortMap) {
 
		// Convert Map to List
		List<Map.Entry<Character, Integer>> list = 
			new LinkedList<Map.Entry<Character, Integer>>(unsortMap.entrySet());
 
		// Sort list with comparator, to compare the Map values
		Collections.sort(list, new Comparator<Map.Entry<Character, Integer>>() {
			public int compare(Map.Entry<Character, Integer> o1,
                                           Map.Entry<Character, Integer> o2) {
				return (o1.getValue()).compareTo(o2.getValue());
			}
		});
 
		// Convert sorted map back to a Map
		Map<Character, Integer> sortedMap = new LinkedHashMap<Character, Integer>();
		for (Iterator<Map.Entry<Character, Integer>> it = list.iterator(); it.hasNext();) {
			Map.Entry<Character, Integer> entry = it.next();
			sortedMap.put(entry.getKey(), entry.getValue());
		}
		return sortedMap;
	}
    public static void main(String args[] ) throws Exception {
        /*
         * Read input from stdin and provide input before running  */
 
         BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        int N = Integer.parseInt(line);
        Map<Character,Integer> map = new TreeMap<Character,Integer>();
        for (int i = 0; i < N; i++) {
         line = br.readLine();
         for(Character c:line.toCharArray()){
         	if(map.containsKey(c)){
         		map.put(c,map.get(c)+1);
         	}
         	else{
         		map.put(c,1);
         	}
         }
         //System.out.println(map);
         line ="";
         Map<Character, Integer> sortedMap = sortByComparator(map);
        // System.out.println(sortedMap);
         for(Object key:sortedMap.keySet()){
             for(int j=0;j<sortedMap.get(key);j++){
             line += key;
             }
         }
         System.out.println(line);
         map.clear();
        }
    }
}
```
#Approach 4
```
import java.util.*;
import java.lang.*;
import java.io.*;
import java.util.regex.Matcher;
import java.util.regex.Pattern;

/* Name of the class has to be "Main" only if the class is public. */
class Codechef
{
    public static void main(String[] args){
	
		Scanner sc = new Scanner(System.in);
		
		
		int t=Integer.parseInt(sc.nextLine());
		
		for(int i = 0; i<t;i++){
			
			
			String str=sc.nextLine();
			Map<Character, Integer> map = new TreeMap<>();
			
			ArrayList<Character> list = new ArrayList<>();
			
			for(int j=0;j<str.length();j++){
				char ch =str.charAt(j);
				list.add(ch);
				if(map.containsKey(ch)){
					int val=map.get(ch);
				map.put(str.charAt(j), ++val);}else map.put(ch, 1);
			
			
			}
			System.out.println(list);
			list.sort(new Comparator<Character>() {
 
			    @Override
			    public int compare(Character o1, Character o2) {
			    	int temp = map.get(o1) - map.get(o2);
			    	if(temp!=0)return temp;
			    	else return o1-o2;
			       
			    }
			});
				System.out.println(list);
			for(int j=0;j<list.size();j++)System.out.print(list.get(j));
			
			System.out.println();
		}
	}
}
```
