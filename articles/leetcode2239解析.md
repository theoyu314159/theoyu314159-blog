#leetcode2239題
##2239. Find Closest Number to Zero

又來到給leetcode easy中隨機挑選的部分了，這次我們選到2239題，讓我們來看一下題目。

![](https://i.imgur.com/dH5ujs4.png)

好的，看起來他希望我們可以做到把全部數字絕對值之後，找到最接近0的那一個數字，如果一樣的話，正數優先被我們選用，那首先，將他排序，這樣就會小到大了:

k=sorted(nums)
small=9999999999999999999999999999999999999999999999999999
smalli=0

上面設了兩個變數，一個是最小的i，一個是數字，接下來我們寫一個簡單的判斷式，如果裡面有0，就直接輸出0:

if 0 in nums:

&emsp; return 0

&emsp; exit(0)

接下來我們給他一個for迴圈，讓他可以每一個數字由小到大一個一個偵測，如果比前一個近就把最接近的換成這一個數字:

for i in range(len(nums)):
           
&emsp;if k[i]<0 and 0-k[i]<small:
      
&emsp;  &emsp;   smalli=k[i]
      
&emsp; &emsp;         small=0-k[i]
      
&emsp;      elif k[i]>0 and k[i]<=small:
      
&emsp;        &emsp;  smalli=k[i]
      
&emsp;         &emsp; small=k[i]

好的，最後我們只要將他return smalli就沒有問題了，不過這樣你會擔心他會不會例外中需要正數輸出的，不用擔心喔，因為我們有由小排到大，所以沒問題喔。

![](https://i.imgur.com/fOjpbfF.png)
           
