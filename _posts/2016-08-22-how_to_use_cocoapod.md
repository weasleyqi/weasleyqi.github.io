---
layout: post
title: Cocoapod Usage
date: 2016-08-22 14:55:01 
tags: iOS Tips
---



get sources: to see my cocoapod sources<br>
search componentName: to search in cocoapod to see weather cocoapod has this component,For example:`search AFNetworking`

##Use Process
* vim Podfile (in the project path) - New Podfile or modify Podfile what style in the Podfile is:(pod "MBProgressHUD")
* complete edit, then :wq - save what modified in the Podfile 
* pod install --verbose --no-repo-update (install the cocoaPod component in current project)
* exit Xcode, and later open workspace to go on some code work

```swift
target ‘YourProjectName’ do 
pod ‘AFNetworking’, ‘~> 2.1’ 
// all other pods goes here 
end
```
