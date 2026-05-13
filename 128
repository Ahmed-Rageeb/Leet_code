class Solution {
public:
    int longestConsecutive(vector<int>& nums) {
        if(nums.size()==0)
        {
            return 0;
        }
        sort(nums.begin(),nums.end());
        int max=1;
        int consecutive=1;
        
        for(int i=1;i<nums.size();i++)
        {
            if(nums[i]-1==nums[i-1] || nums[i]==nums[i-1])
            {
                if(nums[i]==nums[i-1])
                {
                    continue;
                }
                else
                {
                    consecutive++;
                }
                
            }
            else
            {
               consecutive=1; 
            }
            if(consecutive>=max)
            {
                max=consecutive;
            }
        }
        return max;
    }
};
