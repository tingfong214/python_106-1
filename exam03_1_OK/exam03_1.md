﻿# 身分證檢驗 #

## 說明 ##

我國的身分證字號有底下這樣的規則，因此對於任意輸入的身分證字號可以有一些基本的判斷原則，請您來判斷一個身分證字號是否是正常的號碼(不代表確有此號、此人)。<br>
(1) 英文代號以下表轉換成數字<br>

```
      A=10 台北市     J=18 新竹縣     S=26 高雄縣
      B=11 台中市     K=19 苗栗縣     T=27 屏東縣
      C=12 基隆市     L=20 台中縣     U=28 花蓮縣
      D=13 台南市     M=21 南投縣     V=29 台東縣
      E=14 高雄市     N=22 彰化縣     W=32 金門縣
      F=15 台北縣     O=35 新竹市     X=30 澎湖縣
      G=16 宜蘭縣     P=23 雲林縣     Y=31 陽明山
      H=17 桃園縣     Q=24 嘉義縣     Z=33 連江縣
      I=34 嘉義市     R=25 台南縣

```
<br>

```

      {'A':10,'J':18,'S':26,
       'B':11,'K':19,'T':27,
       'C':12,'L':20,'U':28,
       'D':13,'M':21,'V':29,
       'E':14,'N':22,'W':32,
       'F':15,'O':35,'X':30,
       'G':16,'P':23,'Y':31,
       'H':17,'Q':24,'Z':33,
       'I':34,'R':25}

```


(2) 英文轉成的數字, 個位數乘９再加上十位數的數字<br>
(3) 各數字從右到左依次乘１、１、２、３、４．．．．８<br>
(4) 求出(2),(3) 及最後一碼的和<br>
(5) (4)除10 若整除，則為 real，否則為 fake<br>

```
例： T112663836 
此時T = 27
2 + 7*9 + 1*8 + 1*7 + 2*6 + 6*5 + 6*4 + 3*3 + 8*2 + 3*1 + 6 = 180
180除以 10 為整除，因此為 real 
```


## Input Format ##

身分證字號<br>

## Output Format ##

real or fake<br>


## Sample Input 1 ##
```
T112663836
```

## Sample Output 1 ##
```
real
```
## Sample Input 2 ##
```
S154287863
```

## Sample Output 2 ##
```
fake
```

## Hint ##

```


```
