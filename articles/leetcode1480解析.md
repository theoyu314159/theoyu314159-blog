#leetcode1480
##1480. Running Sum of 1d Array

來看一下這次的題目吧，也是從easy random的，這次解1480:

![](https://i.imgur.com/G6Oych0.png)

來他希望我們把陣列中的數，用成前幾個數加起來的樣子，那我們先設陣列和for迴圈:

ans=[]
        
last=0
        
for i in range(len(nums)):

接下來好好運用陣列和變數:

ans.append(last+nums[i])
            
last+=nums[i]

last就是加上上一次的最高數，所以這次加上最高數就放進陣列，接下來我們只要return ans就好了喔:

![](https://i.imgur.com/OPvpBPS.png)
