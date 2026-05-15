class Solution {
public:
    int visit(string &s, vector<int>&dp, int i)
    {
        if(i==s.length())
        {
            return 1;
        }
        if(i>=s.length())
        {
            return 0;
        }
        if(dp[i]!=-1)
        {
            return dp[i];
        }
        if(s[i]=='0')
        {
            return 0;
        }
        int take=visit(s,dp,i+1);
        if(i+1<s.length())
        {
            int num=(s[i]-'0')*10+s[i+1]-'0';
            if(num>=10 && num<=26)
            {
                take+=visit(s,dp,i+2);
            }
        }
        
        return dp[i]=take;
    }
    int numDecodings(string s) {
        vector<int>dp(s.length(),-1);
        return visit(s,dp,0);
    }
};
