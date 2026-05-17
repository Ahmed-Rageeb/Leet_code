class Solution {
public:
    int dp(vector<int>&nums, vector<int>&visit,int i, int size)
    {
        if(i>size)
        {
            return 0;
        }
        if(visit[i]!=-1)
        {
            return visit[i];
        }
        int take=nums[i]+dp(nums,visit,i+2,size);
        int skip=dp(nums,visit,i+1,size);
        return (visit[i]=max(take,skip));
    }
    int rob(vector<int>& nums) {
        vector<int>visit(nums.size(),-1);
        vector<int>visit1(nums.size(),-1);
        if(nums.size()==1)
        {
            return nums[0];
        }
        int first=dp(nums, visit, 0,nums.size()-2);
        int last=dp(nums, visit1, 1,nums.size()-1);
        return max(first,last);
    }
};
