# MCServerUpdateTools 
    服务器版本更新工具

## 🤔️这个可以用来做什么？
   随着1.18以及未来的1.19等版本相继推出，游戏将会加入一些全新的地形。

   对于已经生成的区块来说，这些新地形将不会生成。对于一些已经运行相当久的服务器来说，玩家只有不停向外探索从未生成的区域才能体验到新地形。

   最好的解决方案就是将没有玩家使用的区块全部删除，游戏会在下次有玩家经过时生成新的区块。但是这对于地图相当大的服务器来说仍是一个不可接受的任务，因为地图太大了，玩家居住的又相当分散，服主很难根据mca文件判断哪些应该删除哪些不应该。

   💡这个脚本的诞生就是为了解决这样的苦恼！💡

   脚本会根据玩家的领地自动计算出哪些mca文件是有效的，哪些是无效的。同时还可以根据计算得出的结果自动删除那些无效的区域文件。

   为了防止出现意外删除或者错误删除，脚本还配备了备份功能与恢复备份功能。

   当然备份功能也可以单独使用，如果你只是想找一个轻量化的备份工具的话。

## 🧾目前的功能：
 1. 备份服务器存档；

 2. 自动删除没有玩家居住的 mca 文件；

 3. 备份管理；

## 📕使用方法：
  1. 安装python3；
  2. 克隆项目源码到本地；

```
git clone https://github.com/ColdeZhang/MCServerUpdateTools.git
```

3. 安装依赖；

```
pip3 install tqdm
pip3 install pyyaml
```

4. 运行 main.py；

```
cd MCServerUpdateTools/src
sudo python3 main.py
```



## ⚠️注意️:
 1. 本脚本依赖于领地插件，根据领地区域判断 mca 文件是否被占用。在开始清理 mca 文件前请务必提醒玩家将重要财产圈地。

 2. 脚本尚未在MacOS、Ubuntu以外的环境测试过，请谨慎使用。

## ⌚️计划：
 1. 加入核心替换功能，一件替换原有的旧版本核心；

 2. 编译成可执行文件发布；

 3. 制作可视化用户界面（基于web或者TUI）；