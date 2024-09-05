# 灵夜机器人指令文档

## 关于

机器人使用Python 3编写，使用CoolQ作为框架。

项目已开源！请使用issue来汇报问题！https://github.com/remiliacn/qqBot

## 声明

灵夜机器人的大部分功能使用了`数据收集`接口。该接口将会被用于用户行为分析，并对不常用的功能进行改良或者废除。使用本机器的任何指令将默许为您同意本声明，并愿意提供您的***QQ号、QQ昵称、以及使用命令时的参数***用于数据分析。您的任何敏感信息在没有同意的情况下不会被收集，更将不会被公开（如年龄、性别、聊天记录等）。

数据采集部分源码：
https://github.com/remiliacn/qqBot/blob/03b3713d97de0c2bcdd4ad6e39b14f5ad7ff7d89/awesome/adminControl/setu.py#L107-L159

另外请注意，使用以下指令可能会使您的敏感信息泄露，请谨慎使用：
* ！你群语录
* ！添加语录
* ！翻译
* ！我懂了

## 指令大全

### 独属功能（这些功能由于种种原因，并没有公布源代码）
| 指令        | 备注                         |
|-----------|----------------------------|
| ！在听啥      | 看看bot主人在听什么歌               |
| ！切歌       | 给bot主人切歌，我也不知道我为啥要写这个23333 |
| ！点歌       | 给bot主人点歌，同上，不知道为啥写了个这个功能（x |
| ！灵夜       | 使用ChatGPT查询一些东西            |
| @灵夜 `str` | 跟搭载了LLM的灵夜聊天               |


### 权限类

|       | 其他用名 | 使用权限      | 使用方法         | if_deprecated | 备注                                 |
|-------|------|-----------|--------------|---------------|------------------------------------|
| 添加信任  | None | Owner     | !添加信任 `QQ号`  | False         | None                               |
| 移除信任  | None | Owner     | !移除信任 `QQ号`  | False         | None                               |
| 添加管理  | None | Owner     | !添加管理 `QQ号`  | False         | None                               |
| 删除管理  | None | Owner     | !删除管理 `QQ号`  | False         | None                               |
| 问题    | None | Everyone  | !问题 `QQ号`    | False         | 回答一些乱七八糟的问题，如果有语料默认使用语料，如果没有将会尝试回答 |
| ban   | None | whitelist | !ban `QQ号`   | False         | 禁用用户使用某些功能                         |
| unban | None | whitelist | !unban `QQ号` | False         | 启用被禁用用户使用某些功能                      |
| 添加监控词 | None | Owner     | !添加监控词 `str` | False         | 添加色图功能的监控关键词                       |

### 闲聊类 （不建议用，很烦）

|          | 其他用名        | 使用权限     | 使用方法    | if_deprecated | 备注                     |
|----------|-------------|----------|---------|---------------|------------------------|
| ?        | ？           | Everyone | !?      | False         | 无聊添加的，一般是用于测试机器人是不是死锁了 |
| 你好       | None        | Everyone | !你好     | False         | 没啥用……就是写着玩             |
| 我什么都不行   | 流泪猫猫头、什么都不行 | Everyone | !我什么都不行 | False         | 发一张流泪猫猫头的图片            |
| 威胁       | None        | Everyone | !威胁     | False         | 威胁梗表情包                 |
| 恰柠檬      | 吃柠檬         | Everyone | !恰柠檬    | False         | 发一张吃柠檬的表情包             |
| 迫害       | None        | Everyone | !迫害     | False         | 发一张迫害Vtuber的表情包        |
| 不愧是你     | bksn        | Everyone | !不愧是你   | False         | 发一张不愧是你的表情图            |
| 恰桃       | 恰peach      | Everyone | !恰桃     | False         | 发一张恰桃表情包               |
| 社保       | awsl        | Everyone | !社保     | False         | 发一张社保的表情包或者吐槽信息        |
| otsukare | 辛苦了、おつかれ    | Everyone | !辛苦了    | False         | 发一张辛苦了的图               |

