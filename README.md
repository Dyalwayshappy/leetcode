#两数之和
class solution(object):
    def twosum(self, nums, target):
        for i in range(len(nums)):
            for j in range(i + 1, len(nums)):
                if nums[i] + nums[j] == target:
                    return [i,j]


        return []

#方法2
class Solution:
    def twoSum(self, nums : list[int], target : int) -> list[int]:
        idx = {} #创建一个空的字典
        for j, x in enumerate(nums):  #x = num[j]
            if target - x in idx: #从j的左边开始找num[i]， 满足 num[i] + num[j] (x) == target
                return [idx[target - x], j]
            idx [x] = j
