
---
title: 发版说明
description: 
platform: Cocos
updatedAt: Wed Sep 16 2020 09:27:41 GMT+0800 (CST)
---
# 发版说明
## 简介

该游戏软件包提供游戏语音功能。点击 [游戏产品概述](https://docs.agora.io/cn/Interactive%20Gaming/product_gaming?platform=All%20Platforms) 了解关键特性。

## 2.1.0 版

该版本于 2018 年 2 月 27 日发布。新增特性与修复问题列表详见下文。

### 新增功能

<table>
<colgroup>
<col/>
<col/>
</colgroup>
<tbody>
<tr><td><strong>功能</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr><td>提醒角色状态变化</td>
<td>指挥模式下，新增回调接口提醒频道内用户指挥与被指挥者角色状态发生变化</td>
</tr>
<tr><td>API 名称变化</td>
<td>所有出现 <code>forGaming</code>的 API 类和枚举值名称，<code>forGaming</code>全部删除</td>
</tr>
</tbody>
</table>



### 优化

节省带宽:

-   v2.1.0 以前: 如果你选择不听某人的音频或不看某人的视频，音视频流会照发。

-   v2.1.0 开始: 如果你选择不听或不看某人的流，则不会下发，从而节省带宽;


### 修复问题

-   修复了一系列特定条件下偶现的崩溃;

-   修复了一些语音路由不符合预期的问题;


## 2.0 版

该版本于 2017 年 8 月 26 日发布。新增特性与修复问题列表详见下文。

**新增功能:**

支持禁用语音后可以通过音量键来调节背景音乐

**修复问题:**

-   修复了部分设备上音效播放相关的问题

-   修复了少数安卓手机录音不正常的问题


## 1.1 版

该版本于 2017 年 5 月 25 日发布。新增特性与修复问题列表详见下文。

本次发版主要优化了若干手机的音频问题

## 1.0 版

该版本于 2017 年 5 月 3 日发布。新增特性与修复问题列表详见下文。


该 SDK 首次发版，主要包含以下功能:

-   提供一套 C++ API 支持游戏语音功能

-   多音效播放功能: 包含预加载模式, 音效方位感

-   虚拟立体声功能: 不同 uid 不同方位的听感

-   语音变声功能

-   去杂音模式: 开启后只有人声被保留，其他杂音被滤除

-   压缩包大小

-   性能优化



