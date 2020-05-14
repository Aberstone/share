# 利用两个转换进行1+1=2的证明

### 利用λ-演算中的丘奇数来进行 1 + 1 = 2 的证明

首先在 **λ-演算** 中定义对于任何数`n`，它的丘奇数是将其第一个参数应用到第二个参数上`n`次的函数。 那么关于自然数对应的丘奇数可以得出如下定义：

```haskell
0 = (λ s z . z)
1 = (λ s z . s z)
2 = (λ s z . s(s z))
...
5 = (λ s z . s(s(s(s(s z)))))
```

首先我们可以明确 **λ-演算** 中 加法的定义

```haskell
let add = (λ x y s c . x s (y s z)) = (λ x y . (λ s z . x s (y s z)))
(add 1 1 news newz)
(add (λsz.sz) (λsz.sz) news newz)
/* 利用add的定义 */
((λ s z . (λ s1 z1.s1 z1) s ((λ s2 z2.s2 z2) s z)) news newz)
((λ s z . (λ s1 z1 . s1 z1) s (s z)) news newz)
((λ s z. s(s z)) news newz)
//可知 1 + 1 = 2 （丘奇数）
```

### 

