# 插件合集

需配合[Hoshino(v2)](https://github.com/Ice-Cirno/HoshinoBot)使用

[TOC]

## 分群日程表

### 功能

- **日历|本周日历|今日日历|明日日历**：查看日程表

  > 注意：如果你的hoshino缝合了yobot，使用这条指令时请尽量使用**日历**关键字，因为**日程**关键字和yobot自带的日程功能冲突

- **切换日程**：切换日程表地区

- **设置日程时间**：切换日程表每日推送时间

  > 注意：如果要开启每日推送，每个群需要先设置时间。执行此条命令后会默认执行**开始推送日程**命令，无需重复执行

- **查看日程地区**：查看本群日程表地区

- **查看日程时间**：查看本群日程表推送时间

- **停止推送日程**：停止推送日程

  > 注意：直接禁用本插件并不会停止推送日程，如需要禁用本插件，请先执行此命令

- **开始推送日程**：开始推送日程

### 部署

- 将本项目的`calendar`文件夹，放入`hoshino/modules`文件夹下
- 在hoshino的配置文件中添加`calendar`模块
- 重启hoshino

## pcr-wiki插件

详见[pcr-wiki](https://github.com/pcrbot/pcr-wiki)

## 拉黑插件

### 功能

- **拉黑x分钟@成员**：拉黑指定群员x分钟

- **拉黑x小时@成员**：拉黑指定群员x小时

- **拉黑x天@成员**：拉黑指定群员x天

> 注意：以上命令中的x为正整数。使用的是hoshino自带的拉黑，重启bot后会清空所有拉黑信息

### 部署

将本项目的`botmanage/set_block.py`文件复制到`hoshino/modules/botmanage`下，重启hoshino

### 后续会更新的功能

- 拉黑列表持久化

## 生成器插件

### 功能

- **营销号 主体/事件/另一种说法**：营销号生成器

> 注意：所有参数都是必填的，**不是**选填，`/`也是必要的
>
> 正确命令示例：营销号 洛洛/白嫖代码/洛洛不会写代码

- **狗屁不通 主题**：狗屁不通生成器

> `data.json`为该生成器的词库，可根据需要自行修改

- **记仇 天气/主题**：记仇表情包生成器

> 同营销号，所有参数都是必填的

- **我(有个|一个|有一个)朋友(想问问|说|让我问问|想问|让我问|想知道|让我帮他问问|让我帮他问|让我帮忙问|让我帮忙问问|问)XXX**：无中生友

> 1. 括号内`|`分隔的内容选填
> 2. xxx为生成图片上要说的话，xxx内的“他”和“她”会自动更换为“我”
> 3. 如果命令后没有艾特任何人，则使用随机头像。`config.json`中可配置在某个群随机的头像范围（不在群内的QQ号也可以），如果某个群没在`config.json`里找到配置，则随机全群成员
> 4. 如果命令后艾特某人，则使用被艾特人的头像

- **日记**：舔狗日记生成器

> `diary_data.json`为该生成器的词库，可根据需要自行修改
>
> 若命令后艾特某人，则使用被艾特人的昵称

### 部署

- 将本项目的`generator`文件夹，放入`hoshino/modules`文件夹下
- 在hoshino的配置文件中添加`generator`模块
- 重启hoshino

## 以图搜图

### 功能

- **识图【图片】**：查询图片来源

> 注意：【图片】应该为需要查找的图

### 部署

- 将本项目的`picfinder`文件夹，放入`hoshino/modules`文件夹下
- 在hoshino的配置文件中添加`picfinder`模块
- 去[SauceNAO](https://saucenao.com/)注册账号并获取自己的api_key，将api_key填写到`picfinder.py`第17行对应位置
- 在`picfinder.py`第18行修改你想设置的最低匹配度（默认"70!"指返回70%匹配度以上的结果）
- 重启hoshino

### 后续会更新的功能

- 返回查询结果缩略图

## 以图搜番

### 功能

- **搜番【图片】**：根据图片查询番剧(日本本土二次元番剧)

> 注意：【图片】应该为需要查找的图。此插件对图片要求很高，局部图，清晰度太低的图，查询结果可能会不太准确

### 部署

- 将本项目的`traceanime`文件夹，放入`hoshino/modules`文件夹下
- 在hoshino的配置文件中添加`traceanime`模块
- 在`traceanime.py`第34行修改你想设置的最低匹配度（默认为0.70，低于0.87的结果可能不太准确）
- 重启hoshino

### 后续会更新的功能

- 返回番剧封面，额外信息，匹配到的片段等