class Solution {
public:
    bool jum(vector<int>& nums,vector<int>& visit, int i)
    {
        if(i>=nums.size()-1)
        {
            return true;
        }
        if(nums[i]==0)
        {
            return false;
        }
        if(visit[i]!=-1)
        {
            return visit[i];
        }
        for(int j=1;j<=nums[i];j++)
        {
            if(jum(nums,visit,i+j))
            {
                visit[i]=1;
                return true;
            }
        }
        visit[i]=0;
        return false;
        
    }
    bool canJump(vector<int>& nums) {
        vector<int>visit(nums.size(),-1);
        return jum(nums,visit,0);
    }
};
