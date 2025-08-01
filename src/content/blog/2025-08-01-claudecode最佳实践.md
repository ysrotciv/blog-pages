---
title: 'Claude Code最佳实践(持续更新)'
description: ''
pubDate: 'Aug 01 2025'
heroImage: '../../assets/claude-code.png'
---

### 连接IDE

可以使用/ide命令来让命令行中的claude code连接已经打开相同路径的ide，实现ide对项目的实时检测，待测试

### 多开

claude code多开需要指定不同的路径，不过可以使用`/add-dir /path-you-specify`命令来指定需要添加的路径

### 对未完成的工作进行“存档”

使用`# to memorize`对未完成的工作进行存档
在一篇新文章中看到可以用这个命令来增加新的规则

### 完成任务后提醒

`claude config set --global preferredNotifChannel terminal_bell`

### 利用打包命令节省token

`/clear` 可以用来完成部分工作后清除上下文

`/compact` 可以用来压缩上下文

### 执行shell命令

可以使用`!` + shell命令的形式直接从claude code的对话框中执行shell命令，不需要另开一个新的窗口

### 待实现功能

#### 生成git commit内容

可以利用claude code读取git diff内容来自动生成commit message，git diff内容可以通过webhook获取

### 参考

[claude code 进阶操作一览](:/274dd3f75e2c4c6cb6b12630f1713fd2)