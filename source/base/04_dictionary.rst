Dictionary 字典
====================================

Dictionary (字典) 是除了串列以外 Python 之中最靈活的數據結構類型。列表是 **有序的** 數據類型，而字典是 **無序的** 數據集合。

字典與串列的區別在於，字典當中的元素是通過 ``Key (鍵)`` 來存取，而串列是透過 ``index (索引值)`` 來取值。

字典用 ``{}`` 宣告，由 ``Key (鍵)`` 和與 ``Key (鍵)`` 對應的 ``Value (值)`` 組成，此外在同一個字典中， ``Key (鍵)`` 必須是唯一的，如以下程式範例：

.. code-block:: python

    dict = {}
    dict['one'] = "This is one"
    dict[2] = "This is two" 
    dict2 = {'name':'john' , 'code':6734 , 'dept':'sales'}

    print(dict['one'])
    print(dict[2])
    print(dict2)

以上範例程式輸出結果如下：

.. code-block:: console

    This is one
    This is two
    {'dept': 'sales', 'code': 6734, 'name': 'john'}

在字典中，我們可以使用 ``keys()`` 取得字典裡所有的鍵值，以及 ``values()`` 取得字典裡所有的值。

.. code-block:: python

    dict2 = {'name':'john' , 'code':6734 , 'dept':'sales'}
    print(dict2.keys())
    print(dict2.values)

以上範例程式輸出結果如下：

.. code-block:: console

    ['dept', 'code', 'name']
    ['sales', 6734, 'john']

- 注意：字典的關鍵字必須為不可變類型，且不能重複。

修改字典
-----------------------------------------

向字典添加新內容的方法是增加新的 ``鍵/值`` 對，修改或刪除已有 ``鍵/值`` 對如下實例:

.. code-block:: console

    dict1 = {'Name':'Runoob', 'Age':7, 'Class':'First'}
    
    dict1 ['Age'] = 8 # 更新 Age 
    dict1 ['School'] = "Feng Chia University" # 添加信息

    print ("dict['Age']:", dict1['Age']) 
    print ("dict['School']:", dict1['School'] )

以上範例程式輸出結果如下：

.. code-block:: python

    dict['Age']: 8
    dict['School']: Feng Chia University

刪除字典元素
-----------------------------------------

在 Python 中能刪除單一的元素也能清空字典，而清空只需一項操作。

刪除一個字典可以使用 ``del`` 命令，如下實例：

.. code-block:: python

    dict1 = {'Name':'Runoob', 'Age':7, 'Class':'First'}
    print(dict1)

    del dict1['Name'] #刪除鍵'Name' 
    print(dict1)

    dict1.clear() #清空字典
    print(dict1) 

    del dict1 #刪除字典
    print(dict1)

以上範例程式輸出結果如下：

.. code-block:: console

    {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}
    {'Age': 7, 'Class': 'First'}
    {}

    Traceback (most recent call last)
    <ipython-input-54-529ce8948047> in <module>
        9 
        10 del dict1 #刪除字典
    ---> 11 print(dict1)

    NameError: name 'dict1' is not defined

字典鍵的特性
-----------------------------------------

字典值可以是任何的 Python 對象，既可以是標準的對象，也可以是使用者定義的，但鍵不行。

兩個重要的點需要記住：

1. 不允許同一個鍵出現兩次。創建時如果同一個鍵被賦值兩次，後一個值會被記住，如下實例：

.. code-block:: python

    dict1 = { 'Name':'Runoob', 'Age':7, 'Name':'John'}
    print ("dict1['Name']:", dict1['Name'])

以上範例程式輸出結果如下：

.. code-block:: console

    dict1['Name']: John

2. 鍵必須不可變，所以可以用數字，字串或元組充當，而用串列就不行，如下實例：

.. code-block:: python

    dict1 = {['Name']:'Runoob', 'Age':7}
    print("dict1['Name']:", dict1['Name'])

以上範例程式輸出結果如下：

.. code-block:: console

    Traceback (most recent call last)
    <ipython-input-56-e809afd64406> in <module>
    ----> 1 dict1 = {['Name']:'Runoob', 'Age':7}
        2 print("dict1['Name']:", dict1['Name'])

    TypeError: unhashable type: 'list'

字典內置函數以及方法
-----------------------------------------

Python 字典包含了以下內置函數：

- ``len(dict)``：計算字典元素個數，即鍵的總數
- ``str(dict)``：輸出字典，以可打印的字串表示
- ``type(variable)``：返回輸入的變數類型，如果變數是字典就返回字典類型

Python 字典還包含了以下內置方法：

- ``dict.clear()``：刪除字典內所有元素
- ``dict.copy()``：返回一個字典的複製
- ``dict.fromkeys()``：創建一個新字典，以序列中元素做為字典的鍵，``val`` 為字典所有鍵對應的初始值
- ``dict.get(key, default=None)``：返回指定鍵的值，如果值不在字典中返回 ``default`` 值
- ``key in dict``：如果鍵在 ``字典 dict`` 裡返回 ``true``，否則返回 ``false``
- ``dict.items()``：以串列返回可遍歷的 ``(key, value)`` 元組數組
- ``dict.keys()``：返回一個迭代器，可以使用 ``list()`` 來轉換為串列
- ``dict.setdefault(key, default=None)``：和 ``get()`` 類似，但如果鍵不存在於字典中，將會添加鍵並將值設為 ``default``
- ``dict.update(dict2)``：把字典 ``dict2`` 的鍵/值對更新到 ``dict`` 裡
- ``dict.values()``：返回一個迭代器，可以使用 ``list()`` 來轉換為串列
- ``pop(key[,default])``：刪除字典給定鍵 ``key`` 所對應的值，返回值為被刪除的值。``key`` 值必須給出。否則返回 ``default`` 值
- ``popitem()``：隨機返回並刪除字典中的最後一對鍵和值