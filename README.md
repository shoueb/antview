# 概要

### 1、集成工具

这个项目是站在了几个最优秀的项目肩上完成的，在此对这些开源项目创作者表示感谢。

> 组件功能基于`Vue`完成
> 
> 页面显示基于`Bootstrap`完成
> 
> Dom操作基于`jQuery`完成

----

### 2、设计思路

**问**：后端同学是否可以只编写 `json` 代码，页面就自动渲染出来，并且还能够保持统一风格。

**答**：可以。`luckyview` 就是用来完成这项使命的。

----

Vue框架有个非常好用的功能：**组件**。可以将日常开发过程中使用到的 **基本元素**，封装为一个个的 **基础组件** 。

> 比如：`label`、`input`、`select`、`textarea`、`button` 等等。
> 
> 基础组件的名字和 `html`标签一样，比较容易理解和记忆。 

用这些 **基础组件**，再进行封装，可以拼装成页面上用到的 **高级组件**。

> 比如：`面包屑`、`搜索表单`、`操作按钮组`、`分页表格`、`分页标签` 等。
> 
>  这些就是页面大块组件了，后面的文档中会逐一介绍他们的用法。


### 3、使用示例

##### Html页面


```html
<!-- html start -->
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>VUE实例-列表页</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <!-- 组件：注意此处提供一个id设置为lv.min.js，用于框架自动识别环境 -->
  <script id="lv.js" type="text/javascript" src="http://statictest.luckincoffee.com/lv/lv.js"></script>
</head>
<body>
<!-- 列表页面 -->
<div id="lv-view">
  <lv-view :config="config"></lv-view>
</div>
<!-- 页面配置 -->
<script type="text/javascript" src="page.js"></script>
<!-- 初始化启动脚本 -->
<script type="text/javascript">
  // 建议放在业务逻辑代码最后处，即config对象准备完成 
  lv.start({
    // 选填。配置项填充div的id值，默认 lv-view
    viewId: 'lv-view',
    // 必填。配置项对象
    config: config
  });
</script>
</body>
</html>
<!-- html end -->
