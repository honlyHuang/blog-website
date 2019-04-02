# xdemo

``` html
+ xdemo
    + css
        - bootstrap.css
        - bootstrap.min.css
        - github.css
        - pupup.css
        - rainbow-min.css
        - style.css
        - switch.css
    + fonts
        - 
    + img
    + js
        - background.js chrome插件必须，
        - bootstrap.js 
        - bootstrap.min.js 
        - bootstrap-switch.min.js 
        - content.js chrome插件必须，
        - generic.js rainbow通用语法匹配
        - getGroupList.json 从服务器上获取
        - getid.js 获取用户名
        - getList.json 从服务器上获取
        - javascript.js rainbow匹配javascript语法
        - jquery.min.js 
        - mustache.js 模版引擎
        - option.js 对应option.html
        - popup.js 对应popup.html
        - rainbow-min.js Rainbow is a code syntax highlighting library written in Javascript.
    - LICENSE
    - manifest.json 插件相关信息
    - option.html 插件设置页面
    - popup.html 页面右上角点击弹出的页面
    - README.md 
    - xdemo.crx 打包后
```

### background.js

    - 截屏？？？
    - onActivated 获取localStorage的内容
    - onUpdated 当标签更新时，此事件被触发。插入样式和js文件。
    - UrlRegEX url解析
    - domainMatch 域名匹配

### content.js
