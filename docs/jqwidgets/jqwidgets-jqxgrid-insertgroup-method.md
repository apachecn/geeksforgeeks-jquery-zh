# jQWidgets jqxGrid insertgroup()方法

> 原文:[https://www . geesforgeks . org/jqwidgets-jqxgrid-insert group-method/](https://www.geeksforgeeks.org/jqwidgets-jqxgrid-insertgroup-method/)

**jQWidgets** 是一个 JavaScript 框架，用于为 PC 和移动设备制作基于 web 的应用程序。它是一个非常强大、优化、独立于平台并且得到广泛支持的框架。jqxGrid 用于说明以表格形式显示数据的 jQuery 小部件。此外，它完全支持与数据的连接，以及分页、分组、排序、过滤和编辑。

**插入组()方法**用于插入指定的组。它不返回任何东西。

**语法:**

```
$('#Selector').jqxGrid('insertgroup', groupIndex, 'dataField');
```

**参数:**

*   **组索引:**是该组的规定索引。它是数字类型的。
*   **数据字段:**是所述列的数据字段。它属于字符串类型。

**链接文件:**从给定链接下载 https://www.jqwidgets.com/download/。在 HTML 文件中，找到下载文件夹中的脚本文件。

> <link rel="”stylesheet”" href="”jqwidgets/styles/jqx.base.css”" type="”text/css”">
> <脚本类型=“text/JavaScript”src =“scripts/jquery-1 . 11 . 1 . min . js”></脚本>
> <脚本类型=“text/JavaScript”src =“jqwidgets/jqxcore . js”></脚本>
> <脚本类型=“text/JavaScript”src =“jqwidgets/jqxdata

下面的例子说明了 jQWidgets 中的 jqxGrid insertgroup()方法。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <link rel="stylesheet" 
          href="jqwidgets/styles/jqx.base.css" 
          type="text/css" />
    <script type="text/javascript" 
            src="scripts/jquery-1.11.1.min.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxcore.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxdata.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxbuttons.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxscrollbar.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxmenu.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxgrid.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxgrid.selection.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqx-all.js">
    </script>    
</head>

<body>
    <center>
        <h1 style="color: green">
            GeeksforGeeks
        </h1>

        <h3>jQWidgets jqxGrid insertgroup()
            method
        </h3>
        <br />

        <div id="jqxg"></div>

        <div>
            <input type="button" id="jqxBtn" 
                   style="margin-top: 25px" 
                   value="Click here" />
        </div>

        <div id="log"></div>
    </center>

    <script type="text/javascript">
        $(document).ready(function () {
            var d = new Array();
            var subjectNames =
                ["C++", "Scala", "Java", "C", "R", "JavaScript"];

            var pageNumber =
                ["7", "8", "12", "11", "10", "19"];

            for (var j = 0; j < 7; j++) {
                var r = {};
                r["subjectnames"] =
                    subjectNames[Math.floor(
                        Math.random() * subjectNames.length)
                    ];

                r["pagenumber"] =
                    pageNumber[Math.floor(
                        Math.random() * pageNumber.length)
                    ];
                d[j] = r;

            }
            var src = {
                localdata: d,
                datatype: "array",
            };
            var data_Adapter = new $.jqx.dataAdapter(src);
            $("#jqxg").jqxGrid({
                source: data_Adapter,
                groupable: true,
                height: "240px",
                width: "300px",
                columns: [
                    {
                        text: "Subject Name",
                        datafield: "subjectnames",
                        width: "160px",
                    },
                    {
                        text: "Page No.",
                        datafield: "pagenumber",
                        width: "160px",
                    },
                ],
            });

            $("#jqxBtn").jqxButton({
                width: "180px",
                height: "30px",
            });
            $('#jqxg').jqxGrid('addgroup', 'pagenumber');
            $("#jqxBtn").on("click", function () {
                $('#jqxg').jqxGrid('insertgroup', 1, 'subjectnames');
                $('#log').html("Subject Name is inserted!");
            });
        });
    </script>
</body>

</html>
```

**输出:**

![](img/864e657f1df0eca210258a0410f4872c.png)

**参考:**[https://www . jqwidgets . com/jquery-widgets-documentation/documentation/jqxgrid/jquery-grid-API . htm？搜索=](https://www.jqwidgets.com/jquery-widgets-documentation/documentation/jqxgrid/jquery-grid-api.htm?search=)