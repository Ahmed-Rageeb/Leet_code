/**
 * Definition of Interval:
 * class Interval {
 * public:
 *     int start, end;
 *     Interval(int start, int end) {
 *         this->start = start;
 *         this->end = end;
 *     }
 * }
 */

class Solution {
public:
    bool canAttendMeetings(vector<Interval>& intervals) {
        sort(intervals.begin(),intervals.end(), [](const Interval &a, const Interval &b)
        {
            return a.end<b.end;
        }
        
        );
        for(int i=0;i<intervals.size();i++)
        {
            if(i!=intervals.size()-1 && (intervals[i].end<=intervals[i+1].start))
            {
                continue;
            }
            else
            {
                if(i==intervals.size()-1)
                {
                    return true;
                }
                return false;
            }
        }
        return true;
    }
};
