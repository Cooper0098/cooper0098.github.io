+++
title = 'Linux常用指令'
date = 2024-09-07T20:47:03+08:00

categories = ["Linux"]
tags = ["指令"]

+++

# 常用指令
  1. vim    访问文本
  2. 退出文本并保存       :wq
  3. 返回到上一个文件夹    cd . .
  4. 解压指令         tar  -zxvf   xxxx.tar.gz 




# vi    vim 操作
 1. i o a r  进入vim
 2. 按下esc , 输入**:**   然后输入wq  保存并退出            :q退出      :q!  不保存退出
 3. yy 拷贝    5yy  
 4. dd 删除   5dd
 5. 撤销  u
 6. 行号打开 :set nu




# 关机
 1. shutdown -h  关机 
 2. shutdown -r  重启
 3. reboot  重启
 4. sync  把内存数据存入磁盘



# 注销用户和登录
 1. logout 

 2. 退出root    logout

    


# 压缩/解压指令

 1. tar  -zxvf   xxxx.tar.gz
 2. gzip 文件 压缩
 3. gunzip 解压文件
 4. zip 压缩文件夹
 5. unzip 解压文件夹
 6. -r 递归压缩  zip -r xxxxx.zip  /home/  [将home目录及其包含的的文件和子文件夹都压缩]
 7. -d <可指定目录>   unzip -d /opt/tmp    /home/xxxxx.zip
 8. tar 万能 
 9. tar -c  产生打包文件
 10. -v 显示详细信息 
 11. -f 指定压缩后的文件名
 12. -z 打包并同时压缩
 13. -x 解压.tar文件


# 帮助指令

  1. man ls 列出所有指令

  2. help   +  指令

  3. ls -la

  4. ls  -la /root

     

# 文件目录指令
1. **pwd  显示出地址**   
2. cd ~  回到家目录
3. cd .. 上一目录
4. mkdir 创建目录  
5. mkdir -p /home/.../....  创建指定目录 
6. rmdir 删除空目录    强制删除空目录 rm -rf
7. touch 创建空文件 
8. cp 拷贝  cp hello.txt /bbb
9. cp -r  /home/bbb /opt  把目录复制到指定目录下
10. \cp -r  /home/bbb /opt 强制
11. rm 删除文件或目录 
12. **rm -rf  /home/bbb 强制删除      -f 就是强制删除不提醒**
13. mv 移动指令 
14. cat  查看文件     -n 行号
15. less 分屏查看 
16. echo $HOSTNAME  输出环境变量
17. head 查看文件的前几行 -> 10 行 head  xxxx.c 
18. tail  查看末尾文件 tail  xxxx.c 
19. ln -s  /root      /home/myroot           快捷指令指向  在myroot创建指向/root的快捷方式,  cd myroot 就会直接进入/root



#  文件管理

1. mkdir 创建目录 mkdir  xxxx  
2. 多级目录创建 mkdir  -p  xxx/yyy 
3. mkdir -m  777  xxxx    ,权限设置  , 777 全部  ,  4 读 ,  2  写,   1 执行
4. mv 移动,  重命名或者移动文件 ,   mv   xxx.c   /home/zzz/targetPlace  
5. cp 复制**文件** ,  cp  xxx.c   /home/zzz/targetPlace (目标位置) 
6. cp -r  /home/bbb /opt  把**目录**复制到指定目录下
7. rm  /  rmdir  , rm  文件名  ,  rm  -r  目录名 ,  rmdir  目录名 
8. 更改文件所有权   chown / chgrp  ,  chown -R  root(更改后)   /home/zzz/targetPlace/xxx.c  把xxx.c的所有权改成了 root 
9. chgrp root /home/zzz/targetPlace/yyy.c   同理
10. 更改权限 , chmod  777 xxxx (目录) 
11. ln 创建链接 , 约等于快捷方式 , ln    路径/xxx.c    newxxx.c  ,  删除快捷方式: rm  -rf   newxxx.c 
12.   输入/输出 重新定向 , 如 date >  xx.txt  ,  date >> xx.txt  ,  应用-> 日志 , 脚本, 文件 



![image-20240910112844875](../img/image-20240910112844875.png)   

![image-20240909235340928](../img/image-20240909235340928.png)



# cat命令

1. cat > xxxx.c  创建文件
2. 合并文件 cat tx1.c   tx2.c   >  tx3.c    
3. 末尾添加内容  cat  >> tx.c  



# more命令

1. more -3   tx   查看大型文件



# grep命令

1. 查找文件 grep  -i "abc....."   xxxx.c  不分大小写查找内容
2. grep   -n   "abc....."   xxxx.c   显示匹配行, 同时不分大小写查找内容



# find命令

1. find -name  'tex*'  查找文件,  模糊查找
2. find -name  'te??.c'  同理
3. find  -name  '[a-z]*.c'  查找文件点后缀结尾的文件



# locate 命令

1. 快速定位文件 locate  xxxx



# who 命令

1. who 看用户  
2. who -a 看详细信息
3. whoami   查看当前是谁
4. uname   /  uname  -a   查看 主机信息  -n   -r  -v  -m  -p  -i   -o

# man命令

1. 查看命令手册,  列出说明书  man  ls ---> 列出 ls的说明







# 软件包管理

1. apt-get 命令 下载/卸载/管理 软件包
2. which 命令查找位置





# 文件系统类型

![image-20240911110514902](../img/image-20240911110514902.png)

