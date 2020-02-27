# JavaScirpt简介

JavaScript引擎（虚拟机）：
---
JavaScript可以在任意搭载了JavaScript引擎的设备中执行。  
不同的引擎有不同的代号，例如：
- V8 —— Chrome 和 Opera 中的 JavaScript 引擎。
- SpiderMonkey —— Firefox 中的 JavaScript 引擎。
- ……还有其他一些代号，像“Trident”，“Chakra”用于不同版本的 IE，“ChakraCore”用于 Microsoft Edge，“Nitro”和“SquirrelFish”用于 Safari，等等。

比JavaScript“更好”的语言：
---
- `CoffeeScript` 是 JavaScript 的语法糖，它语法简短，明确简洁。通常使用 Ruby 的人喜欢用。
- `TypeScript` 将注意力集中在增加严格的数据类型。这样就能简化开发，也能用于开发复杂的系统。TypeScript 是微软开发的。
- `Flow` 也添加了数据类型，但是以一种不同的方式。由 Facebook 开发。
- `Dart` 是一门独立的语言。它拥有自己的引擎用于在非浏览器环境中运行（如：手机应用），它也能被编译成 JavaScript 。由 Google 开发。

# 手册与规范

规范：
---
**ECMA-262 规范**包含了大部分深入的、详细的、规范化的关于 JavaScript 的信息。这份规范明确地定义了这门语言。  
[最新的规范草案](https://tc39.es/ecma262/)  

手册：
---
- **MDN（Mozilla） JavaScript 索引**是一本带有用例和其他信息的手册。它是一个获取关于个别语言函数、方法等深入信息的很好的来源。  
你可以在 https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference 找到这本手册。
- **MSDN** —— 一本微软的手册，它包含大量的信息，包括 JavaScript（在里面经常被写成 JScript）。如果有人需要关于 Internet Explorer 的规范细节，最好去看：http://msdn.microsoft.com/。

兼容性表：
---
JavaScript 还是一门还在发展中的语言，经常会添加一些新的功能。

如果想要获得一些关于浏览器和其他引擎的兼容性信息，请看：
- http://caniuse.com —— 每个功能都列有一个支持信息表格，例如想看哪个引擎支持现代加密（cryptography）函数：http://caniuse.com/#feat=cryptography。
- https://kangax.github.io/compat-table —— 一份列有语言功能以及引擎是否支持这些功能的表格。

所有这些资源在实际开发中都有用武之地，因为他们包含了语言细节以及它们被支持的程度等非常有价值的信息。

为了不要让你在真正需要深入了解特定功能的时候捉襟见肘，请记住它们（或者这一页）。

# 代码编辑器

代码编辑器分为两种：IDE（集成开发环境）和轻量编辑器。

# 开发者控制台

浏览器内置的“开发者工具”。  
在浏览器中按下`F12`建打开开发者工具。  
