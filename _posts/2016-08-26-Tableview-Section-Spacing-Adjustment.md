---
layout: post
title: TableView Section Spacing Adjustment
date: 2016-08-20 14:55:01 
tags: iOS Tips
---

```objective-c
- (CGFloat)tableView:(UITableView *)tableView heightForFooterInSection:(NSInteger)section {
    return 0.1;
}
- (CGFloat)tableView:(UITableView *)tableView heightForHeaderInSection:(NSInteger)section {
    return 10;
}
```
在grouped的tableview中，要设置section的头部和脚部的高度时，设置0不是最小值，设置为0.1就好了。