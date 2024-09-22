+++
title = '算法学习记录'
date = 2024-09-10T08:33:32+08:00

categories = ["算法" ] 
tags = ["算法", "记录"]

+++



# 滑动窗口





# 动态规划 DP









# 单调栈







# 合并区间

模板

1. 排序数组
2. 更新合并左右端点

```cpp

    vector<vector<int>> merge(vector<vector<int>> &intervals)
    {

        vector<vector<int>> ans;
        if (intervals.empty())
            return ans;

        sort(intervals.begin(), intervals.end()); // 先排序

        int l = intervals[0][0], r = intervals[0][1]; // 左右端点

        for (int i = 1; i < intervals.size(); i++) // 第二数组开始遍历
        {
            if (intervals[i][0] > r) // 第二数组的左端点大于上一数组的右端点, 则保存上一数组
            {
                ans.push_back({l, r});
                l = intervals[i][0], r = intervals[i][1]; // 更新左右端点
            }
            else
            {
                r = max(r, intervals[i][1]); // 否则更新右端点
            }
        }
        ans.push_back({l, r});
        return ans;
    }

```

