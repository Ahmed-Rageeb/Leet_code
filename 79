class Solution {
public:
    int row,col;
    bool dfs(vector<vector<char>>& board, string word,int i,int j,string temp,vector<vector<int>>&v)
    {
        if(temp.size()>word.size())
        {
            return false;
        }
        if(i<0 || i>=row || j<0 || j>=col)
        {
            return false;
        }
        
        
        if(v[i][j]==1)
        {
            return false;
        }
        temp+=board[i][j];
        if(temp==word)
        {
            return true;
        }
        if(word.compare(0, temp.size(), temp) != 0)
        {
            return false;
        }
        
        v[i][j]=1;
       bool a= dfs(board,word,i+1,j,temp,v) || dfs(board,word,i,j+1,temp,v) || dfs(board,word,i-1,j,temp,v) ||dfs(board,word,i,j-1,temp,v);
        v[i][j]=-1;
        return a;
        
    }
    bool exist(vector<vector<char>>& board, string word) {
        row= board.size();
        col=board[0].size();
        vector<vector<int>>v(row,vector<int>(col,-1));
        for (int i=0;i<row;i++)
        {
            for(int j=0;j<col;j++)
            {
                  if(dfs(board,word,i,j,"",v))
                    {
                        return true;
                    }
                
            }
        }
        return false;
    }
};
