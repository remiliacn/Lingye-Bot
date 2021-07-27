# 灵夜机器人指令文档

## 关于

机器人QQ：`2044450237`

机器人使用Python 3编写，使用CoolQ作为框架。

正在使用dalao写的框架，所以暂时还能用233。

本机器人的测试群：`950167209`

项目以开源！请使用issue来汇报问题！https://github.com/remiliacn/qqBot

## 声明

灵夜机器人的大部分功能使用了`数据收集`接口。该接口将会被用于用户行为分析，并对不常用的功能进行改良或者废除。使用本机器的任何指令将默许为您同意本声明，并愿意提供您的***QQ号、QQ昵称、以及使用命令时的参数***用于数据分析。您的任何敏感信息在没有同意的情况下将不会被公开（如年龄、性别、聊天记录等）。

数据采集部分源码：
https://github.com/remiliacn/qqBot/blob/master/awesome/adminControl/group_admin.py#L81-L112

另外请注意，使用以下指令可能会使您的敏感信息泄露，请谨慎使用：
* ！你群语录
* ！添加语录
* ！翻译
* ！我懂了

## 指令大全

### 权限类

|       | 其他用名 | 使用权限      | 使用方法         | if_deprecated | 备注                                 |
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
| 跟推添加 | None | Admin | !跟推添加 `str` | False | 具体语法请使用本功能查看 |
| 跟推移除 | None | Admin | !跟推移除 `str` | False | 具体语法请使用本功能查看 |

### 闲聊类

|          | 其他用名        | 使用权限     | 使用方法      | if_deprecated | 备注                        |
| -------- | ----------- | -------- | --------- | ------------ | ------------------------- |
| ?        | ？           | Everyone | !?        | False        | 无聊添加的，一般是用于测试机器人是不是死锁了    |
| 你好       | None        | Everyone | !你好       | False        | 没啥用……就是写着玩                |
| 内鬼       | None        | Everyone | !内鬼       | False        | 没啥用……就是写着玩。随机回答你是内鬼或者不是xD |
| 生草       | None        | Everyone | !生草       | True        | 发一条Vtuber的生草语音。          |
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

|     | 其他用名 | 使用权限     | 使用方法 | if_deprecated | 备注                                |
| --- | ---- | -------- | ---- | ------------ | --------------------------------- |
| 赛马  | None | Everyone | !赛马 `int`  | False         | 就是……赛马               |
| 比大小 | None | Everyone | !比大小 | False         | 需要两个玩家。       |
| 轮盘赌 | None | Everyone | !轮盘赌 | False         | 如果机器人有权限会禁言输家 |
| 转轮  | None | Everyone | !转轮  | False         | Change random seed.               |

### 应用类

|      | 其他用名   | 使用权限     | 使用方法          | if_deprecated | 备注          |
| ---- | ------ | -------- | ------------- | ------------ | ----------- |
| 虚拟货币 | - | Everyone | !虚拟货币 `str` | False        | OKEx查询虚拟货币价格 |
| K线 | 股票 | Everyone | !K线 `str` | False        | 查询股票K线图 |

### 帮助类

|        | 其他用名 | 使用权限     | 使用方法          | if_deprecated | 备注                 |
| ------ | ---- | -------- | ------------- | ------------ | ------------------ |
| help   | None | Everyone | !help         | False        | 发送该文档所在网址          |
| 反码     | None | Everyone | !反码 `str`     | False        | 返回CQ码（如果用的话）       |
| 好好说话   | None | Everyone | !好好说话 `str`   | False        | 查询缩写意味             |

### 沙雕娱乐功能

