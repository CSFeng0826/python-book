函數
====================================

函數是可重複使用的，用來實現單一，或相關聯功能的程式碼區塊。

函數能提高應用的模組性，和程式碼的重複利用率。Python 提供了許多內建函數，比如 ``print()``。但也可以自己創建函數，叫做用戶自定義函數。

定義一個函數
-----------------------------------------

你可以定義一個由自己想要功能的函數，以下是簡單的規則：

- 函數程式碼區塊以 ``def`` 關鍵字開頭，後接函數識別字名稱和 ``括號 ()``。
- 任何傳入參數和變數 **必須** 放在括號中間，括號之間可以用於定義參數。
- 函數的第一行程式碼可以選擇性地使用文檔字串 **用於存放函數說明** 。
- 函數內容以 **冒號起始** ，並且縮進。
- ``return [表達式]`` 結束函數，選擇性地返回一個值給調用方。不帶表達式的 ``return`` 相當於返回 ``None`` 。

格式範例如下：

.. code-block:: python
    
    def 函數名稱(参数列表):
        程式碼區塊

定義完函數之後，我們即可使用定義好的函數，如以下程式範例：

.. code-block:: python
    
    def hello() :
        print("Hello World!")

    hello()

以上的輸出結果如下：

.. code-block:: console

    Hello World!

以下為帶有參數的函數範例：

.. code-block:: python
    
    def 函數名稱(参数列表):
        程式碼區塊

定義完函數之後，我們即可使用定義好的函數，如以下程式範例：

.. code-block:: python
    
    def area(width, height):
        return width * height

    def print_welcome(name):
        print("Welcome", name)
        
    print_welcome("Python")

    w = 4
    h = 5
    print("width =", w, " height =", h, " area =", area(w, h))

以上的輸出結果如下：

.. code-block:: console

    Welcome Python
    width = 4  height = 5  area = 20   

return 
-----------------------------------------

``return [表達式]`` 用於退出函數，選擇性地向調用方返回一個表達式。不帶參數值的 ``return`` 返回 ``None`` 。之前的例子都沒有示範如何返回數值，以下實例演示了 ``return`` 的用法：

.. code-block:: python
    
    def sum_num(arg1, arg2):
        total = arg1 + arg2
        print ("函數内的 total:", total)
        return total

    total = sum_num(10, 20)
    print("函數外的 total:", total)

以上的輸出結果如下：

.. code-block:: console

    函數内的 total: 30
    函數外的 total: 30 