# some-algorithms

***二分查找***
def binary_search(list, item):
    left = 0
    right = len(list)-1
    while left <= right:
        mid = (left + right) //  2
        guess = list[mid]
        if guess == item:
            return mid
        if guess > item:
            right = mid - 1
        else:
            left = mid + 1
    return None
if __name__ == '__main__':
    my_list = [1,2,3,4,5,6]
    print(binary_search(my_list, 3))
    print(binary_search(my_list, -1))



---------------------------------------------------------------------------------------------------------

***排序***
def findSmallest(arr):
    smallest = arr[0]
    smallest_index = 0
    for i in range(1, len(arr)):
        if arr[i] < smallest:
            smallest = arr[i]
            smallest_index = i
    return smallest_index

def selectionSort(arr):
    newArr = []
    for i in range(len(arr)):
        smallest = findSmallest(arr)
        newArr.append(arr.pop(smallest))
    return newArr
print(selectionSort([12, 1, 2, 34, 5]))

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

-----------------------------------------------------------------------------------------------------------

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

