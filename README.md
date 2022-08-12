# el-drawer

一个基于 vue2.x 版本的抽屉组件，API 跟 element-ui 保持一致。

## 引入 ElDrawer

在 main.js 中写入以下内容：

```js
import Vue from "vue";
import ElDrawer from "el-drawer";

Vue.use(ElDrawer);
```

在 vue 文件中使用：

```html
<template>
  <div>
    <button @click="visible = true">打开弹窗</button>
    <el-drawer title="我是标题" :visible.sync="visible" :direction="direction">
      <span>我是弹窗的内容!</span>
    </el-drawer>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        visible: false,
        direction: "rtl"
      };
    }
  };
</script>
```

## 特别注意

由于关闭按钮使用了 icon，需要引入字体文件，在 node_modules 文件夹找到 el-drawer, 将 lib 文件夹内的 fonts 文件夹拷贝到项目的 public 或者 static 目录即可

原因如下：

```css
@font-face {
  font-family: element-icons;
  src: url(fonts/element-icons.woff) format("woff"), url(fonts/element-icons.ttf)
      format("truetype");
  font-weight: 400;
  font-display: "auto";
  font-style: normal;
}
```

[API 文档](https://element.eleme.cn/2.15/#/zh-CN/component/drawer)