![image-20240911114224707](../img/image-20240911114224707.png)



1. 更改单位来查看 swap 信息 free -h 

2. 挂载文件系统 sudo  mount  /dev/xxx/yyy/target    , target是挂载点 

3. 卸载已挂载的文件系统  umount   target 

4. 查询磁盘使用情况  df  -h  

5. 检查/修改文件系统 fsck  -C  -t   $type   $路径

6. 在磁盘创建文件系统  mkfs  

7. 建立分区表  fdisk  -l  $路径

8. 压缩工具/命令 , 压缩文件  gzip  xxxx.c  , 压缩目录 gzip  -r    /home  , 解压  gzip   -d  xxxx.c.gz  

9. 压缩工具 tar , tar  --help 详细 ,  tar  -cvf  xxx.tar  (结果)   yyy.c .... (要打包压缩的文件)  

10. tar 解压 tar  -xf  xxx.tar  -C  $解压放置的位置 

11. bzip   **用途**: 用于压缩和解压缩文件，生成 `.bz2` 文件。

    - 压缩:

    ```bash
    bzip2 filename
    ```

    这将生成一个 `filename.bz2` 文件。

    - 解压缩:

      ```bash
      bzip2 -d filename.bz2
      ```

      或者使用 `bunzip2`:

      ```bash
      bunzip2 filename.bz2
      ```

    

12. zip  **用途**: 用于创建和解压缩 ZIP 文件，生成 `.zip` 文件。命令:

    - 压缩:

      ```bash
      zip archive.zip file1 file2
      ```

      这将创建一个 `archive.zip`，包含 `file1` 和 `file2`。

    - 解压缩:

      ```bash
      unzip archive.zip
      ```



# 用户管理

1. 查看用户 cat    /etc/passwd
2. 添加用户  **useradd**   xxxx  
3. 创建用户组 groupadd ,  groupadd   xxxxgroup  ,  查看所有用户组  cat  /etc/group
4. 记录用户操作 ,  history 
5. passwd 改密码
6. 删除用户  userdel  xxxuser
7. 管理用户账号 , usermod    -l  new_name   old_name  改名 
8. 查看用户信息 ,  id  xxxname  
9. 用户切换 ,  su  root  ,  su  xxxname  
10. sudo 以管理者命令执行 



# 进程管理



1. 监视进程 , ps命令 , ps , man  ps 查看功能,  常用 : 显示所有进程 ps  -e   , 显示所有不带终端的进程 ps  -aus  ,  显示用户进程 ps  -u  root  , ps  -u  xxxname ,  ps  -l
2. 跟踪进程命令 top ,    自动更新 4 次后退出 top -n  4;    设置 `top` 刷新时间为 5 秒  top   -d  5 ;    仅监控进程 ID 为 1810 的进程  top  -p  1810  ;  
3. htop 命令 , 升级版 top 命令 
4. 终止进程 kill 命令,   关闭 进程 kill  1201  (进程名) 
5. 设置进程优先级 ,  使用ps命令查看进程nice值并且降序排列, ps  axo  pid,comn,nice  --sort=-nice  ;  查看nice值  ps  -p  1201  -o  nice  ;   修改nice值   renice  -n  10(更改值)  -o  1201 
6. 查看进程属性  pgrep 命令 ,  常用命令 : pgrep  xxxname(进程名)   ;   pgrep  -l  ^xxxname(模糊名字查询)  

# 性能监控

1. 显示和配置网络设备 ,  ifconfig  -help  

<img src="../img/image-20240914002152088.png" alt="image-20240914002152088" style="zoom:80%;" />

![image-20240914002325290](../img/image-20240914002325290.png)

2. 报告cpu统计数据 iostat 命令, 常用:  iostat ;  输出磁盘利用率 iostat  -d  sda1 ; 输出cpu和磁盘利用率  iostat  -t ;  显示cpu和磁盘利用率  iostat -m ; 查看cpu  iostat  -c
2. I/O 监控命令 iotop , 需要root权限  

![image-20240914153126788](../img/image-20240914153126788.png)  

4.  报告cpu统计信息 ,  mpstat  ,  显示cpu中断数  mpstat -I SUM  
4.  虚拟内存统计命令vmstat  -a ;  输出磁盘统计数据 vmatat  -d ;  报告虚拟内存统计信息的命令 vmstat  -s  



# shell 编程基础

![image-20240914225909268](../img/image-20240914225909268.png)

![image-20240914230011901](../img/image-20240914230011901.png)

## shell入门编程实例

![image-20240914231618458](../img/image-20240914231618458.png)

![image-20240914231401858](../img/image-20240914231401858.png)



<p>   
   	其他进阶 shell 编程资料, 在我的 GitHub 上可以下载:    
    <a href="https://github.com/Cooper0098/cooper0098.github.io/tree/master/content/Resource/绝版经典《Linux与Unix Shell编程指南》" target="_blank">     Linux与shell进阶编程   </a> 
</p>




# Linux C++引用



![image-20240915153157020](../img/image-20240915153157020.png)





# Linux C++智能指针

## unique_ptr

![image-20240915222014358](../img/image-20240915222014358.png)

## shared_ptr

![image-20240915222905392](../img/image-20240915222905392.png)

## weak_ptr

![image-20240915225233527](../img/image-20240915225233527.png)

为什么要使用 weak_ptr指针:  为了解决 shared ptr 循环引用问题。



# Linux客户端与服务器















