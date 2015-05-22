# 功能 #
在vimperator这个扩展的hint模式中可以通过拼音首字母过滤中文链接

例如希望打开链接“论坛”，可以在vimperator按f/F进入hint模式，然后输入lt（拼音 **l** un **t** an），便会过滤出“论坛”以及其他类似内容。再比如“vimperator修改版”，可以输入xgb或者vimperatorxgb或者vim空格xgb（当然，通常你不要输入这么多字母，可能输入xg后链接就打开了）。

# 使用 #
```
下载右边的pinyin-hints.js，放到你的vimperator的plugin文件夹下
windows下通常在%USERPROFILE%\vimperator\（不知这是啥？请用运行打开）下
如果没有，请在vimperator文件夹中新建plugin文件夹
如果你用*nix我就不废话了
```
关于曾经的修改版<br />
.xpi是打包好的完整修改版（因为权限问题，可能不会自动安装，下载好后将这个文件拖入firefox就可以像平时一样安装）<br />
修改部分位于你的\_firefox profile文件夹_\extensions\vimperator@mozdev.org\chrome\vimperator.jar\common\content\hints.js（jar文件事实上是zip文件，可以用一般的压缩工具修改）_<br />
之所以做成插件形式是修改版更新比较麻烦<br />

# 背景 #
熟悉vimperator这个扩展的都知道hint模式<br />
hint模式是用来打开链接的<br />
对于英文链接，通过输入连接上的少量内容便可快速打开<br />
但是中文链接只能通过输入序号打开<br />
前一段时间受到[这篇文章](http://xbeta.info/tc-pinyin-quicksearch.htm)的启发<br />
给vimperator也添加了类似的功能<br />

# 原理 #
很简单，vimperator在进入hint模式时会将页面上的可点击元素、元素上的文字等存储在一个数组中<br />
所以只要搞一个unicode到拼音的转换表将文字中的中文字符转换为拼音首字母即可<br />
例如“firefox扩展”被转换为"firefoxkz"<br />

# 已知的问题 #
不能处理多音字，不过从我最近的使用看这一点影响不大,故暂不修改

# 更新 #
**20091104** 在Downloads里有_**clwydyan**_修改的[hints\_2.2b1.js](http://pinyin-hints-vimperator.googlecode.com/files/hints_2.2b1.js)，感谢_**clwydyan**_的支持<br />
**20100731** 添加插件形式