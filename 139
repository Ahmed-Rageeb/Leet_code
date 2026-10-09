class Solution {
public:
    bool dp(string &s, vector<string>& wordDict, vector<int>&v,int i)
    {
       if(i==s.length())
       {
         return true;
       }
       if(v[i]!=-1)
       {
         return v[i];
       }
       for(string temp:wordDict)
       {
         if(i+temp.length()>s.length())
         {
            continue;
         }
         if(s.substr(i,temp.length())==temp)
         {
           
            if(dp(s,wordDict,v,i+temp.length()))
            {
                return v[i]=1;
            }
         }
       }
       return v[i] = 0;

    }
    bool wordBreak(string s, vector<string>& wordDict) {
        vector<int>v(s.length(),-1);
        return dp(s,wordDict,v,0);
    }
};
