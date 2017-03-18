##Babel
####基本使用
1. babel-cli
```
babel xxx.js --out-file out.js
或
babel xxx.js -o out.js
```
2. babel-regiest
```
require("babel-register");
require("./index.js");
```
3. babel-node

直接运行未编译代码，等同node

4. babel-core

使用编程方式使用Babel
```js
var babel=require("babel-core");
//代码
babel.transform("code",options);
//=>{code,map,ast}
//文件
//异步
babel.transformfile('file.js',options,function(err,result){
  resutl;//=>{code,map.ast}
})
//同步
babel.transformFileSync('file.js',options);
//=>{code,map,ast}
//从Babel AST转换
babel.transformFromAst(ast,code,options);
//=>{code,map,ast}
```
####.babelrc
```json
{
  "presets":[],
  "plugins":[]
}
```
#####`babel-preset-es2015`
```json
{
  "presets":[
    "es2015"
  ],
  "plugins":[]
}
```
#####`babel-preset-react`
```json
{
  "presets":[
    "es2015",
    "react"
  ],
  "plugins":[]
}
```
####babel-polyfill
`import "babel-polyfill"`

babel只会转换语法，不换转换api
