---
layout: wiki
title: Vim
categories: Vim
description: 个人最常用的 Vim 常用操作。
keywords: Vim
---

### 移动

**以字（符）为单位**

| 功能 | 按键 |
|:-----|:-----|
| 上   | `k`  |
| 下   | `j`  |
| 左   | `h`  |
| 右   | `l`  |

**以单词为单位**

| 功能                                   | 按键 |
|:---------------------------------------|:-----|
| 前一个单词尾                           | `ge` |
| 后一个单词首                           | `w`  |
| 本单词首（已在本词首则跳到前一单词首） | `b`  |
| 本单词尾（已在本词尾则跳到后一单词尾） | `e`  |

**以屏幕为单位**
 
| 功能                     | 按键     |
|:-------------------------|:---------|
| 向下翻页                 | `CTRL-f` |
| 向上翻页                 | `CTRL-b` |
| 向下翻半页               | `CTRL-d` |
| 向上翻半页               | `CTRL-u` |
| 向上一行                 | `CTRL-y` |
| 向下一行                 | `CTRL-e` |
| 光标移到屏幕上方         | `H`      |
| 光标移到屏幕中间         | `M`      |
| 光标移到屏幕下方         | `L`      |
| 光标所在位置移到屏幕上方 | `zt`     |
| 光标所在位置移到屏幕中间 | `zz`     |
| 光标所在位置移到屏幕下方 | `zb`     |

**行号**

| 功能          | 按键                        |
|:--------------|:----------------------------|
| 跳到第 num 行 | `:num` 或 `numG` 或 `numgg` |

**文件**

| 功能       | 按键 |
|:-----------|:-----|
| 跳到文件头 | `gg` |
| 跳到文件尾 | `G`  |

### 编辑

#### 复制

| 功能             | 按键  |
|:-----------------|:------|
| 复制光标所在单词 | `yiw` |
| 复制光标所在行   | `yy`  |

#### 粘贴

| 功能           | 按键 |
|:---------------|:-----|
| 在光标之后粘贴 | `p`  |
| 在光标之前粘贴 | `P`  |

#### 剪切

| 功能           | 按键 |
|:---------------|:-----|
| 剪切选中区域   | `d`  |
| 剪切光标所在行 | `dd` |

#### 替换

| 功能                              | 按键                |
|:----------------------------------|:--------------------|
| 将全文中的 str1 替换为 str2       | `:%s/str1/str2/g`   |
| 将 1 到 5 行中的 str1 替换为 str2 | `:1,5s/str1/str2/g` |

#### 大小写

| 功能                 | 按键            |
|:---------------------|:----------------|
| 将选中内容大小写互换 | `~`             |
| 将选中内容全转为小写 | `gu`            |
| 将选中内容全转为大写 | `gU`            |
| 将当前行变成小写     | `guu`           |
| 将当前行变成大写     | `gUU`           |
| 将匹配内容替换为大写 | `:%s/xxx/\U&/g` |
| 将匹配内容替换为小写 | `:%s/xxx/\L&/g` |

注：`&` 代表正则表达式全部匹配项，另外还有 `\1`、'\2'、...、`\9` 代表第 1 到 9 个匹配项。

### 选择

| 功能                 | 按键                |
|:---------------------|:--------------------|
| 选中上一次选择的区域 | `gv`                |
| 选中括号内区域       | `vi{`、`vi[`、`vi(` |

### 搜索

| 功能                 | 按键   |
|:---------------------|:-------|
| 向下查找字符串       | `/str` |
| 向上查找字符串       | `?str` |
| 查找下一个           | `n`    |
| 查找上一个           | `N`    |
| 向下查找光标所在单词 | `*`    |
| 向下查找光标所在单词 | `#`    |

### 正则表达式

| 功能           | 按键                |
|:---------------|:--------------------|
| 匹配单词左边界 | `\<`                |
| 匹配单词右边界 | `\>`                |
| 去重           | `:g/^\(.*\)$\n\1/d` |

### 常用

| 功能                    | 按键          |
|:------------------------|:--------------|
| 删除空行                | `:g/^$/d`     |
| 撤销/UNDO               | `u`           |
| 重做/REDO               | `C-r`         |
| 统计行/单词/字符/字节数 | `g C-g`       |
| 去掉 UTF-8 BOM          | `:set nobomb` |
| 保留 UTF-8 BOM          | `:set bomb`   |

### 全局

