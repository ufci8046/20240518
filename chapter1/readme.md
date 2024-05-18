# GenAI_Algorithm_lab1 ==> 二元搜尋樹的各種實作(heap sort)
- `提問詞`:請寫出heap sort的演算法
- `提問詞`:請計算heap sort演算法的時間複雜度
- `提問詞`:請用Python寫出heap sort的演算法
- `提問詞`:請用C寫出heap sort的演算法
- `提問詞`:請用C++寫出heap sort的演算法
- `提問詞`:請用JAVA寫出heap sort的演算法
- `提問詞`:請用Rust寫出heap sort的演算法
- `提問詞`:請用go寫出heap sort的演算法
- `提問詞`:請用C#寫出heap sort的演算法
- `提問詞`:請用Javascript#寫出heap sort的演算法
## heap sort（Binary Search Tree, BST）
## Python實作
- `提問詞`:請寫出heap sort的演算法
- `Copilot的回答`:
  - 當然可以！以下是Heap Sort的Python演算法示例：

# -*- coding: utf-8 -*-

def heapify(arr, n, i):
    largest = i
    l = 2 * i + 1  # left = 2*i + 1
    r = 2 * i + 2  # right = 2*i + 2

    # 如果左子節點存在且大於根節點，則更新最大值
    if l < n and arr[i] < arr[l]:
        largest = l

    # 如果右子節點存在且大於根節點，則更新最大值
    if r < n and arr[largest] < arr[r]:
        largest = r

    # 如果最大值不是根節點，則交換並繼續堆化
    if largest != i:
        arr[i], arr[largest] = arr[largest], arr[i]
        heapify(arr, n, largest)

def heapSort(arr):
    n = len(arr)

    # 建立最大堆
    for i in range(n // 2, -1, -1):
        heapify(arr, n, i)

    # 一次提取元素並重新堆化
    for i in range(n - 1, 0, -1):
        arr[i], arr[0] = arr[0], arr[i]  # 交換
        heapify(arr, i, 0)

# 範例使用的數組
arr = [12, 11, 13, 5, 6, 7]
heapSort(arr)
n = len(arr)

print("排序後的數組：")
for i in range(n):
    print(arr[i])


# 範例使用的數組
arr = [12, 11, 13, 5, 6, 7]
heapSort(arr)
n = len(arr)

print("排序後的數組：")
for i in range(n):
    print(arr[i])
```
這段程式碼實現了Heap Sort演算法，它通過建立一個二叉堆，並重複從堆中提取最大元素（在最大堆的情況下）來排序數組。Heap Sort的時間複雜度為O(n log n)，適用於大型數據集。1

- Online Python Interpreter
  - [Online Python Compiler (Interpreter) - Programiz](https://www.programiz.com/python-programming/online-compiler/)

