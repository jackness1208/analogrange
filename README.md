# analogrange 模拟滑块 组件功能说明
本组件 基于 jQuery 开发

## 组件对 UI 的要求：
* target 为滑块区域, 组件要求滚动区域内有且只有 1个 子级元素， 组件会将该子级元素认定为滑块按钮
```html
<div class="range-box" id='iRange'>
    <div class="range-bar"></div>
</div>
```

## 使用方法
```javascript
analogrange('#iRange', {
    direction: 'x',
    onchange: function(num){
        iVal.innerHTML = Math.round(num * 100) + '%';
    }
});
```
## 参数说明
```javascript
/**
 * @param  {Object|String} target 滑块区域
 * @param  {Object}        op 参数设置
 *                         op.direction             [String]   滑块方向 x|y
 *                         op.onchange              [function] 滑动时触发事件
 *                         op.onready               [function] 初始化完成回调函数
 *                         op.reverse               [boolean]  滑动方向反向, 默认为 false
 * @return {Object}        iRange 方法句柄
 *                         iRange.changeTo(precent) [function] 设置滑块位置
 *                         - precent                [Float]    0-1 之间
 */
analogrange(target, op);
```
## 例子
[例子1](demo/demo.html)
## 更新历史

> 1.1.1 (2016-05-04)
> [FIX] 修复控件不在首屏时候 滚动有问题bug

> 1.1.0 (2016-04-14)
> [ADD] 添加 op.reverse 属性， 用于设置 滑动相反，默认为 自左而右， 自上而下
> [FIX] 修复不同方向组件 会出现混乱问题

> 1.0.0 (2016-01-18)
> * 诞生
