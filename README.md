1.适用于node工程 输出文件日志记录
  日志会以 /_logs/xxx/年-月-日.txt形式输出  
==== 
```js
 npm insatll logs-dir

```


```js
 var logs = require('logs-dir');

 var err_data = "发生错误";

 logs.write('error',err_data);  

```
2.文件 输出夹 _logs/error/2017-8-22.txt; 
====  
3.文件内容
==== 
 ---2017-8-21 11:6:32【发生错误】


 # logs-dir

## Installation

Using npm:
```shell
$ npm insatll logs-dir -s

```

In Node.js:
```js
 var logs = require('logs-dir');

 var err_data = "发生错误";//error log

 logs.write('error',err_data);  //err_data / string  


 var err_list ={"test":"test1"}; //error log

 logs.write('error',JSON.stringify(err_list));  //err_data / object  


```


**result:**<br>
 /_logs/error/year-month-day.txt <br>
 error_content:<br>
 ---2017-8-21 11:6:32【发生错误】<br>

 ---2017-8-21 11:6:32【{"test":"test1"}】<br>
 


## Support

Tested in Chrome 54-55, Firefox 49-50, IE 11, Edge 14, Safari 9-10, Node.js 6-7, & PhantomJS 2.1.1.<br>

