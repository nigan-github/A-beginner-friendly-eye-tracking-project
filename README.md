# A-beginner-friendly-eye-tracking-project
This project integrates existing resources with AI-assisted development to provide a beginner-friendly guide to eye tracking, covering everything from hardware to software. Everyone is welcome to share ideas, ask questions, and contribute to the discussion.
## 0. Eye Tracking Demo| 效果演示

<img width="1006" height="1494" alt="89461c7a895c3029805c56d1312be311" src="https://github.com/user-attachments/assets/aa48070f-f7d3-4fcf-98e5-2cbb460ff3fd" />
<img width="1000" height="1227" alt="24c4073f273a06f8a8117f02e8c4c7d2" src="https://github.com/user-attachments/assets/265e2afb-de97-4c1a-b68f-426c88791a9f" />


## 1. Principles of Eye Tracking | 眼动追踪原理

Eye tracking is a technology used to measure eye movements, estimate gaze direction, and determine gaze positions. Camera-based eye tracking systems capture eye images and extract ocular features to estimate eye movements and gaze direction.

眼动追踪是一种用于测量眼球运动、估计视线方向及确定注视位置的技术。视觉式眼动追踪系统通过摄像头获取眼部图像，提取眼部特征，实现眼球运动检测与视线估计。

### 1.1 Camera Configuration | 摄像头部署方式

- **Near-eye Tracking（近眼式眼动追踪）：** The camera is mounted close to the eye, typically on glasses or a headset, to capture detailed eye images.

  摄像头安装于眼睛附近，通常集成于眼镜或头戴式设备中，以获取清晰的眼部图像。

- **Remote Tracking（远距离眼动追踪）：** The camera is positioned away from the user, typically near a display, enabling eye tracking without wearable devices.

  摄像头安装于距离用户较远的位置，通常位于显示器附近，无需佩戴设备即可实现眼动追踪。

### 1.2 Illumination Methods | 光学成像方式

Near-infrared (NIR) illumination is commonly used to improve pupil contrast. Depending on the relative positions of the light source and camera, two imaging methods can be implemented:

近红外光常用于增强瞳孔与周围组织的对比度。根据光源与摄像头的相对位置，可分为以下两种成像方式：

- **Bright Pupil（明瞳法）：** The light source is positioned close to the camera's optical axis, allowing retinal reflections to enter the camera and produce a bright pupil.

  光源靠近摄像头光轴，眼底反射光进入摄像头，使瞳孔呈现明亮状态。

- **Dark Pupil（暗瞳法）：** The light source is positioned off-axis, reducing retinal reflections captured by the camera and producing a dark pupil.

  光源偏离摄像头光轴，减少进入摄像头的眼底反射光，使瞳孔呈现较暗状态。

### 1.3 Gaze Estimation Methods | 视线估计方法

- **Pupil Center Corneal Reflection (PCCR)（瞳孔中心–角膜反射法）：** Estimates gaze direction using the relative positions of the pupil center and corneal reflections.

  利用瞳孔中心与角膜反射光斑的相对位置估计视线方向。

- **3D Model-Based Tracking（三维眼球模型法）：** Reconstructs a geometric eye model from ocular features, such as pupil ellipses, to estimate the three-dimensional gaze direction.

  根据瞳孔椭圆等眼部特征构建三维眼球几何模型，从而估计三维视线方向。

- **Appearance-Based Tracking（基于外观的方法）：** Estimates gaze directly from eye or facial images using machine learning or deep learning algorithms.

  利用机器学习或深度学习算法，直接根据眼部或面部图像估计视线方向。

### 1.4 Technical Approach of This Project | 本项目技术路线

This project references the open-source 3D-Eye-Tracker project and adopts a near-eye, dark-pupil, infrared imaging approach combined with 3D geometric eye model fitting.

An infrared camera captures close-up eye images. Image processing algorithms detect the pupil contour and fit a two-dimensional ellipse. Multiple pupil observations collected at different gaze angles are then used to initialize a three-dimensional eye model and estimate the eyeball center, pupil diameter, and gaze direction.

