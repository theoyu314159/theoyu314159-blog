# leetcode283題

## 283. Move Zeroes

又來到了這一個隨機取leetcode題目寫的環節了，但是呢?我寫到一半時，我發現了一個天大的問題，我們先看看題目:

![](https://i.imgur.com/EkCahNh.png)

好的，看來我們只能用nums這一個array，我先給你們我的程式，再來看看奇怪的問題:

```

class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        for i in range(len(nums)):
            if nums[i]==0:
                del nums[i]
                nums.append(0)
        return nums

```

我今天不是來講解的，所以就直接探討問題，這一個程式跑起來會有點問題:

![](https://i.imgur.com/VyOCT6O.png)

![](https://i.imgur.com/OaB84aq.png)

好的，我在兩邊執行卻都解果不依樣，但按照邏輯我的程式應該沒問題啊...

求解...
