#leetcode961題
##961. N-Repeated Element in Size 2N Array

又來到這個環節了，從leetcode簡單中隨機挑選一題，這一次抽到961題，來看一下題目吧:
![](https://i.imgur.com/lxpeQjg.png)

好的，看來他要我們取在陣列中出現最多次的數，所以我們就用雙重迴圈吧:

for i in range(len(nums)):
            &emsp; for y in range(len(nums)):

接下來我們做判斷，如果有出現一樣的就輸出，並且要是不同數:

if nums[y] == nums[i] and i!=y:

接下來，我們只要return nums[i]，並且exit避免繼續偵測就好了:

![](https://i.imgur.com/N60xUp6.png)
