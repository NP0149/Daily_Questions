# Move zeroes to end

[Problem Link](https://www.geeksforgeeks.org/problems/move-all-zeroes-to-end-of-array0751/1)

```
class Solution {
    void pushZerosToEnd(int[] arr) {
        // code here
        List<Integer> li=new ArrayList<>();
        for(int i=0;i<arr.length;i++){
            if(arr[i]!=0){
                li.add(arr[i]);
            }
        }
        int indx=0;
        while(indx<arr.length && indx<li.size()){
            arr[indx]=li.get(indx);
            indx++;
        }
        while(indx<arr.length){
            arr[indx]=0;
            indx++;
        }
      return;
    }
}
```

# Complexity Analysis

Time:O(n)

Space:O(number of non zero elements)
