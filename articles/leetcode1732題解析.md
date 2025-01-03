#leetcode1732題
##1732. Find the Highest Altitude
哈囉大家，我們今天要來隨便解一題leetcode，簡單的，所以我就讓leetcode自動幫我隨機選了一個，這次剛好選到1732. Find the Highest Altitude，看起來非常簡單，那我們來時做看看吧，先看一下說明。

![](https://i.imgur.com/K9MdJsF.png)

題目看起來是要請我們計算沿路的最高點，所以我們要記兩個變數，一個是先在當下的數字，另一個是我們紀錄的最告點，所以就先設變數:

high=0

now=0

相信我設的變數非常容易理解，我就不多解釋了，接下來呢，我們要寫一個for迴圈，去一直更改now的值:

for i  in range(len(gian)):

&emsp;now+=gain[i]

接下來，我們在回圈中，除了要記下當下的值，我們也要記錄最高值，所以放一個判斷式:

if now>high:

&emsp;high=now

最後，我們只要return high，最高值，也就是我們答案，就可以送出囉。

![](https://i.imgur.com/SOw24yQ.png)