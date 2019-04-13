# 间隔


间隔类通过设置 `margin` 和 `padding` 属性来指定元素内部或元素之间的间距。取值范围从 `.25rem` 到 `3rem`。

## 语法

语法：`u-{property}{sides}-{size}`

_property_ 取值范围：

- `m` - 表示设置 `margin`
- `p` - 表示设置 `padding`

_sides_ 取值范围：

- `t` - 设置 `margin-top` 或 `padding-top` 
- `b` - 设置 `margin-bottom` 或 `padding-bottom` 
- `l` - 设置 `margin-left` 或 `padding-left` 
- `r` - 设置 `margin-right` 或 `padding-right` 
- `x` - 设置 `*-left` 或 `*-right` 
- `y` - 设置 `*-top` 或 `*-bottom` 
- 空 - 直接对 `margin` 或 `padding` 属性设置(对四个边都起作用)。

_size_ 取值范围：

- `0` - 删除 `margin` 或 `padding`(设置为 `0`)
- `1` - 设置 `margin` 或 `padding` 值为 `$spacer * .25`
- `2` - 设置 `margin` 或 `padding` 值为 `$spacer * .5`
- `3` - 设置 `margin` 或 `padding` 值为 `$spacer`
- `4` - 设置 `margin` 或 `padding` 值为 `$spacer * 1.5`
- `5` - 设置 `margin` 或 `padding` 值为 `$spacer * 3`
- `auto` - 设置 `margin` 的 auto 值。 

注：`$spacer` 值为 `1rem`。若以浏览器默认 `1rem` 等于 `16px` 计算，_size_ 与 _px_ 的换算关系如下：

- `1` ＝ `4px` (`.25rem`)
- `2` ＝ `8px` (`.5rem`)
- `3` ＝ `16px` (`1rem`)
- `4` ＝ `24px` (`1.5rem`)
- `5` ＝ `48px` (`3rem`)

可以通过修改源码 `variables.scss` 文件中定义的 `$spacers` 变量添加额外 size 支持。

## 例子

可以轻松设置水平居中

```html
<div class="u-mx-auto" style="width: 400px;">我 400px 宽，现在水平居中啦</div>
```

可以轻松设置各方向间距。

```html
<div class="u-mx-auto u-py-5 u-px-3" style="max-width: 1200px;">我很宽，水平居中了，而且四边都设置 padding 了。</div>
```

在线例子：[spacing.html](../../examples/utilities/spacing.html)。

（完）