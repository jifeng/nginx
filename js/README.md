# 当 nginx 遇上 javascript

## 历史

* 之前Nginx支持的语言：C, lua，perl
* 2015年9月，nginx宣布支持类JavaScript语言

### nginScript

* nginScript是JavaScript/ECMAscript的子集。它实现了大部分的JavaScript语言的能力，没有完全遵从ECMAScript标准，同时抛弃了JavaScript比较难懂的部分。
* nginScript不是通过V8引擎实现的。而是通过一个更小、能耗更低、更符合nginx应用场景的小虚拟机（VM）来实现。可以理解为nginx为其实现了一套自己的词法解析。
* nginScript是跑在nginx的配置文件里。 比如：nginx.conf文件里。所以nginScript可以完成传统配置文件所能处理的所有事情，同时可以让配置管理动态化。这也是nginScript出现的最重要的原因。
* nginScript是以nginx插件的方式存在。 插件名叫：njs 。和其他nginx插件一样，我们需要重新编译nginx来完成安装。
*nginScript目前是早期研发状态。大家可以通过邮件nginx-devel@nginx.org等方式和nginx团队进行沟通和提出你的诉求。


### 特性

Nginx有一些独特的需求，他们希望nginScript代码片段可以在Nginx处理请求时运行，以此扩展Nginx处理请求和响应的能力。
但是，他们无意创建一个像Node.js那样的持久化的JavaScript应用程序运行时环境。

### link

* https://www.nginx.com/resources/wiki/nginScript/
