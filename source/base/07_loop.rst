循環語法
====================================

Python 中的循環語法有 ``for`` 和 ``while``，控制結構圖如下所示：

..  image:: ../pic/loop.png
    :align: center

while 循環語法
-----------------------------------------

Python 中 ``while`` 語法的一般形式如下：

.. code-block:: python

    while 判斷條件(condition):
        執行語句(statements)

執行流程圖如下：

..  image:: ../pic/while.png
    :align: center

以下實例使用了 ``while`` 來計算 1 到 100 的總和：

.. code-block:: python

    n = 100 
    answer = 0 
    counter = 1 

    while counter <= n :
        answer = answer + counter 
        counter += 1 
        
    print("1 到 %d 之和為: %d" % (n, answer))

以上範例程式輸出結果如下：

.. code-block:: console

    1 到 100 之和為: 5050

- 在 ``while`` 語法中同樣需要注意冒號和縮排。另外在 Python 中沒有 ``do..while`` 循環

**無限循環**

我們可以通過設置條件表達式永遠不為 ``false`` 來實現無限循環，實例如下：

.. code-block:: python

    var = True
    while var == True :   #表達式永遠為true 
        num = int(input("輸入一個數字: ")) 
        print("你輸入的數字是:", num)

當遇到無限循環可以使用 ``CTRL+C`` 來退出當前的無限循環，根據情況不同必須特別注意無限循環的狀況


**簡單語句組**

若 ``while`` 循環中只有一條程式碼，你可以將該程式碼與 ``while`` 寫在同一行中，如以下程式範例：

.. code-block:: python

    flag = True
    while flag: print ('Welcome!')

以上範例程式輸出結果如下：

.. code-block:: console

    Welcome!
    Welcome!
    Welcome!
    .
    .
    .

while...else 循環語法
-----------------------------------------

在 ``while...else`` 在條件語句為 ``false`` 時執行 ``else`` 的語句塊。

語法格式如下：

.. code-block:: python

    while 條件語法:
        程式碼區塊 1
    else:
        程式碼區塊 2

以下實例使用了 ``while...else`` 來循環輸出數字，並判斷大小：

.. code-block:: python

    count = 0
    while count < 5:
        print(count, "大於 5")
        count = count + 1
    else:
        print(count, "大於或等於 5")

以上範例程式輸出結果如下：

.. code-block:: console

    0 大於 5
    1 大於 5
    2 大於 5
    3 大於 5
    4 大於 5
    5 大於或等於 5