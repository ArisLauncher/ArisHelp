# 开发者模式

{% hint style="danger" %}
此功能已下线，敬请期待后续版本。
{% endhint %}

从1.1.70开始，Aris提供了多个开发者插件，用户可以直接在Aris上开发基于HTTP请求的插件。本章以获取实时汇率为例，来介绍开发插件的使用。

首先，输入dddddvlp指令以进入开发者模式。

获取人民币兑换美元汇率的接口地址为[https://api.fixer.io/latest?base=CNY\&symbols=USD](https://api.fixer.io/latest?base=CNY\&symbols=USD)

复制这个地址，并在Aris中执行clipboard->post

此时，终端会输出

```
{"base":"CNY","date":"2017-11-20","rates":{"USD":0.15074}}
```

接下来，你可以通过连接符直接把该输出连接到JGET插件。例如，执行->jget rates

你会得到

```
{"USD":0.15074}
```

再进一步，如果你只需人民币兑换美金的数值，只需要再执行->jget USD。

也就是说，获取人民币兑换美金的数值完整的指令为

[https://api.fixer.io/latest?base=CNY\&symbols=USD->post->jget](https://api.fixer.io/latest?base=CNY\&symbols=USD-%3Epost-%3Ejget) rates->jget usd

## 保存指令

辛辛苦苦写的代码当然要保存一下了。你可以通过add指令把上面的指令集合保存起来，命名为usd。

[https://api.fixer.io/latest?base=CNY\&symbols=USD->post->jget](https://api.fixer.io/latest?base=CNY\&symbols=USD-%3Epost-%3Ejget) rates->jget usd->add usd

之后，你只需要执行usd就可以获取当前的人民币兑美金汇率了。

## **参数**

现在你要关注多个汇率数值，你可以使用$s把货币作为参数，把这个指令保存为currency：

[https://api.fixer.io/latest?base=CNY\&symbols=$s->post->jget](https://www.gitbook.com/book/7doger/aris/edit) rates->jget usd->add currency

接下来再执行USD->currency就可以获取当前的人民币兑美金汇率了

## 分享指令

以上面的例子来说，你可以使用currency->submit来把指令上传到服务器中，这样大家就可以使用你开发的指令了:)。

//TODO to be continued
