# prefix-free
自动添加当前浏览器需要的前缀
# 官网
http://leaverou.github.io/prefixfree/

插件
在-prefix-free之上的额外代码使其更加灵活，将其与不同的API集成等

动态DOM插件
最初是-prefix-free的一部分，它现在是一个单独的插件。它使--prefix-free照顾：

新增 <link>并<style>随后添加到文档中
style之后将具有属性的新元素添加到文档中
style属性更改setAttribute()（Webkit中除外）
通过CSSOM获取和设置无前缀属性，如：
element.style.transform ='rotate（10deg）';
需要注意的事项：
变异事件的声誉很慢，而且当属性发生变化或添加新元素时，变异事件是唯一的方法
style 属性修改在Webkit中不起作用
设置无前缀的CSSOM属性，例如：
element.style.transform ='rotate（5deg）';
将无法在Chrome中使用（阅读将）
立即获取Dynamic DOM插件：

prefixfree.dynamic-dom.js
prefixfree.dynamic-dom.min.js
jQuery插件
一个小插件（我甚至不打扰它，因为它太小），让你通过jQuery的.css方法设置/获取未加前缀的CSS属性。

立即获取jQuery插件：

prefixfree.jquery.js
视口相对单位
用于新vw，vh，vmin，vmax单位的静态polyfill 。

如果本机支持单元，则不会执行任何操作。
这是动态的。在屏幕大小调整时更新像素值。
prefixfree.viewport-units.js
CSS变量
启用基本的CSS变量支持。

如果有一个带前缀的实现，它将添加必要的前缀并使用它
它支持覆盖变量值
限制：
不支持范围。每个变量都在全局范围内，并且同一变量的每个后续声明都会覆盖以前的变量，而不管作用域是什么
这不是动态的。变量被替换一次，然后它们作为普通的CSS值运行



# CALC
width:calc(50% - 20px);

这样书写是无效的因为calc中计算的两个因子同运算符号之间必须存在空格；
