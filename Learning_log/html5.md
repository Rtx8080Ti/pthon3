1.Doctype的作用是 声明文档类型 ，超链接新窗口打开的属性和属性值是 target="_blank" 。  
2.表格合并行的属性是 rowspan ，合并列的属性是 colspan 。（表格属性 colspan 合并列  rowspan 合并行）  
3.在HTML当中，表格控制单元格和单元格间距的属性是 cellspacing，单元格和内容间距的属性是 cellpadding 。  
4.img标签中包含的属性分别有 src;title;alt 。  
5.html标签中有哪些是空标记: < br/ >;< hr/ >;< img/ >;< input/ >;< meta/ >。
  
1.link中rel="stylesheet"属性的作用是 关联样式表.  
2.在HTML上，将表单中input元素的type属性值设置为 submit 时，用于创建提交按钮.  
3.常用的样式创建方式有哪三种 内部样式表 内嵌样式表 外部样式表 .  
4.请简述css样式表的分类，并写出外部样式表的导入方式（两种方法，以及两种方法的区别）？  
&emsp;    1.css样式表的分类有： 内部样式表 内嵌样式表 外部样式表  
&emsp;   2.外部样式表的导入方法 1）< link rel="stylesheet" href="样式表的路径及全称" / > 2)< style > @import url(样式表的路径及全称); < /style > 区别： 1.link为html标签，@import为css所提供得方式 2.@import在ie5以上版本才能识别，link没有兼容问题。  
&emsp;   3.加载顺序的差别，link链接的样式表是跟页面同时进行加载，@import链接的样式表是要等到页面加载完以后再加载，会导致页面当打开时没有样式   
&emsp;    4.使用dom控制样式时的差别：当使用javascript控制dom去改变样式的时候，只能使用link标签，因为@import不是dom可以控制的.  
答案解析: 差别1：老祖宗的差别：link属于HTML标签，而@import完全是CSS提供的一种方式。 link标签除了可以加载CSS外，还可以做很多其它的事情，定义rel连接属性等，@import就只能加载CSS。 差别2：加载顺序的差别：当一个页面被加载的时候，link引用的CSS会同时被加载，而@import引用的CSS 会等到页面全部被下载完再被加载。所以有时候浏览@import加载CSS的页面时开始会没有样式。 差别3：兼容性的差别。：@import是CSS2.1提出的，所以老的浏览器不支持，@import只在IE5以上的才能识识别。 差别4：使用dom控制样式时的差别：当使用javascript控制dom去改变样式的时候，只能使用link标签，因为@import不是dom可以控制的.
