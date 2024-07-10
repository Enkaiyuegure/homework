下列两个过程可以判断解释器是使用应用序还是正则序。  
The following two procedures can determine whether the interpreter is using applicative order or normal order.

```scheme
(define (p) (p))

(define (test x y)
        (if (= x 0)
        0
        y))
```

随后求值此表达式：  
Then evaluate this expression:

```scheme
(test 0 (p))
```

如果是应用序，会看到什么情况？正则序呢？为什么？  
What will you observe if it is applicative order? What about normal order? Why?

---

如果是应用序，那么其遵循“先求值参数而后应用”的求值模型。在此表达式中，解释器会先尝试求出`(p)`，但是`(p)`是个无限嵌套的过程，所以其进入无限循环，得不出结果。  
如果是正则序，那么其遵循“完全展开而后归约”的求值模型。在此表达式中，解释器会先查看`x`与`0`是否相等，得出结果相等，返回结果`0`。而`(p)`因为没有被使用，故不被解释器求值。  
If it is applicative order, it follows the evaluation model of `evaluate the arguments before applying the function`. In this expression, the interpreter will first try to evaluate `(p)`, but `(p)` is an infinitely nested process, so it will enter an infinite loop and will not produce a result.  
If it is normal order, it follows the evaluation model of `fully expand and then reduce`. In this expression, the interpreter will first check if `x` is equal to `0`. If it finds that they are equal, it will return the result `0`. Since `(p)` is not used, it will not be evaluated by the interpreter.
