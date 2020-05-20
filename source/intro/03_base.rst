基礎語法
====================================

Python 識別字
------------------------------------------

識別字 (identifier) 為程式語言中依程式需求自行定義的名稱，例如程式中所用的變數、函數名稱等等。

在 Python 中，識別字是由英文字母 ( a-z, A-Z )、數字 ( 0-9 ) 以及底線 ( _ ) 所組成的。所有的識別字都可以包括英文字母、數字以及底線，但不能以數字回開頭。::

    a1, a_2, var3 ......

除此之外，在 Python 中識別字的字母大小寫是被視為不同的。::

    A1 與 a1 為不同的識別字

以底線開頭的識別字是有特殊意義的。以單底線開頭 ``_foo`` 代表不能直接訪問的類別屬性，需通過類別提供的方法進行訪問；以雙底線開頭的 ``__foo`` 代表類別的私有成員；以雙底線開頭和結尾的 ``__foo__`` 代表 Python 裡特殊方法專用的標識。

Python 保留字
------------------------------------------

在 Python 中，有許多*保留字* (關鍵字) 是不能用來當作常數、變數、函式或任何識別字的名稱。

所有 Python 關鍵字都為小寫英文字母，以下表格為 Python 中的保留字列表。

+------+------+------+---------+-------+------+------+-------+------+
|and   |exec  |not   |assert   |finally|or    |break |for    |pass  |
+------+------+------+---------+-------+------+------+-------+------+
|class |from  |print |continue |global |raise |def   |if     |return|
+------+------+------+---------+-------+------+------+-------+------+
|del   |import|try   |elif     |in     |while |else  |is     |with  |
+------+------+------+---------+-------+------+------+-------+------+
|except|lambda|yield |         |       |      |      |       |      |
+------+------+------+---------+-------+------+------+-------+------+

縮排以及空格
------------------------------------------

Python 與其他語言最大的不同在於，Python 的程式區塊不是使用 ``{}`` 來控制，而是使用縮排，縮排的空格是可變的，但是在程式碼中所有的縮排空格數量必須相同，如下面程式範例，否則會引發錯誤。

.. code-block:: python

    if True:
        print("True")
    else:
        print("False")

若縮排空格數量異常，會引發 ``IndentationError`` 例外，如下面程式碼範例:

.. code-block:: python
    :emphasize-lines: 2

    if True:
    print("True")
    else:
        print("False")

執行以上的程式碼會出現以下錯誤訊息:

.. code-block:: console

    $ python test_indentation.py
      File "test_indentation.py", line 2
        print("True")
            ^
    IndentationError: expected an indented block 

多行語法
------------------------------------------

在 Python 語法中通常以換行符號作為語法的結束，但是在 Python 中我們可以使用*反斜線*將一行的語法分為多行顯示，如下面程式範例：

.. code-block:: python

    test_str = "Hello World!" + \
               "This is example."

若語法為 ``[]``, ``{}`` 或 ``()`` 則不需要反斜線即可實現多行語法，如以下程式範例：

.. code-block:: python

    test_list = ["Hello World!",
                 "This is example."]

Python 引號
------------------------------------------

在 Python 中可以使用單引號 ``'``、雙引號 ``"`` 以及三引號 ``''' or """`` 來表示字串，無論何種引號其開始及結束都必須為同類型的引號，其中三引號可以由多行字串組成。

.. code-block:: python

    str1 = 'word 1'
    str2 = "This is string"
    str3 = """ Hello World!
    This is example."""

Print 輸出
------------------------------------------

在 Python 中可以使用 ``print()`` 進行字串的輸出，``print()`` 默認的輸出是換行的，如以下程式範例：

.. code-block:: python

    str1 = 'word 1'
    str2 = """Hello World!
    This is example."""
    number1 = 10

    print(str1)
    print(str2)
    print(number1)

以上程式範例的輸出結果為：

.. code-block:: console

    word 1
    Hello World!
    This is example.
    10

``print()`` 還有許多應用方式，詳細應用可以參考後續章節。

Python 註解
------------------------------------------

Python 中的單行註解使用 ``#`` 開頭或者於句末使用，如以下程式範例：

.. code-block:: python

    # 註解一
    print("Hello World!")

    print("Hello World!") # 註解二

另外，多行註解使用三引號進行撰寫，如以下程式範例：

.. code-block:: python

    '''
    三個單引號的多行註解
    三個單引號的多行註解
    '''

    """
    三個雙引號的多行註解
    三個雙引號的多行註解
    """