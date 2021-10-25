# Javascript

#Two Sum
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Output: Because nums[0] + nums[1] == 9, we return [0, 1].

``` var twoSum = function(nums, target) {
let ans=[];
let map = new Map();

for(let i=0;i<nums.length;i++)
{
map.set(nums[i],i);
}
for(let i=0;i<nums.length;i++)
{
if(map.has(target-nums[i]) && map.get(target-nums[i])!=i){
ans.push(i)
ans.push(map.get(target-nums[i]));
break;
}
}
return ans;
} ```
