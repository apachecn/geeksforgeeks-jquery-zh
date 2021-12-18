# jQWidgets jqxGrid sorttoglestates 属性

> 原文:[https://www . geeksforgeeks . org/jqwidgets-jqxgrid-sorttoglestates-property/](https://www.geeksforgeeks.org/jqwidgets-jqxgrid-sorttogglestates-property/)

**jQWidgets** 是一个 JavaScript 框架，用于为 PC 和移动设备制作基于 web 的应用程序。它是一个非常强大、优化、独立于平台并且得到广泛支持的框架。jqxGrid 用于说明以表格形式显示数据的 jQuery 小部件。此外，它完全支持与数据的连接，以及分页、分组、排序、过滤和编辑。

**sorttoglestates 属性**用于设置或获取显示的 jqxGrid 的排序切换状态。它是字符串类型，其默认为 2 。

**可能的值如下:**

*   **0:** 用于禁用切换。
*   **1:** 用于启用切换。
*   **2:** 用于启用*移除排序*选项。

**语法:**

设置**sorttoglestates**属性。

```
$('#Selector').jqxGrid({ sorttogglestates: 1});
```

返回**sorttoglestates**属性。

```
var sorttogglestates = 
    $('#Selector').jqxGrid('sorttogglestates');
```

**链接文件:**从给定链接下载 https://www.jqwidgets.com/download/。在 HTML 文件中，找到下载文件夹中的脚本文件。

> <link rel="”stylesheet”" href="”jqwidgets/styles/jqx.base.css”" type="”text/css”">
> <脚本类型=【text/JavaScript】src =【scripts/jquery-1 . 11 . 1 . min . js】></脚本>
> <脚本类型=【text/JavaScript】src =【jqwidgets/jqxcore . js】></脚本>
> <脚本类型=【text/JavaScript】src =【jqwidgets/jqxdata

下面的例子说明了 jQWidgets 中的 jqxGrid sorttogglestates 属性。

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
</head>

<body>
    <center>
        <h1 style="color: green">
            GeeksforGeeks
        </h1>

        <h3>jQWidgets jqxGrid sorttogglestates property </h3>
        <br />

        <div id="jqxg"></div>

        <div>
            <input type="button" id="jqxBtn"
                style="margin-top: 25px" value="Click here" />
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

            for (var j = 0; j < 50; j++) {
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
                sortable: true,
                theme: 'energyblue',
                sorttogglestates: ' 1',
                height: "260px",
                width: "250px",
                columns: [
                    {
                        text: "Subject Name",
                        datafield: "subjectnames",
                        width: "120px",
                    },
                    {
                        text: "Page No.",
                        datafield: "pagenumber",
                        width: "120px",
                    },
                ],
            });

            $("#jqxBtn").jqxButton({
                width: "180px",
                height: "30px",
            });
            $("#jqxBtn").on("click", function () {
                var sts = $('#jqxg').jqxGrid('sorttogglestates');
                $('#log').text("toggle state: " + sts);
            });
        });
    </script>
</body>

</html>
```

**输出:**

![](img/f9d35d10177b5aef9cef0df0e7e923c9.png)

**参考:**[https://www . jqwidgets . com/jquery-widgets-documentation/documentation/jqxgrid/jquery-grid-API . htm？搜索=](https://www.jqwidgets.com/jquery-widgets-documentation/documentation/jqxgrid/jquery-grid-api.htm?search=)