### VUP & VTuber系列功能
|        | 其他用名 | 使用权限     | 使用方法                                              | if_deprecated | 备注       |
|--------|------|----------|---------------------------------------------------|---------------|----------|
| b站监控   | None | Everyone | !b站监控 主播名 房间号 群号（可选）                              | False         | 监控B站开播   | 
| b站动态监控 | None | Everyone | ！b站动态监控 用户名 用户UID 群号（可选）                          | False         | 监控B站动态更新 |
| 切片     | None | Everyone | ！切片 Twitch用户名或VOD链接 起始时间戳（可选） 结束时间戳（可选） 文件另用名（可选） | False         | Twitch切片 |

### 游戏类

|     | 其他用名 | 使用权限     | 使用方法 | if_deprecated | 备注                  |
|-----|------|----------|------|---------------|---------------------|
| 比大小 | None | Everyone | !比大小 | False         | 需要两个玩家。             |
| 轮盘赌 | None | Everyone | !轮盘赌 | False         | 如果机器人有权限会禁言输家       |
| 转轮  | None | Everyone | !转轮  | False         | Change random seed. |

### 帮助类

|      | 其他用名 | 使用权限     | 使用方法        | if_deprecated | 备注           |
|------|------|----------|-------------|---------------|--------------|
| help | None | Everyone | !help       | False         | 发送该文档所在网址    |
| 反码   | None | Everyone | !反码 `str`   | False         | 返回CQ码（如果用的话） |
| 好好说话 | None | Everyone | !好好说话 `str` | False         | 查询缩写意味       |

### 沙雕娱乐功能

|        | 其他用名     | 使用权限      | 使用方法                       | if_deprecated | 备注                                 |
|--------|----------|-----------|----------------------------|---------------|------------------------------------|
| 来个老婆   | None     | Everyone  | !来个老婆                      | False         | AI生成一个不存在的动漫角色                     |
| 你群有多色  | None     | Everyone  | !你群有多色                     | False         | 统计`色图`等功能在群里用了多少次                  |
| 设置R18  | None     | Whitelist | !设置R18                     | False         | 开启或关闭`色图`功能的R18发送功能                |
| 娱乐开关   | None     | Admin     | !娱乐开关                      | False         | 全局娱乐开关                             |
| 设置色图禁用 | None     | Admin     | !设置色图禁用 `qqGroup` `开 or 关` | False         | 关闭或打开一个群的色图功能 Override: `娱乐开关`     |
| 色图     | None     | Everyone  | !色图 `str`                  | False         | 根据关键词搜索色图                          |
| 看看XP   | None     | Everyone  | !看看XP                      | False         | 看看自己最喜欢的关键字的色图或者自己P站收藏的色图          |
| 彩虹屁    | 拍个马屁、舔TA | Everyone  | !彩虹屁 `Optional: [CQ:at]`   | False         | 发送彩虹屁信息，如果有at人，会at那个人然后发彩虹屁信息      |
| 统计     | None     | Everyone  | !统计                        | False         | 会查找使用指令用户的一些功能数据。                  |
| 添加语录   | None     | Everyone  | !添加语录 `Any`                | False         | 添加群语录（群内只读）                        |
| 语录     | 你群语录     | Everyone  | !语录                        | False         | 发送随机已保存本群语录                        |
| 清空语录   | None     | Owner     | !清空语录 `qqGroup`            | False         | 清除群组的所有语录                          |
| 搜图     | None     | Everyone  | !搜图 `图片`                   | False         | 使用SAUCEMAO服务逆搜索图片出处 （也可以回复消息并输入搜图） |


### 自动功能
|                      | 备注          |
|----------------------|-------------|
| get_bilibili_dynamic | 自动b站动态监控    |
| check_bilibili_live  | 自动b站开播监控    |
| check_discord        | 自动discord监控 |

     
