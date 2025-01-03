# leetcode1822題
## 1822. Sign of the Product of an Array
今天來解leetcode的第1822題，讓我們先稍微看一下題目，大致上的意思就是將一個陣列裡面的數字全部*起來，如果出來的數字是負數就回傳-1，正數就回傳1，0就回傳0。

![](https://i.imgur.com/SA22mC1.png)

好的，首先我們希望可以增加速度，所以在程式一開始就直接確認*起來會不會是0，所以我們輸入:

if 0 in nums:
    
&emsp;    return 0
    
&emsp;   exit()

接著，我們需要把東西*起來，我們使用for迴圈，這樣就可以從第一個項目開始往後面的項目*:

for i in range(1,len(nums)):
    
    product=product*nums[i]

ok，最後我們只需要將我們算出的答案做出判斷，再回傳出去就好了:

if product>0:
    
&emsp;  return 1

else:
    
&emsp;   return -1

最後我們上去測試一下，看起來是還可以啦。

![](https://i.imgur.com/TtRN6Yi.png)
