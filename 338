class Solution {
public:
    vector<int> countBits(int n) {
        vector<int>ans(n+1,0);
        for(int i=0;i<=n;i++)
        {
            for(int j=0;j<32;j++)
            {
                if(i & (1<<j))
                {
                    ans[i]++;
                }
            }
        }
        return ans;
    }
};
