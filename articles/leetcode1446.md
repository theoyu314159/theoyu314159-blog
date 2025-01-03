#leetcode1146
##1446. Consecutive Characters

今天又到了random的環節，這次來1446. Consecutive Characters，先稍微看一下題目吧:

![](改天補上pic)

看起來非常簡單，先設個變數吧:

longarr=[]

last=''

longs=0

ans=0


接下來寫迴圈並且判斷長度後放進longarr:

 for i in range(len(s)):
          
  if s[i]==last:
             
   longs+=1
          
  else:
           
     longs=0
         
   longarr.append(longs)
          
  last=s[i]

接下來在迴圈中找出最大的數字:

for k in range(len(longarr)):
          

  if longarr[k]>ans:
            

    ans=longarr[k]

最後return ans就完成囉。

![](pic補上)