| 功能         | 按键 |
|:-------------|:-----|
| 退出         | `:q` |
| 强制执行     | `!`  |
| 执行外部命令 | `:!` |

### 文件操作

| 功能               | 按键      |
|:-------------------|:----------|
| 打开               | `:e`      |
| 打开文件对话框     | `:bro e`  |
| 保存               | `:w`      |
| 另存为对话框       | `:bro w`  |
| 查看历史文件列表   | `:ol`     |
| 查看并打开历史文件 | `:bro ol` |
|重命名当前文件|`:f filename`|

### vimdiff

| 功能                   | 按键          |
|:-----------------------|:--------------|
| 移动到上一个不同处     | `[c`          |
| 移动到下一个不同处     | `]c`          |
| 该差异点使用当前文件的 | `dp`          |
| 该差异点使用其它文件的 | `do`          |
| 手动刷新重新比较       | `:diffupdate` |

### Buffer

| 功能                               | 按键     |
|:-----------------------------------|:---------|
| 查看 Buffer 列表                   | `:ls`    |
| 转到 Buffer 列表中的下一个 Buffer  | `:bn`    |
| 转到 Buffer 列表中的上一个 Buffer  | `:bp`    |
| 转到 Buffer 列表中的 num 号 Buffer | `:bnum`  |
| 你之前待过的一个 Buffer            | `:b#`    |
| 从 Buffer 列表中删除 num 号 Buffer | `:bdnum` |

### 组合命令

可以使用 `|` 来组合命令，比如 `cmd1 | cmd2`。

### 代码

| 功能                    | 按键                           |
|:------------------------|:-------------------------------|
| 格式化代码              | `gg=G`                         |
| 去除 1-20 行首的行号    | `:1,20s/^\\s\*[0-9]\*\\s\*//g` |
| 展开全部折叠            | `zR`                           |
| 展开当前层级折叠        | `zr`                           |
| 全部折叠                | `zM`                           |
| 当前层级折叠            | `zm`                           |
| 切换折叠/展开           | `za`                           |
| 递归折叠/展开当前大区块 | `zA`                           |
| 折叠当前区块            | `zc`                           |
| 递归折叠当前大区块      | `zC`                           |
| 展开当前区块            | `zo`                           |
| 递归展开当前大区块      | `zO`                           |
| 格式化 json 数据        | `:%!python -m json.tool`       |
| 缩进当前行              | `>>`                           |
| 反缩进当前行            | `<<`                           |

### modeline

写法：

```
 vim: set ft=markdown:
 vim: ft=markdown

// vim: noai:ts=4:sw=4
/* vim: noai:ts=4:sw=4 */
```

### 插件

#### CtrlP

基础按键 `C-p`

| 功能                               | 按键      |
|:-----------------------------------|:----------|
| 刷新列表                           | `F5`      |
| 切换文件/缓冲区/MRU                | `C-f/b`   |
| 切换全路径搜索/文件名搜索          | `C-d`     |
| 切换正则表达式模式                 | `C-r`     |
| 上/下一个选项                      | `C-k/j`   |
| 在新标签/垂直分割/水平分割打开文件 | `C-t/v/x` |
| 历史选择记录的上/下一条            | `C-p/n`   |
| 创建文件和它的父路径               | `C-y`     |
| 标记并打开多个文件                 | `C-z C-o` |
| 退出 CtrlP                         | `C-c`     |

#### LeaderF

| 功能                               | 按键                   |
|:-----------------------------------|:-----------------------|
| 打开文件                           | `Leader-f`             |
| 打开缓冲区                         | `Leader-b`             |
| 打开 MRU                           | `Leader-m`（自定义的） |
| 退出                               | `C-c`                  |
| 切换模糊查找和正则查找             | `C-r`                  |
| 粘贴                               | `C-v`                  |
| 清空输入                           | `C-u`                  |
| 上/下一个选项                      | `C-k/j`                |
| 在新标签/垂直分割/水平分割打开文件 | `C-t/]/v`              |
| 刷新列表                           | `F5`                   |

#### vim-table-mode

| 功能           | 按键         |
|:---------------|:-------------|
| 删除列         | `Leader-tdc` |
| 删除行         | `Leader-tdd` |
| 重新格式化表格 | `Leader-tr`  |

#### markdown-preview.nvim

| 功能     | 按键 |
|----------|------|
| 预览     | `F5` |
| 停止预览 | `F6` |

导出 PDF：预览以后，使用浏览器的「打印」功能，打印机选「另存为 PDF」，取消「页眉和页脚」，然后点保存即可。

