# CSS :construction: [WIP]

## 目录

1. 静态检查工具检查未通过
1. 使用通配符（\*）选择器
1. 颜色值大小写不一致（推荐小写）
1. 未合理地使用 CSS Sprites（比如一个页面请求多张小图）
1. 值为 0 时，没有省略 0 后面的单位
1. 没有有效利用 CSS 的继承机制
1. 没有考虑到浏览器兼容性
1. 有没有乱用hack，比如只要兼容chrome的，css就不用使用-ms-开头的
1. 使用浮动时未添加必要的清除指令（clearfix）
1. 选择器层级太深
1. 没有使用position：absolute/relative/fixed，却用了left，top属性
1. 在一个元素上同时使用float(left/right)和position(absolute/fixed)
1. display:inline-block和float或者position共用
1. 可以合并的样式属性，分开写。比如 margin-left:10px; margin-right:5px;

## Specificity

Don't make values and selectors hard to override. Minimize the use of `id`'s
and avoid `!important`.

```css
/* avoid */
.bar {
  color: green !important;
}
.foo {
  color: red;
}

/* recommended */
.foo.bar {
  color: green;
}
.foo {
  color: red;
}
```

## Inheritance

Don't duplicate style declarations that can be inherited.

```css
/* avoid */
div h1, div p {
  text-shadow: 0 1px 0 #fff;
}

/* recommended */
div {
  text-shadow: 0 1px 0 #fff;
}
```

## Brevity

Keep your code terse. Use shorthand properties and avoid using multiple properties when
it's not needed.

```css
/* avoid */
div {
  transition: all 1s;
  top: 50%;
  margin-top: -10px;
  padding-top: 5px;
  padding-right: 10px;
  padding-bottom: 20px;
  padding-left: 10px;
}

/* recommended */
div {
  transition: 1s;
  top: calc(50% - 10px);
  padding: 5px 10px 20px;
}
```

## Language

Prefer English over math.

```css
/* avoid */
:nth-child(2n + 1) {
  transform: rotate(360deg);
}

/* recommended */
:nth-child(odd) {
  transform: rotate(1turn);
}
```

## Vendor prefixes

Kill obsolete vendor prefixes aggressively. If you need to use them, insert them before the
standard property.

```css
/* avoid */
div {
  transform: scale(2);
  -webkit-transform: scale(2);
  -moz-transform: scale(2);
  -ms-transform: scale(2);
  transition: 1s;
  -webkit-transition: 1s;
  -moz-transition: 1s;
  -ms-transition: 1s;
}

/* recommended */
div {
  -webkit-transform: scale(2);
  transform: scale(2);
  transition: 1s;
}
```

## Colors

If you need transparency, use `rgba`. Otherwise, always use the hexadecimal format.

```css
/* avoid */
div {
  color: hsl(103, 54%, 43%);
}

/* recommended */
div {
  color: #5a3;
}

## Drawing

Avoid HTTP requests when the resources are easily replicable with CSS.

```css
/* avoid */
div::before {
  content: url(white-circle.svg);
}

/* recommended */
div::before {
  content: "";
  display: block;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: #fff;
}
```
