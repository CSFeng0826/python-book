String 字串
====================================

之前的章節，我們有介紹字串是如何產生的，這個章節主要說明一些字串的使用方法。

字串與運算符號
-----------------------------------------

在 Python 中字串也可使用運算符號進行操作，主要有以下幾中運算符號：

- ``+``：字符串連接
- ``*``：重複輸出字符串
- ``[]``：通過索引獲取字符串中字符
- ``[ : ]``：截取字符串中的一部分，``str[0:2]`` 是不包含第3個字符的
- ``in``：成員運算符，如果字符串中不包含給定的字符返回 ``True``
- ``not in``：成員運算符，如果字符串中不包含給定的字符返回 ``True``
- ``r/R``：原始字符串為所有的字符串都是直接按照字面的意思來使用，沒有轉義特殊或不能打印的字符。原始字符串除在字符串的第一個引號前加上字母``r``（可以大小寫）以外，與普通字符串有著幾乎完全相同的 語法。
- ``%``：格式字符串

如以下程式範例：

.. code-block:: python
    
    a = "Hello" 
    b = "World" 

    print("a + b 輸出結果：", a + b) 
    print("a * 2 輸出結果：", a * 2) 
    print("a[1] 輸出結果：", a [1]) 
    print("a[1:4] 輸出結果：", a [1:4]) 
    print('H' in a)
    print('H' not in b)

    print('Hello World!\n')
    print(r'Hello World!\n')

以上的輸出結果如下：

.. code-block:: console

    a + b 輸出結果： HelloWorld
    a * 2 輸出結果： HelloHello
    a[1] 輸出結果： e
    a[1:4] 輸出結果： ell
    True
    True
    Hello World!

    Hello World!\n

字串更新
-----------------------------------------

在字串中可以透過擷取字串中的一部分與其他字串拼接，如以下程式範例：

.. code-block:: python
    
    str1 = 'Hello World!' 
    print(str1 [:6] + 'I am john.')

以上的輸出結果如下：

.. code-block:: console

    Hello I am john.

replace()
-----------------------------------------

在 Python 中字串提供一個 ``replace()`` 方法，可以替換字串中的元素，把字符串中的欲替換的字串替换成新字串，如果指定第三個参数則為替換次數，範例程式如下：

.. code-block:: python
    
    str1 = "That is example, that is example, that is example.";
    print(str1.replace("is", "was"))
    print(str1.replace("is", "was", 1))

以上的輸出結果如下：

.. code-block:: console

    That was example, that was example, that was example.
    That was example, that is example, that is example.

轉義字元
-----------------------------------------

在字串中有些字元是有著特殊意義的，譬如 ``\n`` 為換行符號，這些特殊字元，在 Python 中用 ``反斜線 \`` 來表示，如下：

- ``\ (在行尾時)``：續行符
- ``\\``：反斜杠符號
- ``\'``：單引號
- ``\"``：雙引號
- ``\a``：響鈴
- ``\b``：退格 (Backspace)
- ``\000``：空
- ``\n``：換行
- ``\v``：縱向製表符
- ``\t``：橫向製表符
- ``\r``：Enter
- ``\f``：換頁
- ``\oyy``：八進制數，例如：``\o12`` 代表換行，其中 ``o`` 是字母，不是數字 ``0``。
- ``\xyy``：十六進制數，例如：``\x0a`` 代表換行
- ``\other``：其它的字符以普通格式輸出

字符格式化
-----------------------------------------

Python 支持格式化字串的輸出。儘管這樣可能會用到非常複雜的表達式，但最基本的用法是將一個值插入到一個有字串格式符 ``%s`` 的字符串中

.. code-block:: python
    
    print("My name is %s. I am %d years old!" % ('John', 18))

以上的輸出結果如下：

.. code-block:: console

    My name is John. I am 18 years old!

- ``%c``：格式化字元及其ASCII碼
- ``%s``：格式化字串
- ``%d``：格式化整數
- ``%u``：格式化無符號整型
- ``%o``：格式化無符號八進制數
- ``%x``：格式化無符號十六進制數
- ``%X``：格式化無符號十六進制數（大寫）
- ``%f``：格式化浮點數字，可指定小數點後的精度
- ``%e``：用科學計數法格式化浮點數
- ``%E``：作用同 ``%e``，用科學計數法格式化浮點數
- ``%g``：``%f`` 和 ``%e`` 的簡寫
- ``%G``：``%f`` 和 ``%E`` 的簡寫
- ``%p``：用十六進制數格式化變量的地址

此外，Python 中提供以下格式化操作符輔助指令:

- ``*``：定義寬度或者小數點精度
- ``-``：用做左對齊
- ``+``：在正數前面顯示加號 ``+`` 
- ``<sp>``：在正數前面顯示空格
- ``#``：在八進制數前面顯示 ``0``，在十六進制前面顯示 ``0x`` 或者 ``0X``
- ``0``：顯示的數字前面填充 ``0`` 而不是默認的空格
- ``%``：``%%``輸出一個單一的 ``%``
- ``(var)``：映射變量(字典參數)
- ``mn``：``m`` 是顯示的最小總寬度，``n`` 是小數點後的位數

