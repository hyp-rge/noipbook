## 最大公约数:gcd

求解问题：两个整数a,b的最大公约数。

Code：

```c
int gcd(int a,int b){
    if(!b)return a;
    return gcd(b,a%b);
}
```


## 证明
gcd(a,b)=gcd(b,a%b)。

设r=a%b，则有a=kb+r。

设d为a,b的任意一个公因数，则有d∣a，d∣b→d∣r=a−kb；
另设d为b,r的任意一个公因数，则有d∣b，d∣r=a−kb→d∣a=kb+r。
由上可知d既是a,b的公因数，又是b,a%b的公因数，于是最大公约数也成立。命题得证。

http://blog.csdn.net/kanosword/article/details/52955557

## 最小公倍数lcm

根据小学的公式:

```math
lcm(a,b) = a \times b \div gcd(a,b)
```

code

```c
int lcm(int a,int b){
    return a*(b /gcd(a,b));
}
```

## 练习题目

 - luogu P1029 最大公约数和最小公倍数问题
 - luogo P1888 三角函数 入门难度
 - luogu P2651 添加括号III 入门难度
 - luogu P1372 又是毕业季I 洛谷原创 入门难度
 - luogu P4057 [Code+#1]晨跑
