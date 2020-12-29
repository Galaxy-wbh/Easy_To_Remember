最近发现的非常好用的工具Tmux，记录一下在使用这个工具的一些常用命令。



## Tmux常用命令总结

注意，`ctrl+b`是tmux命令唤醒键，`ctrl+b x`表示先按一下`ctrl+b`再按一下`x`键



### 管理会话

#### 新建会话

```Shell
tmux new -s <session-name>
```



#### 分离会话

在tmux窗口中按`ctrl+b d`或者使用如下命令

```shell
tmux detach
```



#### 介入会话

在非tmux窗口中使用如下命令

```shell
# 根据session名称进入
tmux attach -t <session-name>
# 根据session编号进入
tmux attch -t <session-number>
```



#### 杀死会话

在非tmux窗口中使用如下命令

```shell
# 根据session名称进入
tmux kill -t <session-name>
# 根据session编号进入
tmux kill -t <session-number>
```



#### 列出当前会话

在非tmux窗口中使用如下命令

```shell
tmux ls
```



### 窗格管理



#### 划分窗格

在tmux内使用如下命令

```shell
# 划分为上下两个窗格
tmux split-window
# 划分为左右两个窗格
tmux split-window -h
```



#### 切换窗格

在tmux内按下`ctrl+b q`会显示当前窗格的对应的数字编号，按下对应的数字编号就光标就会跳到对应的窗格内



#### 关闭窗格

在tmux内按下`ctrl+b x`会再按下`y`会关闭光标所在的窗格

