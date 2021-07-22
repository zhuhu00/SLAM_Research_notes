> 首次更新于20210404，清明节的日子，开启这方面的学习跟踪，
> 工作有来自于[Recent_SLAM_Research](https://github.com/YiChenCityU/Recent_SLAM_Research)，[Visual_SLAM_Related_Research](https://github.com/wuxiaolang/Visual_SLAM_Related_Research)

# SLAM_Research

@Author:  zhuhu
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



## 1. 经典代码框架及实验室

见[SLAM-approachs](https://github.com/zhuhu00/SLAM_Research_dzh/tree/main/SLAM-approachs)

## 2. 论文更新

除了更新最近的，还将更新之前的，具体是啥还得待定。。

### 2021年6月论文更新

> 将于7.15更新

- [x] [0]A. Jelinek, A. Ligocki, and L. Zalud, “**Robotic Template Library,**” *arXiv:2107.00324 [cs]*, Jul. 2021, Accessed: Jul. 03, 2021. [Online]. Available: http://arxiv.org/abs/2107.00324
  - 一种新的机器人的库，可能之后会和PCL等作为竞争品。
  - 开源：https://github.com/Robotics-BUT/Robotic-Template-Library

#### VT&R方面的论文更新

- [ ] [1]P. Furgale and T. Barfoot, “Stereo mapping and localization for long-range path following on rough terrain,” in *2010 IEEE International Conference on Robotics and Automation*, Anchorage, AK, May 2010, pp. 4410–4416. doi: [10.1109/ROBOT.2010.5509133](https://doi.org/10.1109/ROBOT.2010.5509133).

  [2]P. Furgale and T. Barfoot, “Visual path following on a manifold in unstructured three-dimensional terrain,” in *2010 IEEE International Conference on Robotics and Automation*, May 2010, pp. 534–539. doi: [10.1109/ROBOT.2010.5509140](https://doi.org/10.1109/ROBOT.2010.5509140).

  [3]P. Furgale and T. D. Barfoot, “Visual teach and repeat for long-range rover autonomy: Furgale & Barfoot: Visual Teach and Repeat for Long-Range Rover Autonomy,” *J. Field Robotics*, vol. 27, no. 5, pp. 534–560, Sep. 2010, doi: [10.1002/rob.20342](https://doi.org/10.1002/rob.20342).

  - VT&R的最开始的文章，使用双目相机作为传感器进行long-range的导航问题。
  - 加拿大宇航局，[数据集](http://asrl.utias.utoronto.ca/~ptf/JFR_VTnR/)

- [x] [4]L. Sun *et al.*, “**Robust and Long-term Monocular Teach and Repeat Navigation using a Single-experience Map**,” *2021 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)*, p. 9.

  - 深度Descriptor
  - 开源

- [ ] [5]M. Mattamala, M. Ramezani, M. Camurri, and M. Fallon, “**Learning Camera Performance Models for Active Multi-Camera Visual Teach and Repeat,**” *arXiv:2103.14070 [cs]*, Mar. 2021, Accessed: Jul. 07, 2021. [Online]. Available: http://arxiv.org/abs/2103.14070

  - 

### 2021年5月论文更新

> 此次更新了17篇论文

- [x] [1]J. Delmerico and D. Scaramuzza, “**[A Benchmark Comparison of Monocular Visual-Inertial Odometry Algorithms for Flying Robots](https://doi.org/10/gf74jx)**,” in *2018 IEEE International Conference on Robotics and Automation (ICRA)*, May 2018, pp. 2502–2509. doi: [10/gf74jx](https://doi.org/10/gf74jx).
  - 针对无人机上的power，计算能力，成本问题等，选择了camera和IMU进行状态估计，而没有外界的定位信息。比较累VIO的：[MSCKF](https://github.com/daniilidis-group/msckf_mono)，[OKVIS](https://github.com/ethz-asl/okvis_ros)，[ROVIO](https://github.com/ethz-asl/rovio)，[VINS-Mono](https://github.com/HKUST-Aerial-Robotics/VINS-Mono)，[SVO](http://rpg.ifi.uzh.ch/svo2.html)+[MSF](https://github.com/ethz-asl/ethzasl_msf)，[SVO](http://rpg.ifi.uzh.ch/svo2.html)+[GTSAM](https://bitbucket.org/gtborg/gtsam/)，最终在EuRoC数据集上考虑了位姿估计精度，每帧处理时长，CPU和内存的使用。同时也在4种平台上分别进行了测试。
  - ETH和UZH
- [x] [2]B. Huang, J. Zhao, and J. Liu, “[A Survey of Simultaneous Localization and Mapping with an Envision in 6G Wireless Networks](http://arxiv.org/abs/1909.05214),” *arXiv:1909.05214 [cs]*, Feb. 2020, Accessed: Jun. 15, 2021. [Online]. Available: http://arxiv.org/abs/1909.05214
  - 针对visual和lidar的slam系统进行了综述，介绍了很多个slam系统的特点。VIO，语义，多传感器融合，深度学习在slam中的一些论文，以及水下slam，Camera和IMU标定的算法等。
  - 黄百川，去深圳当计算机竞赛老师
- [x] [3]R. Milijas, L. Markovic, A. Ivanovic, F. Petric, and S. Bogdan, “[A comparison of LiDAR-based SLAM systems for Control of Unmanned Aerial Vehicles](http://arxiv.org/abs/2011.02306),” *arXiv:2011.02306 [cs]*, Mar. 2021, Accessed: Jun. 17, 2021. [Online]. Available: http://arxiv.org/abs/2011.02306
  - 使用激光SLAM对无人机的姿态进行估计，实现反馈控制。对比了loam，HDL graph slam，Cartographer三种算法。在阶跃响应，螺旋轨迹等上面进行了反馈控制和比较。文章将激光SLAM的输出作为无人机的pose sensor，结合IMU，通过DKF（Discrete Kalman Filter）进行预测和控制。
  - 未开源
- [ ] [4]X. Zuo, N. Merrill, W. Li, Y. Liu, M. Pollefeys, and G. Huang, “[CodeVIO: Visual-Inertial Odometry with Learned Optimizable Dense Depth](http://arxiv.org/abs/2012.10133),” Dec. 2020. Accessed: Jun. 05, 2021. [Online]. Available: http://arxiv.org/abs/2012.10133
  - 设计了一种带有实时稠密重建的VIO系统，提出了一种新颖的CVAE神经网络用来**估计深度**并对深度进行编码，充分利用了VIO稀疏深度图的信息，并且拥有很强的泛化能力。
  - 没读懂。。。以后有机会再看看。ICRA2021 best student paper的候选之一。
  - 左星星，浙大，ETH，Guoquan Huang的RPNG组，好像未开源
- [x] [5]X. Gu, W. Yuan, Z. Dai, C. Tang, S. Zhu, and P. Tan, “DRO: Deep Recurrent Optimizer for Structure-from-Motion,” *arXiv:2103.13201 [cs]*, May 2021, Accessed: Jun. 11, 2021. [Online]. Available: http://arxiv.org/abs/2103.13201
  - 提出**zero-order**的循环神经网络优化器（DRO）, 不需要求解梯度, 直接利用神经网络来预测下次更新的方向和步长。**将优化目标cost，放入到神经网络中**，每次迭代都会参考之前尝试的**历史信息**，从而给出更加精准的预测。
  - 阿里云实验室，谭平教授，[开源](https://github.com/aliyun/dro-sfm)，
- [x] [6]K. D. Katyal, A. Polevoy, J. Moore, C. Knuth, and K. M. Popek, “[High-Speed Robot Navigation using Predicted Occupancy Maps](https://arxiv.org/abs/2012.12142),” *arXiv:2012.12142v1[cs.RO]*, p. 7.
  - 一种使用栅格地图的导航算法，由于计算瓶颈和小的FOV，并且使用了GNN从现实世界中训练了一个模型，预测出栅格地图，拓展了控制算法，使汽车在未知区域内的高速规划和导航。其在实验中使用了**D435i和T265作为其的传感器**，然后建出来栅格地图。
  - ICRA2021，约翰霍普金斯大学。
- [ ] [7]R. Voges and B. Wagner, “Interval-Based Visual-LiDAR Sensor Fusion,” *IEEE Robotics and Automation Letters*, vol. 6, no. 2, pp. 1304–1311, Apr. 2021, doi: [10/gkdw6q](https://doi.org/10/gkdw6q).
  - 多传感器融合的方法，主要针对视觉和激光的融合。在视觉特征以点作为信息时，与激光的深度信息的不确定性是未知的，并且这种不确定性无法测量，另一个是针对坐标系的标定等出现的误差。解决方法是将视觉和激光的信息进行分区（块）处理，使得误差限定在一个区间内。使用融合后的信息进行了航位推算。保证了机器人的真实姿态。（略读）之后实现了一个里程计。
- [ ] [8]K. Eckenhoff, P. Geneva, and G. Huang, “MIMC-VINS: A Versatile and Resilient Multi-IMU Multi-Camera Visual-Inertial Navigation System,” *IEEE Transactions on Robotics*, pp. 1–21, 2021, doi: [10/gkdxp9](https://doi.org/10/gkdxp9).
  - 多IMU和多相机的**VINS**系统。
  - **黄国权教授**
- [x] [9]M. Müller and V. Koltun, “OpenBot: Turning Smartphones into Robots,” *arXiv:2008.10631 [cs]*, Mar. 2021, Accessed: Jun. 12, 2021. [Online]. Available: http://arxiv.org/abs/2008.10631
  - 使用手机作为计算平台的低成本小车，可实现跟随，识别，导航等功能。确实是便宜
  - 开源，复现ing，做一个出来玩玩
- [ ] [10]B. Forkel, J. Kallwies, and H.-J. Wuensche, “**Probabilistic Terrain Estimation for Autonomous Off-Road Driving**,” p. 7.
  - 建高程图进行导航，将障碍物分离出来
- [ ] [11]Z. Li *et al.*, “**Revisiting Stereo Depth Estimation From a Sequence-to-Sequence Perspective with Transformers**,” *arXiv:2011.02910 [cs]*, Mar. 2021, Accessed: May 25, 2021. [Online]. Available: http://arxiv.org/abs/2011.02910
  - 利用transformers从seq2seq中进行双目深度估计
  - [开源](https://github.com/mli0603/stereo-transformer)
- [ ] [12]M. Labbé and F. Michaud, “[**RTAB-Map as an open-source lidar and visual simultaneous localization and mapping library for large-scale and long-term online operation**](https://doi.org/10/gf3bgd),” *Journal of Field Robotics*, vol. 36, no. 2, pp. 416–446, 2019, doi: [10/gf3bgd](https://doi.org/10/gf3bgd).
  - RTab Map, 多传感器融合的一个好的框架，论文综述了许多SLAM算法的优缺点。还没读完
  - Introlab，[开源](https://github.com/introlab/rtabmap)
- [x] [13]J. Jeon, S. Jung, E. Lee, D. Choi, and H. Myung, “**Run Your Visual-Inertial Odometry on NVIDIA Jetson: Benchmark Tests on a Micro Aerial Vehicle**,” *IEEE Robotics and Automation Letters*, vol. 6, no. 3, pp. 5332–5339, Jul. 2021, doi: [10/gkpqx8](https://doi.org/10/gkpqx8).
  - 在不同的Nvidia Jason板子上测试了很多的**VI/VIO**系统，主要包括three **mono-VIO**(VINS-Mono, ROVIO, and ALVIO), two **stereoVO** ORB-SLAM2 stereo and VINS-Fusion w/o IMU), and **four stereo-VIO** (VINS-Fusion w/IMU, VINS-Fusion w/GPU, Stereo-MSCKF, and Kimera) lgorithms and benchmark them on **NVIDIA Jetson TX2, Xavier NX, and AGX Xavier boards**. 同时自己建立了一个**[数据集](https://github.com/zinuok/kaistviodataset)**，包扩circle, infinity, square, and pure_rotation 这几种轨迹或者姿态。
  - Benchmark + dataset，韩国KAIST
- [ ] [14]H. Azpurua, M. F. M. Campos, and D. G. Macharet, “**Three-dimensional Terrain Aware Autonomous Exploration for Subterranean and Conﬁned Spaces**,” p. 7.
  - 火星车可通过性研究，使用激光点云生成类似高程图，生成可通过性的地图。
  - Computer Vision and Robotics Laboratory (VeRLab)  
- [x] [15]Z. Qian, K. Patath, J. Fu, and J. Xiao, “**Semantic SLAM with Autonomous Object-Level Data Association**,” *arXiv:2011.10625 [cs]*, Nov. 2020, Accessed: May 31, 2021. [Online]. Available: http://arxiv.org/abs/2011.10625
  - 使用YOLO识别出物体（转化为词袋模型），然后对物体进行标记，最后使用曲面模型求物体进行标注。感觉语义性不是很强。
  - Worcester Polytechnic Institute  
- [ ] [16]Y. Latif, A.-D. Doan, T.-J. Chin, and I. Reid, “**SPRINT: Subgraph Place Recognition for INtelligent Transportation,**” in *2020 IEEE International Conference on Robotics and Automation (ICRA)*, May 2020, pp. 5408–5414. doi: [10/gjn63n](https://doi.org/10/gjn63n).
  - Place Recognition.场景重现识别（针对场景的不同时间段，相机拍摄的照片会不一样）
  - Visual的场景重识别，使用KNN的图像检索+图像采集过程中的时间关系，可以将匹配的位置限制在目前为止看到的场景的子集内。根据图像采集的关系，使用HMM进行缩小子集。
- [ ] [17]D. Wisth, M. Camurri, S. Das, and M. Fallon, “**Unified Multi-Modal Landmark Tracking for Tightly Coupled Lidar-Visual-Inertial Odometry,**” *IEEE Robot. Autom. Lett.*, vol. 6, no. 2, pp. 1004–1011, Apr. 2021, doi: [10/gjjm8s](https://doi.org/10/gjjm8s).
  - 多传感器融合，VI，slam。紧耦合的里程计。

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





