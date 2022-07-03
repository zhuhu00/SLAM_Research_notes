> 日志：
>
> 20220703-更新5月整理的**[ICRA2022](./ICRA2022.md)**的论文，以及终于把5月的整理结束了

# SLAM_Research

@Author:  zhuhu

@E-mail:  huzhu00@gmail.com

@Github:  [zhuhu00](https://github.com/zhuhu00)

# 摘要

​		整理前期主要以**SLAM**为主，包含论文，代码，相关讲解（如果有的话，一般在**泡泡机器人slam**公众号会发布），大概整理几个月会把**激光SLAM**也加上
​		目前收集的资料主要是一个大杂烩，研究的主要内容会从:tada:**动态SLAM，Robust SLAM， Life-long，多传感器融合**去跟进。将会从经典的框架开始，之后如果有时间的话，也会在这个仓库中添加文件夹写相关的基础。不一定能涵盖所有，请合理参考。

1. 开源经典框架：经典、应用广泛的**开源框架**
2. 优秀的作者和实验室：前期为**大杂烩**，后面则为**主要关注的团队和个人**
3. **SLAM的学习资料**：从基础的书籍到视频，数据集，公众号，代码注释等、
4. 近期的论文：整理到的好论文，大概每月一次更新，前期会更新比较快。有关论文的笔记也许~~不会~~放出来了。

**Attention：如果内容出现错误，请一定提出批评和建议，我一定及时修改。**
于2021年4月正式启动（私密）。

首次更新于20210404，清明节的日子，开启这方面的学习跟踪，
灵感来自于[Recent_SLAM_Research](https://github.com/YiChenCityU/Recent_SLAM_Research)，[Visual_SLAM_Related_Research](https://github.com/wuxiaolang/Visual_SLAM_Related_Research)

:fireworks:最近启动一个大工程，以此Repository为基础，在明年4月份读完略读完1k篇论文，主要是对方法的学习，感觉自己看的东西还是太少了。方法论不足。精读一些经典的。

>**一些值得练手的东西**
>
>1. ORB-SLAM2的稠密建图, 建八叉树的地图
>2. 全景重建
>3. 动态环境中的视觉SLAM
>3. 学习的方法提取特征点+描述子+ORB-SLAM

# 目录

1. 经典代码框架
2. 优秀作者及实验室
3. 论文更新

# 0. 会议Paper List（SLAM）

- [**ICRA 2022 SLAM paper list**](./ICRA2022.md);
- CVPR 2022 paper list；

# 1. 经典代码框架及实验室

见[SLAM-approachs](https://github.com/zhuhu00/SLAM_Research_dzh/tree/main/SLAM-approachs)

# 2. 论文更新

## 2022年6月论文更新

## 2022年5月论文更新

- Z. Wang, W. Li, Y. Shen, and B. Cai, “**[4-D SLAM: An Efficient Dynamic Bayes Network-Based Approach for Dynamic Scene Understanding](https://doi.org/10.1109/ACCESS.2020.3042339)**,” *IEEE Access*
  - 语义识别动态后，使用UKF之类的进行动态追踪，但是图的效果不好。
- M. Zhao *et al.*, “[**A General Framework for Lifelong Localization and Mapping in Changing Environment**](http://arxiv.org/abs/2111.10946).”  IROS 2021
  - 高仙机器人的**life-long** 定位的论文
  - 多session的地图表示和一种**高效的在线地图更新策略**，子系统组成：局部激光雷达里程计（LLO）、全局激光雷达匹配（GLM）和位姿图优化（PGR），LLO的作用是构建一系列局部一致的子地图，GLM子系统负责计算传入扫描点云和全局子地图之间的相对约束，并将子映地图和约束插入PGR，PGR是系统中最重要的部分，它从LLO和GLM收集子地图和约束关系，修剪并保存在历史地图中的旧的子地图，并执行姿势图稀疏化和优化。
- D. Menini, S. Kumar, M. R. Oswald, E. Sandstrom, C. Sminchisescu, and L. Van Gool, “[**A Real-Time Online Learning Framework for Joint 3D Reconstruction and Semantic Segmentation of Indoor Scenes**](http://arxiv.org/abs/2108.05246),” RAL&ICRA 2022
  - **[code](https://github.com/suryanshkumar/online-joint-depthfusion-and-semantic)**，**[project page](https://suryanshkumar.github.io/online-joint-depthfusion-and-semantic_project_page/)**，
  - 室内的语义重建：在给定噪声深度图、摄像机轨迹和训练时的2D语义标签的情况下，提出的基于深度神经网络的方法学习将帧上的深度与场景空间中合适的语义标签进行融合
- Y. Liu, J. Liu, Y. Hao, B. Deng, and Z. Meng, “**[A Switching-Coupled Backend for Simultaneous Localization and Dynamic Object Tracking](https://ieeexplore.ieee.org/document/9343683)**,” RAL 2021
  - 视觉SLAM上的追踪，当检测结果不好时，提出了对应的处理办法来实现追踪和定位的效果，论文将追踪分为了两个部分，紧耦合和松耦合，紧耦合就是把动态对象加入到SLAM中，而松耦合则是只使用静态背景进行建图和定位。
  - 清华-孟子阳老师
- M. Frosi and M. Matteucci, “[**ART-SLAM: Accurate Real-Time 6DoF LiDAR SLAM**](https://arxiv.org/abs/2109.05483v1),” RAL&ICRA 2022
  - **[code](https://github.com/MatteoF94)**， 一个快速的激光SLAM系统，受HDL的启发
- D. Henning, T. Laidlow, and S. Leutenegger, “[**BodySLAM: Joint Camera Localisation, Mapping, and Human Motion Tracking**](https://arxiv.org/pdf/2205.02301v1.pdf),” *arXiv:2205.02301
  - 人体构建和SLAM相结合，与AirDOS有点类似
- J. Li, X. Zhang, J. Li, Y. Liu, and J. Wang, “Building and optimization of 3D semantic map based on Lidar and camera fusion,” *Neurocomputing*, vol. 409, pp. 394–407, Oct. 2020, doi: [10.1016/j.neucom.2020.06.004](https://doi.org/10.1016/j.neucom.2020.06.004).
  - 视觉语义信息融合到雷达中，生成语义地图
- P. Ji, Y. Tian, Q. Yan, Y. Ma, and Y. Xu, “CNN-Augmented Visual-Inertial SLAM with Planar Constraints,” *arXiv:2205.02940 [cs]*, May 2022, Accessed: May 10, 2022. [Online]. Available: http://arxiv.org/abs/2205.02940
  - 提出了一种结合了卷积神经网络(CNN)和平面约束优点的鲁棒视觉惯性SLAM系统
- R. Marcuzzi, L. Nunes, L. Wiesmann, I. Vizzo, J. Behley, and C. Stachniss, “**[Contrastive Instance Association for 4D Panoptic Segmentation Using Sequences of 3D LiDAR Scans,](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/marcuzzi2022ral.pdf)**” RAL-ICRA'22
  - 雷达点云的全景分割，波恩大学Cyrill Stachniss组
  - [**code**](https://github.com/PRBonn/contrastive_association)，
- P. Dellenbach, J.-E. Deschaud, B. Jacquet, and F. Goulette, “**[CT-ICP: Real-time Elastic LiDAR Odometry with Loop Closure](https://arxiv.org/abs/2109.12979v2)**.” arXiv
  - KITTI榜单第六名，[code](https://github.com/jedeschaud/ct_icp)，
- Z. Wang, L. Zhang, Y. Shen and Y. Zhou, "**D-LIOM: Tightly-coupled Direct LiDAR-Inertial Odometry and Mapping**," in IEEE Transactions on Multimedia, doi: 10.1109/TMM.2022.3168423.
  - [**code**](https://github.com/peterWon/D-LIOM)，一种紧耦合的直接激光雷达-惯性SLAM框架
- K. Chen, R. Nemiroff, and B. T. Lopez, “[**Direct LiDAR-Inertial Odometry**](https://arxiv.org/abs/2203.03749v2),” *arXiv:2203.03749
  - 第一是基于关键帧的快速LiDAR扫描匹配，它通过将密集的点云配准到具有由非线性运动模型生成的平移和旋转先验的局部子图来构建内部地图。第二种是因子图和高速传播算子，它将扫描匹配器的输出与预先集成的IMU测量融合在一起，以获得最新的姿态、速度和偏差估计
- Y. Huang, T. Shan, F. Chen, and B. Englot, “**DiSCo-SLAM: Distributed Scan Context-Enabled Multi-Robot LiDAR SLAM With Two-Stage Global-Local Graph Optimization,**” RAL 2022
  - **[code](https://github.com/RobustFieldAutonomyLab/DiSCo-SLAM)**，Tixiao Shan，一作有几个好的代码，也可以看看，都是基于LIO-系列的
- F. Langer, A. Milioto, A. Haag, J. Behley, and C. Stachniss, “**[Domain Transfer for Semantic Segmentation of LiDAR Data using Deep Neural Networks](http://ras.papercept.net/images/temp/IROS/files/0060.pdf)**,” IROS 2020
  - 分割网络在不同的传感器上的迁移，如32线到64线
  - 波恩大学RPB组，**[code](https://github.com/PRBonn/lidar_transfer)**
- W. Wang, J. Liu, C. Wang, B. Luo, and C. Zhang, “DV-LOAM: Direct Visual LiDAR Odometry and Mapping,” *Remote Sensing*, vol. 13, no. 16, p. 3340, Aug. 2021, doi: [10.3390/rs13163340](https://doi.org/10.3390/rs13163340).
  - [code](https://github.com/kinggreat24/dv-loam)，武大
- Y.-S. Shin, Y. S. Park, and A. Kim, “DVL-SLAM: sparse depth enhanced direct visual-LiDAR SLAM,” *Auton Robot*, vol. 44, no. 2, pp. 115–130, Jan. 2020, doi: [10.1007/s10514-019-09881-0](https://doi.org/10.1007/s10514-019-09881-0).
  - [**code**](https://github.com/irapkaist/dvl_slam)，[**code2-ros**](https://github.com/xuankuzcr/DVL_SLAM_ROS)，
  - 提出了一个基于直接法视觉SLAM的融合稀疏雷达深度的方法，基于滑窗的优化克服了稀疏雷达深度和异构传感器视角的缺陷，闭环约束
- DynamicFilter: an Online Dynamic Objects Removal Framework for Highly Dynamic Environments，ICRA 2022
  - IJRR大佬，可惜不开源。。
  - 港大
- X. Ma, Y. Wang, B. Zhang, H.-J. Ma, and C. Luo, “**[DynPL-SVO: A New Method Using Point and Line Features for Stereo Visual Odometry in Dynamic Scenes](https://arxiv.org/abs/2205.08207v1)**.” arXiv, May 17, 2022
  - 使用点和线特征的双目视觉里程计，动态去除的论文
  - 东北大学，也还没有开源
- M. T. Lázaro, R. Capobianco, and G. Grisetti, “**[Efficient Long-term Mapping in Dynamic Environments](https://www.researchgate.net/profile/Maria-Lazaro-12/publication/330586668_Efficient_Long-term_Mapping_in_Dynamic_Environments/links/5f26efbe458515b729fe2f1b/Efficient-Long-term-Mapping-in-Dynamic-Environments.pdf)**,” IROS 2018
  - 高效的ICP方案，并且实现了地图实体的合并。由于处理的是2D地图，因此也就没有那么多的需要处理的东西。可以直接用点可视化来去除运动的点云。
  - **[code](https://gitlab.com/srrg-software/srrg_mapper2d_ros)**，
- J. Behley and C. Stachniss, “**[Efficient Surfel-Based SLAM using 3D Laser Range Data in Urban Environments](http://www.roboticsproceedings.org/rss14/p16.pdf)**,” RSS 2018
  - SuMa的论文，面元的SLAM，基于点到面的icp获得位姿更新
  - [**code**](https://github.com/PRBonn/SuMa)
- T. Krajník, J. P. Fentanes, J. M. Santos, and T. Duckett, “**[FreMEn: Frequency Map Enhancement for Long-Term Mobile Robot Autonomy in Changing Environments](http://strands.acin.tuwien.ac.at/publications/y4/krajnik_TRO.pdf)**,” TRO 2017

- G. Kurz, M. Holoch, and P. Biber, “[**Geometry-based Graph Pruning for Lifelong SLAM**](http://arxiv.org/abs/2110.01286).” IROS 2021
  - 我们提出了一种新的方法，该方法考虑了几何准则来选择要剪枝的顶点。这是有效的，易于实现，并导致具有均匀分布的顶点的图形，这些顶点仍然是机器人轨迹的一部分。此外，我们提出了一种新的边际化方法，与现有方法相比，该方法对错误的循环闭包具有更强的鲁棒性。
    主要设计到SLAM后端的优化，当地图或者是因子图更新时，如何对因子图进行剪枝的问题。

- Han Wang, Chen Wang, Chun-Lin Chen, and Lihua Xie, “**[F-LOAM : Fast LiDAR Odometry and Mapping](https://arxiv.org/abs/2107.00822v1)**” IROS 2021
  - [**Code**](https://github.com/wh200720041/floam), 
- [**FD-SLAM: 3-D Reconstruction Using Features and Dense Matching**](https://arxiv.org/abs/2203.13861v1); ICRA 2022
  - 重建的工作，布里斯托大学，[code](https://github.com/xingruiy)
- Quei-An Chen and Akihiro Tsukada，“[**Flow Supervised Neural Radiance Fields for Static-Dynamic Decomposition**](https://drive.google.com/file/d/1kORAX0DOAs7m771EQ693aH7FeRwUqhCy/view)”, ICRA 2022
  - AI葵，[**code**](https://github.com/kwea123?tab=repositories)，nerf+光流的动态物体，去除并修复，[video](https://youtu.be/ixw9AkJpe30)。
- Xin Wei, Ground-SLAM: Ground Constrained LiDAR SLAM for Structured Multi-Floor Environments, Arxiv 2021
  - 海康威视

- X. Liu *et al.*, “**[Large-scale Autonomous Flight with Real-time Semantic SLAM under Dense Forest Canopy](https://arxiv.org/abs/2109.06479v4)**,” RAL 2022
  - 与之前的工作[**SLOAM**](https://github.com/KumarRobotics/sloam)的后续，SLOAM是使用提取柱状物体，进行SLAM的操作。
  - github：https://github.com/KumarRobotics

- W. Ding, S. Hou, H. Gao, G. Wan, and S. Song, “[**LiDAR Inertial Odometry Aided Robust LiDAR Localization System in Changing City Scenes**](https://songshiyu01.github.io/pdf/LIO_W.Ding_S.Song_ICRA2020.pdf),” ICRA 2020
  - 百度出品的使用激光和IMU，在运动场景的定位，并且在之前构建的地图中，针对场景新增加的东西，将会新建相关的地图。
  - life-long SLAM

- A. Milioto, J. Behley, C. McCool, and C. Stachniss, “[**LiDAR Panoptic Segmentation for Autonomous Driving**](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/milioto2020iros.pdf),” IROS 2020
  - 波恩大学RPB组，code，基于rangenet出来的很多工作。

- G. D. Tipaldi, D. Meyer-Delius, and W. Burgard, “**Lifelong localization in changing environments**,” IJRR 2013
  - life-long的定位

- S. Zhu, X. Zhang, S. Guo, J. Li, and H. Liu, “**Lifelong Localization in Semi-Dynamic Environment**,” ICRA 2021
  - 清华，life-long的定位

- C. Qu, S. S. Shivakumar, W. Liu, and C. J. Taylor, “[**LLOL: Low-Latency Odometry for Spinning Lidars**](http://arxiv.org/abs/2110.01725).” Arxiv 2022.4
  - code：https://github.com/versatran01/llol

- A. Reinke *et al.*, “[LOCUS 2.0: Robust and Computationally Efficient Lidar Odometry for Real-Time Underground 3D Mapping](http://arxiv.org/abs/2205.11784).” arXiv
  - DARPA挑战赛的论文，Luca Carlone组，有数据集以及代码:https://github.com/NeBula-Autonomy
  - **Loop Closure Prioritization for Efficient and Scalable Multi-Robot SLAM**

- F. Pomerleau, P. Krüsi, F. Colas, P. Furgale, and R. Siegwart, “**Long-term 3D map maintenance in dynamic environments**,” ICRA 2014
  - 动态环境中，地图更新

- D. J. Yoon, T. Y. Tang, and T. D. Barfoot, “[**Mapless Online Detection of Dynamic Objects in 3D Lidar**](http://arxiv.org/abs/1809.06972).” Conference on Computer and Robot Vision (CRV) 2019
  - 点云动态检测

- L. Di Giammarino, L. Brizi, T. Guadagnino, C. Stachniss, and G. Grisetti, “[**MD-SLAM: Multi-cue Direct SLAM,**](https://arxiv.org/abs/2203.13237v1)” arXiv 2022

- T. Ma and Y. Ou, “[**MLO: Multi-Object Tracking and Lidar Odometry in Dynamic Environment**](http://arxiv.org/abs/2204.11621).” arXiv, Apr. 29, 2022
  - SLAM+MOT了

- Chen Xieyuanli *et al.*, “Moving Object Segmentation in 3D LiDAR Data: A Learning-based Approach Exploiting Sequential Data,” RAL
  - 动态物体的分割，用学习的方法检测，[code](https://github.com/PRBonn/LiDAR-MOS)

- S. Li, X. Chen, Y. Liu, D. Dai, C. Stachniss, and J. Gall, “**Multi-Scale Interaction for Real-Time LiDAR Data Segmentation on an Embedded Platform,**” *IEEE Robotics and Automation Letters*, 2022
  - 点云分割

- A. Hornung, K. M. Wurm, M. Bennewitz, C. Stachniss, and W. Burgard, “**OctoMap: an efficient probabilistic 3D mapping framework based on octrees**,” *Auton Robot*, vol. 34, no. 3, pp. 189–206, Apr. 2013, doi: [10.1007/s10514-012-9321-0](https://doi.org/10.1007/s10514-012-9321-0).
- **Panoptic Multi-TSDFs: a Flexible Representation for Online Multi-resolution Volumetric Mapping and Long-term Dynamic Scene Consistency**， ICRA 2022
  - ETH，[code](https://github.com/ethz-asl/panoptic_mapping)

- I. Vizzo, X. Chen, N. Chebrolu, J. Behley, and C. Stachniss, “**Poisson Surface Reconstruction for LiDAR Odometry and Mapping**,” ICRA 2021
  - https://github.com/PRBonn/puma

- P. Egger, P. V. K. Borges, G. Catt, A. Pfrunder, R. Siegwart, and R. Dubé, “**PoseMap: Lifelong, Multi-Environment 3D LiDAR Localization**,” IROS 2018
  - lifelong slam，ETH SAL组

- D. Paz, H. Zhang, Q. Li, H. Xiang, and H. Christensen, “[**Probabilistic Semantic Mapping for Urban Autonomous Driving Applications**](http://ras.papercept.net/images/temp/IROS/files/2186.pdf),” IROS 2020
  - 语义地图构建，结合视觉的语义信息，构建点云语义地图,一作的**[github](https://github.com/AftermathK)**
- G. Chen, B. Wang, X. Wang, H. Deng, B. Wang, and S. Zhang, “**PSF-LO: Parameterized Semantic Features Based Lidar Odometry,**” ICRA 2021
  - 阿里巴巴达摩院，

- A. Milioto, I. Vizzo, J. Behley, and C. Stachniss, “**RangeNet ++: Fast and Accurate LiDAR Semantic Segmentation,**” IROS 2019
  - 波恩大学RPB组，其github上有对应代码，很多后续工作也是在这个基础上搞出来的。

- Z. Li, L. Li, Z. Ma, P. Zhang, J. Chen, and J. Zhu, “**[READ: Large-Scale Neural Scene Rendering for Autonomous Driving](http://arxiv.org/abs/2205.05509)**,” arXiv:2205.05509
  - code：https://github.com/JOP-Lee/READ-Large-Scale-Neural-Scene-Rendering-for-Autonomous-Driving，浙江大学，阿里巴巴

- X. Tu *et al.*, “Reconstruction of High-Precision Semantic Map,” *Sensors (Basel)*, vol. 20, no. 21, p. 6264, Nov. 2020, doi: [10.3390/s20216264](https://doi.org/10.3390/s20216264).

- L. Sun, Z. Yan, A. Zaganidis, C. Zhao, and T. Duckett, “**Recurrent-OctoMap: Learning State-Based Map Refinement for Long-Term Semantic Mapping With 3-D-Lidar Data**,” RAL
  - life long slam 

- “**[RF-LIO: Removal-First Tightly-coupled Lidar Inertial Odometry in High Dynamic Environments](https://arxiv.org/abs/2206.09463v1)**,” IROS 2021
  - 和之前removert思路类似，但是没开源，西交，动态去除

- S. Pagad, D. Agarwal, S. Narayanan, K. Rangan, H. Kim, and G. Yalla, “**[Robust Method for Removing Dynamic Objects from Point Clouds](https://drive.google.com/file/d/1o73aG85OpuDmAUsjkgKaVwrG6d48aOin/view)**,” ICRA 2020
  - [video](https://www.youtube.com/watch?v=d2rbSP9IkkY)，动态去除

- M. Jaimez, J. Monroy, M. Lopez-Antequera, and J. Gonzalez-Jimenez, “**Robust Planar Odometry Based on Symmetric Range Flow and Multiscan Alignment**,” *IEEE Transactions on Robotics*, 2018

- L. Li *et al.*, “[**SA-LOAM: Semantic-aided LiDAR SLAM with Loop Closure**](http://arxiv.org/abs/2106.11516).” ICRA 2021
  - 作者在这篇论文中提出一个语义辅助回环检测的SLAM方法

- O. Unal, D. Dai, and L. Van Gool, “Scribble-Supervised LiDAR Semantic Segmentation,” *arXiv:2203.08537 [cs]*, Mar. 2022, Accessed: May 13, 2022. [Online]. Available: http://arxiv.org/abs/2203.08537
  - 点云语义分割

- R. Dubé *et al.*, “**SegMap: Segment-based mapping and localization using data-driven descriptors,**” *The International Journal of Robotics Research*, vol. 39, no. 2–3, pp. 339–355, Mar. 2020, doi: [10.1177/0278364919863090](https://doi.org/10.1177/0278364919863090).
  - segmap，太强了。code：https://github.com/ethz-asl/segmap

- J. L. Schonberger, M. Pollefeys, A. Geiger, and T. Sattler, “[**Semantic Visual Localization,**](https://openaccess.thecvf.com/content_cvpr_2018/papers/Schonberger_Semantic_Visual_Localization_CVPR_2018_paper.pdf)” CVPR 2018

- Y. Pan, B. Gao, J. Mei, S. Geng, C. Li, and H. Zhao, “**[SemanticPOSS: A Point Cloud Dataset with Large Quantity of Dynamic Instances](https://arxiv.org/pdf/2002.09147v1.pdf)**,” IV 2020
  - 动态物体室外数据集，北大，[网站](http://www.poss.pku.edu.cn/semanticposs.html)

- S. Gu, S. Yao, J. Yang, and H. Kong, “**[Semantics-Guided Moving Object Segmentation with 3D LiDAR]( http://arxiv.org/abs/2205.03186)**,”  arxiv 2022.05
  - 动态物体的分割网络，也是rangenet的思想那套。

- M. Schorghuber, D. Steininger, Y. Cabon, M. Humenberger, and M. Gelautz, “**[SLAMANTIC - Leveraging Semantics to Improve VSLAM in Dynamic Environments,](https://openaccess.thecvf.com/content_ICCVW_2019/papers/DL4VSLAM/Schorghuber_SLAMANTIC_-_Leveraging_Semantics_to_Improve_VSLAM_in_Dynamic_Environments_ICCVW_2019_paper.pdf)**” ICCV 2019 workshop
  - 视觉SLAM，动态环境。通过语义对点的置信度进行计算，高置信度的点来辅助低置信度的点，最终确定用于定位和建图的部分。

- S. W. Chen *et al.*, “[**SLOAM: Semantic Lidar Odometry and Mapping for Forest Inventory.**](http://arxiv.org/abs/1912.12726)” RAL 2019
  - 泡泡机器人我有写讲解，上一篇就是这一篇的后续了。

- N. Rufus, U. K. R. Nair, A. V. S. S. B. Kumar, V. Madiraju, and K. M. Krishna, “[**SROM: Simple Real-time Odometry and Mapping using LiDAR data for Autonomous Vehicles**.](http://arxiv.org/abs/2005.02042)” IV 2020
  - 较为粗暴的去除可能的运动对象，去除地面后再取出

- Y. Kim, J. Jeong, and A. Kim, “**Stereo Camera Localization in 3D LiDAR Maps**,”IROS 2018
  - 双目基于深度再点云中的定位，正在复现ing

- X. Chen, A. Milioto, E. Palazzolo, P. Giguère, J. Behley, and C. Stachniss, “**SuMa++: Efficient LiDAR-based Semantic SLAM**,” *2019 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)*, pp. 4530–4537, Nov. 2019, doi: [10.1109/IROS40897.2019.8967704](https://doi.org/10.1109/IROS40897.2019.8967704).
  - 经典的semantic slam，也有对运动对象的去除方案。
  - [**code**](https://github.com/PRBonn/semantic_suma)，video

- J. Schauer and A. Nuchter, “**The Peopleremover—Removing Dynamic Objects From 3-D Point Cloud Data by Traversing a Voxel Occupancy Grid**,” *IEEE Robot. Autom. Lett.*, vol. 3, no. 3, pp. 1679–1686, Jul. 2018, doi: [10.1109/LRA.2018.2801797](https://doi.org/10.1109/LRA.2018.2801797).
  - 基于体素遍历的方法的运动对象去除，虽然这种方法有很多的缺点，但是论文提出了很多的trick，来解决这些问题，看起来效果还是不错的。
  - code，video

- Y. B. Can, A. Liniger, O. Unal, D. Paudel, and L. Van Gool, “**[Understanding Bird’s-Eye View of Road Semantics using an Onboard Camera](http://arxiv.org/abs/2012.03040)**,”  ICRA 2022
  - 前视转BEV的研究，**[code](https://github.com/ybarancan/BEV_feat_stitch)**，video



## 2022年2月论文更新

1. [**Autonomous Vehicles: Open-Source Technologies, Considerations, and Development**](https://arxiv.org/pdf/2202.03148.pdf), 有关自动驾驶车辆的**开源框架,思考,及仿真环境**等的综述, 2022
2. **[A Survey on Deep Learning for Localization and Mapping: Towards the Age of Spatial Machine Intelligence](https://arxiv.org/pdf/2006.12567v2.pdf)**,2020, [**website**](https://github.com/changhao-chen/deep-learning-localization-mapping) ,**深度学习在里程计, 定位, 建图, SLAM的综述**
3. 

## 2021年11月论文更新

本月主要关注动态SLAM的整理和语义地图的论文，以及ICRA2022论文集也出来了，快速刷了一遍，把相关的放到了**[ICRA2022.md](./ICRA2022.md)**文件里了。

## 2021年11月论文更新


## 2021年10月论文更新

- [x] [1]Gonzalez Mathieu, et al. “S3LAM: Structured Scene SLAM.” *ArXiv:2109.07339 [Cs]*, Sept. 2021. *arXiv.org*, http://arxiv.org/abs/2109.07339.
  - 语义地图，新的BA形式。
- [x] [2]Yoon Sungho and Kim Ayoung. “**[Line as a Visual Sentence: Context-Aware Line Descriptor for Visual Localization.](http://arxiv.org/abs/2109.04753)**” RAl 2021
  - [code](https://github.com/yosungho/LineTR)，[video](https://youtu.be/Ej4onCkA9pc)，**NLP的思想用到线特征上**。Ayoung kim。
- [ ] [3]N. Chebrolu, T. Läbe, O. Vysotska, J. Behley, and C. Stachniss, “[**Adaptive Robust Kernels for Non-Linear Least Squares Problems**](http://arxiv.org/abs/2004.14938),” RAL 2021
  - 针对非线性最小二乘法的核函数进行的改进。在ICP和BA上进行了验证。目前代码应该是整合到Open3D中了:boom:,
  - 波恩大学的组，[主页](https://www.ipb.uni-bonn.de/)。
- [x] [4]Y. Liu, Y. Fu, F. Chen, B. Goossens, W. Tao, and H. Zhao, “**[Simultaneous Localization and Mapping Related Datasets: A Comprehensive Survey,](http://arxiv.org/abs/2102.04036)**”  [code](https://github.com/robot-pesg/SLAM_Datasets_Survey_JAS)，数据集
- [x] [5]P. Ruhkamp, D. Gao, H. Chen, N. Navab, and B. Busam, “**[Attention meets Geometry: Geometry Guided Spatial-Temporal Attention for Consistent Self-Supervised Monocular Depth Estimation](http://arxiv.org/abs/2110.08192)**,” 3DV 2021
  - 在3D空间中对几何约束进行推理。结合transformer框架，提出了空间注意力机制，通过矫正深度估计来对几何信息做更好的处理。**结合时间和空间的一致性。**
  - TUM
- [ ] [6]Margarita Grinvald, Federico Tombari, Roland Siegwart, and Juan Nieto, **TSDF++: A Multi-Object Formulation for Dynamic Object Tracking and Reconstruction**, in *2021 IEEE International Conference on Robotics and Automation (ICRA)*, 2021. [[Paper](https://arxiv.org/abs/2105.07468)] [[Video](https://youtu.be/dSJmoeVasI0)]
  - [code](https://github.com/ethz-asl/tsdf-plusplus),ETH, 很好的工作:boom:
- [x] [7]M. Shan, Q. Feng, and N. Atanasov, “[**OrcVIO: Object residual constrained Visual-Inertial Odometry,**](https://doi.org/10.1109/IROS45743.2020.9341660)” (IROS 2020)
  - 有两个版本，[21年IROS](http://arxiv.org/abs/2007.15107)也有一篇。
  - [code](https://github.com/shanmo/OrcVIO), [video](http://moshan.cf/orcvio_githubpage/), [Project page](http://moshan.cf/orcvio_githubpage/).
- [ ] [8]K. Minoda, F. Schilling, V. Wüest, D. Floreano, and T. Yairi, “**[VIODE: A Simulated Dataset to Address the Challenges of Visual-Inertial Odometry in Dynamic Environments,](https://doi.org/10.1109/LRA.2021.3058073)**”RAL 2021
  - 动态环境的数据集，包括了静态，动态等级的场景，感觉适合用来作为验证。
  - 东京大学，[code](https://github.com/kminoda/VIODE)

## 2021年9月论文更新

- [ ] Gallagher Louis, et al. “**[A Hybrid Sparse-Dense Monocular SLAM System for Autonomous Driving](http://arxiv.org/abs/2108.07736)**.” .ECMR'21
  - [code](https://github.com/robotvisionmu/DenseMonoSLAM), [video](https://youtu.be/Pn2uaVqjskY).
- [ ] Ferrera Maxime, et al. “[**OV$^{2}$SLAM: A Fully Online and Versatile Visual SLAM for Real-Time Applications**](https://arxiv.org/pdf/2102.04060.pdf).” RAL 2021
  - [code](https://github.com/ov2slam/ov2slam).

## 2021年8月论文更新

这部分论文更多在动态slam上，比7月更加focus。重点关注西班牙的博士所做的四篇文章的内容。以及在国内期刊上发表的一篇综述。

- [x] [1]Y. Liu and J. Miura, “**[RDS-SLAM: Real-Time Dynamic SLAM Using Semantic Segmentation Methods](https://doi.org/10.1109/ACCESS.2021.3050617)**,” *IEEE Access*, vol. 9, pp. 23772–23785, 2021, doi: [10.1109/ACCESS.2021.3050617](https://doi.org/10.1109/ACCESS.2021.3050617).
  - 添加了语义及光流的信息
- [x] [2]Y. Liu and J. Miura, “**[RDMO-SLAM: Real-time Visual SLAM for Dynamic Environments using Semantic Label Prediction with Optical Flow,](https://doi.org/10.1109/ACCESS.2021.3100426)**” *IEEE Access*, pp. 1–1, 2021, doi: [10.1109/ACCESS.2021.3100426](https://doi.org/10.1109/ACCESS.2021.3100426).
  - 与上一篇文章框架类似。上一篇RDS-SLAM是这篇的拓展。
- [x] [3]F. Wimbauer, N. Yang, L. von Stumberg, N. Zeller, and D. Cremers, “**[MonoRec: Semi-Supervised Dense Reconstruction in Dynamic Environments from a Single Moving Camera](http://arxiv.org/abs/2011.11814)**,” *arXiv:2011.11814 [cs]*, May 2021, Accessed: Aug. 10, 2021. [Online]. Available: http://arxiv.org/abs/2011.11814
  - CVPR上的单目重建框架，能去除动态物体
  - 开源
- [x] [4]J. Luiten, T. Fischer, and B. Leibe, “**[Track to Reconstruct and Reconstruct to Track,](https://doi.org/10.1109/LRA.2020.2969183)**” *IEEE Robot. Autom. Lett.*, vol. 5, no. 2, pp. 1803–1810, Apr. 2020, doi: [10.1109/LRA.2020.2969183](https://doi.org/10.1109/LRA.2020.2969183).
  - RAL+ICRA2020的文章，重建中跟踪，跟踪重建。双目+光流+深度+mask
  - 开源
- [ ] [5]B. Bescos, C. Campos, J. D. Tardós, and J. Neira, “**[DynaSLAM II: Tightly-Coupled Multi-Object Tracking and SLAM](https://doi.org/10.1109/LRA.2021.3068640)**,” *IEEE Robotics and Automation Letters*, vol. 6, no. 3, pp. 5191–5198, Jul. 2021, doi: [10.1109/LRA.2021.3068640](https://doi.org/10.1109/LRA.2021.3068640).
  - 大佬的又一篇很优秀的文章。不过暂时还没有开源
- [x] [6]T. Ran, L. Yuan, J. Zhang, D. Tang, and L. He, “**[RS-SLAM: A Robust Semantic SLAM in Dynamic Environments Based on RGB-D Sensor,](https://doi.org/10.1109/JSEN.2021.3099511)**” *IEEE Sensors Journal*, pp. 1–1, 2021, doi: [10.1109/JSEN.2021.3099511](https://doi.org/10.1109/JSEN.2021.3099511).
  - 先把图片分割后，再提取feature，进行tracking等的操作
- [x] [7]Z. Xu, Z. Rong, and Y. Wu, “[**A survey: which features are required for dynamic visual simultaneous localization and mapping?,**](https://doi.org/10.1186/s42492-021-00086-w)” *Vis. Comput. Ind. Biomed. Art*, vol. 4, no. 1, p. 20, Dec. 2021, doi: [10.1186/s42492-021-00086-w](https://doi.org/10.1186/s42492-021-00086-w).
  - 综述。主要是动态点在SLAM中到底有没有效果
- [ ] [8]A. Kim, A. Ošep, and L. Leal-Taixé, “**[EagerMOT: 3D Multi-Object Tracking via Sensor Fusion](http://arxiv.org/abs/2104.14682)**,” *arXiv:2104.14682 [cs]*, Apr. 2021, Accessed: Aug. 03, 2021. [Online]. Available: http://arxiv.org/abs/2104.14682
  - 开源，也是追踪重建类文章
- [x] [10]Y. Sun, M. Liu, and M. Q.-H. Meng, “Motion removal for reliable RGB-D SLAM in dynamic environments,” *Robotics and Autonomous Systems*, 
- [x] [11]T. Qin, S. Cao, J. Pan, and S. Shen, “[**A General Optimization-based Framework for Global Pose Estimation with Multiple Sensors**]( http://arxiv.org/abs/1901.03642),” 
  - 大名鼎鼎的VINS-Fusion
- [x] [12]J. Cheng, Y. Sun, and M. Q.-H. Meng, “Robust Semantic Mapping in Challenging Environments,” *Robotica*, vol. 38, no. 2, pp. 256–270, Feb. 2020, doi: [10.1017/S0263574719000584](https://doi.org/10.1017/S0263574719000584).
- [x] [13]J. Zhang, M. Henein, R. Mahony, and V. Ila, “Robust Ego and Object 6-DoF Motion Estimation and Tracking,” *arXiv:2007.13993 [cs]*, Jul. 2020, Accessed: Aug. 03, 2021. [Online]. Available: http://arxiv.org/abs/2007.13993
  - 使用mask，光流图像对动态物体进行估计。
- [ ] **[16]B. Bescos, J. Neira, R. Siegwart, and C. Cadena, “Empty Cities: Image Inpainting for a Dynamic-Object-Invariant Space,” *arXiv:1809.10239 [cs, stat]*, Feb. 2019, Accessed: Aug. 02, 2021. [Online]. Available: http://arxiv.org/abs/1809.10239**
- [ ] **[17]B. Bescos, C. Cadena, and J. Neira, “Empty Cities: a Dynamic-Object-Invariant Space for Visual SLAM,” *IEEE Trans. Robot.*, vol. 37, no. 2, pp. 433–451, Apr. 2021, doi: [10.1109/TRO.2020.3031267](https://doi.org/10.1109/TRO.2020.3031267).**
- [x] [18]G. Li, X. Liao, H. Huang, S. Song, B. Liu, and Y. Zeng, “Robust Stereo Visual SLAM for Dynamic Environments With Moving Object,” *IEEE Access*, vol. 9, pp. 32310–32320, 2021, doi: [10.1109/ACCESS.2021.3059866](https://doi.org/10.1109/ACCESS.2021.3059866).
- [x] [19]H. Xu, C. Yang, and Z. Li, “OD-SLAM: Real-Time Localization and Mapping in Dynamic Environment through Multi-Sensor Fusion,” in *2020 5th International Conference on Advanced Robotics and Mechatronics (ICARM)*, Dec. 2020, pp. 172–177. doi: [10.1109/ICARM49381.2020.9195374](https://doi.org/10.1109/ICARM49381.2020.9195374).
- [x] [20]Y. Sun, M. Liu, and M. Q.-H. Meng, “Motion removal from moving platforms: An RGB-D data-based motion detection, tracking and segmentation approach,” in *2015 IEEE International Conference on Robotics and Biomimetics (ROBIO)*, Zhuhai, Dec. 2015, pp. 1377–1382. doi: [10.1109/ROBIO.2015.7418963](https://doi.org/10.1109/ROBIO.2015.7418963).
- [x] [21]Y. Liu, Y. Wu, and W. Pan, “Dynamic RGB-D SLAM Based on Static Probability and Observation Number,” *IEEE Transactions on Instrumentation and Measurement*, vol. 70, pp. 1–11, 2021, doi: [10.1109/TIM.2021.3089228](https://doi.org/10.1109/TIM.2021.3089228).
- [x] **[22]B. Bescos, J. M. Fácil, J. Civera, and J. Neira, “DynaSLAM: Tracking, Mapping and Inpainting in Dynamic Scenes,” *IEEE Robot. Autom. Lett.*, vol. 3, no. 4, pp. 4076–4083, Oct. 2018, doi: [10.1109/LRA.2018.2860039](https://doi.org/10.1109/LRA.2018.2860039).**
- [x] [23]D. Pathak, P. Krahenbuhl, J. Donahue, T. Darrell, and A. A. Efros, “Context Encoders: Feature Learning by Inpainting,” *arXiv:1604.07379 [cs]*, Nov. 2016, Accessed: Aug. 02, 2021. [Online]. Available: http://arxiv.org/abs/1604.07379
  - GAN补全图片
- [x] [24]P. Kaveti and H. Singh, “A Light Field Front-end for Robust SLAM in Dynamic Environments,” *arXiv:2012.10714 [cs]*, Dec. 2020, Accessed: Aug. 01, 2021. [Online]. Available: http://arxiv.org/abs/2012.10714
  - 多相机去除动态物体
- [x] [25]J. Cheng, H. Zhang, and M. Q.-H. Meng, “Improving Visual Localization Accuracy in Dynamic Environments Based on Dynamic Region Removal,” *IEEE Transactions on Automation Science and Engineering*, vol. 17, no. 3, pp. 1585–1596, Jul. 2020, doi: [10.1109/TASE.2020.2964938](https://doi.org/10.1109/TASE.2020.2964938).
- [x] [26]J. C. V. Soares, M. Gattass, and M. A. Meggiolaro, “Crowd-SLAM: Visual SLAM Towards Crowded Environments using Object Detection,” *J Intell Robot Syst*, vol. 102, no. 2, p. 50, Jun. 2021, doi: [10.1007/s10846-021-01414-1](https://doi.org/10.1007/s10846-021-01414-1).
  - 将人视为动态物体，去除
- [ ] [27]X.-F. Han, S.-J. Sun, X.-Y. Song, and G.-Q. Xiao, “3D Point Cloud Descriptors in Hand-crafted and Deep Learning Age: State-of-the-Art,” *arXiv:1802.02297 [cs]*, Jul. 2020, Accessed: Aug. 02, 2021. [Online]. Available: http://arxiv.org/abs/1802.02297
- [ ] [28]C.-C. Wang, C. Thorpe, S. Thrun, M. Hebert, and H. Durrant-Whyte, “Simultaneous Localization, Mapping and Moving Object Tracking,” *The International Journal of Robotics Research*, vol. 26, no. 9, pp. 889–916, Sep. 2007, doi: [10.1177/0278364907081229](https://doi.org/10.1177/0278364907081229).
- [ ] [29]Kuen-Han Lin and Chieh-Chih Wang, “Stereo-based simultaneous localization, mapping and moving object tracking,” in *2010 IEEE/RSJ International Conference on Intelligent Robots and Systems*, Taipei, Oct. 2010, pp. 3975–3980. doi: [10.1109/IROS.2010.5649653](https://doi.org/10.1109/IROS.2010.5649653).
- [ ] [30]M. Ferrera, A. Eudes, J. Moras, M. Sanfourche, and G. Le Besnerais, “OV$^{2}$SLAM: A Fully Online and Versatile Visual SLAM for Real-Time Applications,” *IEEE Robot. Autom. Lett.*, vol. 6, no. 2, pp. 1399–1406, Apr. 2021, doi: [10.1109/LRA.2021.3058069](https://doi.org/10.1109/LRA.2021.3058069).
- [ ] [31]D. M. Rosen, K. J. Doherty, A. T. Espinoza, and J. J. Leonard, “Advances in Inference and Representation for Simultaneous Localization and Mapping,” Mar. 2021, Accessed: Mar. 11, 2021. [Online]. Available: https://arxiv.org/abs/2103.05041v1
- [ ] [32]J. Zhang, M. Henein, R. Mahony, and V. Ila, “**VDO-SLAM: A Visual Dynamic Object-aware SLAM System**,” *arXiv:2005.11052 [cs]*, May 2020, Accessed: Jul. 28, 2021. [Online]. Available: http://arxiv.org/abs/2005.11052

## 2021年7月论文更新

> 本月主要关注动态SLAM及SLAM+MOT的内容。

- [x] [1]S. Chen, C.-W. Chang, and C.-Y. Wen, “Perception in the Dark; Development of a ToF Visual Inertial Odometry System,” *Sensors*, vol. 20, no. 5, p. 1263, Feb. 2020, doi: [10.3390/s20051263](https://doi.org/10.3390/s20051263).
  - 还是之前那篇，TOF-VIO

- [ ] [2]M. Mattamala, N. Chebrolu, and M. Fallon, “Ensuring Safe Visual Teach and Repeat Legged Navigation using Local World Representations,” p. 2.
- [ ] [3]G. Kim and A. Kim, “Scan Context: Egocentric Spatial Descriptor for Place Recognition Within 3D Point Cloud Map,” in *2018 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)*, Oct. 2018, pp. 4802–4809. doi: [10.1109/IROS.2018.8593953](https://doi.org/10.1109/IROS.2018.8593953).
- [x] [4]W. Ali, P. Liu, R. Ying, and Z. Gong, “A life-long SLAM approach using adaptable local maps based on rasterized LIDAR images,” *arXiv:2107.07133 [cs]*, Jul. 2021, Accessed: Jul. 21, 2021. [Online]. Available: http://arxiv.org/abs/2107.07133
- [x] [5]X. Qi, W. Wang, Z. Liao, X. Zhang, D. Yang, and R. Wei, “Object Semantic Grid Mapping with 2D LiDAR and RGB-D Camera for Domestic Robot Navigation,” *Applied Sciences*, vol. 10, no. 17, p. 5782, Aug. 2020, doi: [10.3390/app10175782](https://doi.org/10.3390/app10175782).
- [ ] [6]S. Chen, B. Zhou, C. Jiang, W. Xue, and Q. Li, “A LiDAR/Visual SLAM Backend with Loop Closure Detection and Graph Optimization,” *Remote Sensing*, vol. 13, no. 14, p. 2720, Jul. 2021, doi: [10.3390/rs13142720](https://doi.org/10.3390/rs13142720).
- [x] [7]H. Durrant-Whyte and T. Bailey, “Simultaneous Localisation and Mapping (SLAM): Part I The Essential Algorithms,” p. 9.
- [x] [8]M. Henein, “Meta Information in Graph-based Simultaneous Localisation And Mapping,” 2021, doi: [10.25911/7RJ5-XS18](https://doi.org/10.25911/7RJ5-XS18).
- [ ] [9]J. Lee and S.-Y. Park, “PLF-VINS: Real-Time Monocular Visual-Inertial SLAM with Point-Line Fusion and Parallel-Line Fusion,” *IEEE Robot. Autom. Lett.*, pp. 1–1, 2021, doi: [10.1109/LRA.2021.3095518](https://doi.org/10.1109/LRA.2021.3095518).
- [ ] [10]M. Yamaguchi, S. Mori, H. Saito, S. Yachida, and T. Shibata, “Global-Map-Registered Local Visual Odometry Using On-the-Fly Pose Graph Updates,” in *Augmented Reality, Virtual Reality, and Computer Graphics*, vol. 12242, L. T. De Paolis and P. Bourdot, Eds. Cham: Springer International Publishing, 2020, pp. 299–311. doi: [10.1007/978-3-030-58465-8_23](https://doi.org/10.1007/978-3-030-58465-8_23).
- [ ] [11]H. Durrant-Whyte and T. Bailey, “Simultaneous localization and mapping: part I,” *IEEE Robot. Automat. Mag.*, vol. 13, no. 2, pp. 99–110, Jun. 2006, doi: [10.1109/MRA.2006.1638022](https://doi.org/10.1109/MRA.2006.1638022).
- [ ] [12]T. Bailey and H. Durrant-Whyte, “Simultaneous localization and mapping (SLAM): part II,” *IEEE Robot. Automat. Mag.*, vol. 13, no. 3, pp. 108–117, Sep. 2006, doi: [10.1109/MRA.2006.1678144](https://doi.org/10.1109/MRA.2006.1678144).
- [ ] [13]M. Jun, Z. Lilian, H. Xiaofeng, Q. Hao, and H. Xiaoping, “Precise Visual-Inertial Localization for UAV with the Aid of A 2D Georeferenced Map,” p. 8.
- [ ] [14]S. Chen, C.-Y. Wen, Y. Zou, and W. Chen, “Stereo Visual Inertial Pose Estimation Based on Feedforward-Feedback Loops,” *arXiv:2007.02250 [cs]*, Jul. 2020, Accessed: Jul. 13, 2021. [Online]. Available: http://arxiv.org/abs/2007.02250
- [ ] [15]I. Hroob, R. Polvara, S. Molina, G. Cielniak, and M. Hanheide, “Benchmark of visual and 3D lidar SLAM systems in simulation environment for vineyards,” *arXiv:2107.05283 [cs]*, Jul. 2021, Accessed: Jul. 13, 2021. [Online]. Available: http://arxiv.org/abs/2107.05283
- [ ] [16]X. Chen *et al.*, “Moving Object Segmentation in 3D LiDAR Data: A Learning-based Approach Exploiting Sequential Data,” *IEEE Robot. Autom. Lett.*, pp. 1–1, 2021, doi: [10.1109/LRA.2021.3093567](https://doi.org/10.1109/LRA.2021.3093567).
- [ ] [17]G. Kim, A. Kim, and Y. Kim, “A new 3D space syntax metric based on 3D isovist capture in urban space using remote sensing technology,” *Computers, Environment and Urban Systems*, vol. 74, pp. 74–87, Mar. 2019, doi: [10.1016/j.compenvurbsys.2018.11.009](https://doi.org/10.1016/j.compenvurbsys.2018.11.009).
- [ ] [18]L. von Rueden, T. Wirtz, F. Hueger, J. D. Schneider, N. Piatkowski, and C. Bauckhage, “Street-Map Based Validation of Semantic Segmentation in Autonomous Driving,” *arXiv:2104.07538 [cs]*, Apr. 2021, Accessed: Jul. 12, 2021. [Online]. Available: http://arxiv.org/abs/2104.07538
- [x] [19]Z. Min and E. Dunn, “VOLDOR-SLAM: For the Times When Feature-Based or Direct Methods Are Not Good Enough,” *arXiv:2104.06800 [cs]*, Apr. 2021, Accessed: Jul. 12, 2021. [Online]. Available: http://arxiv.org/abs/2104.06800
- [ ] [20]J. C. Virgolino Soares, G. F. Abati, G. H. Duarte Lima, and M. A. Meggiolaro, “Autonomous Navigation System for a Wall-painting Robot based on Map Corners,” in *2020 Latin American Robotics Symposium (LARS), 2020 Brazilian Symposium on Robotics (SBR) and 2020 Workshop on Robotics in Education (WRE)*, Natal, Brazil, Nov. 2020, pp. 1–6. doi: [10.1109/LARS/SBR/WRE51543.2020.9306998](https://doi.org/10.1109/LARS/SBR/WRE51543.2020.9306998).
- [ ] [21]M. Aygün *et al.*, “4D Panoptic LiDAR Segmentation,” *arXiv:2102.12472 [cs]*, Apr. 2021, Accessed: Jul. 12, 2021. [Online]. Available: http://arxiv.org/abs/2102.12472
- [x] [22]H. M. S. Bruno and E. L. Colombini, “LIFT-SLAM: a deep-learning feature-based monocular visual SLAM method,” *Neurocomputing*, vol. 455, pp. 97–110, Sep. 2021, doi: [10.1016/j.neucom.2021.05.027](https://doi.org/10.1016/j.neucom.2021.05.027).
- [ ] [23]R. Bao, R. Komatsu, R. Miyagusuku, M. Chino, A. Yamashita, and H. Asama, “Stereo Camera Visual SLAM with Hierarchical Masking and Motion-state Classification at Outdoor Construction Sites Containing Large Dynamic Objects,” *Advanced Robotics*, vol. 35, no. 3–4, pp. 228–241, Feb. 2021, doi: [10.1080/01691864.2020.1869586](https://doi.org/10.1080/01691864.2020.1869586).
- [ ] [24]S. Cao, X. Lu, and S. Shen, “GVINS: Tightly Coupled GNSS-Visual-Inertial Fusion for Smooth and Consistent State Estimation,” *arXiv:2103.07899 [cs]*, Apr. 2021, Accessed: Jul. 12, 2021. [Online]. Available: http://arxiv.org/abs/2103.07899
- [x] [25]H. Durrant‐Whyte, “Where am I? A tutorial on mobile vehicle localization,” *Industrial Robot: An International Journal*, vol. 21, no. 2, pp. 11–16, Jan. 1994, doi: [10.1108/EUM0000000004145](https://doi.org/10.1108/EUM0000000004145).
- [ ] [26]T. Ort, I. Gilitschenski, and D. Rus, “GROUNDED: The Localizing Ground Penetrating Radar Evaluation Dataset,” presented at the Robotics: Science and Systems 2021, Jul. 2021. doi: [10.15607/RSS.2021.XVII.080](https://doi.org/10.15607/RSS.2021.XVII.080).
- [x] [27]A. G. Toudeshki, F. Shamshirdar, and R. Vaughan, “UAV Visual Teach and Repeat Using Only Semantic Object Features,” *arXiv:1801.07899 [cs]*, Jan. 2018, Accessed: Jul. 07, 2021. [Online]. Available: http://arxiv.org/abs/1801.07899
- [x] [28]T. Krajník, P. Cristóforis, K. Kusumam, P. Neubert, and T. Duckett, “Image features for visual teach-and-repeat navigation in changing environments,” *Robotics and Autonomous Systems*, vol. 88, pp. 127–141, Feb. 2017, doi: [10.1016/j.robot.2016.11.011](https://doi.org/10.1016/j.robot.2016.11.011).
- [x] [29]L. Bertoni, S. Kreiss, T. Mordan, and A. Alahi, “MonStereo: When Monocular and Stereo Meet at the Tail of 3D Human Localization,” *arXiv:2008.10913 [cs]*, Mar. 2021, Accessed: Jul. 07, 2021. [Online]. Available: http://arxiv.org/abs/2008.10913
- [ ] [30]P. Yin, L. Xu, J. Zhang, H. Choset, and S. Scherer, “i3dLoc: Image-to-range Cross-domain Localization Robust to Inconsistent Environmental Conditions,” presented at the Robotics: Science and Systems 2021, Jul. 2021. doi: [10.15607/RSS.2021.XVII.027](https://doi.org/10.15607/RSS.2021.XVII.027).
- [ ] [31]S. Schubert, P. Neubert, and P. Protzel, “Fast and Memory Efficient Graph Optimization via ICM for Visual Place Recognition,” presented at the Robotics: Science and Systems 2021, Jul. 2021. doi: [10.15607/RSS.2021.XVII.091](https://doi.org/10.15607/RSS.2021.XVII.091).
  - RSS2021，用于视觉场景重定位

## 2021年6月论文更新

> 更新了11篇SLAM系统相关论文,VT&R的6篇论文,SLAM的综述或者benchmark论文2篇,其他5篇,其中有四篇来自CVPR 2021

### SLAM系统

- [x] [1]S. Chen, C.-W. Chang, and C.-Y. Wen, “**Perception in the Dark; Development of a ToF Visual Inertial Odometry System**,” *Sensors*, vol. 20, no. 5, p. 1263, Feb. 2020, doi: [10.3390/s20051263](https://doi.org/10.3390/s20051263).

  - **ToF-VIO**，[开源](https://github.com/HKPolyU-UAV/TOF-VIO)

- [x] [2]C. Yu *et al.*, “[**DS-SLAM: A Semantic Visual SLAM towards Dynamic Environments,**](https://doi.org/10.1109/IROS.2018.8593691)” *2018 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)*, pp. 1168–1174, Oct. 2018.

  - 动态的语义SLAM（ORB-SLAM2改进）
  - **代码**：https://github.com/ivipsourcecode/DS-SLAM

- [x] [3]T. Ji, C. Wang, and L. Xie, “**[Towards Real-time Semantic RGB-D SLAM in Dynamic Environments,](http://arxiv.org/abs/2104.01316)**” *arXiv:2104.01316 [cs]*, Apr. 2021, Accessed: Apr. 06, 2021.

  -  框架与DS-SLAM类似，目前还未开源，ORB-SLAM2的改进，
  - 深度和几何方法相结合去除语义信息。动态SLAM

- [ ] [4]A. J. Yang, C. Cui, I. A. Bârsan, R. Urtasun, and S. Wang, “[**Asynchronous Multi-View SLAM,**](http://arxiv.org/abs/2101.06562)” *arXiv:2101.06562 [cs]*, Apr. 2021, Accessed: Jul. 01, 2021. 

  - https://www.cs.toronto.edu/~ajyang/amv-slam/

- [ ] [5]A. Cowley, I. D. Miller, and C. J. Taylor, “[**UPSLAM: Union of Panoramas SLAM,**]( http://arxiv.org/abs/2101.00585)” *arXiv:2101.00585 [cs]*, Jan. 2021, Accessed: Jul. 01, 2021. 

  - ICRA2021

- [ ] [6]H. Wang, C. Wang, and L. Xie, “**[Intensity-SLAM: Intensity Assisted Localization and Mapping for Large Scale Environment,](https://doi.org/10.1109/LRA.2021.3059567)**” *IEEE Robot. Autom. Lett.*, vol. 6, no. 2, pp. 1715–1721, Apr. 2021, doi: [10.1109/LRA.2021.3059567](https://doi.org/10.1109/LRA.2021.3059567).

  - 基于激光雷达强度的SLAM
  - [开源](https://github.com/wh200720041/intensity_slam)
  - Han Wang, 南洋理工

- [ ] [7]L. Li, X. Kong, X. Zhao, T. Huang, and Y. Liu, “**[SSC: Semantic Scan Context for Large-Scale Place Recognition,](http://arxiv.org/abs/2107.00382)**” *arXiv:2107.00382 [cs]*, Jul. 2021, Accessed: Jul. 03, 2021. 

  - IROS 2021
  - [开源](https://github.com/lilin-hitcrt/SSC)

- [ ] [8]Y. Chang, Y. Tian, J. P. How, and L. Carlone, “**[Kimera-Multi: a System for Distributed Multi-Robot Metric-Semantic Simultaneous Localization and Mapping,](http://arxiv.org/abs/2011.04087)**” *arXiv:2011.04087 [cs]*, Nov. 2020, Accessed: Jul. 05, 2021. 

  -  分布式SLAM
  - MIT

- [ ] [9]L. Zhang *et al.*, “An autonomous excavator system for material loading tasks,” *Science Robotics*, vol. 6, no. 55, Jun. 2021, doi: [10.1126/scirobotics.abc3164](https://doi.org/10.1126/scirobotics.abc3164).

  - 百度
  - 传感器有用livox

- [ ] [10]C. Forster, L. Carlone, F. Dellaert, and D. Scaramuzza, “IMU Preintegration on Manifold for E cient Visual-Inertial Maximum-a-Posteriori Estimation,” p. 10.

  [11]C. Forster, L. Carlone, F. Dellaert, and D. Scaramuzza, “IMU Preintegration on Manifold for Efficient Visual-Inertial Maximum-a-Posteriori Estimation,” presented at the Robotics: Science and Systems 2015, Jul. 2015. doi: [10.15607/RSS.2015.XI.006](https://doi.org/10.15607/RSS.2015.XI.006).

  - IMU预积分

- [ ] [11]G. Gallego *et al.*, “**[Event-based Vision: A Survey](https://doi.org/10.1109/TPAMI.2020.3008413)**,” *IEEE Transactions on Pattern Analysis and Machine Intelligence*, pp. 1–1, 2020.

### VT&R方面的论文更新

- [x] [1]P. Furgale and T. Barfoot, “**Stereo mapping and localization for long-range path following on rough terrain,**” in *2010 IEEE International Conference on Robotics and Automation*, Anchorage, AK, May 2010, pp. 4410–4416. doi: [10.1109/ROBOT.2010.5509133](https://doi.org/10.1109/ROBOT.2010.5509133).

  [2]P. Furgale and T. Barfoot, “**Visual path following on a manifold in unstructured three-dimensional terrain**,” in *2010 IEEE International Conference on Robotics and Automation*, May 2010, pp. 534–539. doi: [10.1109/ROBOT.2010.5509140](https://doi.org/10.1109/ROBOT.2010.5509140).

  [3]P. Furgale and T. D. Barfoot, “**Visual teach and repeat for long-range rover autonomy: Furgale & Barfoot: Visual Teach and Repeat for Long-Range Rover Autonomy**,” *J. Field Robotics*, vol. 27, no. 5, pp. 534–560, Sep. 2010, doi: [10.1002/rob.20342](https://doi.org/10.1002/rob.20342).

  - VT&R的最开始的文章，使用双目相机作为传感器进行long-range的导航问题。
  - 加拿大宇航局，[数据集](http://asrl.utias.utoronto.ca/~ptf/JFR_VTnR/)

- [x] [4]L. Sun *et al.*, “**Robust and Long-term Monocular Teach and Repeat Navigation using a Single-experience Map**,” *2021 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)*, p. 9.

  - 深度学习的Descriptor
  - 开源

- [ ] [5]M. Mattamala, M. Ramezani, M. Camurri, and M. Fallon, “**Learning Camera Performance Models for Active Multi-Camera Visual Teach and Repeat,**” *arXiv:2103.14070 [cs]*, Mar. 2021, Accessed: Jul. 07, 2021. [Online]. Available: http://arxiv.org/abs/2103.14070

  - ICRA2021, 牛津的四足，作为主动slam的其中一个方面，在给定路径的同时，能够安全进行VT&R的工作，
  - 在仿真和实际中都进行了测试，同时在ICRA 2021的workshop中进行了介绍这种方法的安全性。
  
- [ ] [6]D. Dall’Osto, T. Fischer, and M. Milford, “[**Fast and Robust Bio-inspired Teach and Repeat Navigation,**](http://arxiv.org/abs/2010.11326)” *arXiv:2010.11326 [cs]*, Mar. 2021, Accessed: Jul. 07, 2021.

  - 新的思路去进行VT&R的工作

### SLAM综述：

- [x] [1]G. Huang, “**Visual-Inertial Navigation: A Concise Review,**” *arXiv:1906.02650 [cs]*, Jun. 2019, Accessed: Nov. 18, 2020. [Online]. Available: http://arxiv.org/abs/1906.02650
  - Guoquan Huang
  - VIN的综述

### SLAM Benchmark 

- [ ] [1]M. Bujanca *et al.*, “**SLAMBench 3.0: Systematic Automated Reproducible Evaluation of SLAM Systems for Robot Vision Challenges and Scene Understanding**,” in *2019 International Conference on Robotics and Automation (ICRA)*, Montreal, QC, Canada, May 2019, pp. 6351–6358. doi: [10/ghqdqd](https://doi.org/10/ghqdqd).
  - 对动态SLAM和环境理解（类似语义分割）的slam的Benchmark
  - [开源](https://github.com/mihaibujanca/slambench3)

### 其他

- [x] [0]A. Jelinek, A. Ligocki, and L. Zalud, “**Robotic Template Library,**” *arXiv:2107.00324 [cs]*, Jul. 2021, Accessed: Jul. 03, 2021. [Online]. Available: http://arxiv.org/abs/2107.00324
  - 一种新的机器人的库，可能之后会和PCL等作为竞争品。
  - 开源：https://github.com/Robotics-BUT/Robotic-Template-Library
- [ ] [2]Q. Zhou, T. Sattler, M. Pollefeys, and L. Leal-Taixé, “**To Learn or Not to Learn: Visual Localization from Essential Matrices,**” in *2020 IEEE International Conference on Robotics and Automation (ICRA)*, May 2020, pp. 3319–3326. doi: [10/gh9smf](https://doi.org/10/gh9smf).
  - 视觉定位，基于学习或者基于传统方法的比较，提出了新的方法
- [ ] J. Li and G. H. Lee, “**[DeepI2P: Image-to-Point Cloud Registration via Deep Classification](http://arxiv.org/abs/2104.03501)**,” arXiv:2104.03501 [cs], Apr. 2021, Accessed: Jul. 29, 2021.CVPR
  - 点云和图像的配准
- [ ] M. Geppert, V. Larsson, P. Speciale, J. L. Schonberger, and M. Pollefeys, “[**Privacy Preserving Localization and Mapping From Uncalibrated Cameras**](https://openaccess.thecvf.com/content/CVPR2021/papers/Geppert_Privacy_Preserving_Localization_and_Mapping_From_Uncalibrated_Cameras_CVPR_2021_paper.pdf),” p. 11.
  - ETH做的关于云端SLAM的隐私保护问题，出现了隐私保护的文章，主要针对需要云服务的一些SLAM应用，目前已经做了几篇文章
  - 还未开源，目前这部分还不知道能做啥，
- [ ] P. Karkus, S. Cai, and D. Hsu, “**Differentiable SLAM-net: Learning Particle SLAM for Visual Navigation,**” arXiv:2105.07593 [cs, stat], May 2021, Accessed: Jul. 29, 2021. [Online]. Available: http://arxiv.org/abs/2105.07593，CVPR
- [ ] S. H. Lee and J. Civera, “**Rotation-Only Bundle Adjustment,**” arXiv:2011.11724 [cs], Mar. 2021, Accessed: Jul. 29, 2021. [Online]. Available: http://arxiv.org/abs/2011.11724
  - MATLAB的代码
  - 对旋转的BA

## 2021年5月论文更新

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
- [x] [12]M. Labbé and F. Michaud, “[**RTAB-Map as an open-source lidar and visual simultaneous localization and mapping library for large-scale and long-term online operation**](https://doi.org/10/gf3bgd),” *Journal of Field Robotics*, vol. 36, no. 2, pp. 416–446, 2019, doi: [10/gf3bgd](https://doi.org/10/gf3bgd).
  - RTab Map, 多传感器融合的一个好的框架，论文综述了许多SLAM算法的优缺点。**还没读完**
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

## 2021年4月论文更新

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





