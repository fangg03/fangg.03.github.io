# fangg.03.github.io
hi

# 比較 int 整數 及 long long int 很長很長的整數 的差別。 
```cpp
#include <stdio.h>
int main()
{
    int n=9876543210;
    printf("int 印出來 %d\n", n);

    long long int a=9876543210;
    printf("long long int 印出來 %lld\n", a); ///是小寫L
}

```
# 上週的最大公因數, 改用 long long int 很長很長的整數來計算。
```cpp
#include <stdio.h>
int main()
{
    long long int a,b;
    scanf("%lld %lld", &a, &b);

    long long int ans;
    for(long long int i=1 ; i<=a ; i++){
        if(a%i==0 && b%i==0) ans=i;
    }
    printf("最大公因數是:%lld\n", ans);

}

```
# 輾轉相除法=改用 long long int 很長很長的整數來計算。
```cpp
#include <stdio.h>
int main()
{
    long long int a, b, c;
    scanf("%lld %lld", &a, &b);
    while(1){
        c =a % b;
        printf("a:%lld b:%lld c:%lld\n", a, b, c);
        if( c==0 ) break;
        a = b;
        b = c;
    }
    printf("答案是: %lld\n", b);
}

```
# 剝皮。
```cpp
#include <stdio.h>
int main()
{
    int n;
    scanf("%d", &n);

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;

    printf("現在的個位數:%d\n", n%10);
    n = n/10;
}
```
# 判斷質數
```
#include <stdio.h>
int main()
{
    int n;
    scanf("%d", &n);
    int bad=0;
    for(int i=2; i<n; i++){
        if( n%i==0 ) bad=1;
    }
    if( bad==0 ) printf("%d 是質數", n);
    else printf("%d 不是質數", n);
}
```
# 總和(熟悉迴圈)
```
#include <stdio.h>
int main()
{
    printf("請輸入 5個數字(要加起來): ");

    int n;
    int sum=0;
    for(int i=0; i<5; i++){
        scanf("%d", &n);
        sum += n;
    }
    printf("總和是:%d", sum);
}
```
# 直角星星(for迴圈)
```
# #include <stdio.h>
int main()
{
    int n;
    scanf("%d", &n);

    for(int i=1; i<=n; i++){
        for(int k=1; k<=n-i; k++) printf(" ");

        for(int k=1; k<=i; k++) printf("*");

        printf("\n");
    }
}
```
# 直角星星(for迴圈) 2.0
```
#include <stdio.h>
int main()
{
    int n;
    scanf("%d", &n);

    for(int i=1; i<=n; i++){
        for(int k=1; k<=n-i; k++) printf(" ");

        for(int k=1; k<=i; k++) printf("*");

        printf("\n");
    }
}
```
#　直角星星(while迴圈)

```
#include <stdio.h>
int main()
{
    int n;
    scanf("%d", &n);

    for(int i=1; i<=n; i++){
        for(int k=1; k<=n; k++){
            if(k<=n-i) printf(" ");
            else printf("*");
        }
        printf("\n");
    }
}
```
# 直角星星(while迴圈)2.0
```
#include <stdio.h>
int main()
{
    int n;
    scanf("%d", &n);

    int i=1;
    while(i<=n){
        int k=1;
        while(k<=n){

            if(k<=n-i) printf(" ");
            else printf("*");

            k++;
        }
    printf("\n");
    i++;
    }
}
