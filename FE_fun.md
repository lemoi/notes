###一些前端小技巧
1.滑动条的修改方法
```css
::-webkit-scrollbar {
  -webkit-appearance: none;
}
::-webkit-scrollbar-button {
  display: none;
}
::-webkit-scrollbar-track {
  background: #fff;
}
::-webkit-scrollbar-thumb {
  min-height: 48px;
  background: #d2d2d2;
  background-clip: padding-box;
  border: 3px solid #fff;
  border-radius: 5px;
}
::-webkit-scrollbar-thumb:active {
  background: #888;
  border-width: 2px;
}
::-webkit-scrollbar {
  width: 10px;
}
```
2.url RegExp匹配
```
/^([^:\/?#]+:)?(?:\/\/(?:([^:@\/?#]*)(?::([^:@\/?#]*))?@)?(([^:\/?#]*)(?::(\d*))?))?([^?#]*)(\?[^#]*)?(#[\s\S]*)?/

protocol = m[1] || "";
username = m[2] || "";
password = m[3] || "";
host = m[4] || "";
hostname = m[5] || "";
port = m[6] || "";
pathname = m[7] || "";
search = m[8] || "";
hash = m[9] || "";
```