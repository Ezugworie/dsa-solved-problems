````java
/* 
   Time Complexity
     Best Time Complexity:O(n)
	 Average Time Complexity:O(n^2)
	 Worst Time Complexity:O(n^2)
     
   Space Complexity
     No auxiliary space is required in Linear Search implementation.
	 Hence space complexity is:O(1)
*/

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
