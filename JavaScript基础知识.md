# Hello,World!

“script”标签
---
JavaScript程序可以在`<script>`标签的帮助下插入到 HTML 文档的任何地方。  

`<script>` 标签中包裹了 JavaScript 代码，当浏览器遇到 `<script>` 标签，代码会自动运行。

现代的标记
---
`<script>` 标签有一些现在很少用到的属性，但是我们可以在老代码中找到它们：

`type` 属性：`<script type=…>`  
在老的 HTML4 标准中，要求 script 标签有 `type` 属性。通常是 `type="text/javascript"`。这样的属性声明现在已经不再需要。而且，现代 HTML 标准 —— HTML5 已经完全改变了此属性的实际含义。现在，该属性可以被用于 JavaScript 模块。但那是一个高级一点的话题，我们将会在此教程的其他章节中探讨 JavaScript 模块。

`language` 属性：`<script language=…>`  
这个属性是为了显示脚本使用的语言。这个属性现在已经没有任何意义，因为语言默认就是 JavaScript。不再需要使用它了。

外部脚本
---

脚本文件可以通过src属性添加到 HTML 文件中。  
```javascript
<script src="/path/to/script.js"></script>
```
这里，`/path/to/script.js` 是脚本文件从站点根目录开始的绝对路径。当然也可以提供当前页面的相对路径。例如，`src ="script.js"` 表示当前文件夹中的 `"script.js"` 文件。

我们也可以提供一个完整的 URL 地址，例如：
```javascript
<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/3.2.0/lodash.js"></script>
```
要附加多个脚本，请使用多个标签：
```javascript
<script src="/js/script1.js"></script>
<script src="/js/script2.js"></script>
…
```
**注意：**
- 使用独立文件的好处是浏览器会下载它，然后将它保存到浏览器的缓存中。  
之后，其他页面想要相同的脚本就会从缓存中获取，而不是下载它。所以文件实际上只会下载一次。  
这可以节省流量，并使得页面（加载）更快。
- 如果设置了 `src` 属性，`script` 标签内容将会被忽略。

# 代码结构

分号
---
当存在分行符号（换行）时，在大多数情况下可以省略分号。  
JavaScript将分行符号理解为“隐式”的分号。被称为**自动分号插入**。
当然会导致不可预料的错误。

# 现代模式："use strict"

这个指令看上去像一个字符串 `"use strict"` 或者 `'use strict'`。当它处于脚本文件的顶部时，则整个脚本文件都将以“现代”模式进行工作。当使用`"use strict"`则无法取消。确保总是使用`"use stirct"`

`"use strict"` 可以被放在函数主体的开头，而不是整个脚本的开头。这样则可以只在该函数中启用严格模式。但通常人们会在整个脚本中启用严格模式。

浏览器控制台中：
---
当使用浏览器控制台去测试功能时，请注意 `use strict` 默认不会被启动。

有时，使用 `use strict` 会产生一些不一样的影响，你会得到错误的结果。

你可以试试按下 `Shift+Enter` 去输入多行代码，然后将 `use strict` 置顶，就像这样：
```javascript
'use strict'; <Shift+Enter 换行>
//  ...你的代码
<按下 Enter 以运行>
```
它在大部分浏览器中都有效，像 Firefox 和 Chrome。

如果依然不行，那确保 `use strict` 被开启的最可靠的方法是，像这样将代码输入到控制台：
```javascript
(function() {
  'use strict';

  // ...你的代码...
})()
```

