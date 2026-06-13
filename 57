class Solution {
public:
    vector<vector<int>> insert(vector<vector<int>>& intervals, vector<int>& newInterval) {
        int insert=0;
        if(intervals.size()==0)
        {
            vector<vector<int>>ans;
            ans.push_back(newInterval);
            return ans;
        }
        int i=0;
        for(i=0;i<intervals.size();i++)
        {
            if(newInterval[0]>intervals[i][0])
            {
                insert++;
            }
            else
            {
                intervals.insert(intervals.begin()+insert,newInterval);
                break;
            }
        }
        if(i==intervals.size())
        {
            intervals.insert(intervals.begin()+insert,newInterval);
        }
        for(int i=1;i<intervals.size();i++)
        {
            if(intervals[i][0]>intervals[i-1][1])
            {
                cout<<intervals[i][0];
                cout<<intervals[i-1][1];
                continue;
            }
            else
            {
                intervals[i-1][1]=max(intervals[i][1],intervals[i-1][1]);
                intervals.erase(intervals.begin()+i);
                i--;

            }
            
        }
        return intervals;
    }
};
