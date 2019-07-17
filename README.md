# some-algorithms
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
