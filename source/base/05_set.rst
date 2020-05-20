Set 集合
====================================

Set (集合) 為 Python 中一個無序且內容不重複的序列，主要功能是進行元素之間的關係測試和刪除重複元素。

可以使用大括號 ``{}`` 或者 ``set()`` 函數創建集合，如以下範例程式：

- 注意：創建一個空集合必須用 ``set()`` 而不是 ``{}`` ，因為 ``{}`` 是用來創建一個空字典。

.. code-block:: python

    set1 = {'Tom', 'Jim', 'Mary', 'Tom', 'Jack', 'Rose'}
    print(set1)

由於集合本身為不重複的元素序列，因此重複的元素會被自動去掉，以上範例程式輸出結果如下：

.. code-block:: console

    {'Mary', 'Jim', 'Rose', 'Jack', 'Tom'}

集合添加元素
-----------------------------------------

將元素 ``x`` 添加到集合 ``s`` 中，如果元素已存在，則不進行任何操作語法，格式如下：

.. code-block:: python

    set1 = set(("Google", "Runoob", "Taobao")) 
    set1.add("Facebook") 
    print(set1) 

以上範例程式輸出結果如下：

.. code-block:: console

    {'Runoob', 'Google', 'Taobao', 'Facebook'}

還有一個方法，也可以添加元素，且參數可以是串列、元組、字典等，語法格式如下：

.. code-block:: python

    set1 = set(("Google", "Runoob", "Taobao")) 

    set1.update({5}) 
    print(set1) 

    set1.update({1, 3}) 
    print(set1)  

以上範例程式輸出結果如下：

.. code-block:: console

    {'Runoob', 'Google', 5, 'Taobao'}
    {1, 3, 5, 'Taobao', 'Runoob', 'Google'}

集合移除元素
-----------------------------------------

透過 ``remove()`` 方法將元素 ``x`` 從集合 ``s`` 中移除，如果素不存在，則會發生錯誤，語法格式如下：

.. code-block:: python

    set1 = set(("Google", "Runoob", "Taobao")) 
    set1.remove("Taobao") 
    print(set1) 

以上範例程式輸出結果如下：

.. code-block:: console

    {'Runoob', 'Google'}

此外還有一個 ``discard()`` 方法也是移除集合中的元素，且如果元素不存在，不會發生錯誤。格式如下所示：

.. code-block:: python

    set1 = set(("Google", "Runoob", "Taobao")) 
    set1.discard("Facebook") #不存在不會發生錯誤
    print(set1) 

以上範例程式輸出結果如下：

.. code-block:: console

    {'Runoob', 'Google', 'Taobao'}

也可以透過 ``pop()`` 方法 **隨機** 刪除集合中的一個元素，語法格式如下：

.. code-block:: python

    set1 = set(("Google", "Runoob", "Taobao")) 
    x = set1.pop()
    print(set1) 
    print(x)

以上範例程式輸出結果如下：

.. code-block:: console

    {'Google', 'Taobao'}
    Runoob

計算集合元素個數
-----------------------------------------

透過 ``len()`` 方法計算集合 ``s`` 元素個數，語法格式如下：

.. code-block:: python

    set1 = set(("Google", "Runoob", "Taobao")) 
    print(len(set1))

以上範例程式輸出結果如下：

.. code-block:: console

    3

清空集合
-----------------------------------------

透過 ``clear()`` 方法清空集合 ``s``

.. code-block:: python

    set1 = set(("Google", "Runoob", "Taobao")) 
    print(set1)
    set1.clear()
    print(set1)

以上範例程式輸出結果如下：

.. code-block:: console

    {'Runoob', 'Google', 'Taobao'}
    set()  

判斷元素是否在集合中存在
-----------------------------------------

判斷元素 ``x`` 是否在集合 ``s`` 中，存在返回 ``True``，不存在返回 ``False``

.. code-block:: python

    set1 = set(("Google", "Runoob", "Taobao")) 
    print("Google" in set1)
    print("Runoob" not in set1)

以上範例程式輸出結果如下：

.. code-block:: console

    True
    False 

集合內置方法
-----------------------------------------

Python 集合包含了以下內置方法：

- ``add()``：為集合添加元素
- ``clear()``：移除集合中的所有元素
- ``copy()``：複製一個集合
- ``difference()``：返回多個集合的差集
- ``difference_update()``：移除集合中的元素，該元素在指定的集合也存在
- ``discard()``：刪除集合中指定的元素
- ``intersection()``：返回集合的交集
- ``intersection_update()``：返回集合的交集
- ``isdisjoint()``：判斷兩個集合是否包含相同的元素，如果沒有返回 ``True``，否則返回 ``False``
- ``issubset()``：判斷指定集合是否為該方法參數集合的子集
- ``issuperset()``：判斷該方法的參數集合是否為指定集合的​​子集
- ``pop()``：隨機移除元素
- ``remove()``：移除指定元素
- ``symmetric_difference()``：返回兩個集合中不重複的元素集合
- ``symmetric_difference_update()``：移除當前集合中在另外一個指定集合相同的元素，並將另外一個指定集合中不同的元素插入到當前集合中
- ``union()``：返回兩個集合的並集
- ``update()``：給集合添加元素