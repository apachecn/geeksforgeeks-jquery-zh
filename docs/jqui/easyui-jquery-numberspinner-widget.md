# easy ui jquery number sponsors widget

> 原文:[https://www . geesforgeks . org/easy ui-jquery-number spinner-widget/](https://www.geeksforgeeks.org/easyui-jquery-numberspinner-widget/)

EasyUI 是一个 HTML5 框架，用于使用基于 jQuery、React、Angular 和 Vue 技术的用户界面组件。它有助于构建交互式 web 和移动应用程序的功能，为开发人员节省了大量时间。

在本文中，我们将学习如何使用 jQuery 易用户界面设计一个数字微调器。numberspinner 小部件结合了一个可编辑的文本框和两个小按钮，用户可以从一系列数值中进行选择。

**jQuery 易 UI 下载:**

```
https://www.jeasyui.com/download/index.php
```

**语法:**

```
<input class="easyui-numberspinner">
```

**属性:**

*   **宽度**:该部件的宽度。
*   **高度**:这个部件的高度。
*   **值**:初始化值。
*   **分钟**:最小允许值。
*   **最大值**:最大允许值。
*   **增量**:点击微调按钮时的增量值。
*   **可编辑**:定义用户是否可以直接在字段中输入值。
*   **禁用**:定义是否禁用该字段。
*   **只读**:定义组件是否只读。
*   **旋转对齐**:定义旋转按钮的对齐方式。

#### 方法:

*   **选项:**返回选项对象。
*   **设置值:**设置数字微调器值。

**属性:**

*   **启动:当用户单击向上微调按钮时，**启动。
*   **按下向下按钮:**当用户点击向下微调按钮时触发。

**CDN 链接:**首先，添加项目所需的 jQuery Easy UI 脚本。

> <！–易 UI 的 jQuery 库–>
> <脚本类型=“text/JavaScript”src =“jQuery . easui . min . js”>
> </脚本> <！–易 UI Mobile 的 jQuery 库–>
> <脚本类型=“text/JavaScript”src =“jQuery . easui . Mobile . js”>
> </脚本>

**示例:**

## 超文本标记语言

```
<!doctype html> 
<html> 

<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" 
          content="initial-scale=1.0, 
                    maximum-scale=1.0, user-scalable=no"> 

    <!-- EasyUI specific stylesheets-->
    <link rel="stylesheet" type="text/css"
        href="themes/metro/easyui.css"> 

    <link rel="stylesheet" type="text/css"
        href="themes/mobile.css"> 

    <link rel="stylesheet" type="text/css"
        href="themes/icon.css"> 

    <!--jQuery library -->
    <script type="text/javascript" src="jquery.min.js"> 
    </script> 

    <!--jQuery libraries of EasyUI -->
    <script type="text/javascript"
        src="jquery.easyui.min.js"> 
    </script> 

    <!--jQuery library of EasyUI Mobile -->
    <script type="text/javascript"
        src="jquery.easyui.mobile.js"> 
    </script> 
    <script type="text/javascript"> 
      $(document).ready(function (){ 
        $('#gfg').numberspinner({ 
          min: 10,
            max: 100,
            editable: false

        }); 
      }); 
    </script> 
</head> 
<body>

    <h1>GeeksforGeeks</h1>
    <h3>EasyUI jQuery numberspinner widget</h3>
    <input id="gfg" class="easyui-numberpinner">
</body>
</html>
```

**输出:**

![](img/df5ae6a42c6902efbd6613d9db646dd4.png)

**参考:**T2】http://www.jeasyui.com/documentation/