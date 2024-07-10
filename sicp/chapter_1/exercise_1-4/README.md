描述下列过程的行为  
Describe the behavior of the below procedure

```scheme
(define (a-plus-abs-b a b)
        ((if (> b 0) + -) a b))
```

由过程名可知，此值是`a`加上`b`的绝对值。  
于是在`if`表达式中先判断`b`是否大于`0`。  
如果大于`0`，`b`的绝对值是`b`本身，算式为`a + b`；反之，`b`的绝对值是`b`的相反数，算式为`a - b`。  
From the name of the procedure, it is known that this value is `a` plus the absolute value of `b`.  
Therefore, in the `if` expression, it is first determined whether `b` is greater than `0`.  
If it is, the absolute value of `b` is `b` itself, and the formula is `a + b`.  
Otherwise, the absolute value of b is the negation of `b`, and the formula is `a - b`.
