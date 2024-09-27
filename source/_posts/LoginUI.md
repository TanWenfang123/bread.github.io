---
title: LoginUI
date: 2024-09-27 10:59:36
tags:
---
ArkUI 是华为 HarmonyOS 提供的声明式 UI 开发框架，它支持使用 XML 布局文件和 TypeScript/JavaScript 编程语言来构建跨设备的用户界面。在 ArkUI 中，你可以使用多种组件来构建你的应用界面，包括基础布局组件、控件组件等。

以下是一个简单的示例，展示如何在 ArkUI 中编写一个首页子组件，这个组件使用了几个常用的组件，如 Stack（堆叠布局）、Text（文本显示）、Image（图片显示）和 Button（按钮）。

1. 创建组件文件
首先，在你的项目中创建一个新的 ArkUI 组件文件，例如 HomePage.hml（用于定义布局）和 HomePage.ts（用于定义逻辑）。

2. 编写布局文件（HomePage.hml）

xml

```
<stack class="container">  
    <image class="logo" src="/common/images/logo.png"></image>  
    <text class="title">欢迎来到我的应用</text>  
    <button class="button" onclick="onButtonClick">点击我</button>  
</stack>
```


3. 编写样式文件（可选，但推荐）
ArkUI 支持在 .css 文件中定义样式，然后在 .hml 文件中通过 class 引用。假设你的样式定义在 HomePage.css 中：

css

```
.container {  
    flex-direction: column;  
    align-items: center;  
    justify-content: center;  
    height: 100%;  
}  
  
.logo {  
    width: 100px;  
    height: 100px;  
    margin-bottom: 20px;  
}  
  
.title {  
    font-size: 24px;  
    color: #333;  
    margin-bottom: 20px;  
}  
  
.button {  
    width: 200px;  
    height: 50px;  
    background-color: #007DFF;  
    color: white;  
    text-align: center;  
    line-height: 50px;  
    border-radius: 5px;  
}
```

4. 编写逻辑文件（HomePage.ts）

```
typescript
export default {  
    onButtonClick() {  
        console.log('按钮被点击了！');  
        // 这里可以添加更多的逻辑，比如页面跳转等  
    }  
}
```

5. 引用组件
在你的主页面或父组件中，你可以通过 <import> 标签来引入这个子组件，并使用 <element> 标签来显示它。

xml

```
<!-- 在父组件的.hml文件中 -->  
<import src="HomePage.hml"></import>  
<element name="home-page" src="HomePage.hml"></element>  
  
<stack>  
    <home-page></home-page>  
</stack>
```

注意：以上示例中的路径和文件名需要根据你的项目结构进行调整。

这就是在 ArkUI 中编写和使用一个简单首页子组件的基本步骤。你可以根据需要添加更多的组件和样式来丰富你的应用界面。