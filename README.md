# 《自动驾驶更新笔记 Autopilot Updating Notes》

![封面](./imgs/1.jpg)
### 重点
**由于作者水平有限，希望大家积极提交改进意见**, 您可对相关xxx.md进行修改,并将意见记录在modify_log.txt中。**我将对修改内容进行整理，确保文档的准确性**。

## 一、内容简介
随着各大科技公司积极布局，自动驾驶成为新的风口。本文旨在总结分享自动驾驶的技术方案，希望帮助大家对相关知识的学习了解。

## 二、自动驾驶分级（SAE 美国汽车工程协会）
![自动驾驶分级](./imgs/2.jpg)

## 三、架构
![架构](./imgs/3.jpg)
自动驾驶系统主要包含三部分：环境感知、决策规划以及运动控制。感知层对车辆周边环境进行感知识别，用于获取环境信息；决策层充当人类驾驶员的角色，主要解决三个核心问题：“我在哪？我要去哪？我该如何去？”；控制层保证各项硬件系统稳定的运行在计算好的最佳设定值上；保证各项子系统的运行维持在最优的区间范围；规避可能性风险，精准调控至最佳路径。


## 四、目录

**1.基础** \
|-- 1.1 知识铺垫 \
|---- [1.1.1 Frenet坐标系](./ch01_%E5%9F%BA%E7%A1%80/1.1%20%E7%9F%A5%E8%AF%86%E9%93%BA%E5%9E%AB/1.1.1%20Frenet%E5%9D%90%E6%A0%87%E7%B3%BB/readme.md) \
|---- [1.1.2 卡尔曼滤波-KalmanFilter](./ch01_%E5%9F%BA%E7%A1%80/1.1%20%E7%9F%A5%E8%AF%86%E9%93%BA%E5%9E%AB/1.1.2%20%E5%8D%A1%E5%B0%94%E6%9B%BC%E6%BB%A4%E6%B3%A2-KalmanFilter/readme.md) \
|---- [1.1.4 Transformer](./ch01_%E5%9F%BA%E7%A1%80/1.1%20%E7%9F%A5%E8%AF%86%E9%93%BA%E5%9E%AB/1.1.4%20Transformer/readme.md) \
|-- 1.2 数据集 \
|---- [1.2.1 Argoverse](./ch01_%E5%9F%BA%E7%A1%80/1.2%20%E6%95%B0%E6%8D%AE%E9%9B%86/1.2.1%20Argoverse.md) \
|-- [1.3 NLP自然语言处理](./ch01_%E5%9F%BA%E7%A1%80/1.3%20NLP%E8%87%AA%E7%84%B6%E8%AF%AD%E8%A8%80%E5%A4%84%E7%90%86/readme.md) \
|-- [1.4 强化学习](./ch01_%E5%9F%BA%E7%A1%80/1.4%20%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0/) \
[**2. 硬件**](./ch02_%E7%A1%AC%E4%BB%B6/README.md) \
|-- [2.1 传感器](./ch02_%E7%A1%AC%E4%BB%B6/2.1%20%E4%BC%A0%E6%84%9F%E5%99%A8/README.md) \
|---- [2.1.1 摄像头](./ch02_%E7%A1%AC%E4%BB%B6/2.1%20%E4%BC%A0%E6%84%9F%E5%99%A8/2.1.1%20%E6%91%84%E5%83%8F%E5%A4%B4.md) \
|---- [2.1.2 激光雷达](./ch02_%E7%A1%AC%E4%BB%B6/2.1%20%E4%BC%A0%E6%84%9F%E5%99%A8/2.1.2%20%E6%BF%80%E5%85%89%E9%9B%B7%E8%BE%BE.md) \
|---- [2.1.3 毫米波雷达](./ch02_%E7%A1%AC%E4%BB%B6/2.1%20%E4%BC%A0%E6%84%9F%E5%99%A8/2.1.3%20%E6%AF%AB%E7%B1%B3%E6%B3%A2%E9%9B%B7%E8%BE%BE.md) \
|---- [2.1.4 超声波雷达](./ch02_%E7%A1%AC%E4%BB%B6/2.1%20%E4%BC%A0%E6%84%9F%E5%99%A8/2.1.4%20%E8%B6%85%E5%A3%B0%E6%B3%A2%E9%9B%B7%E8%BE%BE.md) \
|---- [2.1.5 GPS定位导航](./ch02_%E7%A1%AC%E4%BB%B6/2.1%20%E4%BC%A0%E6%84%9F%E5%99%A8/2.1.5%20GPS%E5%AE%9A%E4%BD%8D%E5%AF%BC%E8%88%AA.md) \
|---- [2.1.6 IMU惯性传感器](./ch02_%E7%A1%AC%E4%BB%B6/2.1%20%E4%BC%A0%E6%84%9F%E5%99%A8/2.1.6%20IMU%E6%83%AF%E6%80%A7%E4%BC%A0%E6%84%9F%E5%99%A8.md) \
|-- [2.2 计算设备](./ch02_%E7%A1%AC%E4%BB%B6/2.2%20%E8%AE%A1%E7%AE%97%E5%8D%95%E5%85%83/README.md) \
|-- 2.3 辅助单元 \
|---- [2.3.1 V2X](./ch02_%E7%A1%AC%E4%BB%B6/2.3%20%E8%BE%85%E5%8A%A9%E5%8D%95%E5%85%83/2.3.1%20V2X.md) \
|---- [2.3.2 黑匣子](./ch02_%E7%A1%AC%E4%BB%B6/2.3%20%E8%BE%85%E5%8A%A9%E5%8D%95%E5%85%83/2.3.2%20%E9%BB%91%E5%8C%A3%E5%AD%90.md) \
**3. 感知** \
|-- 3.1 2D目标检测 \
|---- [3.1.1 车道线检测](./ch03_%E6%84%9F%E7%9F%A5/3.1%202D%20%E7%9B%AE%E6%A0%87%E6%A3%80%E6%B5%8B/3.1.1%20%E8%BD%A6%E9%81%93%E7%BA%BF%E6%A3%80%E6%B5%8B.md) \
|-- [3.2 3D目标检测](./ch03_%E6%84%9F%E7%9F%A5/3.2%203D%20%E7%9B%AE%E6%A0%87%E6%A3%80%E6%B5%8B/readme.md) \
|---- [3.2.1 基于LiDAR的3D目标检测](./ch03_%E6%84%9F%E7%9F%A5/3.2%203D%20%E7%9B%AE%E6%A0%87%E6%A3%80%E6%B5%8B/3.2.1%20%E5%9F%BA%E4%BA%8ELiDAR%E7%9A%843D%E7%9B%AE%E6%A0%87%E6%A3%80%E6%B5%8B/readme.md) \
|---- [3.2.2 基于摄像头的3D目标检测](./ch03_%E6%84%9F%E7%9F%A5/3.2%203D%20%E7%9B%AE%E6%A0%87%E6%A3%80%E6%B5%8B/3.2.2%20%E5%9F%BA%E4%BA%8E%E6%91%84%E5%83%8F%E5%A4%B4%E7%9A%843D%E7%9B%AE%E6%A0%87%E6%A3%80%E6%B5%8B/readme.md) \
|-- [3.3 BEV鸟瞰图](./ch03_%E6%84%9F%E7%9F%A5/3.3%20BEV%E9%B8%9F%E7%9E%B0%E5%9B%BE/README.md) \
|-- [3.4 定位](./ch03_%E6%84%9F%E7%9F%A5/3.4%20%E5%AE%9A%E4%BD%8D/readme.md) \
**4. 策略规划** \
|-- [4.1 预测](./ch04_%E7%AD%96%E7%95%A5%E8%A7%84%E5%88%92/4.1%20%E9%A2%84%E6%B5%8B/readme.md) \
|---- [4.1.1 基于车道序列的预测](./ch04_%E7%AD%96%E7%95%A5%E8%A7%84%E5%88%92/4.1%20%E9%A2%84%E6%B5%8B/4.1.1%20%E5%9F%BA%E4%BA%8E%E8%BD%A6%E9%81%93%E5%BA%8F%E5%88%97%E7%9A%84%E9%A2%84%E6%B5%8B.md) \
|-- [4.2 路线规划](./ch04_%E7%AD%96%E7%95%A5%E8%A7%84%E5%88%92/4.2%20%E8%B7%AF%E7%BA%BF%E8%A7%84%E5%88%92/README.md) \
|-- 4.3 轨迹规划 \
|---- [4.3.1 笛卡尔坐标下的规划](./ch04_%E7%AD%96%E7%95%A5%E8%A7%84%E5%88%92/4.3%20%E8%BD%A8%E8%BF%B9%E8%A7%84%E5%88%92/4.3.1%20%E7%AC%9B%E5%8D%A1%E5%B0%94%E5%9D%90%E6%A0%87%E4%B8%8B%E7%9A%84%E8%A7%84%E5%88%92.md) \
|---- 4.3.2 Lattice规划 \
**5. 控制** \
|-- 5.1 PID控制 \
|-- 5.2 线性二次调节器（LQR）\
|-- 5.3 模型控制预测（MPC）\
**6. 产品** \
|-- [6.1 ADAS](./ch06_产品/6.1%20ADAS/README.md) \
**7. 工具** \
|-- 7.1 可视化 \
|---- [7.1.1 AVS（Autonomous Visualization System）](./ch07_%E5%B7%A5%E5%85%B7/7.1%20%E5%8F%AF%E8%A7%86%E5%8C%96/7.1.1%20AVS%EF%BC%88Autonomous%20Visualization%20System%EF%BC%89/readme.md) \
|-- 7.2 仿真 \
|---- [7.2.1 Carla仿真](./ch07_%E5%B7%A5%E5%85%B7/7.2%20%E4%BB%BF%E7%9C%9F/7.2.1%20Carla%E4%BB%BF%E7%9C%9F/readme.md) \
|-- [7.3 TensorRT 加速](./ch07_%E5%B7%A5%E5%85%B7/7.3%20TensorRT%E5%8A%A0%E9%80%9F/readme.md) \
|---- [7.3.1 TensorRT安装配置](./ch07_%E5%B7%A5%E5%85%B7/7.3%20TensorRT%E5%8A%A0%E9%80%9F/7.3.1%20TensorRT%E5%AE%89%E8%A3%85%E9%85%8D%E7%BD%AE.md) \
|---- [7.3.2 TensorRT加速原理](./ch07_%E5%B7%A5%E5%85%B7/7.3%20TensorRT%E5%8A%A0%E9%80%9F/7.3.2%20TensorRT%E5%8A%A0%E9%80%9F%E5%8E%9F%E7%90%86.md) \
|---- [7.3.3 TensorRT源码分析](./ch07_%E5%B7%A5%E5%85%B7/7.3%20TensorRT%E5%8A%A0%E9%80%9F/7.3.3%20TensorRT%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.md) \
|-- 7.4 SNPE 加速 \
**8. 厂商方案** \
|-- [8.1 特斯拉 AI Day2022](./ch08_%E5%8E%82%E5%95%86%E6%96%B9%E6%A1%88/8.1%20%E7%89%B9%E6%96%AF%E6%8B%89%20AI%20Day2022/README.md) \
|---- [8.1.1 路径以及运动规划算法](./ch08_%E5%8E%82%E5%95%86%E6%96%B9%E6%A1%88/8.1%20%E7%89%B9%E6%96%AF%E6%8B%89%20AI%20Day2022/8.1.1%20%E8%B7%AF%E5%BE%84%E4%BB%A5%E5%8F%8A%E8%BF%90%E5%8A%A8%E8%A7%84%E5%88%92%E7%AE%97%E6%B3%95.md) \
|---- [8.1.2 环境感知算法](./ch08_%E5%8E%82%E5%95%86%E6%96%B9%E6%A1%88/8.1%20%E7%89%B9%E6%96%AF%E6%8B%89%20AI%20Day2022/8.1.2%20%E7%8E%AF%E5%A2%83%E6%84%9F%E7%9F%A5%E7%AE%97%E6%B3%95.md) \
|---- [8.1.3 训练算法、设施、软件](./ch08_%E5%8E%82%E5%95%86%E6%96%B9%E6%A1%88/8.1%20%E7%89%B9%E6%96%AF%E6%8B%89%20AI%20Day2022/8.1.3%20%E8%AE%AD%E7%BB%83%E7%AE%97%E6%B3%95%E3%80%81%E8%AE%BE%E6%96%BD%E3%80%81%E8%BD%AF%E4%BB%B6.md) \
|---- [8.1.4 数据标注、采集、虚拟化](./ch08_%E5%8E%82%E5%95%86%E6%96%B9%E6%A1%88/8.1%20%E7%89%B9%E6%96%AF%E6%8B%89%20AI%20Day2022/8.1.4%20%E6%95%B0%E6%8D%AE%E6%A0%87%E6%B3%A8%E3%80%81%E9%87%87%E9%9B%86%E3%80%81%E8%99%9A%E6%8B%9F%E5%8C%96.md)


