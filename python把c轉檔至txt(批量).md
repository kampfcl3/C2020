# python把c轉檔至txt(批量)

## ch2轉檔程式
```

textlist = ["prog2_1.c","prog2_2.c","prog2_3.c","prog2_4.c","prog2_5.c","prog2_6.c","prog2_7.c"]

textdata = "github_ch2.txt"
for i in range(7):
    with open("D:/a/ch2/"+textlist[i],"r",encoding="big5") as fileObject:



        line = fileObject.read()
        print(line)
    with open("D:/a/ch2/"+textdata, "a",encoding="utf-8") as listdata:
        listdata.write("```\n")
        listdata.write(line)
        listdata.write("```\n")


```
```
由於.c檔案的編碼不是utf8所以要改用big5編碼。
```
## 資料來源
> [編碼參考資料1](https://openhome.cc/Gossip/Encoding/Python.html)  
> [編碼參考資料2](https://openhome.cc/Gossip/Encoding/SourceFile.html)  
> [編碼參考資料3](https://kknews.cc/zh-tw/code/3xqak23.html)  
> [can't decode byte 0xb3問題](https://www.itread01.com/content/1544590633.html)  


## 其他
> [.c和.h檔案的區別](https://www.itread01.com/content/1541109847.html)  
