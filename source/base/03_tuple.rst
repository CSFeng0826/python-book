Tuple 元組
====================================

Tuple (元組) 與串列非常相似，不同之處在於元組的元素不能修改。元組的宣告方式為 ``小括號()`` ，元素之間用逗號隔開。

元組中的元素類型也可以不相同，如以下範例程式：

.. code-block:: python

    tuple1 = ('abcd', 786, 2.23, 'runoob', 70.2)
    print (tuple) #輸出完整元組
    print (tuple[0]) #輸出元組的第一個元素
    print (tuple[1:3]) #輸出從第二個元素開始到第三個元素
    print (tuple[2:]) #輸出從第三個元素開始的所有元素

以上範例程式輸出結果如下：

.. code-block:: console

    ('abcd', 786, 2.23, 'runoob', 70.2)
    abcd
    (786, 2.23)
    (2.23, 'runoob', 70.2)

雖然元組的元素不可改變，但它可以包含可變的對象，比如 ``list (串列)`` 。

構造包含 0 個或 1 個元素的元組比較特殊，所以有一些額外的語法規則：

.. code-block:: python

    tup1 = () # 空元組
    tup2 = (20,) # 一個元素，需要在元素後添加逗號

修改元組
-----------------------------------------

元組中的元素值是不允許修改的，但可以對元組進行連接組合，如下實例:

.. code-block:: python
    
    tuple1 = (12, 34.56) 
    tuple2 = ('abc', 'xyz') 

    #以下修改元組元素操作是非法的。
    # tup1[0] = 100 

    #創建一個新的元組
    tuple3 = tuple1 + tuple2 
    print(tuple3) 

以上的輸出結果如下：

.. code-block:: console

    (12, 34.56, 'abc', 'xyz')

刪除元組
-----------------------------------------

元組中的元素值是不允許刪除的，但可以使用 ``del`` 語句來刪除整個元組，如下實例；

.. code-block:: python
    
    tuple1 = ('Google', 'Runoob', 1997, 2000) 
    print(tuple1) 

    del tuple1 
    print("刪除後的元組tuple:") 
    print(tuple1)

以上的輸出結果如下：

.. code-block:: console

    ('Google', 'Runoob', 1997, 2000)
    刪除後的元組tuple:
    
    Traceback (most recent call last)
    <ipython-input-40-32585f2b89c6> in <module>
        4 del tuple1
        5 print("刪除後的元組tup:")
    ----> 6 print(tuple1)

    NameError: name 'tuple1' is not defined

元組運算符
-----------------------------------------

元組中的操作符與字串相似，有以下幾種操作符：

- ``+``：組合元組
- ``*``：重複元組數量
- ``in、not in``：檢查員素是否存在於元組中

如以下程式範例：

.. code-block:: python
    
    print((1, 2, 3) + (4, 5, 6))
    print(('Hi!',) * 4)
    print(3 in (1, 2, 3))

以上的輸出結果如下：

.. code-block:: console

    (1, 2, 3, 4, 5, 6)
    ('Hi!', 'Hi!', 'Hi!', 'Hi!')
    True

元組內置函數
-----------------------------------------

Python 元組包含了以下內置函數

- ``len(tuple)``：計算元組元素個數
- ``max(tuple)``：返回元組中元素最大值
- ``min(tuple)``：返回元組中元素最小值
- ``tuple(iterable)``：將可迭代序列轉換為元組

如以下程式範例：

.. code-block:: python

    tuple1 = {10, 9, 8, 7, 6}

    print("元組長度為", len(tuple1))
    print("元組最大值為", max(tuple1))
    print("元組最小值為", min(tuple1))

    list1 = [1, 2, 3, 4, 5]
    print("將串列轉換為元組", tuple(list1))

以上的輸出結果如下：

.. code-block:: console

    元組長度為 5
    元組最大值為 10
    元組最小值為 6
    將串列轉換為元組 (1, 2, 3, 4, 5)