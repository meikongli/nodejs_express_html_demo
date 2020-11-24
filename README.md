# nodejs_express_html_demo 此项目为 node.js 加 express 加 html 结合的demo 

##如何创建项目
1,先安装node.js 和 express (自己去网上搜索一堆安装教程)
2,创建项目
 2.1 express 项目名称
 2.2 cd 项目名称
 2.3 npm install
 2.4 cd bin  (进入bin里面启动项目)
 2.5 node www (启动项目) 也可以用另外一种方式启动 npm start
 
3,nodejs+express生成的项目, 将jade模板引擎改为html模板
 3.1 项目文件夹下安装ejs模块
 npm install ejs --save

 3.2 2.app.js文件中新增代码
var ejs = require('ejs');

app.engine('.html', ejs.__express);
app.set('view engine', 'html');


4,views文件夹下删除原来以.jade结尾的文件，新建index.html
 4.1 示例
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>
  <h1>Hello, Express is very Good!</h1>
</body>
</html>
