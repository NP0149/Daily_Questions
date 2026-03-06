# Check Binary String

[Problem Link](https://leetcode.com/problems/check-if-binary-string-has-at-most-one-segment-of-ones/?envType=daily-question&envId=2026-03-06)


```
class Solution {
    public boolean checkOnesSegment(String s) {
        HashMap<Character,Integer> hm=new HashMap<>();
        for(int i=0;i<s.length();i++){
            if(!hm.containsKey(s.charAt(i))){
            hm.put(s.charAt(i),i);
            }
            else if(Math.abs(hm.get(s.charAt(i))-i)==1){
                hm.put(s.charAt(i),i);
                continue;
            }
            else{
                return false;
            }
        }
        return true;
    }
}
```

# Complexity Analysis

Time:O(n)

Space:O(n)
