+++
title = 'Hugo博客的图片上传'
date = 2024-09-08T16:33:57+08:00

categories = ["技术分享"]
tags = ["博客", "图片显示"]

+++



# 目前我的解决办法



1. 在 `posts` 目录下创建一个名为 `img` 的文件夹，用于存储照片。该文件夹的路径为 `..\content\posts\img`。
2. 将需要使用的照片复制并放入 `img` 文件夹中。在 Markdown 文档中使用照片时，可以通过相对位置进行引用。例如，引用的路径为 `"../img/photo1.jpg"`。请注意，使用 `"../"` 可确保照片在博客页面上正确显示。
3. 若想在**本地**上查看 Markdown 文档中展示的照片，可以使用 `"./"` 作为引用路径。例如，引用的路径为 `"./img/photo1.jpg"`。   
4. 注意图片命名，确保照片文件名中**不包含空格**。

      


有问题的话, 欢迎在评论区留言, 我会尽快回复！
