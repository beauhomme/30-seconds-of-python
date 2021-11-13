---
title: list_prime_numbers
tags: math,intermediate
firstSeen: 2021-11-13T21:00:00-04:00
---

Returns a list of all Prime numbers between two numbers 

* Takes two postive numbers and returns a list of all prime numbers between them. 
* Where no numbers are provided, the function will by default return prime numbers between 0 and 10

```py
def list_prime_numbers(min=0, max=10):
    primelist = []

    def checkPrime(num):
        flag = False

        if num > 1:
            for i in range (2, num):
                if num%i==0:
                    flag = True
                    break

        if num<=1 or flag:
            return 'NonPrime'
        else:
            return 'Prime'

    for i in range(min, max+1):
        if checkPrime(i)=='Prime':
            primelist.append(i)

    return primelist
```

```py
list_prime_numbers() # [2, 3, 5, 7]
list_prime_numbers(10, 30) # [11, 13, 17, 19, 23, 29]
```
