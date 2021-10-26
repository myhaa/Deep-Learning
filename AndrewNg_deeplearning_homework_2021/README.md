# 吴恩达深度学习笔记

## 第7章-深度学习中的正则化

## 第8章-深度学习中的优化

## 第9章-卷积神经网络

### 卷积层

#### padding

* 为什么需要padding
  * 层数越多，输出的size越小
  * 图像边缘的大部分信息都丢失了，因为图像边缘的像素点较少被使用
* padding类型
  * valid padding：不需要padding n*n f*f  ->  (n+f-1) * (n+f-1)
  * same padding: 需要padding，保持输入输出size一致 n*n f*f  ->  (n+2p+f-1) * (n+2p+f-1)
* 为什么卷积核的size，即f总是奇数？
  * 如果是偶数，只能使用一些不对称padding，2p+f-1=0 -> p=(f-1)/2
  * 一个奇数filter，有一个中心点，会更方便于指出filter的位置