#leetcode1317題
##1317. Convert Integer to the Sum of Two No-Zero Integers

這次又來到隨機從leetcode的easy選一個來寫的環節了，這一次要來寫這一題，1317題，看一下題目吧:

![](https://i.imgur.com/4GfJznp.png)

好的，看起來他要叫我們讓數字可以兩個加起來跟n依樣，並且不能有0出現，所以我們需要先寫一個for迴圈來判斷:

for i in range(1,n):

再來，我們需要做判斷式，我就直接寫在一行，請大家自己判讀囉:

if (n-i)%10 !=0  and '0' not in str(n-i) and '0' not in str(i):

我們把該判斷的都判斷好了，接下來只要找到後return [i,n-i]就好了:

![](https://i.imgur.com/VUtLjFh.png)
