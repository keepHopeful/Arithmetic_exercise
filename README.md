# Arithmetic
There are some important arithmetic which i've learned.
算法原理：

（1）基本查找：使用数组遍历，从而查找到目标元素

（2）二分查找：首先假定数组为严格递增的整数数组，如：1，2，3，4，5，6，7，8，9，10
         首先定义索引min，索引max，以及索引mid，对于数组，初始值min=0，max=arr.length-1，mid=(min+max)/2
         将目标元素值与索引为mid的元素作比较（以下简称mid值），若相等则退出循环，如果mid值偏大，则max值变成mid-1，
         如果mid值较小，则min值变成mid+1，以此为循环。
         当min>max时，循环结束，并代表该数组中并没有目标元素。


（3）插值查找：
         原理与二分查找法相似，唯一不同的是对mid的改变，二分查找中每一次max或min值发生变化后对新的min值的获取
         都是通过对min和max取中间值获取的。此处获取mid值时是mid=min+(num-arr[min])/(arr[max]-arr[min])*(max-min)
         注意：该算法只是当各元素分布较为均匀的时候才更能降低复杂度，然而当元素彼此间差距过大时反而会导致复杂度增加

（4）斐波拉契查找：
         与二分查找法原理相同，不同的是mid取值是利用了黄金分割率（0.618），mid=min+黄金分割点左半边长度-1


（5）分块查找：对于一串数据：{16,5,9,12,21,18,
                           32,23,37,26,45,34,
                           50,48,61,52,73,66}      //一般分成的块数在n开根块
          //这一串数据有一个特点：可以被分成若干块，而这若干块之间满足：上一块中的最大值小于下一块中的所有值
          对于这类数据，我们可以利用分块查找法查找目标元素：首先判断目标元素位于哪一块中，再利用遍历查找到目标元素


（6）哈希查找：对于一串数据：{27，22，30，40，36，
                           13，19，16，20，
                           7，10，
                           43，50，48}      
          //这串数据有一个特点：能够分成若干块，而对这若干块而言，各自内部元素的取值范围并没有交集
          对这种数据在分组后可以利用哈希查找查找目标元素：首先判断目标元素位于哪一块中，再利用遍历查找到目标元素


（7）数表查找：如题设要求：现在要求生成100个1-1000的随机数，将这100个数存储到数组中，要求每次完成并存储的随机数都不重复
          实现：那么在每次生成随机数的时候都需要去检查已生成的数，完成遍历，如果不存在，再存储，否则不存储
          利用数表查找的原理：我们可以将这些随机数的范围分为几大块：1-100，101-200，201-300，301-400，401-500，501-600，
          .....901-1000；对于首次生成的数就将其放到对应范围的块中，当再一次生成随机数是，如果他所属的模块中已经有数了，那么
          就先遍历验证该数是否已经存在，若不存在就将该数存储，若已经存在那么就重新生成随机数知道满足100个数


（8）选择排序： 以从小到达排序为例
          对每一个索引的元素依次与其后方所有的元素依次作比较，若前者大那么交换二者
          每一轮外层循环都能将一个最小的数确定在数组最左侧
          即：遍历交换，每一层外部循环就将一个最小值放到最左侧


（9）冒泡排序：按从小到大排序为例
          将前一个元素与后一个元素作比较，若后一个更小则交换两个的位置
          每一次遍历可以将一个最大的元素移动到数组末尾
          如此遍历一个循环即可
          即：相邻交换，每一层外部循环都会把一个最大数放到最右侧

（10）全排列思想：
         目标：将1，2，3，4，5，6，这六个数进行全排列，结果：包含这六个整数不重复构成的全部整数
         方法：利用递归思想，将1-6这六个数依次放置在首位，再对余下的五个数进行全排列，递归的出口是递归的首项与最后一项指向同
         一个数时，结束递归调用。

          
















                           
