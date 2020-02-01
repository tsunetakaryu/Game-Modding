# Skyrim SE 上古卷轴重制版部署流程

编撰／Ryusa

这个是针对重制版的部署流程，传奇版可用于参考。

2. 部分模组测试：传奇版动作文件不再能直接使用（会摆大字）；装备基本上可以直接用，但 SMP 的不行。
3. 传奇版与重制版的 ENB 同样不通用，因为使用的 DirectX 版本不一样。



## 0、系统需求

如缺少 D3Dcompiler_43.dll，则需要安装 DX June 2010：https://www.microsoft.com/en-us/download/confirmation.aspx?id=8109
这个问题在我的 Windows 10 操作系统中遇到了，所以在这里写下来。



## 1、框架工具的部署

### SKSE

> 万物之始？

- 下载：http://skse.silverlock.org （下载 Current SE Build）

部署：解压至 Skyrim Special Edition 目录，例如 `steamapps\common\Skyrim Special Edition`。

### HDT 相关

> 摇晃的好文明，靠它了！

- 通用框架：http://www.9damaomods.com/thread-61877-1-1.html
- SMP 插件：http://www.9damaomods.com/thread-61878-1-1.html
- 高跟鞋框架：http://www.9damaomods.com/thread-39231-1-1.html
- 或者考虑这个链接（包含了通用框架和 SMP 插件，不知道为什么我是用这个才管用）：https://www.nexusmods.com/skyrimspecialedition/mods/30872?tab=files

部署：提取 Data 文件夹的内容，粘贴到 Data 目录，例如 `steamapps\common\Skyrim Special Edition\Data`。

### BodySlide

> 用于生成特定标准的身形模型。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/201/?tab=files
- 部署 1：手动解压至 Data 目录（但版本更新时需要重新手动替换）。
- 部署 2：使用 MO 2 安装，然后在右侧“数据”选项卡中找到 BodySlide.exe 右键添加为可执行程序。（推荐！）
- 部署 3：使用 MO 2 安装，通过 Explore Virtual Folder 找到 BodySlide.exe 并运行。
- 注意现阶段暂无任何 UUNP 预设。

### FNIS

> 用于刷新动作文件，防止人物摆大字。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/3038
- 部署 1：手动解压至 Data 目录（但版本更新时需要重新手动替换）。
- 部署 2：使用 MO 2 安装，然后在右侧“数据”选项卡中找到 GenerateFNISforUsers.exe 右键添加为可执行程序。（可能会有 BUG）
- 部署 3：使用 MO 2 安装，通过 Explore Virtual Folder 找到 GenerateFNISforUsers.exe 并运行。（推荐！）

### Enhance Character Editor (ECE)

> 捏脸用的。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/17121
- 捏脸预设存放在 `你的文档\My Games\Skyrim Special Edition\CME_save`，它的路径是与 MO 2 profile 无关的。

### Net Immerse

> 这个框架用于叠加层的显示，例如纹身。

- 参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=183075

### XP32 最大兼容骨骼

下载：https://www.nexusmods.com/skyrimspecialedition/mods/1988/?tab=description

注意 ECE 用户也需要下载 RaceMenu：

> [Enhanced Character Edit SE](https://www.nexusmods.com/skyrimspecialedition/mods/12302/?)\Vanilla users:
> [Racemenu 0.4.2](https://www.nexusmods.com/skyrimspecialedition/mods/19080)﻿ or newer (extract the RaceMenu bsa and install only the nioverride.pex and the skee.dll/ini)

注意如果安装 SOS 等插件需要重新检查补丁。

### RaceMenu High Heels Fixes

> 与 HDT 大佬的高跟鞋框架类似，有些模组会需要。

下载：https://www.nexusmods.com/skyrimspecialedition/mods/18045?tab=description

### JContainers SE

> 有些模组会需要它，例如纹身插件。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/16495



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

### FileAccess Interface for Skyrim SE Scripts (FISSes)

> 有些界面定制的模组会需要它。



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

> 游戏中打开地图会报错，但是不影响使用。

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
>
> 使用 ENB 之后进入游戏会黑屏，左上角的文字是说在为 Shader 设置缓存，如果觉得等待过长，可以在 enblocal.ini 中关闭该功能，但要在显卡设置中启用 Shader 缓存。
>
> 在 enblocal.ini 的设置中设置显存：
>
> [MEMORY]
>
> VideoMemorySizeMb=6144

#### Aequinoctium ENB（强烈推荐）

- 参考：https://www.nexusmods.com/skyrimspecialedition/mods/16008
- 需要配合 Aequinoctium 天气使用
- 使用心得：比较接近传奇版的 CR Realistic 292 Remastered Edition

#### ISO ENB（比较推荐）

- 参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=141439

#### Re-Engaged ENB（人物拍照挺不错的）

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/1089

### 光照优化 Enhanced Lights and FX

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/2424/?tab=files
- 注意如果使用了 SMIM，则需要对应的补丁。



## 7、人物美化

注意身形有 CBBE、UNP 流派区分；UUNP 的迭代为 BHUNP，推荐使用。

### 材质包：Demoniac- High Quality Glossy Female Body Texture 8K 4K 2K

- 分流：http://www.9damaomods.com/thread-81591-1-2.html
- 备注：在 ECE 以及 Bodyslide 之后安装这个进行覆盖，注意它只是材质包，不包含身形文件，但安装时可选兼容 CBBE 或是 UNP 身形。
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

### 材质包：The Pure

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/20583
- 备注：注意它只是材质包，不包含身形文件，但安装时可选兼容 CBBE 或是 UNP 身形

### Botox for Skyrim SSE

> NPC 美化，用来打个底是极好的。

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/16533?tab=files
- 参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=112288

### Yundao HDT Hair

> 晕倒大大的 HDT 发型包，注意它是以装备的形式存在的。
>
> 注意传奇版的与重制版不通用。
>
> 注意 Nexus 上面的版本比较旧，建议下载 9DM 的资源。

- 下载：http://www.9damaomods.com/forum.php?mod=viewthread&tid=156907

### CBBE - 3BBB 身形

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/30174

### UNP - BHUNP 身形

- 下载：https://www.nexusmods.com/skyrimspecialedition/mods/31126
- 使用心得：完全兼容 UUNP 或 UNP 默认预设（即 Zeroed Sliders），因此传奇版的服装模组如果是 UNP 默认身形，或是 UUNP 带有 BodySlide 工具则在刷成 *Zeroed Sliders* 之后也可以使用。但对于带有物理效果（SMP）的传奇版服装模组不一定适用。




## 8、事件互动

### 任务

#### Skyrim Unbound

> 不一样的开局，用于快速自定义开局，测试模组环境等。

参考：http://www.9damaomods.com/forum.php?mod=viewthread&tid=3571



## 9、动作

- 整合动作包：http://www.9damaomods.com/forum.php?mod=viewthread&tid=153613