formate/f-string 格式化函數
-----------------------------------------

Python 提供了一種格式化字串的函數 ``str.format()``，它增強了字串格式化的功能

基本語法是通過 ``{}`` 和 ``:`` 來代替以前的 ``%``。

``format`` 函數可以接受不限個參數，位置可以不按順序

如以下程式範例：

.. code-block:: python
    
    print("{} {}".format("hello", "world"))    # 不設置指定位置，按默認顺序
    
    print("{0} {1}".format("hello", "world"))  # 設置指定位置

    print("{1} {0} {1}".format("hello", "world"))  # 設置指定位置

以上的輸出結果如下：

.. code-block:: console

    hello world
    hello world
    world hello world

數字格式化
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

下表展示了 ``str.format()`` 格式化數字的多種方法：

+----------+-------+----------+-----------------------------------+
|Number    |Format |Output    |Description                        |
+==========+=======+==========+===================================+
|3.1415926 |{:.2f} |3.14      |Keep two decimal places            |
+----------+-------+----------+-----------------------------------+
|3.1415926 |{:+.2f}|+3.14     |Keep two decimal places with signed|
+----------+-------+----------+-----------------------------------+
|-1        |{:+.2f}|-1.00     |Keep two decimal places with signed|
+----------+-------+----------+-----------------------------------+
|2.71828   |{:.0f} |3         |Without decimals                   |
+----------+-------+----------+-----------------------------------+
|5         |{:0>2d}|05        |Zero padding (fill left, width 2)  |
+----------+-------+----------+-----------------------------------+
|5         |{:x<4d}|5xxx      |x padding (fill right, width 4)    |
+----------+-------+----------+-----------------------------------+
|10        |{:x<4d}|10xx      |x padding (fill right, width 4)    |
+----------+-------+----------+-----------------------------------+
|1000000   |{:,}   |1,000,000 |Number format separated by comma   |
+----------+-------+----------+-----------------------------------+
|0.25      |{:.2%} |25.00%    |Percentage format                  |
+----------+-------+----------+-----------------------------------+
|1000000000|{:.2e} |1.00e+09  |Exponential format                 |
+----------+-------+----------+-----------------------------------+
|13        |{:>10d}|________13|Right align (default, width 10)    |
+----------+-------+----------+-----------------------------------+
|13        |{:<10d}|13________|Left aligned (width 10)            |
+----------+-------+----------+-----------------------------------+
|13        |{:^10d}|____13____|Center aligned (width 10)          |
+----------+-------+----------+-----------------------------------+

f-string 是 Python3.6 之後版本添加的，稱之為字面量格式化字串，是新的格式化字串的語法

f-string 格式化字串以 ``f`` 開頭，後面跟著字串，字串中的表達式用大括號 ``{}`` 包起來，它會將變量或表達式計算後的值替換進去

.. code-block:: python
    
    name = 'John'
    print(f'Hello {name}')  #替換變數

    print(f'{1+2}')         #使用表達式

    dict1 = {'name':'John', 'height':'175' }
    print(f'{dict1["name"]}: {dict1["height"]}cm')

以上的輸出結果如下：

.. code-block:: console

    Hello John
    3
    John: 175cm

在 Python 3.8 後的版本中可以使用 ``=`` 來拼接運算表達式與結果，如以下範例：

.. code-block:: python
    
    print(f'{x+1=}')   # Python 3.8

以上的輸出結果如下：

.. code-block:: console

    x+1=2

Unicode 字串
-----------------------------------------

在 Python2 中，普通字串是以 8 位 ASCII 碼進行存儲的，而 Unicode 字串則存儲為 16 位 Unicode 字串，這樣能夠表示更多的字符集。使用的語法是在字符串前面加上前綴 ``u``。

在 Python3 中，所有的字串都是 Unicode 字串。

Q&A
-----------------------------------------

must be string
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

在這個錯誤當中，通常是資料型態應更改為 string 格式，可以使用 ``str()`` 函數進行轉換。

.. code-block:: python

    num = 10.5
    print(type(num))
    str1 = str(num)
    print(type(str1))

以上的輸出結果如下：

.. code-block:: console

    <class 'float'>
    <class 'str'>

not all arguments converted during string formatting
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

在這個錯誤中，提供的資料數量多於或少於 format 的格式，如以下範例：

.. code-block:: python

    strs=(1,2,3,4)
    print('strs= %s' % strs)

以上的輸出結果如下：

.. code-block:: console

    >>> print('strs= %s' % strs)
    Traceback (most recent call last):
    File "<pyshell#43>", line 2, in <module>
        print('strs= %s' % strs)
    TypeError: not all arguments converted during string formatting

應該更改為

.. code-block:: python

    strs=(1,2,3,4)
    print('strs= %s,%s,%s,%s' % strs)

以上的輸出結果如下：

.. code-block:: console

    1,2,3,4
