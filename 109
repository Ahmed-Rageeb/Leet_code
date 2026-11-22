class Solution {
public:
    uint32_t reverseBits(uint32_t n) {
        cout<<n;
        string b="";
        for(int i=0;i<32;i++)
        {
            if(n & (1<<i))
            {
               b+='1'; 
            }
            else
            {
                b+='0';
            }
        }
        uint32_t res=0;
        for(int i=31;i>=0;i--)
        {
            if(b[i]=='1')
            {
                res|=(1<<(31-i));
            }
        }


        return res;
    }
};
