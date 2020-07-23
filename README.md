# daka_02
条件语句和循环语句

#这次所学的是条件和循环语句
与C做一个横向的对比的话可以发现：python有以下特点：
（1）if、else、elif、for、while的后面写完条件后要打上冒号，并且强制缩进
（2）python有assert关键词，可以用来在程序中置入检查点
（3）python的for循环里面用“ in ”判断条件成立与否
（4)有几个特殊的函数range()、enumerarte()
（5）它的推导式很有意思，能把计算、循环、判断都整合到一条语句里。不过要注意它的一些格式：
           列表[] 元组() 字典{} 集合{.....[]}
 (6)next()函数：
      next() 返回迭代器的下一个项目。
      next() 函数要和生成迭代器的iter() 函数一起使用。
      # 首先获得Iterator对象:
    it = iter([1, 2, 3, 4, 5])
    # 循环:
    while True:
        try:
            # 获得下一个值:
            x = next(it)
            print(x)
        except StopIteration:
            # 遇到StopIteration就退出循环
            break
            #用了next之后第一个元素就被删除了。
    
练习题：
    1.编写一个Python程序来查找那些可以被7除以5的整数的数字，介于1500和2700之间。
    
    x = [i for i in range(1500,2700) if i%7==0 and i%5==0]
    print(x)

    2.龟兔赛跑游戏
        
    v1=int(input())
    v2=int(input())
    t=int(input())
    s=int(input())
    l=int(input()) 
    distance1,distance2 = 0, 0  
    i = 0
    while distance1 < l and distance2 < l:
        distance1 += v1
        distance2 += v2
        i +=1
        if(distance1 == l or distance2 == l):
        break
        if(distance1 - distance2 >= t):
            distance1 -= s*v1    
                        
    if distance1 > distance2:
        print("R")
    elif distance1 < distance2:
        print("T")
    else:
        print("D") 
    print(i)
