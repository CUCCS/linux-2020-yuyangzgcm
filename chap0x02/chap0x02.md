## 你了解vim有哪几种工作模式？
- `Normal mode`
- `Insert mode`
- `Replace mode`
- `Command-line mode`
- `compatible mode`
- `Visual mode`
## Normal模式下，从当前行开始，一次向下移动光标10行的操作方法？如何快速移动到文件开始行和结束行？如何快速跳转到文件中的第N行？
- 一次向下移动光标10行的操作： `j 10`
- 快速移动到文件开始行： `gg`
- 快速移动到文件结束行： `G`
- 快速跳转到文件中的第N行： `NG`
## Normal模式下，如何删除单个字符、单个单词、从当前光标位置一直删除到行尾、单行、当前行开始向下数N行？
- 单个单词： `x`
- 单个单词： `dw`
- 从当前光标位置一直删除到行尾:    `d$`
- 单行：`dd`
- 当前行开始向下数N行： `N dd`

## 如何在vim中快速插入N个空行？如何在vim中快速输入80个-？
- 从下一行开始插入N个空行 ：`N o <Esc>`
- 从上一行开始插入N个空行 ： `N O <Esc>`
- 在vim中快速输入80个- ：`80 i - <Esc>`
## 如何撤销最近一次编辑操作？如何重做最近一次被撤销的操作？
- 撤销最近一次编辑操作： `u` 
- 重做最近一次被撤销的操作： `CTRL-R`
## vim中如何实现剪切粘贴单个字符？单个单词？单行？如何实现相似的复制粘贴操作呢？
- 剪切粘贴单个字符 ：`x p`
- 剪切粘贴单个单词 : `dw p`
- 剪切粘贴单行 ：`dd p`
- 复制粘贴单个字符 ：`yl p`
- 复制粘贴单个单词 ：`yw p`
- 复制粘贴单行 ：`yy p`
## 为了编辑一段文本你能想到哪几种操作方式（按键序列）？
1. `vim filename`打开文件
2. `i <Esc>`、`d [motion]`、`A`等对文件进行操作
3. `<Esc> : wq` 保存

## 查看当前正在编辑的文件名的方法？查看当前光标所在行的行号的方法？
- 查看当前正在编辑的文件名：`normal mode下 :f` 
- 查看当前光标所在行的行号：`CTRL-G`

## 在文件中进行关键词搜索你会哪些方法？如何设置忽略大小写的情况下进行匹配搜索？如何将匹配的搜索结果进行高亮显示？如何对匹配到的关键词进行批量替换？
- 进行关键词搜索： `/key-word(/g)`、`?key-word`
- 设置忽略大小写的情况下进行匹配搜索： `set ic`
- 将匹配的搜索结果进行高亮显示： `sel hls `
- 对匹配到的关键词进行批量替换
    - `:#,#s/old/new/g`，`#`为行号，对选定范围内进行替换
    - `:%s/old/new/g`，对整个文件进行替换
    - `:%s/old/new/gc`，对整个文件替换，每次替换是询问是否替换


## 在文件中最近编辑过的位置来回快速跳转的方法？
- `Normal`模式下：
    - `CTRL-O` ：向前
    - `CTRL-I` : 向后
## 如何把光标定位到各种括号的匹配项？例如：找到(, [, or {对应匹配的),], or }
- 将光标放在`(`或`[`或`{`上，`%`
## 在不退出vim的情况下执行一个外部程序的方法？
- `:!+外部命令`,如：`:!ls`
## 如何使用vim的内置帮助系统来查询一个内置默认快捷键的使用方法？如何在两个不同的分屏窗口中移动光标？

- 使用vim的内置帮助系统来查询一个内置默认快捷键的使用方法：
    - Normal 模式 ： `:help command`
    - Insert 模式 : `:help i_command`
    - Command-line模式 : `:help c_command`
    - Visual模式 : `v_command`
- 在两个不同的分屏窗口中移动光标：`CTRL-W CTRL-W`



## Lesson 1
[![asciicast](https://asciinema.org/a/RhTSGMHvwpqEyxAcXeOgPpuvt.svg)](https://asciinema.org/a/RhTSGMHvwpqEyxAcXeOgPpuvt)
- `:q!` : 不保存退出
- `wq` : 保存退出
- `x` : 删除单个字符
- `i` : 在光标后进行插入
- `A` : 行尾插入

## Lesson 2
[![asciicast](https://asciinema.org/a/IzHmA0hipmMZacwnWJy2o12IP.svg)](https://asciinema.org/a/IzHmA0hipmMZacwnWJy2o12IP)
- `dw` : 删除光标开始到下一个词之间的内容
- `d$` : 删除当行光标后的所有内容
- `dd` : 删除整行
- `operator [number] motion` : 该操作的作用数量，如`d2w`删除两个单词
- `0` : 光标移到行首
- `u` : 取消上一次操作
- `U` : 取消一行里的所有改变
- `CTRL-R` : 重做被取消的操作

## Lesson 3
[![asciicast](https://asciinema.org/a/B3zHey3VF2zdYeuUY7Rw1O1SL.svg)](https://asciinema.org/a/B3zHey3VF2zdYeuUY7Rw1O1SL)
- `p` : 输出被删除的内容
- `r` : 替换光标上的字符
- `c$` : 改变从光标位置到行尾内容
- `ce` : 改变从光标到词尾内容

## Lesson 4
[![asciicast](https://asciinema.org/a/OfvCwSojTSYnvQEMx5U4qjCqb.svg)](https://asciinema.org/a/OfvCwSojTSYnvQEMx5U4qjCqb)
- `CTRL-G` : 显示光标在文件中的位置和文件状态
- `G` : 到文件尾部
- `number G` : 跳到`number`行
- `gg` : 跳到第一行
- `/word` : 向后找
- `?/word` : 向前找
- `%` : 匹配`{}、[]、()`
- `:s/old/new`，替换第一个，`/g`进行单行的全局替换
- `:#,#s/old/new/g`，`#`为行号，对选定范围内进行替换
- `:%s/old/new/g`，对整个文件进行替换
- `:%s/old/new/gc`，对整个文件替换，每次替换是询问是否替换


## Lesson 5
[![asciicast](https://asciinema.org/a/7LmUETBfwDTEwTYc6UQ2yvKp3.svg)](https://asciinema.org/a/7LmUETBfwDTEwTYc6UQ2yvKp3)
- `:!command` : 执行外部命令
- `:w filename` : 当前vim打开文件内容写入`filename`文件中
- `v motion :w filename` : 将选中行内容写入`filename`
- `:r filename` : 搜索`filename`文件，将其内容显示在光标下方
- `:r !cmd` : 将`cmd`的输出显示

## lession 6
[![asciicast](https://asciinema.org/a/ygxTenb9VS2Y649Nuy5waMiQ6.svg)](https://asciinema.org/a/ygxTenb9VS2Y649Nuy5waMiQ6)
- `o` : 光标下打开一行，进入插入模式
- `O` : 光标上打开一行
- `a` : 光标后插入
- `A` : 行尾插入
- `e` : 移动到单词尾部
- `y` : copy  `p` : paste
- `R` : 进入替换模式
- `:set ic` : 忽略大小写
- `:set is` : 显示搜索短语的部分匹配
- `hls` : 高亮匹配短语

## lession 7
[![asciicast](https://asciinema.org/a/Z2VBd1sWv8l8abe0Vn8uWjieh.svg)](https://asciinema.org/a/Z2VBd1sWv8l8abe0Vn8uWjieh)

