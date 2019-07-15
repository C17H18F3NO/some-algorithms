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
