# const

> const是constant，常數的縮寫  
```
1.常數是恆常不變的數值
2.一但經初始化就無法再改變其值
3.必須在宣告的時候便初始化
```
### 錯誤1
```
const int number; 

錯誤: const必須初始化
```
未給初始值會出錯

### 錯誤2
```
const double PI = 3.14;
PI = 4.0; 

錯誤: 常數無法修改
```
事後無法修改
###  const指標
```
char c = 'A';

const char * p1 = &c;
char * const p2 = &c;
const char *  const p3 = &c;
```
const 指標一樣必須初始化，但可以放在char *前面或後面(或前後都放)

> 1.限制「不可以改變p1地址本身」  
```
char c = 'A';
const char * p1 = &c;
*p1 = 'B'; //不合法，不可透過地址改變值
char other = 'C';
p1 = &other; //合法，可以改變指標本身
```
> 2.限制「不可以透過地址去改變變數p2的內容」  
```
char c = 'A';
char * const p2 = &c;
*p2 = 'B'; //合法，可透過地址改變值
char other = 'C';
p2 = &other; //不合法，不可以改變指標本身
```
> 3.不可改變地址也不可利用地址去改變變數內容  
```
char c = 'A';
const char *  const p3 = &c;
*p3 = 'B'; //不合法，不可透過地址改變值
char other = 'C';
p3 = &other; //不合法，不可以改變指標本身
```
### 例外:
> 變數是const，但指向它的指標不是會怎樣?
```
int main()
{
    const char c = 'A';
    char * const p = &c;
    *p = 'D';
    return 0;
}
```
我們設定字元c是一個const char，
根據const的效果，字元c一旦設定就不能修改

再設定p是一個不能改變地址的指標指向c(但根據上述效果說明，p所指的內容改變則不受限制)，
那麼請問可否透過*p = 'D';改變變數c的值呢?

> 答案是程式無法編譯通過
```
const char的效果使得字元c無法被修改，
char * const p = &c的效果又可以修改指標所指的內容

所以矛盾
```
## 資料來源
> [【c/c++學習筆記】難懂的const關鍵字，const v.s. 指標](https://ithelp.ithome.com.tw/articles/10230783)

