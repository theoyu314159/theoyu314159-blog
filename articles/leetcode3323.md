# leetcode3232
## 3232. Find if Digit Game Can Be Won

又到了隨機挑題目的環節了，這一次挑到3232. Find if Digit Game Can Be Won，來看看題目吧:

![](https://imgur.com/GmYloIl)

好的看來他要我們比較看能不能用小於10的數字獲勝或用>10的獲勝，所以就先來比較吧:

```
alice=0
        
bob=0
     

   for i in range(len(nums)):

            if nums[i]<10:

                alice+=nums[i]

            else:

                bob+=nums[i]
```

好的接下來查看有沒有依樣，就完成囉:

```
return alice != bob
```


我們就直接使用!=來解決:

![](https://imgur.com/ubWPJCi)
