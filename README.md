# AJAX 扩展工具

## 适用场景：

* 按钮被多次点击，发出多个请求。此时使用 old 模式保证使用第一次点击请求
* tab切换，发出多个请求。此时使用 new 模式保证使用最后一次请求
* auto模式，根据url和请求参数判断使用 old 还是 new模式

## 使用方法：

扩展了$.ajax，增加了参数

```
    $.ajax({
        name: '请求标识', // 标识相同表示是一个single，则会根据rule进行判断处理
        rule: 'new/old/auto' // 默认new
    });
```
