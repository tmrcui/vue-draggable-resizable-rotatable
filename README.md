# vue-draggable-resizable-rotatable

> Vue2 Component for draggable, resizable and rotatable elements.<br>
>在 [vue-draggable-resizable](https://github.com/mauricius/vue-draggable-resizable)的基础上支持了旋转功能和其他属性。

## Install and basic usage

```bash
$ npm install --save vue-draggable-resizable-rotatable
```

下面是新增的属性和事件,原有属性请在[vue-draggable-resizable](https://github.com/mauricius/vue-draggable-resizable)中查看。

### Props

#### rotatable
Type: `Boolean`<br>
Required: `false`<br>
Default: `true`

定义组件是否支持旋转
```html
<vue-draggable-resizable :rotatable="true">
```

#### r
Type: `Number`<br>
Required: `false`<br>
Default: `0`

定义初始旋转角度
```html
<vue-draggable-resizable :r="0">
```

#### deselectCancel
Type: `String`<br>
Required: `false`<br>

定义点击组件外的其他区域时阻止取消选中的选择器
```html
<vue-draggable-resizable :deselectCancel=".selector">
```

### Events

#### rotating
Required: `false`<br>
Parameters:
* `rotate` 旋转的角度

旋转时触发
```html
<vue-draggable-resizable :rotating="onRotating">
```

#### rotatestop
Required: `false`<br>
Parameters:
* `rotate` 旋转的角度

旋转结束时触发
```html
<vue-draggable-resizable :rotatestop="onRotateStop">
```
