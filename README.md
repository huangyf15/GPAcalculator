# README

本项目是专为清华大学本科生工作助理（本科生辅导员）设计的 GPA 计算与排序工具。

## 使用须知

### 使用方法

#### 方案1：下载发行版直接运行（推荐）

1. 在 `Releases` 界面下载发行版  `GPAsorter-THU.exe`
2. 仔细阅读输入输出，按要求导出成绩表格原始文件
3. 打开命令行或双击左键直接运行已编译好的可执行程序

#### 方案2：个性化定制后编译运行

* 开发环境要求
  * python 3.7+
  * pyinstaller
* 脚本编译运行：下载源码至 `your_path` 文件夹，在 `your_path/GPAsorter-THU` 中打开命令行运行 `Shell` 脚本 `run.sh` 进行编译，编译好的可执行程序将被置于 `dist` 文件夹内并自动直接运行。如在 git bash 界面下，可运行如下命令
```
PS your_path/GPAsorter-THU
$ sh run.sh
```
其中，`your_path` 是指运行 `git clone` 下载此项目时所在的文件路径。

### 输入输出

1. 输入文件要求为 `.txt` 文本文件，需要将从信息门户“管理”界面导出的成绩表格中的必要数据粘贴到该文本文件，至少包括学号、姓名、教学班级、课程号、课程名、成绩、绩点成绩、考试时间、学分、课程属性、重修补考标志、特殊课程标记等信息。
  * 注：下载时会出现两项名称为“特殊课程标记”，请勾选值为“第一学位课程”的那一项（一般该项位置靠后）。
2. 运行程序时需要用户在命令行键入输入/输出文件的名称（不带后缀名，均默认为 `.txt` 文本文件）；输入/输出文件默认位于可执行程序所在文件夹，否则需要另行前缀相对路径（以**可执行程序的所在路径**为基准）。

## 功能特性

* 适合清华成绩体系，自动识别各种课程类型
  * 经过多次手动验证，所得数据结果有保证，示例输入/输出文件见 `test` 文件夹
  * 加入数据预验证环节，帮助用户快速锁定问题，并提示输入数据必需类型
* 设置弹性选项，适应不同标准下的成绩计算需求
  * 允许选择文本文件采用的字符编码方案（默认选择 UTF-8 方案）
  * 允许选择是否在任选课中剔除双学位和辅修课程（默认选择剔除）
  * 允许选择是否在已重修通过科目中剔除挂科记录（默认选择剔除）
  * 允许选择在计算 GPA 时是否剔除已通过科目中的 P/F 课程（默认选择剔除）

## 致谢

* 感谢生命科学系李天奇学长的前期开发工作！
