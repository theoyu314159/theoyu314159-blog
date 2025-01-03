#leetcode992題
##922. Sort Array By Parity II
今天我們來解leetcode的第992題，922. Sort Array By Parity II，一樣式我們讓leetcode從easy裡面隨機挑選的，那我們就來稍微看一下他的題目描述吧。

![](https://i.imgur.com/c3f4Uj4.png)

好的，看起來他希望我們能將他給的陣列中的數字排成一個偶數一個奇數，或是一個奇數一個偶數的排法，所以我們應該只要先把他的偶數和奇數區分出來就好了吧?

讓我們先設定三個陣數，分別是奇數,偶數,答案:

ans=[]
        
odd=[]
        
even=[]

接著呢，我們要來將偶數跟奇數區分一下，我們用%2來區分好了，就是看到能不能整除2，能的話就是偶數，不能就是奇數:

for i in range(len(nums)):
    
    &emsp;if nums[i]%2==0:
        
        &emsp;&emsp;odd.append(nums[i])
    
    &emsp;else:
        
        &emsp;&emsp;even.append(nums[i])

好的，既然我們已經分類好了，我們就可以來將他存到ans裡面了，我們使用for迴圈去跑奇數或偶數的長度，然後讓他每次回圈先新增奇數再新增偶數，或先新增偶數再新增奇數:

 for y in range(len(odd)):
    
    &emsp;ans.append(odd[y])
    
    &emsp;ans.append(even[y])
最後return ans 就完成囉。

![](https://i.imgur.com/C8f4uZG.png)
    