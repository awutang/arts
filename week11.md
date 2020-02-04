
#### Algorithm
  Construct Binary Tree from Preorder and Inorder Traversal 根据先序及中序遍历结果得到二叉树
  recursive 递归写法实现不易
  https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/submissions/

#### review
  - https://medium.com/@Bar_Code/purpose-and-perspective-through-what-why-and-how-e158bf63e764
  1. 做一件事情时明白what（你做的事情是什么），why(这件事情为什么要去做)，how(如何做这件事情)，你只有明白这件事情为啥要去做，才能知道怎么去做，否则做出来的东西就不是用户所需要的，比如学习红黑树，第一步搞清楚是什么，第二步明白为什么会造出这么一个数据结构-红黑树，从而就明白了红黑树具体在什么场景下使用即第三步。
  2. 更进一步，可以从三个角色分别去问自己这三个问题，从自己，团队，用户去理解，可以更进一步搞清楚事情的意图与背景。
  
  
3.tip
  tips1:Java中可以通过System.getEnv()获取环境变量；System.getProperties()获取系统属性（系统的相关属性,包括文件编码,操作系统名称,区域,用户名等）
  环境变量：指的是当前机器操作系统环境变量，包括用户环境变量和系统环境变量，对于windows是将系统属性-->高级-->环境变量中设置的变量显示在此(对于linux是将通过export设置的变量显示在此)
  ）；系统属性指的是jvm的环境变量，比如在idea中设置的-DPROJECT_ID=public

4.Share
  https://juejin.im/entry/59b740fdf265da06633d02cf
  https://www.jianshu.com/p/2581342317ce
  关于零拷贝，涉及到：
    1.用户态与内核态的切换，
    2.cpu copy 与 dma(direct memory access):硬件与软件的交互，不涉及cpu
   read()、write() -->mmap()、write()--》sendFile()   减少一次cpu copy ,两次上下文切换 sendFile()是Linux的函数。
