
-----------------------------------------------------------------------------------------------------------


***倒计时***
i = input("input:")
i = int(i)
def countdown(i):
    print(i)
    if i <= 0:
        return
    else:
        countdown(i - 1)
countdown(i)

------------------------------------------------------------------------------------------------------------

***咳咳***
def word():
    print("不能")
    word2()
    print("切记")
    word3()
def word2():
    print("打游戏")
def word3():
    print("控制住你自己")
word()


---------------------------------------------------------------------------------------------------------


***阶乘***
def fact(x):
    if x == 1:
        return 1
    else:
        return x * fact(x - 1)
x = input("input:")
x = int(x)
print(fact(x))


------------------------------------------------------------------------------------------------------------


***快速排序***
def quicksort(array):
    if len(array) < 2:
        # 为空或者只包含一个元素的数组是有序的
        return array
    else:
        # 选择基标准
        pivot = array[0]
        # 由所有小于等于基标准的元素组成的子数组
        less = [i for i in array[1:] if i <= pivot]
        # 由所有大于基标准的元素组成的子数组
        greater = [i for i in array[1:] if i > pivot]
        return quicksort(less) + [pivot] + quicksort(greater)
print(quicksort([9, 5, 12, 3, 4, 25, 9, 45]))

------------------------------------------------------------------------------------------------------------

***广度优先搜索***

------------------------------------------------------------------------------------------------------------

***第n个斐波那契数列的数，（兔子序列，形如：0,1，1，2，3，5，8，13，21，34，55......）***
def fibonacci_sequence(n):
    # 第零个为0
    if n == 0:
        return 0
    # 第一个和第二个为1
    elif  n == 1 or n == 2:
        return 1
    # 第二个以后的数为前两个之和
    elif n >= 2:
        return fibonacci_sequence(n - 1) + fibonacci_sequence(n - 2)
    else:
        return -1
print(fibonacci_sequence(25))




