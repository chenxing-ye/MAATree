# MaaPiCli 操作说明~~（翻译文档）~~

- [MaaPiCli 操作说明~~（翻译文档）~~](#maapicli-操作说明翻译文档)
  - [选择ADB](#选择adb)
  - [选择设备](#选择设备)
  - [选择资源](#选择资源)
  - [添加任务](#添加任务)
  - [功能菜单](#功能菜单)
  - [进阶使用](#进阶使用)

## 选择ADB

当您初次下载，没有配置时会出现下面界面：

```plaintext
Welcome to use Maa Project Interface CLI!
MaaFramework: v4.0.0

Version: v0.0.1

### Select ADB ###

        1. Auto detect
        2. Manual input

Please input [1-2]:
```

这里 Version 后跟着的是当前资源版本。  
`### Select ADB ###` 翻译过来是当前操作为 `选择 ADB（Android Debug Bridge，这里一般用来操作模拟器）`。  
后面列出选项：

1. 自动检测（推荐，在目标模拟器启动时选择）
2. 手动输入（参考[ADB 路径](连接设置.md#adb-路径)和[ADB 连接地址](连接设置.md#连接地址)填写）

后面 `Please input [1-2]:` 翻译过来是 `请输入 [选项范围]`，请根据需要选择。

这里我们输入 1 后回车，进入下一步。

## 选择设备

紧跟上一步，选择自动检测可到此步骤，显示为：

```plaintext
Finding device...

## Select Device ##

        1. MuMuPlayer12
                D:/Program Files/Netease/MuMu Player 12/shell/adb.exe
                127.0.0.1:16384

Please input [1-1]:
```

这里因为只开了一个模拟器，只显示一条选项，直接输入 1 后回车，完成此步骤

## 选择资源

```plaintext
### Select resource ###

        1. 官服
        2. B服

Please input [1-2]:
```

这里根据需要的资源进行选择，主要和 `启动游戏`、`主线扫荡` 和 `活动刷取` 等功能。

## 添加任务

这里是添加任务，显示如下：

```plaintext
### Add task ###

        1. 启动游戏
        2. 自动主线扫荡(确保剩余足够的体力药)
        3. 每日物资
        4. 探索活动奖励领取
        5. 领取邮件
        6. 扫荡一次素材关卡
        7. 行会签到及捐赠
        8. 自动助战任务(+领取每日奖励)
        9. 自动紧纳罗
        10. 9.25新版自动多人战
        11. 开始自动桃园乡
        12. 自动神眠
        13. 自动炼金(仅保留8级及以上奥秘)
        14. 自动推图(请前往能看到未通关关卡的地方再开始运行)

Please input multiple [1-14]:
```

## 进阶使用

- 在命令行中添加 `-d` 参数运行即可跳过交互直接运行任务，如 `./MaaPiCli.exe -d`
- 2.0 版本已支持 mumu 后台保活，会在 run task 时获取 mumu 最前台的 tab，并始终使用这个 tab（即使之后被切到后台了）
