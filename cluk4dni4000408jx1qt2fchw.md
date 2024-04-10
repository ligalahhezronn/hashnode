---
title: "Nano Editor"
seoTitle: "Nano  Kali-linux"
seoDescription: "Nano Kali-linux"
datePublished: Wed Apr 03 2024 18:06:35 GMT+0000 (Coordinated Universal Time)
cuid: cluk4dni4000408jx1qt2fchw
slug: nano-editor
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1712154082231/b1f7fd03-8514-4dc7-9e24-e759c6cbed8d.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1712166824791/613e3116-4834-47b2-b5e7-a86eb0820ba8.jpeg
tags: linux, nano, linux-for-beginners

---

Nano is pre-installed in Kali-Linux. But you can install it on Ubuntu using the aptitude package manager: `sudo apt-get install nano`

Nano can be opened by simply typing `nano` within the terminal. It will give you a bit of information in regard to the buffer that you have just created.

`Ctrl + G` basic help.

You can type in whatever you want in nano. It can be text or code.

`Ctrl + O` save the file. This will prompt you to give the file a name and the extension that you want to use. For example, file.txt, file.c or file.py. The extension basically depends on the content of the file.

`Enter` saves the text within the file.

`Ctrl + X` exit the editor. And if you have any changes, it will prompt you to save or to discard them. This is usually denoted by yes or no answer.

When you list the files, you should see the file you created. `ls`

You can as well open another file from within the editor. Let's say you were editing a file, and you want to move on to the next one. `Ctrl + R` that will prompt you for the file name of the file that you want to access. Within the same buffer. The reason why this is possible is because changing buffers actually is just leaving one buffer active as you move to the next one.

`Alt + >` & `Alt + <` switching between buffers.

`Alt + A` select a region of text that you want to copy. This will tell you that \[mark set\] the mark has been set. Use your arrows to select the data that you want to copy. `Alt + ^` that will copy the data.

`Ctrl + U` paste the data that you have copied.

`Ctrl + K` cut.

`Alt + \` top.

`Alt + /` bottom.

`Alt + G` will ask you for the line number that you want to move to.

`Ctrl + W` when you are looking for a string.

`Ctrl + R` replace a string.

`Ctrl + Y` & `Ctrl + V` page up and page down.

`Ctrl + I` tab.

`Ctrl + D` delete.

These should encapsulate everything that you will ever need when using nano.

If you have any other commands and shortcuts for nano, you can simply comment it in the comment section, and I will update it in this article.