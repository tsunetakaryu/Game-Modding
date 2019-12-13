# Skyrim SE 上古卷轴重制版部署流程

编撰／Ryusa

这个是针对重制版的部署流程，传奇版可用于参考。

## 0、系统需求

如缺少 D3Dcompiler_43.dll，则需要安装 DX June 2010：https://www.microsoft.com/en-us/download/confirmation.aspx?id=8109





## 1、框架工具的部署

### SKSE

> 万物之始？

- 下载：http://skse.silverlock.org（下载 Current SE Build）

部署：解压至 Skyrim Special Edition 目录，例如 `steamapps\common\Skyrim Special Edition`。

### HDT 相关

> 摇晃的好文明，靠它了！

- 通用框架：http://www.9damaomods.com/thread-61877-1-1.html
- SMP 插件：http://www.9damaomods.com/thread-61878-1-1.html
- 高跟鞋框架：http://www.9damaomods.com/thread-39231-1-1.html

部署：提取 Data 文件夹的内容，粘贴到 Data 目录，例如 `steamapps\common\Skyrim Special Edition\Data`。

### Bodyslide

> 用于生成特定标准的身形模型。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/201/?tab=files

### FNIS

> 用于刷新动作文件，防止人物摆大字。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/3038

### ECE

> 捏脸用的。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/17121

### Net Immerse

> 这个框架用于叠加层的显示，例如纹身。

- 参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=183075

### XP32 最大兼容骨骼

下载：https://www.nexusmods.com/skyrimspecialedition/mods/1988/?tab=description

注意 ECE 用户也需要下载 RaceMenu：

> [Enhanced Character Edit SE](https://www.nexusmods.com/skyrimspecialedition/mods/12302/?)\Vanilla users:
> [Racemenu 0.4.2](https://www.nexusmods.com/skyrimspecialedition/mods/19080)﻿ or newer (extract the RaceMenu bsa and install only the nioverride.pex and the skee.dll/ini)

注意如果安装 SOS 等插件需要重新检查补丁。



## 2、外部工具

### LOOT

> 排序工具，MO 2 自带。

### MOD Organizer 2

> 沙箱化模组管理软件。

### NifSkope 2

> 模型预览、编辑工具。

### Wrye Bash

> 可以为模组打补丁。

### Cathedral Assets Optimizer

> 可以将传奇版模组转化为重制版。

参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=182238



## 3、增强框架

### PapyrusUtil SE SKSE 拓展功能插件

下载：https://www.nexusmods.com/skyrimspecialedition/mods/13048/?

参考：http://www.9damaomods.com/thread-36840-1-1.html



## 4、补丁

### Unofficial Skyrim Special Edition Patch

> 这个补丁的修正内容存在争议，例如可能会把良性 BUG 给修正，请自行斟酌使用。

下载：http://www.nexusmods.com/skyrimspecialedition/mods/266/?

参考：http://www.9damaomods.com/thread-19279-1-1.html

### SSE Engine Fixes

下载：https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files

### HDT 半透明修复

> 未找到。

### Skin Shaders for ENB

> 针对使用 ENB 时的人物光照优化

参考：http://www.9damaomods.com/thread-144727-1-1.html



## 5、GUI 增强

### SkyUI

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/12604?tab=files

### 定制化界面布局等

- 参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=141207

### 彩色地图标志

- 参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=10631

### 终极中文字体字库

> 1.9 GB，408 款字体，……

- 参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=32236

### AddItemMenu

> 获取模组装备不再困难。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/17563
- 注意前置需要 UIExtensions：https://www.nexusmods.com/skyrimspecialedition/mods/17561



## 6、环境美化

### 材质包

- 选项 1，压缩包大小 50 GB，部署后大约 150 GB：http://www.9damaomods.com/forum.php?mod=viewthread&tid=172174 （建议下载 4 GB 封装版，百度下载大体积文件容易损坏）

### ENB

> 有些 ENB 安装包不包含 ENB 核心文件，需要自行到该网站下载：http://enbdev.com/download.html
>
> 下载后，将 .dll 文件部署到 Skyrim Special Edition 目录即可。

####Visceral 电影风格

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/21779?tab=description

#### 童话风

- 低配：http://www.9damaomods.com/forum.php?mod=viewthread&tid=89546

#### 神话时代 **Mythical ENB**

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/11660?tab=description

### 光照优化 Enhanced Lights and FX

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/2424/?tab=files
- 注意如果使用了 SMIM，则需要对应的补丁。



## 7、人物美化

注意身形有 CBBE、UNP 流派区分，对于 UNP 目前比较流行的是 UUNP。

### Demoniac- High Quality Glossy Female Body Texture 8K 4K 2K

- 分流：http://www.9damaomods.com/thread-81591-1-2.html
- 备注：在 ECE 以及 Bodyslide 之后安装这个进行覆盖
- 该美化包的注解如下：

```
若您在使用ENB，建议您打开enblocal.ini，
把 FixTintGamma 的值改为 False。该功能会导致锋线问题。

若您在使用NLA ENB，建议您打开enbseries.ini，
关闭 EnableMultipleWeathers功能（改成False）。
光泽效果与NLA的天气功能有兼容性问题。

安装后若您觉得光泽效果不够给力的话，
请打开enbseries.ini，适当调节一下以下的项目值：

[ENVIRONMENT]
...

SpecularAmountMultiplierSunrise=3
SpecularAmountMultiplierDay=3
SpecularAmountMultiplierSunset=3
SpecularAmountMultiplierNight=4
SpecularAmountMultiplierInteriorDay=6
SpecularAmountMultiplierInteriorNigh=6

SpecularPowerMultiplierSunrise=6
SpecularPowerMultiplierDay=8
SpecularPowerMultiplierSunset=6
SpecularPowerMultiplierNight=6
SpecularPowerMultiplierInteriorDay=6
SpecularPowerMultiplierInteriorNight=6

这些值是我个人建议而已，并不需要改的一模一样。
```

###Botox for Skyrim SSE

> NPC 美化，用来打个底是极好的。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/16533?tab=files
- 参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=112288

### Yundao HDT Hair

> 晕倒大大的 HDT 发型包，注意它是以装备的形式存在的。



## 8、事件互动

###任务

#### Skyrim Unbound

> 不一样的开局，用于快速自定义开局，测试模组环境等。

参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=3571



## 9、动作

- 整合动作包：http://www.9damaomods.com/forum.php?mod=viewthread&tid=153613