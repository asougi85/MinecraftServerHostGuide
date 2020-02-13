# 第三节 什么是插件？
> 插件（Plugin）是遵循 Bukkit 或 Sponge 接口规范编写的ava程序。

插件只能运行在支持 BukkitAPI 或SpongeAPI 的服务端下，一般无法独立运行。因为插件需要调用的服务端的函数和数据。

但也有例外，例如 MyPet 插件单独打开后是可视化宠物编辑器。

插件可以拓展服务端的功能，增强游戏性，给玩家更好的游戏体验。

选取优秀插件，形成完美配合，可以让服务器在众多对手中脱颖而出。

## 插件类型

插件没有原理上的隔阂，只有功能上的区别，可以根据用途大致分为以下几种类型：
  
|类型|描述|样例|
|:---:|:---|:---|
|管理|提高服务器的可管理性和管理效率|`SkyPerms`、`LuckPerms`|
|安全|维护服务器稳定，阻绝外挂等非法行为|`NoCheatPlus`|
|聊天|提供多样化的聊天功能|`PrefixManager`|
|开发|作为开发库帮助其他开发者编写插件|`Vault`、`ProtocolLib`|
|经济|通过货币、市场机制，促进物品流通，玩家交流|`Vault`、`iEconomy`|
|创世1|提供更高效的地图修改与维护功能|`WorldEdit`|
|创世2|修改世界生成机制，创造不同于原版的世界|`PlotSquard`|
|修复|修复服务端或者其他插件的一些特性~~Bug~~|`chestfix`|
|娱乐|让玩家从插件中发现趣味|`Fart`、`Bed War`|
|综合|拥有不同层面多样化功能的插件|`Essential`|
|信息|可以收集服务器信息、帮助服主或玩家更好地获取信息的插件|`CoreProtect`|
|机制|增加游戏机制，改善玩家体验，改善游戏耐玩性|`Citizens`|
|网页|增加网页端内容|`WebBan`|
|RPG|给Minecarft添加角色扮演类游戏要素|`DungeonsXL`、`MyHero`|
|传送|加入多样化的传送功能|`RandomTeleport`|
|其他|无法用以上要素概括的其他类型插件|`Trash`|

## 插件的安装与卸载
安装插件前，请先确定您的服务端版本。一些服务端支持Bukkit插件，而另一些支持Sponge插件。关于服务端和支持插件的对应关系，我们已经在第一单元第一节进行过详细介绍。
在下载插件前，请留意插件所适用的服务器版本，以免安装不兼容的插件，引起报错。

### Bukkit插件
#### 安装
1. 我们已经在[第一单元第二节](Structure.md)了解到，Bukkit插件安装在位于根目录的 `plugins` 文件夹中。  
2. ① 插件的后缀名为 `.jar`，如果后缀正确，请直接将插件放到 `plugins` 目录里，然后启动游戏。  
② 如遇到后缀不正确的插件，请先确认是否为压缩文件，然后用压缩软件将其解压到 `plugins` 文件夹里面。
4. 运行服务器

#### 卸载
1. 保存地图后，关闭服务器
2. 将 `plugins` 文件夹内的插件删除
3. 如果想连同**插件数据**一起删除，请删除 `/plugins/插件名` 文件夹。

#### 配置文件
Bukkit插件的配置文件被保存在 `/plugins/插件名` 文件夹中。  

---
### Sponge插件  
#### 安装
1. 默认情况下，Sponge插件安装在位于根目录的 `mods` 文件夹中。但Sponge提供了其他更多的可选插件位置，详情可以阅读[Sponge官方中文文档](https://docs.spongepowered.org/stable/zh-CN)  
2. 请直接将插件放到 `mods` 目录里，然后启动游戏。  
4. 运行服务器

#### 卸载
1. 关闭服务器
2. 将 `mods` 文件夹内的插件删除

#### 配置文件
默认情况下，Sponge插件的配置文件被保存在根目录的 `config` 文件夹中，但实际情况有时并非如此。必要时请查阅对应插件的文档来获得帮助。

---
### 配置文件的编辑
配置文件**没有固定的文件名**，但是Bukkit插件配置文件一般为`YAML`格式的文本文档，后缀名为 `.yml` 。Sponge插件配置文件一般为`HOCON`或`YAML`格式的文本文档，后缀名为`.conf`  
配置文件可以用 Windows 自带的记事本打开。但是我们更推荐使用[准备工作](Preparation.md)中提到的`NotePad++`或`EditPlus`、`Sublime Text`和`Vim` 等专业文本编辑器进行修改，以免出现各种问题。  
关于如何编辑`YAML`文件，我们将在[第二单元第二节](Yaml.md)进行更细致的讲解。  
关于如何编辑`HOCON`文件，请查阅Sponge官方中文文档中的[Hocon简介](https://docs.spongepowered.org/stable/zh-CN/server/getting-started/configuration/hocon.html)。