|         | 其他用名        | 使用权限      | 使用方法                     | if_deprecated | 备注                                  |
| ------- | ----------- | --------- | ------------------------ | ------------ | ----------------------------------- |
| 来个老婆    | None        | Everyone  | !来个老婆                    | False        | AI生成一个不存在的动漫角色                      |
| shadiao | 沙雕图、来一张沙雕图  | Everyone  | !沙雕图                     | False        | 发送一个网上瞎找的沙雕图                        |
| 你群有多色   | None        | Everyone  | !你群有多色                   | False        | 统计`色图`和`验车`等功能在群里用了多少次               |
| 理智查询    | None        | Everyone  | !理智查询                    | False        | 看看还有多少理智                            |
| 理智补充    | None        | Admin     | !理智补充                    | False        | 补充理智                                |
| happy   | None        | Owner     | !happy                   | False        | 打开欢乐时光                              |
| 设置R18   | None        | Whitelist | !设置R18                   | False        | 开启或关闭`色图`功能的R18发送功能                 |
| 掉落查询    | None        | Everyone  | !掉落查询 `str`              | False        | 查询掉落物在PCR游戏中的掉落关卡                   |
| 娱乐开关    | None        | Admin     | !娱乐开关                    | False        | 全局娱乐开关                              |
| 色图状态查询  | None        | Admin     | !色图状态查询                  | False        | 查询色图功能是否在本群开放  |
| 设置色图禁用  | None        | Admin     | !设置色图禁用 `qqGroup`        | False        | 关闭或打开一个群的色图功能 Override: `娱乐开关`         |
| 验车      | None        | Everyone  | !验车 `str`                | False        | 根据番号获取AV信息                          |
| 色图      | None        | Everyone  | !色图 `str`                | False        | 根据关键词搜索色图                           |
| 嘴臭一个    | 骂我、你再骂、小嘴抹蜜 | Everyone  | !嘴臭一个 `Optional: [CQ:at]`     | False        | 机器人嘴臭                               |
| 彩虹屁     | 拍个马屁、舔TA    | Everyone  | !彩虹屁 `Optional: [CQ:at]` | False        | 发送彩虹屁信息，如果有at人，会at那个人然后发彩虹屁信息       |
| 方舟十连      | None        | Everyone  | !方舟十连                      | False        | 没有黑幕的10连明日方舟抽卡模拟                     |
| 方舟限定      | None        | Admin  | !方舟限定 `开|关`                   | False        | 将本次方舟卡池的UP率改为限定卡池UP率                     |
| 下源      | None        | Everyone  | !下源                      | False        | 下载所提供的YouTube视频                     |
| 统计      | None        | Everyone  | !统计                      | False        | 会查找使用指令用户的一些功能数据。                     |
| ghs      | None        | Everyone  | !ghs                      | False        | 发送随机色图。                     |
| 添加语录      | None        | Everyone  | !添加语录 `Any`                     | False        | 添加群语录（群内只读）                    |
| 语录      | 你群语录        | Everyone  | !语录                      | False        | 发送随机已保存本群语录                |
| 清空语录      | None        | Owner  | !清空语录 `qqGroup`                      | False        | 清除群组的所有语录                |
| 方舟UP      | 方舟up        | Admin  | !方舟UP `干员名 星级`                     | False        | 设定卡池UP                    |
| 方舟UP重置      | 方舟up重置        | Admin  | !方舟UP重置                    | False        | 清除目前UP的卡池内容                   |
| 添加干员      | None        | Admin  | !添加干员 `干员名 星级`                     | False        | 添加新的干员                 |
| 说     | None        | Everyone  | !说 `str`                     | False        | 使用tts功能将文字转化为语音发出                |
| 仓库搜索     | None        | Everyone  | !仓库搜索 `str`                     | False        | 查里番本子之类的功能。用了就知道了（                |
| 搜图      | None        | Everyone  | !搜图 `图片`                     | False        | 使用SAUCEMAO服务逆搜索图片出处 （也可以回复消息并输入搜图）                 |
| 图片识别 | None | Everyone | !图片识别 `图片` | False | OCR识别图片内文字（支持多语种） | 

### 自动功能
|         | 备注 |
| ------- | ----------------------------------- |
| getTweet | 自动跟推 |
| forDownload | 自动下源，代码请见[这里](https://github.com/remiliacn/Vtuber-YouTube) |
| youtubeNotify | 如果下好了视频提醒 |
| fillSanity | 每50秒补充一次理智 |

### 自然语言处理

1. 使用正则表达式判定用户发出的句子是否为全部重复字符或为回文句
   * 回文句判定条件：
      * `text_string == text_string[::-1] and len(text_string) > 5`
   * 全部重复判定条件：
      * `re.fullmatch(r'^(.*?)\1+$', text_string) and repeat_count >= 3`

2. 提炼问句
    * 大概思路：
      * `re.match(r'(.*?)是个?(什么|啥)', text_string)`
      * 提取Group1内容
      * 如果Group1内容较少，直接查询
      * 如果Group1是句子，进行中文分词，并加入副词“是”来指定最后一个名词位置
      * 搜索最后一个名词的定义 
     
