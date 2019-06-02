# Meanshift图像分割 项目分工文档





一、项目简述

​	实现Meanshift的图像分割算法的GPU版本，完成测试、性能计算、调优。

二、项目主要参考资料

​	1、拟参照github上的这份使用C++写完的CPU版本的代码<https://github.com/bbbbyang/Mean-Shift-Segmentation>

​	2.这篇论文<https://courses.csail.mit.edu/6.869/handouts/PAMIMeanshift.pdf>



三、实现的初步构想（实现的架构按照github上的CPU版本的架构）

​	1. main.cpp :

​	main.cpp完成整个项目的架构、以及性能计算。

​	main.cpp包括 确定Filtering和Segmentation的参数（静态指定），图像的打开、颜色空间的转换。

​	

​	2.MeanShift.cpp 这个.cpp主要有两个函数 

​		`1.MeanShift::MSFiltering(Mat& Img)`

​		`2.MeanShift::MSSegmentation(Mat& Img)`



​	3.Meanshift.h这个文件实现一个Meanshift的类，这个类提供了上面提到的MSFiltering和MSSegmentation这两个接口，以及hs,hr这两个参数。



四、代码分工

​	1.两个人实MSFiltering这个函数以及调优方法.( A、B )

​	2.两个人实现MSSegmentation这个函数以及调优方法（C、D）

​	3.一个人实现main函数、以及架构。（F）

​	4.性能测试 （F）

​	

五、书面报告的撰写

​	1.Introduction部分 A

​	2.算法介绍部分 由对应实现者撰写

​	3.优化方法以及优化结果 由相应实现者撰写

​	4.报告审查	B



六、课堂展示的分工

​	1.Introduction与算法概要 A

​	2.Filtering 以及优化方法 B

​	3.Segmentation以及优化方法 C或者D



五、任务的timeline

​	1.F同学拟在第一周周四之前完成架构编写。

​	2.完成Filtering与Segmentation的同学拟在第二周之前完成基础版本。

​	3.第二周周五之前拟完成Filtering与Segmentation的优化版本。





六、合作方法

​	讨论使用git还是通过qq文件合作。