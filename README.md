# 灵夜机器人指令文档

## 关于

机器人QQ：`2044450237`

机器人使用Python 3编写，使用CoolQ作为框架。

另外感谢[nonebot](https://github.com/nonebot)以及[python-aiocqhttp](https://github.com/cqmoe/python-aiocqhttp)的制作者[RichardChien](https://github.com/richardchien)的辛苦奉献！

项目将在2020-08-13停止。

## 指令大全

### 权限类

|       | 其他用名 | 使用权限      | 使用方法         | ifDeprecated | 备注                                 |
| --------- | ---- | --------- | ------------ | ------------ | ---------------------------------- |
| 添加信任  | None | Owner     | !添加信任 `QQ号`  | False        | None                               |
| 移除信任  | None | Owner     | !移除信任 `QQ号`  | False        | None                               |
| 添加管理  | None | Owner     | !添加管理 `QQ号`  | False        | None                               |
| 删除管理  | None | Owner     | !删除管理 `QQ号`  | False        | None                               |
| 救救bot | None | Everyone  | !救救bot `str` | True         | 目前被`我懂了`指令替代                       |
| 救救孩子  | None | Everyone  | !救救孩子 `str`  | True         | 目前被`我懂了`指令替代                       |
| 我懂了   | None | Owner     | !我懂了 `str`   | False        | 替代了原来的`救救孩子`和`救救bot`指令。如果输入为$，将会把本语料设置为只可读状态。只有Owner权限的用户可对此进行再次更改             |
| 问题    | None | Everyone  | !问题 `QQ号`    | False        | 回答一些乱七八糟的问题，如果有语料默认使用语料，如果没有将会尝试回答 |
| 移除语料  | None | whitelist | !移除语料 `str`  | False        | 移除已添加的语料                           |
| 语料查询  | None | Everyone  | !语料查询 `str`  | False        | 查询已添加语料                            |
| ban   | None | whitelist | !ban `QQ号`   | False        | 禁用用户使用某些功能                         |
| unban | None | whitelist | !unban `QQ号` | False        | 启用被禁用用户使用某些功能                      |
| 添加监控词 | None | Owner | !添加监控词 `str` | False | 添加色图功能的监控关键词 |

### 闲聊类

|          | 其他用名        | 使用权限     | 使用方法      | ifDeprecated | 备注                        |
| -------- | ----------- | -------- | --------- | ------------ | ------------------------- |
| ?        | ？           | Everyone | !?        | False        | 无聊添加的，一般是用于测试机器人是不是死锁了    |
| 你好       | None        | Everyone | !你好       | False        | 没啥用……就是写着玩                |
| 内鬼       | None        | Everyone | !内鬼       | False        | 没啥用……就是写着玩。随机回答你是内鬼或者不是xD |
| 生草       | None        | Everyone | !生草       | False        | 发一条Vtuber的生草语音            |
| 我什么都不行   | 流泪猫猫头、什么都不行 | Everyone | !我什么都不行   | False        | 发一张流泪猫猫头的图片               |
| 威胁       | None        | Everyone | !威胁       | False        | 威胁梗表情包                    |
| 恰柠檬      | 吃柠檬         | Everyone | !恰柠檬      | False        | 发一张吃柠檬的表情包                |
| 迫害       | None        | Everyone | !迫害       | False        | 发一张迫害Vtuber的表情包           |
| 不愧是你     | bksn        | Everyone | !不愧是你     | False        | 发一张不愧是你的表情图               |
| 恰桃       | 恰peach      | Everyone | !恰桃       | False        | 发一张恰桃表情包                  |
| 社保       | awsl        | Everyone | !社保       | False        | 发一张社保的表情包或者吐槽信息           |
| votekick | None        | Everyone | !votekick | False        | 沙雕功能……                    |
| otsukare | 辛苦了、おつかれ    | Everyone | !辛苦了      | False        | 发一张辛苦了的图                  |

### 游戏类

|     | 其他用名 | 使用权限     | 使用方法 | ifDeprecated | 备注                                |
| --- | ---- | -------- | ---- | ------------ | --------------------------------- |
| 赛马  | None | Everyone | !赛马 `int`  | False         | 就是……赛马               |
| 比大小 | None | Everyone | !比大小 | False         | 需要两个玩家。       |
| 轮盘赌 | None | Everyone | !轮盘赌 | False         | 如果机器人有权限会禁言输家 |
| 转轮  | None | Everyone | !转轮  | False         | Change random seed.               |

### 应用类

|      | 其他用名   | 使用权限     | 使用方法          | ifDeprecated | 备注          |
| ---- | ------ | -------- | ------------- | ------------ | ----------- |
| b站话题 | bTopic | Everyone | !bTopic `str` | False        | 使用关键词查询B站话题 |

### 工作类

|         | 其他用名 | 使用权限     | 使用方法     | ifDeprecated | 备注                          |
| ------- | ---- | -------- | -------- | ------------ | --------------------------- |
| 添加任务    | None | Admin    | !添加任务    | False        | 添加一个按时提醒的任务                 |
| 删除任务    | None | Admin    | !删除任务    | False        | 移除一个按时提醒的任务                 |
| 标记完成    | None | Admin    | !标记完成    | False        | 标记一个任务完成，该任务将不会再被提醒         |
| 移除staff | None | Admin    | !移除staff | False        | 移除一个负责该任务的人                 |
| 查询任务    | None | Everyone | !查询任务    | False        | Print unfinished job detail |

### 帮助类

|        | 其他用名 | 使用权限     | 使用方法          | ifDeprecated | 备注                 |
| ------ | ---- | -------- | ------------- | ------------ | ------------------ |
| help   | None | Everyone | !help         | False        | 发送该文档所在网址          |
| 翻译     | None | Everyone | !翻译 `str`     | False        | 翻译文字到中文，或者翻译到英文和日文 |
| 日语词典   | None | Everyone | !日语词典 `str`   | True         | 可能用不了了。查日语词用的      |
| 最新地震   | None | Everyone | !最新地震         | False        | 最新的地震信息获取          |
| 日日释义   | None | Everyone | !日日释义 `str`   | True         | 可能用不了了。查日语词用的      |
| 注音     | None | Everyone | !注音 `str`     | True        | 对汉字注罗马音，好像API出问题用不了了            |
| 释义nico | None | Everyone | !释义nico `str` | False        | 查询nico百科的解释        |
| 周公解梦   | None | Everyone | !周公解梦 `str`   | True         | 可能用不了了             |
| 反码     | None | Everyone | !反码 `str`     | False        | 返回CQ码（如果用的话）       |
| 好好说话   | None | Everyone | !好好说话 `str`   | False        | 查询缩写意味             |
| 查车票    | None | Everyone | !查车票          | True         | 在12306里查车票信息       |

### 沙雕娱乐功能

|         | 其他用名        | 使用权限      | 使用方法                     | ifDeprecated | 备注                                  |
| ------- | ----------- | --------- | ------------------------ | ------------ | ----------------------------------- |
| 来个老婆    | None        | Everyone  | !来个老婆                    | False        | AI生成一个不存在的动漫角色                      |
| shadiao | 沙雕图、来一张沙雕图  | Everyone  | !沙雕图                     | False        | 发送一个网上瞎找的沙雕图                        |
| PCR     | None        | Everyone  | !PCR                     | False        | 发出最新的PCR讯息                          |
| 你群有多色   | None        | Everyone  | !你群有多色                   | False        | 统计`色图`和`验车`等功能在群里用了多少次               |
| 理智查询    | None        | Everyone  | !理智查询                    | False        | 看看还有多少理智                            |
| 理智补充    | None        | Admin     | !理智补充                    | False        | 补充理智                                |
| happy   | None        | Owner     | !happy                   | False        | 打开欢乐时光                              |
| 设置R18   | None        | Whitelist | !设置R18                   | False        | 开启或关闭`色图`功能的R18发送功能                 |
| 设置撤回    | None        | Everyone  | !设置撤回                    | True         | 设置要多久才撤回。现在是和跟推功能一起撤回的所以deprecated。 |
| 掉落查询    | None        | Everyone  | !掉落查询 `str`              | False        | 查询掉落物在PCR游戏中的掉落关卡                   |
| 娱乐开关    | None        | Admin     | !娱乐开关                    | False        | 全局娱乐开关                              |
| 色图状态查询  | None        | Admin     | !色图状态查询                  | False        | 查询色图功能是否在本群开放 Override: `设置色图禁用`    |
| 设置色图禁用  | None        | Admin     | !设置色图禁用 `qqGroup`        | False        | 关闭一个群的色图功能 Override: `娱乐开关`         |
| 删除色图禁用  | None        | Admin     | !删除色图禁用 `qqGroup`        | False        | 打开一个群的色图功能 Override: `娱乐开关`         |
| 验车      | None        | Everyone  | !验车 `str`                | False        | 根据番号获取AV信息                          |
| 色图      | None        | Everyone  | !色图 `str`                | False        | 根据关键词搜索色图                           |
| 嘴臭一个    | 骂我、你再骂、小嘴抹蜜 | Everyone  | !嘴臭一个                    | False        | 机器人嘴臭                               |
| 彩虹屁     | 拍个马屁、舔TA    | Everyone  | !彩虹屁 `Optional: [CQ:at]` | False        | 发送彩虹屁信息，如果有at人，会at那个人然后发彩虹屁信息       |
| 方舟十连      | None        | Everyone  | !方舟十连                      | False        | 没有黑幕的10连明日方舟抽卡模拟                     |
| 下源      | None        | Everyone  | !下源                      | False        | 下载所提供的YouTube视频                     |
| 统计      | None        | Everyone  | !统计                      | False        | 会查找使用指令用户的一些功能数据。                     |
| ghs      | None        | Everyone  | !ghs                      | False        | 发送随机色图。                     |

### 自动功能
|         | 备注 |
| ------- | ----------------------------------- |
| getTweet | 自动跟推 |
| forDownload | 自动下源，代码请见[这里](https://github.com/remiliacn/Vtuber-YouTube) |
| getPCRInfo | 自动查询PCR消息 |
| youtubeNotify | 如果下好了视频提醒 |
| fillSanity | 每50秒补充一次理智 |
