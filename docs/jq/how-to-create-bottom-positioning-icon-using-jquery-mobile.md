# 如何使用 jQuery Mobile 创建底部定位图标？

> 原文:[https://www . geesforgeks . org/如何创建-底部-定位-图标-使用-jquery-mobile/](https://www.geeksforgeeks.org/how-to-create-bottom-positioning-icon-using-jquery-mobile/)

**jQuery Mobile** 是一种基于网络的技术，用于制作可在所有智能手机、平板电脑和台式机上访问的响应内容。在本文中，我们将使用 jQuery Mobile 制作底部定位图标。

**方法:**首先，添加项目所需的 jQuery Mobile 脚本。

> <link rel="”stylesheet”" href="”http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.css”">
> <脚本 src = " http://code . jquery . com/jquery-1 . 11 . 1 . min . js "></脚本>
> <脚本 src = " http://code . jquery . com/mobile/1 . 4 . 5/jquery . mobile-1 . 4 . 5 . min . js "></脚本>

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head>
    <link rel="stylesheet"href=
"http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.css"/>

    <script src=
"http://code.jquery.com/jquery-1.11.1.min.js">
    </script>

    <script src=
"http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.js">
    </script>
</head>

<body> 
    <center>
        <h1>GeeksforGeeks</h1>
        <h4>Icon positioning bottom using 
            button tag in jQuery Mobile
        </h4>
    </center>

    <button id="gfg" data-role="button" 
        data-icon="arrow-d" data-iconpos="bottom">
        A button
    </button>
</body>

</html>
```

**输出:**

![](img/ca92245ef2ff71b5014676ccb9d32c57.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head>
    <link rel="stylesheet" href=
"http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.css"/>

    <script src=
"http://code.jquery.com/jquery-1.11.1.min.js">
    </script>

    <script src=
"http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.js">
    </script>
</head>

<body> 
    <center>
        <h1>GeeksforGeeks</h1>
        <h4>Icon positioning bottom 
            using anchor tag in jQuery Mobile
        </h4>
    </center>

    <a href="https://www.geeksforgeeks.org/" 
       data-role="button" data-icon="arrow-d" 
       data-iconpos="bottom">An Anchor</a>
</body>

</html>
```

**输出:**

![](img/be75f40d8160cfb1a4e6224457b27b99.png)