### 命令行

打开 Vim 时跳转到指定行：

```
vim +[num] filename
```

num 表示行号，不填则跳转到文件末尾。

### 打造VIM编辑器IDE

安装vim、ctags、cscope

```shell
sudo apt install vim exuberant-ctags cscope
```

配置/etc/vim/vimrc或~/.vimrc

```shell
set nu # 设置行号
```

#### ctags

使用

```shell
ctags -R . # 生成tags
vim -t tag # tag
:ts # tag list
:tp # tag preview
:tn # tag next
ctrl-] # enter
ctrl-t # back
```

配置vimrc

```shell
set tags=path/tags
```

#### cscope

使用方法

```shell
find . -name "*.[h|c]" > cscope.files
cscope -bkq -i cscope.files
cscope -d 
# exit: ctrl-d
```

vim中常用命令

```shell
:cscope find s ---- 查找C语言符号，即查找函数名、宏、枚举值等出现的地方  
:cscope find g ---- 查找函数、宏、枚举等定义的位置，类似ctags所提供的功能  
:cscope find d ---- 查找本函数调用的函数  
:cscope find c ---- 查找调用本函数的函数  
:cscope find t ---- 查找指定的字符串  
:cscope find e ---- 查找egrep模式，相当于egrep功能，但查找速度快多了  
:cscope find f ---- 查找并打开文件，类似vim的find功能  
:cscope find i ---- 查找包含本文件的文 
```

#### vim插件

开启插件~/.vimrc

```shell
filetype plugin on
```

**omnicppcomplete**

功能：补全结构体的成员以及类成员

下载地址：

[http://www.vim.org/scripts/script.php?script_id=1520](http://www.vim.org/scripts/script.php?script_id=1520)

[https://github.com/vim-scripts/OmniCppComplete](https://github.com/vim-scripts/OmniCppComplete)

安装：在~/.vim目录下解开压缩包

tags生成命令：

```shell
ctags -R --C-kinds=+p --fields=+aS --extra=+q
```

**taglist**

下载地址：<https://github.com/yegappan/taglist>

配置

```
let Tlist_Show_One_File=1 "不同bai时显示多个文件du的zhitag，只显示当前文件的
let Tlist_Exit_OnlyWindow=1 "如果taglist窗口是最后一dao个窗口，则退出vim
let Tlist_Ctags_Cmd="/usr/bin/ctags" "将taglist与zhuanctags关联 ！
```

操作命令：

":TlistToggle"：打开左边的tag窗口，再输一次自动关闭，按ctrl+w可以在窗口之间进行切换

":TlistOpen"：Open and jump to the taglist window. 

":TlistClose"：Close the taglist window.

":TlistToggle"：Open or close (toggle) the taglist window.

**echofunc**

功能：自动提示函数原型

下载地址：<http://www.vim.org/scripts/script.php?script_id=1735>

定义两个快捷键来切换函数的不同定义。

```
let g:EchoFuncKeyNext='<S-n>' 
let g:EchoFuncKeyPrev='<S-p>' 
```

**nerdtree**

nerdtree是一个用于浏览文件系统的树形资源管理。

下载地址：<https://github.com/scrooloose/nerdtree>

vimrc配置信息：

```
let NERDTreeWinPos='right'
let NERDTreeWinSize=30
map <F2> :NERDTreeToggle<CR>
```

配置之后可以使用`:NERDTree`或者配置的快捷键`F2`开启。


**pathogen**

pathogen一般作为vim新手的第一个插件，用来统一管理vim插件包。

官方解释：非常容易的管理你的 ‘runtimepath’ ，在实际项目中，vim-pathogen可以在它的私有文件夹下非常轻松的安装插件和管理运行时文件

复制以下代码到你的终端

```
mkdir -p ~/.vim/autoload ~/.vim/bundle &&
curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim
```

添加以下代码到你的.vimrc 文件中(文件位于用户的家目录下，如果不存在该文件，可以新建一个)

```
execute pathogen#infect()
syntax on
filetype plugin indent on
```

此时pathogen已经成功安装，可以安装以下插件测试下

```
cd ~/.vim/bundle &&
git clone https://github.com/tpope/vim-sensible.git

```
参考地址： <https://github.com/tpope/vim-pathogen>

**SuperTab**

自动补全功能，给了Tab键“超能力”的 SuperTab 插件。

下载地址：[https://github.com/ervandew/supertab.git](https://github.com/ervandew/supertab.git)
