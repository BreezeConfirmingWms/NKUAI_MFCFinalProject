# NKUAI-MFC智能系统设计与仿真设计结课作业



**时间:2023-6-4 ，课程：大三**



## 项目介绍



​	本项目是南开大学人工智能学院选修课23年春季开设的智能系统设计选修课，最终的大作业设计为使用MFC，**编写可以设置PID参数和输入为阶跃响应(幅值)和正弦脉冲(幅值，基线，相频)，关于弹簧重物系统的控制可视化软件**，安排时间为两周，整体难度不大，知识点都是课堂内传授内容，也没有在文档类以上实现更偏底层的一些可视化交互。

​	考虑到本人使用大概两个晚上完成了大作业，但是其余同学基本都做了一周左右且最后的效果还不是很理想(主要集中在对于设备坐标系的相对参考变换和图像不协调的问题上），最后本项目评分98，再加上github和gitee上没有往届资料参考，特此开源。

:smile:    :desktop_computer:



## 项目结构

* 自定义了CDlgSetArg类为非模态对话框，可以设置参数，ui如下:

  <img src="https://raw.githubusercontent.com/BreezeConfirmingWms/NKUAI_MFCFinalProject/main/images/image-20230608115523226.png" alt="image-20230608115523226" style="zoom:50%;" />

* 在View中自定义了求解器PIDSolver，使用龙格库塔法求解二阶的线性常微分方程，默认情况下pid 0.1s计算一次，而RK方法计算的精度为十分位，也即0.01s计算一次。

###  运行结果

​		![image-20230608120128630](https://raw.githubusercontent.com/BreezeConfirmingWms/NKUAI_MFCFinalProject/main/images/image-20230608120128630.png)





<img src="https://raw.githubusercontent.com/BreezeConfirmingWms/NKUAI_MFCFinalProject/main/images/image-20230608120229172.png" alt="image-20230608120229172" style="zoom:50%;" />

<img src="https://raw.githubusercontent.com/BreezeConfirmingWms/NKUAI_MFCFinalProject/main/images/image-20230608120324030.png" alt="image-20230608120324030" style="zoom:67%;" />

##  代码补充



(TODO...)