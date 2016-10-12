# 安全 :construction: [WIP]

## 目录

1. [XSS]应将用户输入的数据进行 HtmlEncode
1. [XSS]应将重要的cookie标识为http only
1. [XSS]应过滤或移除特殊的Html标签
1. [XSS]应过滤javascript事件的标签
1. [CSRF]对于HTTP请求应加上token等认证信息
1. [postMessage]使用postMessage时应验证来源的可信
1. [WebStorage]用户的 sessionID 放入 sessionStorage，而不是放入 LocalStorage
1. [WebStorage]不应把敏感重要的数据存储在 WebStorage 里
1. [WebSQL]应使用参数形式构造 SQL，不使用字符串拼接方式
1. [WebSQL]不应在本地数据库里存放敏感的数据
