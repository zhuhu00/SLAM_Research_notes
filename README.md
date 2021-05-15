> 首次更新于20210404，清明节的日子，开启这方面的学习跟踪，
> 工作有来自于[Recent_SLAM_Research](https://github.com/YiChenCityU/Recent_SLAM_Research)，[Visual_SLAM_Related_Research](https://github.com/wuxiaolang/Visual_SLAM_Related_Research)

# SLAM_Research

@Author:  
@E-mail:  huzhu00@gmail.com
@Github:  [zhuhu00](https://github.com/zhuhu00)

## 摘要

​		整理前期主要以**视觉SLAM**为主，包含论文，代码，相关讲解（如果有的话），大概整理几个月会把**激光SLAM**也加上
​		目前收集的资料主要是一个大杂烩，研究的主要内容会从**多传感器融合以及TOF相机相关**去调整。将会从经典的框架开始，之后如果有时间的话，也会在这个仓库中添加文件夹写相关的基础。不一定能涵盖所有，请合理参考。

1. 开源经典框架：经典、应用广泛的**开源框架**
2. 优秀的作者和实验室：前期为**大杂烩**，后面则为**主要关注的团队和个人**
3. **SLAM的学习资料**：从基础的书籍到视频，数据集，公众号，代码注释等、
4. 近期的论文：整理到的好论文，大概每月一次更新，前期会更新比较快。有关论文的笔记也许~~不会~~放出来了。

**Attention：如果内容出现错误，请一定提出批评和建议，我一定及时修改。**
于2021年4月正式启动（私密）。

>一些好的工作
>
>目前没有，哈哈哈哈

## 目录

1. 经典代码框架
2. 优秀作者及实验室
3. 论文更新



## 1. 经典代码框架

这部分主要工作来自于[Visual_SLAM_Related_Research](https://github.com/wuxiaolang/Visual_SLAM_Related_Research)，目前自己正在学习和重新整理。将会在他的基础上进行整理和汇总学习。

### 1.1 Geometric SLAM



## 2. 优秀作者及实验室

这部分内容一开始也是借鉴[Visual_SLAM_Related_Research](https://github.com/wuxiaolang/Visual_SLAM_Related_Research)，之后会重新整理和学习。



## 3. 论文更新

除了更新最近的，还将更新之前的，具体是啥还得待定。。

### 2021年5月论文更新

> 将于6月15日更新

### 2021年4月论文更新

> 此次更新21篇论文

- [ ] [0] Fond, Antoine et al. “[End-to-end learning of keypoint detection and matching for relative pose estimation](End-to-end learning of keypoint detection and matching for relative pose estimation).” (2021).
  - 相对位置估计的**关键点检测和匹配**的**端到端学习**
  - arxiv上, 暂时无代码

- [ ] [1]D. Geromichalos, M. Azkarate, E. Tsardoulias, L. Gerdes, L. Petrou, and C. P. D. Pulgar, “SLAM for autonomous planetary rovers with global localization,” Journal of Field Robotics, vol. 37, no. 5, pp. 830–847, 2020, doi: 10/ggrq3v.

  - 适用于全局定位的自主行星漫游车的SLAM
  - 使用粒子滤波器和扫描匹配，研究目的是为了支持远距离、低监督行星探索。
  - 火星车等的SLAM，地图的可通过性

- [ ] [2]M. Azkarate, L. Gerdes, L. Joudrier, and C. J. Pérez-del-Pulgar, “A GNC Architecture for Planetary Rovers with Autonomous Navigation,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 3003–3009. doi: 10/gjxsmn.

  - 针对火星车的GNC（Guidance，Navigation，Control）设计的一种系统，
  - 欧洲宇航局

- [ ] [3]Y. Zhao and P. A. Vela, “Good Feature Selection for Least Squares Pose Optimization in VO/VSLAM,” in 2018 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), Oct. 2018, pp. 1183–1189. doi: 10/ghs5cg.

  - 对特征选择的策略，使用对位姿估计最有帮助的特征。还提出另一种解决NP-hard Max-logDet的算法
  - 佐治亚理工学院[Yipuzhao](https://sites.google.com/site/zhaoyipu/)，作者有很多关于“Good”的文章

- [ ] [4]A. J. Ben Ali, Z. S. Hashemifar, and K. Dantu, “Edge-SLAM: edge-assisted visual simultaneous localization and mapping,” in Proceedings of the 18th International Conference on Mobile Systems, Applications, and Services, New York, NY, USA, Jun. 2020, pp. 325–337. doi: 10/ghdxk5.

  - 边缘辅助的VSLAM，将系统进行分离，能够将一部分进程分析到其他设备中运行。
  - [开源](http://droneslab.github.io/edgeslam)
  - 纽约布法罗大学

- [ ] [5]Z. Hashemifar and K. Dantu, “Practical Persistence Reasoning in Visual SLAM,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), Paris, France, May 2020, pp. 7307–7313. doi: 10/gjww5h.

  - 视觉SLAM中实用且持续的推理

- [ ] [6]R. F. Salas-Moreno, R. A. Newcombe, H. Strasdat, P. H. J. Kelly, and A. J. Davison, “SLAM++: Simultaneous Localisation and Mapping at the Level of Objects,” in 2013 IEEE Conference on Computer Vision and Pattern Recognition, Portland, OR, USA, Jun. 2013, pp. 1352–1359. doi: 10/ggmwnd.

  - 基于对象级的SLAM
  - 在建图过程中将3维物体重建出来

- [ ] [7]Y. Zhao, J. S. Smith, S. H. Karumanchi, and P. A. Vela, “Closed-Loop Benchmarking of Stereo Visual-Inertial SLAM Systems: Understanding the Impact of Drift and Latency on Tracking Accuracy,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 1105–1112. doi: 10/gjv95x.

  - 针对视觉估计在闭环中的延迟和漂移做了个可以评估的方式，

  - 开源地址：https://github.com/ivalab/meta_ClosedLoopBench
  - Yipu Zhao. 

- [ ] [8]Y. Fan, R. Wang, and Y. Mao, “Stereo Visual Inertial Odometry with Online Baseline Calibration,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 1084–1090. doi: 10/gjn63d.

  - 一种针对双目相机的在线标定视觉惯性里程计
  - 美团-点评Group

- [ ] [9]P. Gao and H. Zhang, “Long-term Place Recognition through Worst-case Graph Matching to Integrate Landmark Appearances and Spatial Relationships,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 1070–1076. doi: 10/gjv2qx.

  - 位置识别，用于同一个场景中的地标会发生变化等的情况，

- [ ] [10]M. Henein, J. Zhang, R. Mahony, and V. Ila, “Dynamic SLAM: The Need For Speed,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 2123–2129. doi: 10/gjv2md.

  - Dynamic SLAM：对速度的需求，对场景中运动的物体进行实时速度预测
  - 澳大利亚国立大学

- [ ] [11]K. Wang, K. Wang, and S. Shen, “FlowNorm: A Learning-based Method for Increasing Convergence Range of Direct Alignment,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), Paris, France, May 2020, pp. 2109–2115. doi: 10/gjv2j2.

  - 港科

- [ ] [12]B. Li, D. Zou, D. Sartori, L. Pei, and W. Yu, “TextSLAM: Visual SLAM with Planar Text Features,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 2102–2108. doi: 10/gjv2jf.

  - TextSLAM: 具有平面文本特征的VSLAM
  - 上交导航定位实验室
  - 识别环境中的文字信息的SLAM系统，是否算语义呢？（未开源）使用文字的平面信息

- [ ] [13]H. Wang, C. Wang, and L. Xie, “Intensity Scan Context: Coding Intensity and Geometry Relations for Loop Closure Detection,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 2095–2101. doi: 10/gjn69q.

  - Intensity Scan Context: 用于回环检测的编码强度和几何关系，使用激光的强度投影，进行回环的检测
  - 南洋理工大学，RI in CMU

- [ ] [14]C. Schulz and A. Zell, “Real-Time Graph-Based SLAM with Occupancy Normal Distributions Transforms,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 3106–3111. doi: 10/gjn65h.

  - 具有正态分布变换的实时图SLAM。根据正态分布变化改进了Cartographer，设计了一个新的回环系统。

  - 德国杜宾根大学

- [ ] [15]R. Nakashima and A. Seki, “Uncertainty-Based Adaptive Sensor Fusion for Visual-Inertial Odometry under Various Motion Characteristics,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 3119–3125. doi: 10/gjn6z5.

  - 不同运动特性下基于不确定度的视觉惯性里程计自适应传感器融合，自适应的使用状态的不确定性
  - 日本东芝

- [ ] [16]J. Lin and F. Zhang, “Loam livox: A fast, robust, high-precision LiDAR odometry and mapping package for LiDARs of small FoV,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 3126–3131. doi: 10/gjv2hr.

  - Loam_livox: 将loam集成到livox激光雷达中
  - 港大MARS实验室，专门做livox相关的。
  - 开源

- [ ] [17]S. Zhao, H. Zhang, P. Wang, L. Nogueira, and S. Scherer, “Super Odometry: IMU-centric LiDAR-Visual-Inertial Estimator for Challenging Environments,” arXiv:2104.14938 [cs], Apr. 2021, Accessed: May 04, 2021. [Online]. Available: http://arxiv.org/abs/2104.14938

  - Super Odometry：以IMU为中心的LiDAR视觉惯性估计器，可用于具有挑战性的环境，弱光，浓雾等
  - DARPA挑战赛的一部分工作
  - CMU，东北大学

- [ ] [18]P. Yin et al., “Stabilize an Unsupervised Feature Learning for LiDAR-based Place Recognition,” in 2018 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), Oct. 2018, pp. 1162–1167. doi: 10/gjn63m.

  - 稳定的无监督特征学习在激光位置识别中的应用
  - CMU，沈阳自动化所

- [ ] [19]P. Yin, L. Xu, J. Zhang, and H. Choset, “FusionVLAD: A Multi-View Deep Fusion Networks for Viewpoint-Free 3D Place Recognition,” IEEE Robotics and Automation Letters, vol. 6, no. 2, pp. 2304–2310, Apr. 2021, doi: 10/gjn7bs.

  - FusionVLAD：用于无视点3d位置的多视图深度融合网络

- [ ] [20]C. Won, H. Seok, Z. Cui, M. Pollefeys, and J. Lim, “OmniSLAM: Omnidirectional Localization and Dense Mapping for Wide-baseline Multi-camera Systems,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 559–566. doi: 10/gh5kp8.

  - OmniSLAM：宽基线多相机系统的全向定位和密集映射





