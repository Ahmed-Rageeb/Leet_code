class Solution {
public:
    vector<vector<string>> groupAnagrams(vector<string>& strs) {
        map<string,int>m;
        vector<vector<string>>ans;
        for(int i=0;i<strs.size();i++)
        {
            vector<int>freq(26,0);
            for(int j=0;j<strs[i].length();j++)
            {
                freq[strs[i][j]-'a']++;
            }
            string temp;
            for(int i=0;i<26;i++)
            {
                temp+=to_string(freq[i])+ "#";
            }
            if(m.find(temp)!=m.end())
            {
                auto it=m.find(temp);
                ans[it->second].push_back(strs[i]);
            }
            else
            {
                int index=ans.size();
                m[temp]=index;
                ans.push_back({strs[i]});
            }

        }
        return ans;
    }
};
