# 通用 :construction: [WIP]

## 目录

1. [应统一文件命名风格](#%E7%BB%9F%E4%B8%80%E6%96%87%E4%BB%B6%E5%91%BD%E5%90%8D%E9%A3%8E%E6%A0%BC)
1. [应将文件分类存放](#%E6%B2%A1%E6%9C%89%E5%B0%86%E6%96%87%E4%BB%B6%E5%88%86%E7%B1%BB%E5%AD%98%E6%94%BE)
1. [应采用 UTF-8 编码](#%E9%87%87%E7%94%A8%E9%9D%9E%20UTF-8%20%E7%BC%96%E7%A0%81)
1. [保持一致的缩进风格](#%E4%BF%9D%E6%8C%81%E4%B8%80%E8%87%B4%E7%9A%84%E7%BC%A9%E8%BF%9B%E9%A3%8E%E6%A0%BC)
1. [应删除无用的空格/空行](#%E5%BA%94%E5%88%A0%E9%99%A4%E6%97%A0%E7%94%A8%E7%9A%84%E7%A9%BA%E6%A0%BC/%E7%A9%BA%E8%A1%8C)
1. [应使用空行划分逻辑相关的一组代码](#%E5%BA%94%E4%BD%BF%E7%94%A8%E7%A9%BA%E8%A1%8C%E5%88%92%E5%88%86%E9%80%BB%E8%BE%91%E7%9B%B8%E5%85%B3%E7%9A%84%E4%B8%80%E7%BB%84%E4%BB%A3%E7%A0%81)
1. [应添加必要的注释](#%E5%BA%94%E6%B7%BB%E5%8A%A0%E5%BF%85%E8%A6%81%E7%9A%84%E6%B3%A8%E9%87%8A)
1. [应对文件进行压缩](#%E6%9C%AA%E5%AF%B9%E8%BE%93%E5%87%BA%E6%96%87%E4%BB%B6%E8%BF%9B%E8%A1%8C%E5%8E%8B%E7%BC%A9%EF%BC%88JS/CSS%EF%BC%89)

## 统一文件命名风格

  - 文件与文件夹统一以小写字母、连线符命名

  ```bash
  # avoid:
  src/app/vueComponents/CButton.vue
  # recommended:
  src/app/vue-components/c-button.vue
  ```

## 应将文件分类存放

  - 文件应按功能、类型等分类存放

  ```bash
  # recommended:
  src
  ├─assets
  ├─components
  ├─routes
  ├─static
  │  ├─i18n
  │  └─images
  ├─store
  │  ├─constants
  │  ├─modules
  │  └─plugins
  ├─themes
  │  └─default
  │      ├─components
  │      │  └─images
  │      ├─fonts
  │      ├─variables
  │      └─views
  ├─utils
  └─views
  ```

## 应采用 UTF-8 编码

  - 未特殊要求的情况下，文件应统一采用不带 BOM 的 UTF-8 编码

## 保持一致的缩进风格

  - 同一个项目应保持一致的代码缩进风格，增强可读性

## 应删除无用的空格/空行

  - 无用的行尾空格
  - 无用的空行

## 应使用空行划分逻辑相关的一组代码

  - 比如两个函数之间要使用空行分隔

```js
// avoid:
function a() {
  ...
}
function b() {
  ...
}

// recommended:
function a() {
  ...
}

function b() {
  ...
}
```

## 应添加必要的注释

  - 对于逻辑比较复杂，或容易引起歧义的地方，应添加注释说明

```js
// recommended:
// a is 0, false or empty
if (a == '') {
  alert('empty')
}
```

## 应对文件进行压缩

  - 应使用代码压缩工具对 HTML、CSS、JS 文件进行压缩
