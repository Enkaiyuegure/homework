求出下列表达式的值。
Calculate the value of the following expression.

1. 10

```scheme
10
```

2. 12

```scheme
(+ 5 3 4)
```

3. 8

```scheme
(- 9 1)
```

4. 3

```scheme
(/ 6 2)
```

5. 6

```scheme
(+ (\* 2 4) (- 4 6))
```

6. a=3

```scheme
(define a 3)
```

7. b=4

```scheme
(define b (+ a 1))
```

8. 19

```scheme
(+ a b (\* a b))
```

9. false

```scheme
(= a b)
```

10. 4

```scheme
(if (and (> b a) (< b (* a b)))
    b
    a)
```

11. 16

```scheme
(cond ((= a 4) 6)
      ((= b 4) (+ 6 7 a))
      (else 25))
```

12. 6

```scheme
(+ 2 (if (> b a) b a))
```

13. 16

```scheme
(* (cond ((> a b) a)
         ((< a b) b)
         (else -1))
    (+ a 1))
```
