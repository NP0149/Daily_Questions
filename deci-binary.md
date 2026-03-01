# deci binary 

[Problem Link](https://leetcode.com/problems/partitioning-into-minimum-number-of-deci-binary-numbers/?envType=daily-question&envId=2026-03-01)


Always the biggest number is deci-binary

```
class Solution {
    public int minPartitions(String s) {
     int n=s.length();
     List<Integer> li=new ArrayList<>();
     for(int i=0;i<s.length();i++){
        li.add((int)s.charAt(i)-48);
     }
     int max=Integer.MIN_VALUE;
     for(int i=0;i<li.size();i++){
        max=Math.max(max,li.get(i));
     }
     return max;
    }
}
```
