## U盘安装 macOS 系统的方法

如果你对系统有洁癖或原本系统已凌乱不堪，那么可能还是希望能格式化「全新安装 macOS」的

不过由于苹果官方只提供了 macOS 的升级程序，并没提供完整 dmg 镜像，想要全新安装的话，只能自己制作一个 macOS Mojave 的U盘启动盘/安装盘了。这样以后给 Mac 重装系统、在没网络的情况下给多台机器装机都方便许多……

制作 macOS Mojave 正式版 USB 启动盘的方法有很多，用户可以选择使用命令行来创建，也可以选择第三方U盘制作工具来制作，大家可以根据自己的喜好选择。

1. 准备一个 8GB 或更大容量的 U盘
2. 下载好 macOS Mojave 正式版的安装程序备用，先不要启动安装
3. 打开 “应用程序 → 实用工具 → 磁盘工具”，将U盘「抹掉」(格式化) 成「Mac OS X 扩展（日志式）」格式、GUID 分区图，并将 U 盘命名为「Mojave」。注意：这个盘符名称必须与后面的命令里的名称一致
4. 打开 “应用程序→实用工具→终端”，将下面的一段命令复制并粘贴进去：

> 如要制作 macOS Mojave 启动盘，U盘名称要改成「Mojave」(必须与下面命令对应)，然后拷贝这段命令：

<code>
sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/Mojave /Applications/Install\ macOS\ Mojave.app --nointeraction
</code>

> 如要制作 macOS High Sierra 启动盘，U盘名称要改成 HighSierra (要与下面命令对应)，拷贝这段命令：

<code>
sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/HighSierra --applicationpath /Applications/Install\ macOS\ High\ Sierra.app --nointeraction
</code>

> 如要制作「旧版本的 macOS Sierra」，U盘名称改成 Sierra，拷贝这段命令：

<code>
sudo /Applications/Install\ macOS\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/Sierra --applicationpath /Applications/Install\ macOS\ Sierra.app --nointeraction
</code>

5. 回车并执行该命令，这时会提示让你输入管理员密码，便会开始制作过程了
6. 请耐心等待直到屏幕最后出现 Done. 字样即表示大功告成了！
