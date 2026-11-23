class Solution {
public:
    vector<vector<int>> pacificAtlantic(vector<vector<int>>& heights) {
        vector<vector<bool>>pac(heights.size(),vector<bool>(heights[0].size()));
        vector<vector<bool>>alt(heights.size(),vector<bool>(heights[0].size()));
        vector<vector<int>>res;
        for(int c=0;c<heights[0].size();c++)
        {
            dfs(0,c,pac,heights);
            dfs(heights.size()-1,c,alt,heights);
        }

        for(int r=0;r<heights.size();r++)
        {
            dfs(r,0,pac,heights);
            dfs(r,heights[0].size()-1,alt,heights);
        }
        for(int i=0;i<heights.size();i++)
        {
            for(int j=0;j<heights[0].size();j++)
            {
                if(pac[i][j] && alt[i][j])
                {
                    res.push_back({i,j});
                }
            }
        }
        return res;

    }
    void dfs(int row,int col,vector<vector<bool>>&oce, vector<vector<int>>& heights)
    {
        oce[row][col]=true;
        vector<pair<int,int>>dr={{1,0},{-1,0},{0,1},{0,-1}};
        for (auto d:dr)
        {
            int dx=row+d.first;
            int dy=col+d.second;
            if(dx>=0 && dx<heights.size() && dy>=0 && dy<heights[0].size()&& !oce[dx][dy] && heights[row][col]<=heights[dx][dy])
            {
                dfs(dx,dy,oce,heights);
            }
        }
    }
};
