# **第七章：开发者模式**

从1.1.70开始，Aris提供了多个开发者插件，用户可以直接在Aris上开发基于HTTP请求的插件。本章以获取实时汇率为例，来介绍开发插件的使用。

首先，输入dddddvlp指令以进入开发者模式。

获取人民币兑换美元汇率的接口地址为https://api.fixer.io/latest?base=CNY&symbols=USD

复制这个地址，并在Aris中执行clipboard-&gt;post

此时，终端会输出

```
{"base":"CNY","date":"2017-11-20","rates":{"USD":0.15074}}
```

接下来，你可以通过连接符直接把该输出连接到JGET插件。例如，执行-&gt;jget rates

你会得到

```
{"USD":0.15074}
```

再进一步，如果你只需人民币兑换美金的数值，只需要再执行-&gt;jget usd（请注意，Aris的开发者插件忽略大小写）

也就是说，获取人民币兑换美金的数值完整的指令为

https://api.fixer.io/latest?base=CNY&symbols=USD-&gt;post-&gt;jget rates-&gt;jget usd



//TODO to be continiued

