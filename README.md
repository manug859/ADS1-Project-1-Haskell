# Haskell

## Proyecto 1

### Summary
Introduction into Haskell concepts such as types, functions and high order function.

### Some interesting functions of this project 

``` haskell 
paratodo'' :: [a] -> (a -> Bool) -> Bool
paratodo'' xs f = paratodo' xs f
```
Where 'f' is any function with 'a -> Bool'

### Example
``` haskell 
paratodo'' :: [a] -> (a -> Bool) -> Bool 
paratodo'' xs f = paratodo' xs esPrimo

esPrimo :: Int -> Bool
esPrimo n = (n>1) && not(existeDivisor n [2..n-1])

existeDivisor :: Int -> [Int] -> Bool
existeDivisor n xs = existe' xs (divisor n)

divisor :: Int -> Int -> Bool--6)d.1)
divisor n x = mod n x == 0

existe' :: [a] -> (a -> Bool) -> Bool --b)
existe' [] f = False
existe' (x:xs) f = f x || existe' xs f
```
