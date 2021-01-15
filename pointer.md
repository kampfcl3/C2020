# pointer指標
## 例題
> *((char*)ptr+4))
```
#include<stdio.h> 
main() 
{ 
    int a[]={0,2,4,6,8}; 
    int *ptr; 
    ptr=a; 
    printf("%d", *((char*)ptr+4)); 
} 
```
將int *轉換成(char *)字串指標
由於int 通常占據4個位元，所以將其+4

## 參考資料
> [uwenku](http://hk.uwenku.com/question/p-hsgekaxg-xn.html)  
