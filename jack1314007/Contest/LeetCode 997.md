## Find the Town Judge
#### Question
In a town, there are N people labelled from 1 to N.  There is a rumor that one of these people is secretly the town judge.

If the town judge exists, then:

* The town judge trusts nobody.
* Everybody (except for the town judge) trusts the town judge.
* There is exactly one person that satisfies properties 1 and 2.

You are given trust, an array of pairs trust[i] = [a, b] representing that the person labelled a trusts the person labelled b.

If the town judge exists and can be identified, return the label of the town judge.  Otherwise, return -1.

**Example 1**
<pre>
<b>Input:</b> N = 2, trust = [[1,2]] 
<b>Output:</b> 2
</pre>

**Example 2**
<pre>
<b>Input:</b> N = 3, trust = [[1,3],[2,3]]
<b>Output:</b> 3
</pre>

**Example 3**
<pre>
<b>Input:</b> N = 3, trust = [[1,3],[2,3],[3,1]]
<b>Output:</b> -1
</pre>

**Example 4**
<pre>
<b>Input:</b> N = 3, trust = [[1,2],[2,3]]
<b>Output:</b> -1
</pre>

**Example 5**
<pre>
<b>Input:</b> N = 4, trust = [[1,3],[1,4],[2,3],[2,4],[4,3]]
<b>Output:</b> 3
</pre>
#### Solution
##### Approach #1

```java
class Solution {
    public int findJudge(int N, int[][] trust) {
        
        HashMap<Integer, Set<Integer>> inbound = new HashMap<>();
        HashMap<Integer, Set<Integer>> outbound = new HashMap<>();
        
        for(int i = 1; i <= N; i++){
            inbound.put(i,new HashSet());
            outbound.put(i,new HashSet());
        }
        
        for(int[] item : trust){
            int start = item[0];
            int end = item[1];
            inbound.get(start).add(end);
            outbound.get(end).add(start);
        }
        
        for(int i = 1; i <= N; i++){
            if((outbound.get(i).size() == N-1)&&(inbound.get(i).size() == 0)){
                return i;
            }
        }
        
        return -1;
    }
    
}
```
##### Complexity

* Time complexity: $O()$
* Space complexity: $O()$