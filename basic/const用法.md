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

