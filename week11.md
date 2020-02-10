
#### Algorithm
  - Path Sum II 求出sum为期望值的所有路径
  - https://leetcode.com/problems/path-sum-ii/submissions/

#### review
  - https://medium.com/@Bar_Code/purpose-and-perspective-through-what-why-and-how-e158bf63e764
  1. 做一件事情时明白what（你做的事情是什么），why(这件事情为什么要去做)，how(如何做这件事情)，你只有明白这件事情为啥要去做，才能知道怎么去做，否则做出来的东西就不是用户所需要的，比如学习红黑树，第一步搞清楚是什么，第二步明白为什么会造出这么一个数据结构-红黑树，从而就明白了红黑树具体在什么场景下使用即第三步。
  2. 更进一步，可以从三个角色分别去问自己这三个问题，从自己，团队，用户去理解，可以更进一步搞清楚事情的意图与背景。
  
#### tip
  tips：
  - sql注入一般是因为将输出串拼接到sql中导致sql逻辑发生变化，这一过程发生在编译阶段。用PreparedStatement可以解决问题，因为PreparedStatement在编译阶段编译的是带有占位符的sql语句，运行阶段才将输入串作为参数放入sql语句中，因此不会造成sql逻辑的变化。
  - https://blog.csdn.net/ls5718/article/details/52123140
  
#### Share
  - https://benjaminwhx.com/2018/04/28/%E3%80%90%E7%BB%86%E8%B0%88Java%E5%B9%B6%E5%8F%91%E3%80%91%E8%B0%88%E8%B0%88ThreadLocal/
  - ThreadLocal内存泄漏本质原因不是因为弱引用，而是由于ThreadLocalMap的生命周期跟Thread一样长，如果都没有手动删除对应key，都会导致内存泄漏，但是使用弱引用可以多一层保障：弱引用ThreadLocal对象不会内存泄漏，对应的value在下一次ThreadLocalMap调用set,get,remove的时候会被清除。可以分两种情况考虑：
    1. key 使用强引用：引用ThreadLocal对象的对象被回收了，但是ThreadLocalMap还持有ThreadLocal的强引用，如果没有手动删除，ThreadLocal不会被回收，导致Entry内存泄漏。
    2. key 使用弱引用：引用ThreadLocal的对象被回收了，由于ThreadLocalMap持有ThreadLocal的弱引用，即使没有手动删除，ThreadLocal也会被回收。value在下一次ThreadLocalMap调用set,get的时候会被清除。
  
  
