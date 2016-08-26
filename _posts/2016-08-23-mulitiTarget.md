---
layout: post
title: iOS多版本控制
date: 2016-08-23
tags: iOSTips 
---

在项目的开发过程中我们经常会遇到要开发两个版本，一个是测试，一个是正式版，两个版本对应的bundleid、API路径都不一致，每次打包都需要修改好多东西，一不小心还有可能出错，甚至会出现非常严重的后果。为此，在一个project中添加多个Target可以完美的解决这个烦恼。接下来我就简单的给大家介绍下步骤。
首先，先建一个singleView的Project。

![](/assets/2016/mt01.png)

我们从新建好的工程中可以看出，目前只有一个target。我们需要再建一个，鼠标点击当前的Target，然后右击，有个`Duplicate`。

![](/assets/2016/mt02.png)

点击duplicate之后，Xcode会提示我们需要复制一个什么样的Target，我们根据自己的要求选择是iPhone的target还是iPad的target，我们以iPhone的target为例。

![](/assets/2016/mt03.png)

此时，我们从工程中可以看出，多了一个`MultiTargetDemo copy`的Target，并且多在工程的导航处多了一个`MultiTargetDemo copy-Info.plist`的文件，这个plist文件就是对应copy的target的，我们修改下名称。

![](/assets/2016/mt04.png)

重命名之后，target找不到plist文件了，我们可以看到target页面中有个`Choose Info.plist`的按钮

![](/assets/2016/mt05.png)

我们选择我们自己的plist文件。

![](/assets/2016/mt06.png)

你以为到这就结束了？NO No No，我们看看Scheme，Scheme的名字还是以copy结尾的那个名字，我们需要对这边也修改下。点击Scheme的`Manage Schemes`，修改Scheme的名字。

![](/assets/2016/mt01.png)

接下来，我们就可以同时部署两套证书啦。
在代码中进行Target的判断。

```
#ifdef MultiTargetDemo
#else
#endif
```