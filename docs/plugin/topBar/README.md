# Top Bar

<div style="margin: 0 130px">

![top-bar](./top-bar.png)
</div>

## 组件示例

```html
   <dweb-top-bar id="topbar" title="Ar 扫雷" background-color="#eeee" foreground-color="#000"  overlay="0.4" >
        <dweb-top-bar-button id="aaa">
            <dweb-icon source="Filled.AddCircle" ></dweb-icon>
        </dweb-top-bar-button>
        <dweb-top-bar-button id="ccc">
            <dweb-icon source="https://objectjson.waterbang.top/test-vue3/vite.svg" type="AssetIcon"></dweb-icon>
        </dweb-top-bar-button>
    </dweb-top-bar>
```

## dweb-top-bar

包含属性`background-color`,`foreground-color`,`hidden`, `overlay`,`title`。

### `title`

控制主标题。

### `background-color`

控制`topBar`的背景颜色。

### `foreground-color`

`topBar`内容的首选颜色。控制返回键，标题，内置icon的颜色。

> 或许应该再给几个属性？ `icon-color`,`title-color`,`back-color`

### `overlay`

是否开启`topBar`遮罩,也就是背景变透明，建议传递值`0~1`之间。
默认值：1 , 也就是不透明。

## dweb-top-bar-button

包含属性:`disabled`。`hidden`(还没写,要不要这个属性嘞？)

> 点击下拉菜单？

### `disabled`

禁止触发所有事件，包括无障碍事件。但是还是看得见。

## dweb-icon

包含属性：`type`, `description`, `size`, `source`。

### `source`

建议传递svg格式图片，注意如果使用自定义图片则无法定义其颜色。

### `type`

设置icon的类型，如果要传递自定义图片，`Android`需要指定 `type="AssetIcon"`。

### `description`

无障碍服务用来描述这个图标代表什么的文本。(⚠️ 未测试)

### `size`

控制图标大小。