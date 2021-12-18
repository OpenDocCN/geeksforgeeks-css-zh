# SASS sass:字符串模块

> 原文:[https://www.geeksforgeeks.org/sass-sassstring-module/](https://www.geeksforgeeks.org/sass-sassstring-module/)

**sass:string** 模块可以轻松组合、搜索或拆分字符串。以下是可以使用此模块的功能列表。

**1。string.quote()函数:**该函数返回一个带引号的字符串。

*   **语法:**

    ```css
    string.quote(string)
    quote(string)
    ```

*   **例:**

    ```css
    @debug string.quote(GeeksForGeeks);
    @debug string.quote("GeeksForGeeks");
    ```

*   **输出:**

    ```css
    "GeeksForGeeks"
    "GeeksForGeeks"

    ```

**2。string.index()函数:**该函数返回字符串子串的第一个索引，如果字符串不包含给定的子串，则返回 null。

*   **语法:**

    ```css
    string.index(string, substring)
    str-index(string, substring)
    ```

*   **例:**

    ```css
    @debug string.index("Geeks For Geeks", "Geeks"); 
    @debug string.index("Geeks For Geeks", "For");
    ```

*   **输出:**

    ```css
    1
    7

    ```

**3。string.insert()函数:**该函数返回给定索引处插入给定插入子字符串的字符串副本。

*   **Syntax:**

    ```css
    string.insert(string, insert, index)
    str-insert(string, insert, index)
    ```

    如果给定的索引大于字符串的长度，则插入子字符串会添加到字符串的末尾。如果索引小于字符串的负长度，则将插入子字符串添加到字符串的开头。

*   **例:**

    ```css
    @debug string.insert("Geeks Geeks", " For", 7); 
    @debug string.insert("Geeks Geeks", " For", -7);
    ```

*   **输出:**

    ```css
    "Geeks For Geeks"
    "Geeks For Geeks"

    ```

**4。string.length()函数:**该函数返回给定字符串的字符总数。

*   **语法:**

    ```css
    string.length(string)
    str-length(string)
    ```

*   **例:**

    ```css
    @debug string.length("Geeks For Geeks"); 
    @debug string.length(GFG); 
    @debug string.index("");
    ```

*   **输出:**

    ```css
    15
    3
    0

    ```

**5。string.slice()函数:**该函数返回从给定为“start-at”的索引处开始，到给定为“end-at”的索引处结束的字符串切片(两者都包括)。

*   **语法:**

    ```css
    string.slice(string, start-at, end-at: -1)
    str-slice(string, start-at, end-at: -1)
    ```

*   **例:**

    ```css
    @debug string.slice("Geeks For Geeks", 6); 
    @debug string.slice("Geeks For Geeks", 1, 5); 
    @debug string.slice("Geeks For Geeks", 1, -7);
    ```

*   **输出:**

    ```css
    For Geeks
    Geeks
    Geeks For

    ```

**6。string.to-upper-case()函数:**该函数返回给定字符串的副本，ASCII 字母转换为大写。

*   **语法:**

    ```css
    string.to-upper-case(string)
    to-upper-case(string)
    ```

*   **例:**

    ```css
    @debug string.to-upper-case("Geeks For Geeks"); 
    @debug string.to-upper-case(geeks for geeks); 
    ```

*   **输出:**

    ```css
    "GEEKS FOR GEEKS"
    GEEKS FOR GEEKS

    ```

    **7。string . to-小写()函数:**该函数返回给定字符串的副本，ASCII 字母转换为小写。

    *   **语法:**

        ```css
        string.to-lower-case(string)
        to-lower-case(string)
        ```

    *   **例:**

        ```css
        @debug string.to-lower-case("Geeks For Geeks"); 
        @debug string.to-lower-case(geeks for geeks); 
        ```

    *   **输出:**

        ```css
        "geeks for geeks"
        geeks for geeks

        ```

    **8。string.unique-id()函数:**该函数返回一个随机生成的字符串，该字符串是一个有效的 CSS 标识符，在当前的 Sass 编译中是唯一的。

    *   **语法:**

        ```css
        string.unique-id()
        unique-id()
        ```

    *   **例:**

        ```css
        @debug string.unique-id();  
        @debug string.unique-id(); 
        ```

    *   **输出:**

        ```css
        uabtrnzug
        u6w1b1def

        ```

    **9。string.unquote()函数:**该函数将给定的字符串作为未加引号的字符串返回。这个函数会产生不是有效 CSS 的字符串，所以这个函数一定要谨慎使用。

    *   **语法:**

        ```css
        string.unquote(string)
        unquote(string)
        ```

    *   **例:**

        ```css
        @debug string.unquote(GeeksForGeeks);
        @debug string.unquote(".color: green");
        ```

    *   **输出:**

        ```css
        GeeksForGeeks
        .color: green

        ```