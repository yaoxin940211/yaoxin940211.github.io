---
title: '[VSCODE] 使用小技巧'
date: 2019-03-14 21:22:00
tags: [VSCode, Tips]
---
<!-- toc -->

# VSCode使用小技巧
<!--More-->
## 给python和lua增加region功能
>打开D:\Program Files\Microsoft VS Code\resources\app\extensions, 把路径改为自己的，打开 python 和 lua 目录，修改其中的 language-configuration.json 文件，在配置文件最后加上如下代码
### python
```
"folding": {
	"offSide": true,
	"markers": {
		"start": "^\\s*#\\s*region\\b",
		"end": "^\\s*#\\s*endregion\\b"
	}
}
```
### lua
```
"folding": {
    "offSide": true,
    "markers": {
        "start": "^\\s*--\\s*region\\b",
        "end": "^\\s*--\\s*endregion\\b"
    }
}
```
> 改完后记得要重启vscode才会生效