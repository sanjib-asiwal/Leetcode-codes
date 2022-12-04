class Solution {
public:
    int minimumAverageDifference(vector<int>& nums) {
        int n=nums.size();
        long long arr[n];
        arr[0]=nums[0];
        for(int i=1;i<n;i++){
            arr[i]=arr[i-1]+nums[i];
        }
        //subscribe @codeved
        long long temp=0,ans=INT_MAX;
        int idx=0;
        for(int i=0;i<n-1;i++){
            temp=abs(arr[i]/(i+1)-(arr[n-1]-arr[i])/(n-i-1));
            if(temp<ans){
                ans=temp;
                idx=i;
            }
        }
        temp=arr[n-1]/n;
        if(temp<ans){
            idx=n-1;
        }
        return idx;
    }
};
