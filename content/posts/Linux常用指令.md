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
1. pwd  显示出地址   
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
12. rm -rf  /home/bbb 强制删除      -f 就是强制删除不提醒
13. mv 移动指令 
14. cat  查看文件     -n 行号
15. less 分屏查看 
16. echo $HOSTNAME  输出环境变量
17. head 查看文件的前几行 -> 10 行 head  xxxx.c 
18. tail  查看末尾文件 tail  xxxx.c 
19. ln -s  /root      /home/myroot           快捷指令指向  在myroot创建指向/root的快捷方式,  cd myroot 就会直接进入/root

# cat命令

1. cat > xxxx.c  创建文件
2. 合并文件 cat tx1.c   tx2.c   >  tx3.c    
3. 末尾添加内容  cat  >> tx.c  



# more命令

1. more -3   tx   查看大型文件









