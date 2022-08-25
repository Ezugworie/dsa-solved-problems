````java
// time complexity of this solution is O(n*n)
public int[] sortArray(int[] nums) {
        for(int i = 1; i < nums.length; i++){  
            //using insertion sort
             int currentValue = nums[i];
            
            int j = i - 1;
            while(j >=0 && nums[j] > currentValue){
                nums[j + 1] = nums[j];
                j--;
            }
            
            nums[j + 1] = currentValue;
        }
        
        return nums;
    }
````