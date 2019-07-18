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
