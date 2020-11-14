# ChemInk

## 功能

* 处理手写化学方程式，仅包含字符，不具备结构式处理能力

## 原理简述

1. 用 yolov3-tiny 目标检测模型做字符切割，在很小的程度上支持连笔

2. 用 densenet 结构的卷积网络对检测框中的字符进行二次分类

3. 用字典按位加权的方法从语言层面进一步筛选合理结果

4. 用判断无根树同构的方法生成饱和烷烃的所有非光学同分异构体

5. 使用位压缩，实现在 16GB 内存的家用 PC 上获取 6 亿多个 28 碳烷烃的异构体

6. 用化合价表设计了相对完备的方程式配平方法

7. 用旋转基本图元的方法进行简单的球棍模型渲染

8. 由 opencv 推理目标检测网络、fdeep 推理单字符卷积网络，由 glu 提供三维基本图元

## 阶段性完结【演示】

![结果演示](./docs/final-term/结题考核演示.gif)

## 链接

[目标检测实现的结构式识别（半成品）](https://github.com/Xuguodong1999/COCR)

## 路线图 2021：接入 COCR-dev 分支

1. 共享 libtorch 的 crnn 和 yolo 模型
2. 替换掉 chemink 目录下的代码
3. 用 qt3d 去掉 glu 依赖
