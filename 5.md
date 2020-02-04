# 第五章：Alias详解

从1.0.90开始，alis加入Aris全家桶。具体来说，Alias包含了两个指令，add和rm。

## add

add指令用于把网站/app/联系人/指令结合添加到侧栏并且可以搜索到。

当输入是一个网址时，会把这个地址作为书签添加到侧栏并可以在桌面搜索到。

当输入时一个app或者联系人时，只会把它添加到侧栏。

当输入时一个指令集合时，例如（cd download/file-&gt;latest）时，会把这串指令作为快捷指令添加到侧栏并可以搜索到。

## rm

如果需要删除添加的指令，使用&lt;名称&gt;-&gt;rm即可。

## **指令集合**

如果你需要把某个文件夹下的最新文件（例如某浏览器的下载文件夹）发送给QQ好友，那么你会使用：

```text
cd browser/download/files->latest->qq
```

如果经常要使用这个指令的话，你就可以通过这条指令加入：

```text
cd browser/download/files->latest->qq->add keke
```

这样，下一次你执行keke的时候，就会自动把文件夹/browser/download/files下最新的文件分享到QQ中。

通过add指令添加的任何指令集会被添加到侧栏的文件夹中，也就是说，你可以通过add添加单个应用到文件夹中。

