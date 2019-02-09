---
layout: post
#标题配置
title:  动态规划 
#时间配置
date:   2019-02-08 17:46:45 +0800
#大类配置
categories: document
#小类配置
tag: 教程
---

* content
{:toc}

#Python： lamda, map, filter, reduce
python zen 函数，有趣又有用的python单行函数。

###lambda 简单的单行函数，不可使用return 命令
```
mx = lambda x,y: x if x > y else y 
print(mx( 12, 15)) 

    lst = [i for i in range(1, 11)]

# normal
    def sq( lst):
          for i in range(len(lst)):
                  lst[i] = lst[i] ** 2
                  return lst

                  print(sq(lst))

#generation 
    def sq(lst):
          for i in range(len(lst)):
                  yield lst[i] ** 2

                  print(list(sq(lst)))

# lambda 单行函数
    print( list( map( lambda x : x**2, arr ) ) )
    print( [x**2 for x in arr] )                   

    ```
###map，对list 中的每一个元素，应用同一函数 （源自Lisp命令）
    ```
    lst = [i for i in range(1, 11)]
    print(list(map(lambda x: x**2, lst)))

    def sq(x):
          return x**2
          print(list(map(sq, lst)))
          ```
###filter 过滤list 中的元素
          ```
          lst = [i for i in range(1, 11)]
          print(list(filter(lambda x: x>2, lst)))
    ```
###reduce 类似递归
    List, [m, n, p]  ==> Reduce ==> f[f[m, n], p]
    ```
    from functools import reduce
    lst = [i for i in range(1, 11)]
    print(reduce(lambda x,y: x+y, lst))
    ```
