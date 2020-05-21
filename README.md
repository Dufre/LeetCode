
[TOC]
# 常用数据结构

## 数组/字符串（Array/String）
- 优点
    - 构建一个数组非常简单
    - 能在O(1)的时间里根据下标(index)查询某个元素
- 缺点
    - 构建时必须分配一段连续的空间
    - 查询某个元素是否存在时需要遍历整个数组，耗费O(n)的时间
    - 删除和添加某个元素时，同样需要耗费O(n)的时间

**典型题目：**
题目太多，下一版总结

## 链表（Linked-list）

- 分类
    - 单链表
    - 双链表
- 优点
    - 灵活地分配内存空间
    - 能在O(1)时间内删除或者添加元素
- 缺点
    - 查询元素需要O(n)时间
- 解题技巧
    - 利用快慢指针（有时候需要用到三个指针）
        - 翻转链表
            - [206. 反转链表](https://leetcode-cn.com/problems/reverse-linked-list/)
        - 寻找倒数第k个节点
            - [19. 删除链表的倒数第N个节点](https://leetcode-cn.com/problems/remove-nth-node-from-end-of-list/)
        - 判断链表是否有环
            - [141. 环形链表](https://leetcode-cn.com/problems/linked-list-cycle/)
            - [142. 环形链表 II](https://leetcode-cn.com/problems/linked-list-cycle-ii/)
        - 相交链表
            - [160. 相交链表](https://leetcode-cn.com/problems/intersection-of-two-linked-lists/)
    - 构建一个虚假的链表头
        - 两个排序链表，进行整和排序
        - 将链表的奇偶数按原定顺序分离，生成前半部分为奇数，后半部分为偶数的链表
- 解题技巧
    - 在纸上画出节点之间的相互关系
    - 画出修改的方法

**典型题目**
- `easy`
- `medium`
- `hard`
    - [25. K 个一组翻转链表](https://leetcode-cn.com/problems/reverse-nodes-in-k-group/)

## 栈（Stack）
- 特点
    - 后进先出（LIFO）
- 基本思想
    - 可以用一个单链表来实现
    - 只关心上一次的操作
    - 处理完上一次的操作后，能在O(1)时间内查找到更前一次的操作

**典型题目：**
- `easy`
    - [20. 有效的括号](https://leetcode-cn.com/problems/valid-parentheses/)
- `medium`
    - [227. 基本计算器 II](https://leetcode-cn.com/problems/basic-calculator-ii/)
    - [739. 每日温度](https://leetcode-cn.com/problems/daily-temperatures/)
- `hard`
    - [42. 接雨水](https://leetcode-cn.com/problems/trapping-rain-water/)
    - [84. 柱状图中最大的矩形](https://leetcode-cn.com/problems/largest-rectangle-in-histogram/)
    - [224. 基本计算器](https://leetcode-cn.com/problems/basic-calculator/)
    - [772. 基本计算器 III](https://leetcode-cn.com/problems/basic-calculator-iii/)

## 队列（Queue）
- 特点
    - 先进先出（FIFO）
- 基本思想
    - 双链表
    - 需要按照一定的数据来处理数据，而要处理的数据在不断变化
- 常用场景
    - BFS常用

典型例题
- 基本概念
    - [622. 设计循环队列](https://leetcode-cn.com/problems/design-circular-queue/)
- BFS相关
    - [752. 打开转盘锁](https://leetcode-cn.com/problems/open-the-lock/)
## 双端队列（Deque）
- 基本实现
    - 可以利用一个双链表
    - 队列的头尾两端能在O(1)的时间内进行数据的查看，添加和删除
- 常用场景
    - 实现一个长度动态变化的窗口或者连续区间

典型题目：
- `easy`
- `medium`
    - [641. 设计循环双端队列](https://leetcode-cn.com/problems/design-circular-deque/)
- `hard`
    - [239. 滑动窗口最大值](https://leetcode-cn.com/problems/sliding-window-maximum/)
## 树（Tree）

- 树的共性
    - 结构直观
    - 通过树问题来考察递归算法  
- 面试常考的树的形状
    - 普通二叉树
    - 平衡二叉树
    - 完全二叉树
    - 二叉搜索树
    - 四叉树
    - 多叉树
- 特殊的树
    - 红黑树
    - 自平衡二叉搜索树
- 考点
    - 遍历
        - 前序遍历（Preorder Traversal）
            - 构造树
            - 搜索
        - 中序遍历（Inorder Traversal）
            - 二叉搜索树
        - 后序遍历（Postorder Traversal）
           - 收集信息自下而上（leetcode 250）

**前序/中序/后序遍历**
- [144. 二叉树的前序遍历](https://leetcode-cn.com/problems/binary-tree-preorder-traversal/)
- [94. 二叉树的中序遍历](https://leetcode-cn.com/problems/binary-tree-inorder-traversal/)
- [145. 二叉树的后序遍历](https://leetcode-cn.com/problems/binary-tree-postorder-traversal/)

**层次/ZigZag遍历**
- [102. 二叉树的层序遍历](https://leetcode-cn.com/problems/binary-tree-level-order-traversal/)
- [103. 二叉树的锯齿形层次遍历](https://leetcode-cn.com/problems/binary-tree-zigzag-level-order-traversal/)


## 哈希表

典型题目

- `easy`
    - [1. 两数之和](https://leetcode-cn.com/problems/two-sum/)
    - [387. 字符串中的第一个唯一字符](https://leetcode-cn.com/problems/first-unique-character-in-a-string/)
- `medium`  
    - [3. 无重复字符的最长子串](https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/)
- `hard`

# 高级数据结构

## 优先队列（Priority Queue）
- 与普通队列的区别
    - 保证每次去取出的元素是队列中优先级最高的
    - 优先级别可自定义
- 最常用的场景
    - 从杂乱无章的数据中按照一定的顺序（或者优先级）筛选数据
- 本质
    - 二叉堆的结构，利用一个数组结构来实现完全二叉树
- 特性
    - 数组里的第一个元素array[0]拥有最高的优先级
    - 给定一个下标i，那么对于元素array[i]而言
        - 父节点对应的元素下标是(i-1)/2
        - 左侧子节点对应的元素下标是2*i+1
        - 右侧子节点对应的元素下标是2*i+2
        - 数组中每个元素的优先级都必须要高于它两侧子节点
- 基本操作
    - 向上筛选（sift up/bubble up）
    - 向下筛选（sift down/bubble down）
- 优先队列的初始化
    - 时间复杂度（O(n)）

典型例题：
典型例题：
- `easy`
- `medium`
    - [347. 前 K 个高频元素](https://leetcode-cn.com/problems/top-k-frequent-elements/)
- `hard`

## 图（Graph）
- 基本知识点
    - 阶、度
    - 树、森林、环
    - 有向图、无向图、完全有向图、完全无向图
    - 连通图、联通分量
- 图的存储和表达方式
    - 邻接矩阵
    - 邻接链表
- 围绕图的算法
    - 图的遍历：深度优先、广度优先
    - 环的检测：有向图、无向图
    - 拓扑排序
    - 最短路径算法：Dijkstra、Bellman-Ford、Floyd Warshall
    - 连通性相关算法：Kosaraju、Tarjan、求解孤岛的数量、判断是否为树
    - 图的着色、旅行商问题等
- 必须熟练掌握的知识点
    - 图的存储和表达方式：邻接矩阵、邻接链表
    - 图的遍历：深度优先、广度优先
    - 二部图的检测（Bipartite）、树的检测、环的检测（有向图、无向图）
    - 拓扑排序
    - 联合-查找算法（Union-Find）
    - 最短路径：Dijkstra、Bellman-Ford
- 应用场景
    - 社交网络中，人与人的关系
    - 地图，求起始点到目的地的最短路径
- 遍历的时候用到的数据结构
    - 队列
        - 遍历节点，搜索列表
    - hash/map
        - 记录已遍历的节点
    - 二维数组
        - 邻接矩阵
        - 邻接表
        - 边缘列表

典型例题：
- `easy`
- `medium`
   - [207. 课程表](https://leetcode-cn.com/problems/course-schedule/)
   - [210. 课程表 II](https://leetcode-cn.com/problems/course-schedule-ii/)
   - [743. 网络延迟时间](https://leetcode-cn.com/problems/network-delay-time/)
   - [785. 判断二分图](https://leetcode-cn.com/problems/is-graph-bipartite/)
- `hard`
    
## 前缀树（Trie）
- 基本知识
    - 也称字典树
- 应用场景
    - 字典查找
    - 搜索框输入搜索文字，会罗列以搜索词开头的相关搜索
    - 汉语拼音输入法联想功能
- 重要性质
    - 每个节点至少包含两个基本属性
        - children：数组或者集合，罗列出每个分支当中包含的所有字符
        - isEnd：布尔值，表示该节点是否为某个字符串的结尾
    - 根节点是空的
    - 除了根节点，其他所有节点都可能是单词的结尾，叶子节点一定都是单词的结尾
- 最基本的操作
    - 创建
        - 遍历一遍输入的字符串，对每个字符串的字符进行遍历
        - 从前缀树的根节点开始，将每个字符加入到节点的children字符集当中
        - 如果字符集已经包含了这个字符，跳过
        - 如果当前字符是字符串的最后一个，把当前节点的isEnd标记为真
    - 搜索
        - 从前缀树的根节点出发，逐个匹配输入的前缀字符
        - 如果遇到了，继续往下一层搜索

典型例题：
- `easy`
- `medium`
    - [208. 实现 Trie (前缀树)](https://leetcode-cn.com/problems/implement-trie-prefix-tree/)
    - [211. 添加与搜索单词 - 数据结构设计](https://leetcode-cn.com/problems/add-and-search-word-data-structure-design/)
- `hard`
    - [212. 单词搜索 II](https://leetcode-cn.com/problems/word-search-ii/)
    - [336. 回文对](https://leetcode-cn.com/problems/palindrome-pairs/)
## 线段树（Segment Tree）
从一个例题出发
假设一个数组array[0...n-1]，里面有n个元素，现在我们要经常对这个数组做两件事：
1. 更新数组元素的数值
2. 求数组任意一段区间里元素的总和（或者平均值）

方法一：遍历一遍数组（时间复杂度`O(n)`）
方法二：线段树（时间复杂度`O(logn)`）

- 概念
    - 一种按照二叉树的形式存储数据的结构，每个节点保存的都是数组里某一段的总和
- 应用场合
    - 图片中修改像素的颜色
    - 任意矩形区间的灰度平均值

典型例题：
- `easy`
    - [303. 区域和检索 - 数组不可变](https://leetcode-cn.com/problems/range-sum-query-immutable/)
- `medium`
    - [307. 区域和检索 - 数组可修改](https://leetcode-cn.com/problems/range-sum-query-mutable/)
- `hard`
    - [315. 计算右侧小于当前元素的个数](https://leetcode-cn.com/problems/count-of-smaller-numbers-after-self/)
## 树状数组（Fenwick Tree/Binary Indexed Tree）
从一个例题出发
假设一个数组array[0...n-1]，里面有n个元素，现在我们要经常对这个数组做两件事：
1. 更新数组元素的数值
2. 求数组前k个元素的总和（或者平均值）

方法一：线段树（时间复杂度`O(logn)`）
方法二：树状数组（时间复杂度`O(logn)`）

- 基本特征
    - 利用数组来表示多叉树的结构，和优先队列有些类似
    - 优先队列是用数组来表示完全二叉树，而树状数组是多叉树
    - 树状数组的第一个元素是空节点
    - 如果节点tree[y]是tree[x]的父节点，那么需要满足y=x-(x&(-x))

典型例题：
- `easy`
- `medium`
- `hard`
    - [308. 二维区域检索 - 可变](https://leetcode-cn.com/problems/range-sum-query-2d-mutable/)

# 排序算法
## 基本的排序算法
### 冒泡排序

**算法思想**
从头部开始。每两个元素比较大小进行交换，直到这一轮当中最大或最小的元素被放置在数组的尾部，然后，不断地重复这个过程，直到所有元素都排好位置。

**复杂度分析**
- 空间复杂度（`O(1)`）
- 时间复杂度（`O(n^2)`）
    - 给定的数组按照顺序已经排好（`O(n)`）
        - 只需要进行n-1的比较，两两交换次数为0，是最好的情况
    - 给定的数组按照逆序对排列(`O(n^2)`)
        - 需要进行n(n-1)/2次比较，是最坏的情况
    - 给定的数组杂乱无章
        - 平均时间复杂度是O(n^2)
        
```java
void sort(int[] nums){
    boolean hasChange = true;
    for (int i=0; i<nums.length-1 && hasChange==true; i++){
        hasChange = false;
        for (int j=0; j<nums.length-1-i; j++){
            if (nums[j]>nums[j+1]){
                hasChange = true;
                swap(nums, j, j+1);
            }
        }
    }
}
```
### 插入排序

**算法思想**
不断地将尚未排好序的数插入到已经排好序的部分

**与冒泡排序对比**
- 在冒泡排序中，经过每一轮的排序处理后，数组后端的数是排好序的
- 在插入排序中，经过每一轮的排序处理后，数组前端的数都是排好序的

**复杂度分析**
- 空间复杂度（`O(1)`）
- 时间复杂度（`O(n^2)`）
    - 给定的数组按照顺序已经排好（`O(n)`）
        - 只需要进行n-1的比较，两两交换次数为0，是最好的情况
    - 给定的数组按照逆序对排列(`O(n^2)`)
        - 需要进行n(n-1)/2次比较，是最坏的情况
    - 给定的数组杂乱无章
        - 平均时间复杂度是O(n^2)
        
```java
void sort(int[] nums){
    for (int i=1; i<nums.length;i++){
        for (int j=i-1; j>=0 && nums[j]>nums[i]; j--){
            nums[j+1] = nums[j];
        }
        nums[j+1] = nums[i];
    }
}
```

### 选择排序
## 常考的排序算法
### 快速排序
**算法思想**
- 把原始的数组筛选成较小和较大的两个子数组，然后递归地排序两个子数组
- 在分成较小和较大的两个子数组过程中，如何选定一个基准值尤为关键

**复杂度分析**
- 时间复杂度
    - T(n) = 2*T(n/2) + O(n)
    - 把规模大小为n的问题分解成n/2的两个子问题
    - 和基准值进行n-1次比较，n-1次比较的复杂度就是O(n)
    - 整体的复杂度就是O(nlogn)
    - 最复杂的情况
        - 每次在选择基准值的时候，都不幸选择了子数组里的最大或最小值
- 空间复杂度（O(logn)）
    - 每次递归的过程只需要开辟O(1)的存储空间来完成交换操作实现直接对数组的修改
    - 递归次数为logn，所以整体的空间复杂度完全取决于压堆栈的次数
    
```java
void sort(int[] nums, int lo, int hi){
    if (lo > hi)
        return;
    int t = partition(nums, lo, hi);
    
    sort(nums, lo, t-1);
    sort(nums, t+1, hi);
}

int partition(int[] nums, int lo, int hi){
    int index = randRange(lo, hi);
    swap(nums, index, hi);
    
    for (int i=lo, j=lo; j<hi; j++){
        if (nums[j] <= nums[hi])
            swap(nums, i++, j);
    }
    
    swap(nums, i, hi);
    
    return i;
}
```
### 归并排序
**算法思想**
- 把数组从中间划分成两个子数组；
- 一直递归地把子数组划分成更小的子数组，直到子数组里面只有一个元素；
- 依次按照递归的返回顺序，不断地合并排好序的子数组，直到最后把整个数组的顺序排好

**复杂度分析**
- 时间复杂度
    - T(n) = 2*T(n/2) + O(n)
    - 对于规模为n的问题，一共要进行log(n)层的大小切分
    - 每一层的合并复杂度都是O(n)
    - 整体的复杂度就是O(nlogn)
- 空间复杂度（O(n)）

```java
void sort(int[] nums, int lo, int hi){
    int mid = lo + (hi - low)/2;
    sort(nums, lo, mid);
    sort(nums, mid+1, hi);
    
    merge(nums, lo, mid, hi);
}

void merge (int[] nums, int lo, int mid, int hi){
    int[] tmp = nums.clone();
    int k = lo; i = lo; j = mid+1;;
    
    while(i<=mid && j<=hi){
        if (copy[i] <= copy[j])
            nums[k++] = copy[i++];
        else
            nums[k++] = copy[j++];
    }
    while (i<=mid)
        nums[k++] = copy[i++];
    while (j<=hi)
        nums[k++] = copy[j++];
}
```
### 拓扑排序
- 应用场合
    - 将图论里的顶点按照相连的性质进行排序
    - 一般用来理清具有依赖关系的任务
- 前提
    - 必须有向图
    - 图里没有环

**复杂度分析**
- 时间复杂度（O(n)）
    - 统计顶点的入度需要O(n)的时间
    - 接下来每个顶点被遍历一次，同样需要O(n)的时间

典型例题
- [207. 课程表](https://leetcode-cn.com/problems/course-schedule/)
- [210. 课程表 II](https://leetcode-cn.com/problems/course-schedule-ii/)
- [269. 火星词典](https://leetcode-cn.com/problems/alien-dictionary/)

## 其他排序算法
### 堆排序
### 桶排序

# 递归和回溯

## 递归算法

- 基本性质：调用自身函数
    - 把大规模的问题不断地变小，再进行推导
- 算法思想
    - 要懂得如何将一个问题的规模变小
    - 再利用从小规模问题中得出的结果
    - 结合当前的值或者情况，得出最终的结果
- 通俗理解（自顶向下）
    - 把要实现的递归函数，看成已经实现好的
    - 直接利用解决一些子问题
    - 思考：如何根据子问题的解以及当前面对的情况得出答案
- 时间复杂度分析
    - 迭代法（`T(n) = a* T(n/b) + f(n)`）
    - 公式法（3种情况）

递归写法结构总结：

```java
function fn(n){
    //第一步：判断输入或者状态是否非法？
    if (input/state is invalid){
        return;
    }
    
    //第二步：判断递归是否应当结束？
    if (match condition){
        return some value;
    }
    
    //第三步：缩小问题规模
    result1 = fn(n1)
    result2 = fn(n2)
    ...
    
    //第四步：整合结果
    return combine(result1, result2)
}
```

典型例题：
- `easy`
- `medium`
    - [91. 解码方法](https://leetcode-cn.com/problems/decode-ways/)
    - [247. 中心对称数 II](https://leetcode-cn.com/problems/strobogrammatic-number-ii/)
- `hard`

## 回溯算法

- 与暴力搜索最大的区别
    - 一步一步向前试探，对每一步探测的情况评估，再决定是否继续，可避免走弯路
- 回溯算法的精髓
    - 出现非法的情况时，可退到之前的情景，可返回一步或多步
    - 再去尝试别的路径和办法
- 时间复杂度
    - 参考递归算法的计算

```java
function fn(n) {
    //第一步：判断输入或者状态是否非法？
    if (input/state is invalid){
        return;
    }
    
    //第二步：判断递归是否应当结束
    if (match condition){
        return some value;
    }
    
    //遍历所有可能出现的情况
    for (all possible cases){
        //第三步：尝试下一步的可能性
        solution.push(case)
        //递归
        result = fn(m)
        //第四步：回溯到上一步
        solution.pop(case)
    }
}
```

典型例题：
- `easy`
- `medium`
   - [22. 括号生成](https://leetcode-cn.com/problems/generate-parentheses/)
   - [39. 组合总和](https://leetcode-cn.com/problems/combination-sum/)
   - [46. 全排列](https://leetcode-cn.com/problems/permutations/)
   - [78. 子集](https://leetcode-cn.com/problems/subsets/)
- `hard`
   - [52. N皇后 II](https://leetcode-cn.com/problems/n-queens-ii/)
   - [10. 正则表达式匹配](https://leetcode-cn.com/problems/regular-expression-matching/)
   - [44. 通配符匹配](https://leetcode-cn.com/problems/wildcard-matching/)

# BFS/DFS
## DFS

- 算法思想
    - 从起点出发，选择一个可选方向不断向前，直到无法继续为止
    - 然后尝试另外一种方向，直到最后走到终点
- 应用
    - DFS解决的是连通性问题，即给定一个起始点和一个终点，判断是否有一条路径能从起点连接到终点
    - 很多情况下，连通的路径有很多条，只需要找出一条即可，DFS只关心路径存在与否，不在乎其长短
- 实现
    - 递归
        - 代码简洁
        - 递归的时候需要将当前程序中的变量以及状态压入到系统的栈里面
        - 压入和弹出栈都需要较多的时间，如果压入很深的栈，会造成运行效率低下
    - 非递归
        - 用栈来处理
- 借用的数据结构
    - 队列
- 复杂度分析（借用图论的知识）
    - 邻接表表示图（V个顶点，E条边）
        - 访问所有顶点的时间为O(V)
        - 查找所有顶点的邻居的时间为O(E)
        - 总的时间复杂度是O(V+E)
    - 邻接矩阵（V个顶点，E条边）
        - 查找每个顶点的邻居需要O(V)的时间
        - 查找整个矩阵需要O(V^2)的时间

## BFS

- 算法思想
    - 从起始点出发，一层一层地进行
    - 每层当中的点距离起始点的步数都是相同的
- 应用
    - 一般用来解决最短路径问题
    - 社交应用程序中两个人之间需要经过多少朋友介绍才能互相认识
- 借用的数据结构
    - 队列
- 双端BFS
    - 同时从起始点和终点开始进行的，广度优先的搜索称为双端BFS
    - 双端BFS可以大大地提高搜索的效率
- 复杂度分析（借用图论的知识）
    - 邻接表表示图（V个顶点，E条边）
        - 访问所有顶点的时间为O(V)
        - 查找所有顶点的邻居的时间为O(E)
        - 总的时间复杂度是O(V+E)
    - 邻接矩阵（V个顶点，E条边）
        - 查找每个顶点的邻居需要O(V)的时间
        - 查找整个矩阵需要O(V^2)的时间

典型例题：
- `easy`
- `medium`
   - [490. 迷宫](https://leetcode-cn.com/problems/the-maze/)
   - [505. 迷宫 II](https://leetcode-cn.com/problems/the-maze-ii/)
- `hard`
   - [499. 迷宫 III](https://leetcode-cn.com/problems/the-maze-iii/)

# 动态规划

- 定义
    - 一种数学优化的方法，同时也是编程的方法
- 基本属性
    - 最优子结构（Optimal Substructure）
    - 状态转移方程
    - 重叠子问题（Overlapping Sub-problems）
    
## 线性规划
- 特点
    - 各个子问题的规模以现行的方式分布
    - 子问题的最佳状态或结果可以存储在一维线性的数据结构中，例如一维数组，哈希表等
    - 通常我们会用dp[i]表示第i个位置的结果，或者从0开始到第i个位置为止的最佳状态或结果
- 基本形式
    - 当前所求的值仅仅依赖于有限个先前计算好的值，即dp[i]仅仅依赖于有限个dp[i],其中j<i
        - 典型题目
            - [62. 不同路径](https://leetcode-cn.com/problems/unique-paths/)
            - [70. 爬楼梯](https://leetcode-cn.com/problems/climbing-stairs/)
            - [198. 打家劫舍](https://leetcode-cn.com/problems/house-robber/)
    - 当前所求的值仅仅依赖于所有先前计算和的值，即dp[i]是各个dp[j]的某种组合，其中j由0遍历到i-1
        - 典型题目
            - [300. 最长上升子序列](https://leetcode-cn.com/problems/longest-increasing-subsequence/)

## 区间规划
- 特点
    - 各个子问题的规模由不同区间来定义
    - 子问题的最佳状态或结果可以存储在二维数组中
    - 这类问题的时间复杂度一般为多项式时间，即对于一个大小为n的问题，时间复杂度不会超过n的多项式倍数
- 典型题目
    - [516. 最长回文子序列](https://leetcode-cn.com/problems/longest-palindromic-subsequence/)
    - 0-1背包问题
## 约束规划
- 解题思想
    - 应当采用什么样的数据结构来曹村什么样的计算结果
- 巩固与加深：算法复杂度


# 二分搜索算法

- 特点
    - 看似简单，写对很难
    - 变形很多
    - 在面试中常用来考察code能力
- 定义
    - 二分搜索也称折半搜索，是一种在有序数组中查找某一特定元素的搜索算法
- 运用前提
    - 数组必须是排好序的
    - 输入并不一定是数组，也可能是给定一个区间的起始和终止的位置
- 优点
    - 时间复杂度为O(lgn)，是一种非常高效的搜索
- 缺点
    - 要求待查找的数组或区间是排好序的
    - 若要求对数组进行动态地删除和插入操作并完成查找，平均复杂度会变为O(n)
    - 采取自平衡的二叉查找树
        - 可在O(nlogn)的时间内用给定的数据构建出一颗二叉查找树
        - 可在O(logn)的时间内对数据进行搜索
        - 可在O(logn)的时间内完成删除和插入的操作
- 应用
    - 输入的数组或区间是有序的，且不会常变动，要求从中找出一个满足条件的元素
- 核心思想
    - 确定搜索的范围和区间
    - 取中间的数判断是否满足条件
    - 如果不满足条件，判定应该往哪个半边继续进行搜索
- 题目变形
    - 找确定的边界
        - 确定的边界，边界的数值等于要找的目标数
        - [34. 在排序数组中查找元素的第一个和最后一个位置](https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
    - 找模糊的边界
        - 模糊的边界，即边界的值不等于目标的值，而是大于或小于目标的值
        - [278. 第一个错误的版本](https://leetcode-cn.com/problems/first-bad-version/)
    - 不定长的边界
    - 旋转数组查找
        - [33. 搜索旋转排序数组](https://leetcode-cn.com/problems/search-in-rotated-sorted-array/)

典型例题：
- `easy`
    - [278. 第一个错误的版本](https://leetcode-cn.com/problems/first-bad-version/)
- `medium`
    - [33. 搜索旋转排序数组](https://leetcode-cn.com/problems/search-in-rotated-sorted-array/)
    - [34. 在排序数组中查找元素的第一个和最后一个位置](https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
- `hard`
    - [4. 寻找两个有序数组的中位数](https://leetcode-cn.com/problems/median-of-two-sorted-arrays/)

# 贪婪算法

- 特点
    - 是一种比较直观的算法
    - 难以证明它的正确性
- 定义
    - 贪婪是一种在每一步选中都采取在当前状态下最好或最优的选择，从而希望导致结果是最好或最优的算法
- 优点
    - 对于一些问题，贪婪算法非常直观有效
- 缺点
    - 往往，它得到的结果并不是正确的
    - 贪婪算法容易过早地做出决定，从而没有办法达到最优解
- 应用
    - 当局部最优策略能产生全局最优策略的时候，才能用贪婪算法

典型例题：
- `easy`
- `medium`
    - [253. 会议室 II](https://leetcode-cn.com/problems/meeting-rooms-ii/)
- `hard`




