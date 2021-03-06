# tornado

* [Tornado 官方文档](http://www.tornadoweb.cn/documentation#)
    - 重要的部分基本涉及
* [Tornado book](http://demo.pythoner.com/itt2zh/index.html)

* [Github reg](https://github.com/tornadoweb/tornado)

## tornado 模板

* 扩展Tornado模板
    - 自动转义 防止xss | {% raw mailLink %} #输出不转义的内容
    - [UI模块](http://demo.pythoner.com/itt2zh/ch3.html#ch3-2)

[控制流表达式](http://demo.pythoner.com/itt2zh/ch2.html#ch2-2)
```
Tornado模板语言的一个最好的东西是在if和for语句块中可以使用的表达式没有限制。因此，你可以在你的模板中执行所有的Python代码。

同样，你也可以在你的控制语句块中间使用{% set foo = 'bar' %}来设置变量。你还有很多可以在控制语句块中做的事情，但是在大多数情况下，你最好使用UI模块来做更复杂的划分。我们稍后会更详细的看到这一点。
```
[在模板中使用函数](http://demo.pythoner.com/itt2zh/ch2.html#ch2-2-3)
```
escape(s)
替换字符串s中的&、<、>为他们对应的HTML字符。

url_escape(s)
    使用urllib.quote_plus替换字符串s中的字符为URL编码形式。
json_encode(val)
    将val编码成JSON格式。（在系统底层，这是一个对json库的dumps函数的调用。查阅相关的文档以获得更多关于该函数接收和返回参数的信息。）
squeeze(s)
    过滤字符串s，把连续的多个空白字符替换成一个空格。
```
