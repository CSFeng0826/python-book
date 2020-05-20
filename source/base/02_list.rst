Python 串列
====================================

本章節會介紹串列的一些進階操作，例如新增、刪除等等。

串列的新增
-----------------------------------------

在 Python 中可以對串列的數據項進行修改或更新，也可以使用 ``append()`` 方法來添加串列的元素，如以下程式範例：

.. code-block:: python
    
    list1 = ['Google','Runoob' , 1997, 2000] 
    print("第三個元素為:", list1[2]) 

    list1[2] = 2001 
    print("更新後的第三個元素為:", list1[2])

    list1.append("test") 
    print("更新後的串列為:", list1)  

以上的輸出結果如下：

.. code-block:: console

    第三個元素為: 1997
    更新後的第三個元素為: 2001
    更新後的串列為: ['Google', 'Runoob', 2001, 2000, 'test']

串列的刪除
-----------------------------------------

在 Python 中可以使用 ``del`` 語句來刪除串列的元素，也可以使用串列的 ``remove()`` 方法進行元素的刪除，如以下程式範例：

.. code-block:: python
    
    list1 = ['Google', 'Runoob', 1997, 2000] 
    print("原始列表:", list1) 

    del list1[2] 
    print("刪除第三個元素:", list1) 

    list1.remove('Google')
    print("remove 後的串列:", list1) 

以上的輸出結果如下：

.. code-block:: console

    原始列表: ['Google', 'Runoob', 1997, 2000]
    刪除第三個元素: ['Google', 'Runoob', 2000]
    remove 後的串列: ['Runoob', 2000]

串列的腳本操作符
-----------------------------------------

串列對中的操作符與字串相似，有以下幾種操作符：

- ``+``：組合串列
- ``*``：重複串列數量
- ``in、not in``：檢查員素是否存在於串列中

如以下程式範例：

.. code-block:: python
    
    print([1, 2, 3] + [4, 5, 6])
    print(['Hi!'] * 4)
    print(3 in [1, 2, 3]) 

以上的輸出結果如下：

.. code-block:: console

    [1, 2, 3, 4, 5, 6]
    ['Hi!', 'Hi!', 'Hi!', 'Hi!']
    True

串列的函數以及方法
-----------------------------------------

在 Python 中可以使用內建的方法計算串列的數據，有以下幾種：

- ``len(list)``：回傳串列元素個數
- ``max(list)``：返回串列元素最大值
- ``min(list)``：返回串列元素最小值
- ``list(seq)``：將元祖轉換為串列

如以下程式範例：

.. code-block:: python
    
    list1 = [1, 2, 3, 4, 5]
    tuple1 = {10, 9, 8, 7, 6}

    print("串列長度為", len(list1))
    print("串列最大值為", max(list1))
    print("串列最小值為", min(list1))
    print("將元組轉換為串列", list(tuple1))

以上的輸出結果如下：

.. code-block:: console

    串列長度為 5
    串列最大值為 5
    串列最小值為 1
    將元組轉換為串列 [6, 7, 8, 9, 10]

此外，串列也有自己的方法可以進行操作，有以下幾種方法：

- ``list.append(obj)``：在串列末尾添加新的對象
- ``list.count(obj)``：統計某個元素在串列中出現的次數
- ``list.extend(seq)``：在串列末尾一次性追加另一個序列中的多個值
- ``list.index(obj)``：從串列中找出某個值第一個匹配的索引位置
- ``list.insert(index, obj)``：將對象插入串列
- ``list.pop([index=-1])``：移除串列中的一個元素（默認最後一個元素），並且返回該元素的值
- ``list.remove(obj)``：移除串列中某個值的第一個匹配項
- ``list.reverse()``：反向串列中元素
- ``list.sort(key=None, reverse=False)``：對原串列進行排序
- ``list.clear()``：清空串列
- ``list.copy()``：複製串列