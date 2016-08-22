---
layout: post
title: Cocoapod Usage
date: 2016-08-22 14:55:01 
tags: iOS Tips
---

#How to use cocoapod<br>

get sources: to see my cocoapod sources<br>
search componentName: to search in cocoapod to see weather cocoapod has this component

##Use Process
1. vim Podfile (in the project path) - New Podfile or modify Podfile what style in the Podfile is:(pod "MBProgressHUD")
2. complete edit, then :wq - save what modified in the Podfile 
3. pod install --verbose --no-repo-update (install the cocoaPod component in current project)
4. exit Xcode, and later open workspace to go on some code work

target ‘YourProjectName’ do 
pod ‘AFNetworking’, ‘~> 2.1’ 
// all other pods goes here 
end