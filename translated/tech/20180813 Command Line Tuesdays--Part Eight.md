命令行星期二——第八部分
================================================================================
唷，唷，极客们！我们回来了，来完成最后一章的CLT。今天，我们将讨论一下任务控制。在这个里头，我们也将学习怎样来控制运行在我们计算机上的进程！

### 一个例子 ###

正如我们所学的，我们可以直接在CLI中输入程序名称来运行该程序。例如，dolphin。如果我们输入：

    dolphin

……dolphin，这个文件管理器，就打开了。如果在进程打开时你查看终端，你就不能访问命令提示符了，而且你也不能在同一个窗口中写一个新命令进去了。如果你终止dolphin，提示符又会出现了，而你又能输入一个新命令到shell中去了。那么，我们怎么能在CLI运行一个程序时，同时又能获得提示符以便进一步发命令。

    dolphin &

……现在你让dolphin文件管理器在后台运行了，终端就可以空出来输入你需要的另外一个命令了。

现在，假设你忘了在dolphin后面输入‘&’字符，你只需要输入‘ctrl+z’，它会停止你的进程并把它放到空闲列表中去。要继续停止的进程，输入：

    bg

……它会从后台重启进程。

### jobs, ps ###

由于我们在后台运行着进程，你可以使用jobs或者使用ps来来列出它们。试试吧，只要输入jobs或者输入ps就行了。下面是我得到的结果：

    nenad@linux-zr04:~> ps
    PID TTY          TIME CMD
    8356 pts/1    00:00:00 bash
    8401 pts/1    00:00:00 dolphin
    8406 pts/1    00:00:00 kbuildsycoca4
    8456 pts/1    00:00:00 ps

### 杀死进程 ###

如果有个进程无响应了，怎么来处理掉它呢？可以使用kill命令。让我们在先前提到的dolphin进程上试试。首先，我们必须使用ps来鉴别该进程的PID。在我上述情况中，dolphin的PID是8401。那么让我们来杀死它，我只要输入：

    kill 8401

……那么，它就把dolphin给杀死了。

### Kill更多细节 ###

Kill的存在，不仅仅是为了终止进程，它最初是设计用来发送信号给进程。当然，有许多kill信号可以使用，根据你使用的应用程序不同而不同。请看下面的表：

![](https://news.opensuse.org/wp-content/uploads/2014/08/snapshot1.png)

务必试试这些信号。

### 结尾 ###

我们以本节课来结束我们的CLT系列和周二必达，我希望其他像我这样的新手们能设法在他们的思想中摆脱控制台的神秘而学习掌握一些基本技能。现在对你们而言，所有剩下来要做的事，就是尽情摆弄它吧（只是别把/目录搞得太乱七八糟，因而你也不会诋毁什么东西了 :D）。
We’ll be seeing a lot more of each other soon, as there’s more series of articles from where these came from. Stay tuned, and meanwhile…
我们将在不久的将来看到其它更多的东西，因为有更多的系列文章来自这些文章的出处。别走开，同时…… 
### ……尽情享受！ ###

--------------------------------------------------------------------------------

via: https://news.opensuse.org/2014/08/12/command-line-tuesdays-part-eight/

作者：[Nenad Latinović][a]
译者：[GOLinux](https://github.com/GOLinux)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创翻译，[Linux中国](http://linux.cn/) 荣誉推出

[a]:https://news.opensuse.org/author/holden87/