本项目参考开源项目 3D-Eye-Tracker，采用近眼式红外暗瞳成像与三维眼球几何模型相结合的眼动追踪方案。

通过红外摄像头近距离采集眼部图像，利用图像处理算法提取瞳孔轮廓并进行二维椭圆拟合。进一步结合不同视线角度下的瞳孔观测结果建立三维眼球模型，实现眼球中心、瞳孔直径及三维视线方向的估计。

### 1.5 References | 参考资料

1. [YutaItoh / 3D-Eye-Tracker](https://github.com/YutaItoh/3D-Eye-Tracker)
2. [JEOresearch](https://github.com/JEOresearch/EyeTracker/tree/main)

## 2. Camera Selection | 摄像头的选择
For beginners, the required hardware can be purchased directly from online shopping platforms such as Taobao(https://item.taobao.com/item.htm?abbucket=13&id=607636857800&mi_id=00005sir7R9VxTKud8jcXHDX1EIdmDA9XZTitSUxySfJLAI&ns=1&priceTId=213e030917955788657404356e1a52&skuId=5545237762697&spm=a21n57.1.hoverItem.1&utparam=%7B%22aplus_abtest%22%3A%221ff74010226bd5d7e4d918fc5cf220ac%22%7D&xxc=taobaoSearch). In this project, we selected a near-eye camera, with focal length and field of view (FOV) as the key parameters to consider. Hardware stability and image quality have a significant impact on the accuracy and reliability of eye tracking. 
## 3. Software Development | 软件功能的实现

By referring to existing open-source projects, such as [3D-Eye-Tracker](https://github.com/YutaItoh/3D-Eye-Tracker), and leveraging AI-assisted programming, beginners can develop their own eye tracking software. By incorporating calibration procedures used in commercial eye tracking systems, such as EyeLink, and further refining the code with AI assistance, a basic functional eye tracking application can be developed.

参考 [3D-Eye-Tracker](https://github.com/YutaItoh/3D-Eye-Tracker) 等现有开源项目，结合 AI 辅助编程，初学者即可完成眼动追踪软件的开发。进一步参考 EyeLink 等商业眼动追踪系统的校准流程，利用 AI 对软件代码进行修改和优化，即可获得初步可用的眼动追踪软件。

## 4. Limitations and Future Directions | 现存问题与展望

Although this eye tracking prototype was successfully developed using a USB camera and AI-assisted programming, several limitations remain:

尽管基于 USB 摄像头和 AI 辅助编程初步实现了眼动追踪功能，但目前的演示系统仍存在以下问题：

1. **Sensitivity to Head Movement | 对头部运动敏感**

   Head movement introduces significant tracking errors. Therefore, the user's head needs to remain relatively stationary during operation.

   头部晃动会引入较大的追踪误差，因此使用过程中需要保持头部相对固定。

2. **Calibration and Accuracy | 校准与准确度**

   Frequent recalibration is required, and relatively large gaze estimation errors may remain even after calibration.

   系统需要频繁进行重新校准，且校准后仍可能存在较大的视线估计误差。

3. **Hardware Reliability | 硬件可靠性**

   The USB connection of the camera is prone to loosening, which may affect the stability and continuity of image acquisition.

   摄像头的 USB 接口容易松动，可能影响图像采集的稳定性和连续性。

Future improvements will focus on head movement compensation, calibration optimization, gaze estimation accuracy, and hardware reliability.

后续将重点围绕头部运动补偿、校准算法优化、视线估计准确度及硬件可靠性等方面开展改进。

## 5. Open Discussion | 开放交流

Everyone is welcome to discuss the technical details of this project, share suggestions, and explore potential improvements. We are also open to exchanging other innovative ideas in science and technology. We are passionate about meaningful scientific research and technological innovation, and look forward to learning and exploring together.

欢迎大家讨论本项目的相关技术细节，提出改进建议，共同探索潜在的优化方案。如果有其他科学研究或技术创新方面的想法，也欢迎交流。我们对有意义的科学研究和技术创新充满兴趣，期待与大家共同学习和探索。
