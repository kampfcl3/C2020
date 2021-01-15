# main函式命令行輸入
```
int main(int argc, char* argv[])
{
  statement1
}
```
用途:
  開啟檔案時給予的輸入資料，將其使用在main函式中。

## 名詞解釋
> argc
```
型別: int
輸入的資料總數(包含程式名)
```
> * argv[]
```
型別: char * array
儲存輸入的資料
ex:
argv[0] = test.exe
argv[1] = data1
argv[2] = data2
```
## 開啟方法
在cmd中將程式exe開啟
```
cmd:
D://a/hello.exe hello world
```

## 參考資料
> [welkin 痞客幫:參數解釋](https://welkinchen.pixnet.net/blog/post/18122440--int-main%28int-argc%2C-char%2A-argv%5B%5D%29-%E5%8F%83%E6%95%B8%E7%9A%84%E4%BD%9C%E7%94%A8)  
