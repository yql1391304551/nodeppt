# 开启

打开"运行"对话框（Win+R），输入cmd，打开控制台命令窗口，也可以通过cmd /c命令（执行完命令后关闭cmd窗口） 和 cmd /k（执行完命令后保留cmd窗口) 命令的方式来直接运行命令

在文件夹空白处按住Shift，然后右键弹出快捷菜单，可以看到“在此处打开命令行窗口”

# 控制台命令窗口中一些技巧

复制内容：选中所需复制的内容，然后右键即可

粘贴内容：右键

使用上下方向键，翻看使用过的命令

命令参数的路径：要使用反斜杠'\'，不要使用正斜杠'/'  

如：`del d:\test2\file\my.txt`

命令参数的路径：若存在空格，应使用双引号将路径引起来  
如：`del "d:\program files\file\my.txt"`

文件及目录名中不能包含：`\ `、`/ `、`: `、`* `、`? `、` < `、`> `、`|`

# 常用命令

---

### 获取帮助

`command /?`  查看command命令帮助说明

### 中断命令执行

`Ctrl + Z`

### 文件/目录


#### cd   切换目录

`cd` 显示当前目录

`cd ..` 进入父目录

`cd /d d:` 进入上次d盘所在的目录（或在直接输入：d:）

`cd /d d:\` 进入d盘根目录

`cd d:` 显示上次d盘所在的目录

`cd /d d:\src` 进入d:\src目录

#### dir  显示目录中的内容

`dir` 显示当前目录中的子文件夹与文件

`dir /b` 只显示当前目录中的子文件夹与文件的文件名

`dir /p` 分页显示当前目录中的子文件夹与文件

`dir /ad` 显示当前目录中的子文件夹

`dir /a-d` 显示当前目录中的文件

`dir c:\test` 显示c:\test目录中的内容

`dir keys.txt` 显示当前目录中keys.txt的信息

`dir /S` 递归显示当前目录中的内容

`dir key*` 显示当前目录下以key开头的文件和文件夹的信息

`dir /AH /OS` 只显示当前目录中隐藏的文件和目录，并按照文件大小从小到大排序

#### tree 显示目录结构
`tree d:\myfiles` 显示d:\myfiles目录结构

#### ren  文件或目录重命名

`ren rec.txt rec.md` 将当前目录下的rec.txt文件重命名为rec.md

`ren c:\test test_01`将c盘下的test文件夹重命名为test_01

#### md  创建目录

`md test` 在当前目录中创建test文件夹

`md test_1 test_2` 在当前目录中同时创建test_1h和test_2文件夹

`md d:\test\test_1` 创建d:\test\movie目录

#### rd  删除目录

`rd movie` 删除当前目录下的movie空文件夹

`rd /s /q d:\test` 使用安静模式删除d:\test（除目录本身外，还将删除指定目录下的所有子目录和文件）

#### copy 拷贝文件

`copy key.txt c:\doc` 将当前目录下的key.txt拷贝到c:\doc下（若doc中也存在一个key.txt文件，会询问是否覆盖）

`copy jobs c:\doc ` 将当前目录下jobs文件夹中文件（不递归子目录）拷贝到c:\doc下（若doc中也存在相应的文件，会询问是否覆盖）

`copy key.txt c:\doc\key_bak.txt` 将当前目录下的key.txt拷贝到c:\doc下，并重命名为key_bak.txt（若doc中也存在一个key_bak.txt文件，会询问是否覆盖）

`copy /Y key.txt c:\doc` 将当前目录下的key.txt拷贝到c:\doc下（不询问，直接覆盖写）

`copy key.txt +` 复制文件到自己，实际上是修改了文件日期

`copy /Y key1.txt + key2.txt key.txt` 将当前目录下的key1.txt与key2.txt的内容合并写入key.txt中（不询问，直接覆盖写）

`copy /B art_2.7z.* art_2.7z` 将当前目录下的art_2.7z.开头的所有文件（按照名称升序排序）依次合并生成art_2.7z

`copy /B art_2.7z.001+art_2.7z.002 art_2.7z` 将当前目录下的art_2.7z.001、art_2.7z.002文件合并生成art_2.7z

#### move 移动文件

`move *.png test` 将当前目录下的png图片移动到当前目录下test文件夹中 （若test中也存在同名的png图片，会询问是否覆盖）

`move /Y *.png test` 将当前目录下的png图片移动到当前目录下test文件夹中 （不询问，直接覆盖写）

`move 1.png d:\test\2.png` 将当前目录下的1.png移动到d盘test文件夹中，并重命名为2.png （若test中也存在同名的png图片，会询问是否覆盖）

`move test d:\new` 若d盘中存在new文件夹，将当前目录下的test文件夹移动到d盘new文件夹中；若不存在，将当前目录下的test文件夹移动到d盘，并重命名为new

#### del 删除文件   注意：目录及子目录都不会删除

`del test` 删除当前目录下的test文件夹中的所有非只读文件（子目录下的文件不删除；删除前会进行确认；等价于del test\*）

`del /f test` 删除当前目录下的test文件夹中的所有文件（含只读文件；子目录下的文件不删除；删除前会进行确认；等价于del /f test\*）

`del /f /s /q test d:\test2\*.doc` 删除当前目录下的test文件夹中所有文件及d:\test2中所有doc文件（含只读文件；递归子目录下的文件；删除前不确认）

### 文件查看
---
#### type 显示文本文件内容

`type c:\11.txt` 显示c盘中11.txt的文本内容

`type c:\1.txt | more` 分页显示c盘中1.txt的文本内容

#### more 逐屏的显示文本文件内容

`more conf.ini` 逐屏的显示当前目录下conf.ini的文本内容   【空格：下一屏 q：退出 】

### 其他
---
#### cls  清除屏幕

#### time  显示或设置当前时间

`time /t` 显示当前时间

`time hh:mm:ss` 设置新的当前时间

#### date  显示或设置当前日期

`date /t` 显示当前日期

`date YYYY/MM/DD` 设置新的当前日期

#### start  运行某程序或命令

`start /max xxx.exe` 最大化的方式启动

`start /min xxx.exe ` 最小化的方式启动

`strat iexplore "www.qq.com"` 启动ie并打开www.qq.com网址

#### exit  退出当前cmd窗口实例

`exit 0` 退出当前cmd窗口实例，并将过程退出代码设置为0（0表示成功，非0表示失败）

#### color  设置当前cmd窗口背景色和前景色（前景色即为字体的颜色）

`color` 恢复到缺省设置

`color 02` 将背景色设为黑色，将字体设为绿色

---
* 0 黑色
* 1 蓝色
* 2 绿色
* 3 浅绿色
* 4 红色
* 5 紫色
* 6 黄色
* 7 白色
* 8 灰色
* 9 淡蓝色
* A 淡绿色
* B 淡浅绿色
* C 淡红色
* D 淡紫色
* E 淡黄色
* F 亮白色