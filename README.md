# 微信小程序 wepyjs 第三方 wepy-com-formio 组件

![formio]()

## 说明

http://www.formio.net/
https://github.com/formio

偶然了解formio这个很强大的表单渲染组建，根据官方的宣传，我们可以在自定义界面进行可视化设计，设计结果将会保存为JSON对象，展示界面仅需要加载JSON对象即可生产丰富的表单界面；由此可以想象，如果我们需要一个快速的程序构建平台，标准的接口构建服务 + Formio表单设计服务 即可解决这样的问题，可以实现快速的功能构建。

组件依赖:
[wepyjs v1.1.9+](https://github.com/wepyjs/wepy)。
[formiojs v2.29.5+](https://github.com/formio/formio.js)

## 使用

### 安装组件
```
npm install wepy-com-formio --save
```

### 引入组件
```javascript
// index.wpy
<template>
    <component id="formio"></component>
</template>
<script>
    import wepy from 'wepy';
    import formio from 'wepy-com-formio';

    export default class Index extends wepy.page {
        components = {
            formio: formio
        };
    }
</script>
```


### 调用方法
```javascript
let promise = this.$invoke('formio', 'build', {
    form: 'form id',
    src: 'https://examples.form.io/example',
});

promise.then((d) => {
    console.log('formio done');
});
```

## 更多说明
参考[wepy-com-toast] (https://github.com/wepyjs/wepy-com-toast)
参考[vue-formio] (https://github.com/formio/vue-formio)
