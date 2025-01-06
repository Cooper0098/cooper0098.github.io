+++
title = '解决VsCode的git提交问题'
date = 2025-01-06T21:03:12+08:00



categories = ["git"] 
tags = ["git" , "提交失败"]

+++



# 解决VsCode的git提交失败问题



## 取消代理设置

可能是因为魔法的原因连接不上.   

这是最常见的解决方法之一，通过在终端执行以下命令，可以取消 Git 的代理设置：

```bash
git config --global --unset http.proxy 
```

```bash
git config --global --unset https.proxy
```

这样就可以清除 Git 的代理设置，让其直接连接网络进行操作。





