# Awesome 3D Gaussian Splatting Resources 

A curated list of papers and open-source resources focused on 3D Gaussian Splatting, intended to keep pace with the anticipated surge of research in the coming months. If you have any additions or suggestions, feel free to contribute. Additional resources like blog posts, videos, etc. are also welcome.

## Table of contents

- [Seminal Paper introducing 3D Gaussian Splatting](#seminal-paper-introducing-3d-gaussian-splatting)
<br>

- [Autonomous Driving](#autonomous-driving)
- [Avatars](#avatars)
- [Classic work](#classic-work)
- [Compression](#compression)
- [Diffusion](#diffusion)
- [Dynamics and Deformation](#dynamics-and-deformation)
- [Editing](#editing)
- [Language Embedding](#language-embedding)
- [Mesh Extraction and Physics](#mesh-extraction-and-physics)
- [Misc](#misc)
- [Regularization and Optimization](#regularization-and-optimization)
- [Rendering](#rendering)
- [Reviews](#reviews)
- [SLAM](#slam)
- [Sparse](#sparse)

<br>

- [Data](#data)
- [Courses](#courses)

<br>

- [Open Source Implementations](#open-source-implementations)
  * [Reference](#reference)
  * [Unofficial Implementations](#unofficial-implementations)
  * [2D Gaussian Splatting](#2d-gaussian-splatting)
  * [Game Engines](#game-engines)
  * [Viewers](#viewers)
  * [Utilities](#utilities)
  * [Other](#other)
<br>

- [Blog Posts](#blog-posts)
- [Tutorial Videos](#tutorial-videos)
- [Credits](#credits)


<details span>
<summary><b>Update Log:</b></summary>
<br>

 **March 6, 2024**:
 - 1 paper added: Splat-Nav

 **March 5, 2024**:
 - 1 paper added: 3DGStream
 - Code releases 
 - New viewer added

 **March 2, 2024**:
 - 1 paper added: 3D Gaussian Model for Animation and Texturing
 - New section: Courses that also teach 3DGS.

 **February 28, 2024**:
 - VastGaussian

 **February 27, 2024**:
- 2 papers added: Spec-Gaussian and GEA
- SC-GS code released

 **February 24, 2024**:
- 2 papers added: Identifying unnecessary Gaussians and Gaussian Pro

 **February 23, 2024**:
 - Corrected Authors and updated abstract for EndoGS: Deformable Endoscopic Tissues Reconstruction with Gaussian Splatting

 **February 21, 2024**:
 - Added one paper: Reshaping SLAM: a Survey

 **February 20, 2024**:
 - GaussianObject code released
 - Added one paper: GaussianHair

 **February 19, 2024**:
 - Blog post added: NeRFs vs. 3DGS.

 **February 16, 2024**:
 - 2 papers added: IM-3D and GES
 - GaMeS code released

 **February 14, 2024**:
 - Added viewer: VulkanSplatting - cross-platform, high performance 3DGS renderer in C++ and Vulkan Compute

 **February 13, 2024**:
 - Code releases: (16th Jan 2024) Real-time Photorealistic Dynamic Scene Representation and Rendering with 4D Gaussian Splatting
 - 3 papers added: 3DGala, ImplicitDeepFake, and 3D Gaussians as a New Vision Era.
 
 **February 9, 2024**:
 - 1 paper added: HeadStudio

 **February 8, 2024**:
 - 3 papers added: Rig3DGS, Mesh-based GS, and LGM
 **February 6, 2024**:
 - Added 2 papers: SGS-SLAM and 4D Gaussian Splatting

 **February 5, 2024**:
 - Moved SWAGS to Dynmatics and Deformation section
 - Added 2 paper: GaussianObject and GaMeSh
 - GS++ renamed to Optimal Projection
 
 **February 2, 2024**:
  - Added 6 papers: VR-GS, Segment Anything, Gaussian Splashing, GS++, 360-GS, and StopThePop
  - TRIPS code release

 **January 30, 2024**:
  - Code changes: GaussianAvatars code changed to private

 **January 29, 2024**:
 - Added 2 papers: LIV-GaussMap and TIP-Editor

 **January 26, 2024**:
 - Removed retracted paper: Animatable 3D Gaussians for High-fidelity Synthesis of Human Motions
 - 3 papers added: EndoGaussians, PSAvatar, and GauU-Scene

 **January 25, 2024**:
 - Added viewer: Splatapult - 3d gaussian splatting renderer in C++ and OpenGL, works with OpenXR for tethered VR

 **January 24, 2024**:
 - Added utility: GSOPs (Gaussian Splat Operators) for SideFX Houdini
 - Code releases: GaussianAvatars

 **January 23, 2024**:
 - 3 papers added: Amortized Gen3D, Deformable Endoscopic Tissues, Fast dynamic 3D Object Generation
 - Code releases: Animatable Avatars, Compressed 3D Gaussians, GaussianAvatar
 
 **January 13, 2024**:
 - 4 papers added: CoSSegGaussians, TRIPS, Gaussian Shadow Casting for Neural Characters and DISTWAR

 **January 9, 2024**:
 - 1 paper added: A Survey on 3D Gaussian Splatting (The first survey)
 
 **January 8, 2024**:
 - 4 papers added: SWAGS (added paper from 2023 which I forgot to add before, ), first review paper, compressed 3DGS, and an application paper for Characterizing Satellite Geometry.
 
 **January 7, 2024**:
 - 1 Open source implementation: taichi-splatting - work is originally derived off Taichi 3D Gaussian Splatting, with significant re-organisation and changes.

 **January 5, 2024**:
 - 3 papers added: FMGS, PEGASUS, and Repaint123.

 **January 2, 2024**:
 - 1 paper added: Street Gaussians.

 **January 2, 2024**:
 - Deblurring Gaussians paper link updated.
 - SAGA code released.
 - 2 papers from 2023 added: Text2Immersion and 2D-Guided 3DG Segmentation.
 - Mathematical supplemend of gsplat lib.
 - Add years in categories.
 - GSM code released.

 **December 29, 2023**:
 - 1 paper added (apparently missed that one before): Gaussian-Head-Avatar.
 - Blog post head avatars added.

 **December 29, 2023**:
 - 3 papers added: DreamGaussian4D, 4DGen, and Spacetime Gaussian.

 **December 27, 2023**:
 - 3 papers added: LangSplat, Deformable 3DGS, and Human101.
 - Blog post added: Comprehensive Review of 3DGS.

 **December 25, 2023**:
 - Efficient 3D Gaussian Representation for Monocular/Multi-view Dynamic Scenes code released. 
 - GPS-Gaussian code released.

 **December 24, 2023**:
 - 2 papers added: Self-Organization Gaussian Grids and Gaussian Splitting.
 - Added repo for enhancing Gaussian rendering to model more complex scenes. 

 **December 21, 2023**:
 - 3 papers added: Splatter Image, pixelSplat, and align your gaussians.
 - Gaussian Grouping code released.

 **December 19, 2023**:
 - 2 papers added: GAvatar and GauFRe.

 **December 18, 2023**:
  - Added utility: SpectacularAI - Conversion scripts for different 3DGS conventions.
  - SuGaR code released.

 **December 16, 2023**:
  - Added WebGL viewer 3: Gauzilla.

 **December 15, 2023**:
  - 4 papers added: DrivingGaussian, iComMa, Triplane, and 3DGS-Avatar.
  - Relightable Gaussians code released.

 **December 13, 2023**:
  - 5 papers added: Gaussian-SLAM, CoGS, ASH, CF-GS, and Photo-SLAM.

 **December 11, 2023**:
  - 2 papers added: Gaussian Splatting SLAM and Denoising Scores for 3D Generation.
  - ScaffoldGS code released.

 **December 8, 2023**:
  - 2 papers added: EAGLES and MonoGaussianAvatar.

 **December 7, 2023**:
  - LucidDreamer code released.
  - 9 papers added: GauHuman, HeadGaS, HiFi4G, Gaussian-Flow, Feature-3DGS, Gaussian-Avatar, FlashAvatar, Relightable, and Deblurring Gaussians.

 **December 5, 2023**:
  - 9 papers added: NeuSG, GaussianHead, GaussianAvatars, GPS-Gaussian, Neural Parametric Gaussians for Monocular Non-Rigid Object Reconstruction, SplaTAM, MANUS, Segment Any, and Language embedded 3D Gaussians.

 **December 4, 2023**:
  - 8 papers added: Gaussian Grouping, MD Splatting, DynMF, Scaffold-GS, SparseGS, FSGS, Control4D, and SC-GS.

 **December 1, 2023**:
  - 4 papers added: Compact3D, GaussianShader, Periodic Vibration Gaussian and Gaussian Shell Maps for Efficient 3D Human Generation.
  - Created Table of contents for each category and added line breaks.

 **November 30, 2023**:
  - Added Unreal game engine implementation.
  - 5 papers added: LightGaussian, FisherRF, HUGS, HumanGaussian, CG3D, and Multi Scale 3DGS.
  
 **November 29, 2023**:
  - Added two papers: Point and Move and IR-GS.

 **November 28, 2023**:
  - Added five papers: GaussinEditor, Relightable Gaussians, GART, Mip-Splatting, HumanGaussian.

 **November 27, 2023**:
  - Added two papers: Gaussian Editing and Compact 3D Gaussians.

 **November 25, 2023**:
  - Animatable Gaussians project added (paper not yet released).

 **November 22, 2023**:
  - 3 new GS papers added: Animatable, Depth-Regularized, and Monocular/Multi-view 3DGS.
  - Added some classic papers.
  - Added another GS paper also called LucidDreamer.

 **November 21, 2023**:
  - 3 new GS papers added: GaussianDiffusion, LucidDreamer, PhysGaussian.
  - 2 more GS papers added: SuGaR, PhysGaussian.

 **November 21, 2023**:
  - Added the paper GS-SLAM

**November 17, 2023**:
  - Added PlayCanvas implementation to Game Engines section.

 **November 16, 2023**:
  - Deformable 3D Gaussians code released.
  - Drivable 3D Gaussian Avatars paper added. 

 **November 8, 2023**:
  - Some notes about the 3DGS implementation and unsive/rsal format discussion.

 **November 4, 2023**:
  - Added 2D gaussian splatting.
  - Added very detailed (technical) blog post explaining 3D gaussian splatting.

 **October 28, 2023**:
  - Added Utilities Section.
  - Added 3DGS Converter for editing 3DGS .ply files in Cloud Compare to Utilities.
  - Added Kapture (for bundler to colmap model conversion) and Kapture image cropper script with conversion instructions to Utilities.

 **October 23, 2023**:
  - Added python WebGL viewer 2.
  - Added Intro to gaussian splatting (and Unity viewer) video blog.

  **October 21, 2023**:
  - Added python OpenGL viewer.
  - Added typescript WebGPU viewer.

  **October 20, 2023**:
  - Made abstracts readable (removed hyphenations).
  - Added Windows tutorial.
  - Other minor text fixes.
  - Added Jupyter notebook viewer.

**October 19, 2023**: 
  - Added Github page link for Real-time Photorealistic Dynamic Scene Representation.
  - Re-ordered headings.
  - Added other unofficial implementations.
  - Moved Nerfstudio gsplat and fast: C++/CUDA to Unofficial Implementations.
  - Added Nerfstudio, Blender, WebRTC, iOS & Metal viewers.

**October 17, 2023**: 
  - GaussianDreamer code released.
  - Added Real-time Photorealistic Dynamic Scene Representation.

**October 16, 2023**: 
  - Added Deformable 3D Gaussians paper.
  - Dynamic 3D Gaussians code released.
**October 15, 2023**: Initial list with first 6 papers.
</details>

<br>

## Seminal Paper introducing 3D Gaussian Splatting:
### 3D Gaussian Splatting for Real-Time Radiance Field Rendering
**Authors**: Bernhard Kerbl, Georgios Kopanas, Thomas Leimkühler, George Drettakis

<details span>
<summary><b>Abstract</b></summary>
Radiance Field methods have recently revolutionized novel-view synthesis
of scenes captured with multiple photos or videos. However, achieving high
visual quality still requires neural networks that are costly to train and render,
while recent faster methods inevitably trade off speed for quality. For
unbounded and complete scenes (rather than isolated objects) and 1080p
resolution rendering, no current method can achieve real-time display rates.
We introduce three key elements that allow us to achieve state-of-the-art
visual quality while maintaining competitive training times and importantly
allow high-quality real-time (≥ 30 fps) novel-view synthesis at 1080p resolution.
First, starting from sparse points produced during camera calibration,
we represent the scene with 3D Gaussians that preserve desirable properties
of continuous volumetric radiance fields for scene optimization while
avoiding unnecessary computation in empty space; Second, we perform
interleaved optimization/density control of the 3D Gaussians, notably optimizing
anisotropic covariance to achieve an accurate representation of the
scene; Third, we develop a fast visibility-aware rendering algorithm that
supports anisotropic splatting and both accelerates training and allows real-time
rendering. We demonstrate state-of-the-art visual quality and real-time
rendering on several established datasets.
</details>
  
  [📄 Paper (Low Resolution)](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/3d_gaussian_splatting_low.pdf) | [📄 Paper (High Resolution)](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/3d_gaussian_splatting_high.pdf) | [🌐 Project Page](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/) | [💻 Code](https://github.com/graphdeco-inria/gaussian-splatting) | [🎥 Short Presentation](https://youtu.be/T_kXY43VZnk?si=DrkbDFxQAv5scQNT) | [🎥 Explanation Video](https://www.youtube.com/live/xgwvU7S0K-k?si=edF8NkYtsRbgTbKi)

<br>

## Autonomous Driving:
## 2024:
### 1. Street Gaussians for Modeling Dynamic Urban Scenes  
**Authors**: Yunzhi Yan, Haotong Lin, Chenxu Zhou, Weijie Wang, Haiyang Sun, Kun Zhan, Xianpeng Lang, Xiaowei Zhou, Sida Peng 
<details span>
<summary><b>Abstract</b></summary>
This paper aims to tackle the problem of modeling dynamic urban street scenes from monocular videos. Recent methods extend NeRF by incorporating tracked vehicle poses to animate vehicles, enabling photo-realistic view synthesis of dynamic urban street scenes. However, significant limitations are their slow training and rendering speed, coupled with the critical need for high precision in tracked vehicle poses. We introduce Street Gaussians, a new explicit scene representation that tackles all these limitations. Specifically, the dynamic urban street is represented as a set of point clouds equipped with semantic logits and 3D Gaussians, each associated with either a foreground vehicle or the background. To model the dynamics of foreground object vehicles, each object point cloud is optimized with optimizable tracked poses, along with a dynamic spherical harmonics model for the dynamic appearance. The explicit representation allows easy composition of object vehicles and background, which in turn allows for scene editing operations and rendering at 133 FPS (1066×1600 resolution) within half an hour of training. The proposed method is evaluated on multiple challenging benchmarks, including KITTI and Waymo Open datasets. Experiments show that the proposed method consistently outperforms state-of-the-art methods across all datasets. Furthermore, the proposed representation delivers performance on par with that achieved using precise ground-truth poses, despite relying only on poses from an off-the-shelf tracker.
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.01339.pdf) | [🌐 Project Page](https://zju3dv.github.io/street_gaussians/) | [💻 Code (not yet)](https://github.com/zju3dv/street_gaussians) 

## 2023:
### 1. DrivingGaussian: Composite Gaussian Splatting for Surrounding Dynamic Autonomous Driving Scenes  
**Authors**: Xiaoyu Zhou, Zhiwei Lin, Xiaojun Shan, Yongtao Wang, Deqing Sun, Ming-Hsuan Yang 
<details span>
<summary><b>Abstract</b></summary>
We present DrivingGaussian, an efficient and effective framework for surrounding dynamic autonomous driving scenes. For complex scenes with moving objects, we first sequentially and progressively model the static background of the entire scene with incremental static 3D Gaussians. We then leverage a composite dynamic Gaussian graph to handle multiple moving objects, individually reconstructing each object and restoring their accurate positions and occlusion relationships within the scene. We further use a LiDAR prior for Gaussian Splatting to reconstruct scenes with greater details and maintain panoramic consistency. DrivingGaussian outperforms existing methods in driving scene reconstruction and enables photorealistic surround-view synthesis with high-fidelity and multi-camera consistency.
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.07920.pdf) | [🌐 Project Page](https://pkuvdig.github.io/DrivingGaussian/) | [💻 Code (not yet)]() 

<br>

## Avatars:
## 2024:
### 1. GaussianBody: Clothed Human Reconstruction via 3d Gaussian Splatting 
**Authors**: Mengtian Li, Shengxiang Yao, Zhifeng Xie, Keyu Chen, Yu-Gang Jiang 
<details span>
<summary><b>Abstract</b></summary>
In this work, we propose a novel clothed human reconstruction method called GaussianBody, based on 3D Gaussian Splatting. Compared with the costly neural radiance based models, 3D Gaussian Splatting has recently demonstrated great performance in terms of training time and rendering quality. However, applying the static 3D Gaussian Splatting model to the dynamic human reconstruction problem is non-trivial due to complicated non-rigid deformations and rich cloth details. To address these challenges, our method considers explicit pose-guided deformation to associate dynamic Gaussians across the canonical space and the observation space, introducing a physically-based prior with regularized transformations helps mitigate ambiguity between the two spaces. During the training process, we further propose a pose refinement strategy to update the pose regression for compensating the inaccurate initial estimation and a split-with-scale mechanism to enhance the density of regressed point clouds. The experiments validate that our method can achieve state-of-the-art photorealistic novel-view rendering results with high-quality details for dynamic clothed human bodies, along with explicit geometry reconstruction. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.09720.pdf)  

### 2. PSAvatar: A Point-based Morphable Shape Model for Real-Time Head Avatar Creation with 3D Gaussian Splatting 
**Authors**: Zhongyuan Zhao, Zhenyu Bao, Qing Li, Guoping Qiu, Kanglin Liu 
<details span>
<summary><b>Abstract</b></summary>
Despite much progress, achieving real-time high-fidelity head avatar animation is still difficult and existing methods have to trade-off between speed and quality. 3DMM based methods often fail to model non-facial structures such as eyeglasses and hairstyles, while neural implicit models suffer from deformation inflexibility and rendering inefficiency. Although 3D Gaussian has been demonstrated to possess promising capability for geometry representation and radiance field reconstruction, applying 3D Gaussian in head avatar creation remains a major challenge since it is difficult for 3D Gaussian to model the head shape variations caused by changing poses and expressions. In this paper, we introduce PSAvatar, a novel framework for animatable head avatar creation that utilizes discrete geometric primitive to create a parametric morphable shape model and employs 3D Gaussian for fine detail representation and high fidelity rendering. The parametric morphable shape model is a Point-based Morphable Shape Model (PMSM) which uses points instead of meshes for 3D representation to achieve enhanced representation flexibility. The PMSM first converts the FLAME mesh to points by sampling on the surfaces as well as off the meshes to enable the reconstruction of not only surface-like structures but also complex geometries such as eyeglasses and hairstyles. By aligning these points with the head shape in an analysis-by-synthesis manner, the PMSM makes it possible to utilize 3D Gaussian for fine detail representation and appearance modeling, thus enabling the creation of high-fidelity avatars. We show that PSAvatar can reconstruct high-fidelity head avatars of a variety of subjects and the avatars can be animated in real-time (≥ 25 fps at a resolution of 512 × 512 ). 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.12900.pdf)  

### 3. Rig3DGS: Creating Controllable Portraits from Casual Monocular Videos 
**Authors**: Alfredo Rivero, ShahRukh Athar, Zhixin Shu, Dimitris Samaras 
<details span>
<summary><b>Abstract</b></summary>
Creating controllable 3D human portraits from casual smartphone videos is highly desirable due to their immense value in AR/VR applications. The recent development of 3D Gaussian Splatting (3DGS) has shown improvements in rendering quality and training efficiency. However, it still remains a challenge to accurately model and disentangle head movements and facial expressions from a single-view capture to achieve high-quality renderings. In this paper, we introduce Rig3DGS to address this challenge. We represent the entire scene, including the dynamic subject, using a set of 3D Gaussians in a canonical space. Using a set of control signals, such as head pose and expressions, we transform them to the 3D space with learned deformations to generate the desired rendering. Our key innovation is a carefully designed deformation method which is guided by a learnable prior derived from a 3D morphable model. This approach is highly efficient in training and effective in controlling facial expressions, head positions, and view synthesis across various captures. We demonstrate the effectiveness of our learned deformation through extensive quantitative and qualitative experiments.
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.03723.pdf) | [🌐 Project Page](http://shahrukhathar.github.io/2024/02/05/Rig3DGS.html) 

### 4. HeadStudio: Text to Animatable Head Avatars with 3D Gaussian Splatting 
**Authors**: Zhenglin Zhou, Fan Ma, Hehe Fan, Yi Yang 
<details span>
<summary><b>Abstract</b></summary>
Creating digital avatars from textual prompts has long been a desirable yet challenging task. Despite the promising outcomes obtained through 2D diffusion priors in recent works, current methods face challenges in achieving high-quality and animated avatars effectively. In this paper, we present HeadStudio, a novel framework that utilizes 3D Gaussian splatting to generate realistic and animated avatars from text prompts. Our method drives 3D Gaussians semantically to create a flexible and achievable appearance through the intermediate FLAME representation. Specifically, we incorporate the FLAME into both 3D representation and score distillation: 1) FLAME-based 3D Gaussian splatting, driving 3D Gaussian points by rigging each point to a FLAME mesh. 2) FLAME-based score distillation sampling, utilizing FLAME-based fine-grained control signal to guide score distillation from the text prompt. Extensive experiments demonstrate the efficacy of HeadStudio in generating animatable avatars from textual prompts, exhibiting visually appealing appearances. The avatars are capable of rendering high-quality real-time (≥40 fps) novel views at a resolution of 1024. They can be smoothly controlled by real-world speech and video. We hope that HeadStudio can advance digital avatar creation and that the present method can widely be applied across various domains. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.06149.pdf) |  [🌐 Project Page](https://zhenglinzhou.github.io/HeadStudio-ProjectPage/) | [💻 Code (not yet)](https://github.com/ZhenglinZhou/HeadStudio/)

### 5. ImplicitDeepfake: Plausible Face-Swapping through Implicit Deepfake Generation using NeRF and Gaussian Splatting 
**Authors**: Georgii Stanishevskii, Jakub Steczkiewicz, Tomasz Szczepanik, Sławomir Tadeja, Jacek Tabor, Przemysław Spurek 
<details span>
<summary><b>Abstract</b></summary>
Numerous emerging deep-learning techniques have had a substantial impact on computer graphics. Among the most promising breakthroughs are the recent rise of Neural Radiance Fields (NeRFs) and Gaussian Splatting (GS). NeRFs encode the object's shape and color in neural network weights using a handful of images with known camera positions to generate novel views. In contrast, GS provides accelerated training and inference without a decrease in rendering quality by encoding the object's characteristics in a collection of Gaussian distributions. These two techniques have found many use cases in spatial computing and other domains. On the other hand, the emergence of deepfake methods has sparked considerable controversy. Such techniques can have a form of artificial intelligence-generated videos that closely mimic authentic footage. Using generative models, they can modify facial features, enabling the creation of altered identities or facial expressions that exhibit a remarkably realistic appearance to a real person. Despite these controversies, deepfake can offer a next-generation solution for avatar creation and gaming when of desirable quality. To that end, we show how to combine all these emerging technologies to obtain a more plausible outcome. Our ImplicitDeepfake1 uses the classical deepfake algorithm to modify all training images separately and then train NeRF and GS on modified faces. Such relatively simple strategies can produce plausible 3D deepfake-based avatars.
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.06390.pdf) | [💻 Code (not yet)](https://github.com/quereste/implicit-deepfake)

### 6. GaussianHair: Hair Modeling and Rendering with Light-aware Gaussians 
**Authors**: Haimin Luo, Min Ouyang, Zijun Zhao, Suyi Jiang, Longwen Zhang, Qixuan Zhang, Wei Yang, Lan Xu, Jingyi Yu 
<details span>
<summary><b>Abstract</b></summary>
Hairstyle reflects culture and ethnicity at first glance. In the digital era, various realistic human hairstyles are also critical to high-fidelity digital human assets for beauty and inclusivity. Yet, realistic hair modeling and real-time rendering for animation is a formidable challenge due to its sheer number of strands, complicated structures of geometry, and sophisticated interaction with light. This paper presents GaussianHair, a novel explicit hair representation. It enables comprehensive modeling of hair geometry and appearance from images, fostering innovative illumination effects and dynamic animation capabilities. At the heart of GaussianHair is the novel concept of representing each hair strand as a sequence of connected cylindrical 3D Gaussian primitives. This approach not only retains the hair's geometric structure and appearance but also allows for efficient rasterization onto a 2D image plane, facilitating differentiable volumetric rendering. We further enhance this model with the "GaussianHair Scattering Model", adept at recreating the slender structure of hair strands and accurately capturing their local diffuse color in uniform lighting. Through extensive experiments, we substantiate that GaussianHair achieves breakthroughs in both geometric and appearance fidelity, transcending the limitations encountered in state-of-the-art methods for hair reconstruction. Beyond representation, GaussianHair extends to support editing, relighting, and dynamic rendering of hair, offering seamless integration with conventional CG pipeline workflows. Complementing these advancements, we have compiled an extensive dataset of real human hair, each with meticulously detailed strand geometry, to propel further research in this field. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.10483.pdf)

### 7. GEA: Reconstructing Expressive 3D Gaussian Avatar from Monocular Video  
**Authors**: Xinqi Liu, Chenming Wu, Xing Liu, Jialun Liu, Jinbo Wu, Chen Zhao, Haocheng Feng, Errui Ding, Jingdong Wang 
<details span>
<summary><b>Abstract</b></summary>
This paper presents GEA, a novel method for creating expressive 3D avatars with high-fidelity reconstructions of body and hands based on 3D Gaussians. The key contributions are twofold. First, we design a two-stage pose estimation method to obtain an accurate SMPL-X pose from input images, providing a correct mapping between the pixels of a training image and the SMPL-X model. It uses an attention-aware network and an optimization scheme to align the normal and silhouette between the estimated SMPL-X body and the real body in the image. Second, we propose an iterative re-initialization strategy to handle unbalanced aggregation and initialization bias faced by Gaussian representation. This strategy iteratively redistributes the avatar's Gaussian points, making it evenly distributed near the human body surface by applying meshing, resampling and re-Gaussian operations. As a result, higher-quality rendering can be achieved. Extensive experimental analyses validate the effectiveness of the proposed model, demonstrating that it achieves state-of-the-art performance in photorealistic novel view synthesis while offering fine-grained control over the human body and hand pose.
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.16607.pdf) |  [🌐 Project Page](https://3d-aigc.github.io/GEA/) | [💻 Code (not yet)]()


## 2023:
### 1. Drivable 3D Gaussian Avatars 
**Authors**:  Wojciech Zielonka, Timur Bagautdinov, Shunsuke Saito, Michael Zollhöfer, Justus Thies, Javier Romero
<details span>
<summary><b>Abstract</b></summary>
We present Drivable 3D Gaussian Avatars (D3GA), the
first 3D controllable model for human bodies rendered with
Gaussian splats. Current photorealistic drivable avatars
require either accurate 3D registrations during training,
dense input images during testing, or both. The ones based
on neural radiance fields also tend to be prohibitively slow
for telepresence applications. This work uses the recently
presented 3D Gaussian Splatting (3DGS) technique to render realistic humans at real-time framerates, using dense
calibrated multi-view videos as input. To deform those
primitives, we depart from the commonly used point deformation method of linear blend skinning (LBS) and use
a classic volumetric deformation method: cage deformations. Given their smaller size, we drive these deformations
with joint angles and keypoints, which are more suitable for
communication applications. Our experiments on nine subjects with varied body shapes, clothes, and motions obtain
higher-quality results than state-of-the-art methods when
using the same training and test data.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.08581.pdf) | [🌐 Project Page](https://zielon.github.io/d3ga/) | [🎥 Short Presentation](https://youtu.be/C4IT1gnkaF0?si=zUJLm8adM68pVvR8) 

### 2. SplatArmor: Articulated Gaussian splatting for animatable humans from monocular RGB videos 
**Authors**: Rohit Jena, Ganesh Subramanian Iyer, Siddharth Choudhary, Brandon Smith, Pratik Chaudhari, James Gee 
<details span>
<summary><b>Abstract</b></summary>
We propose SplatArmor, a novel approach for recovering detailed and animatable human models by `armoring' a parameterized body model with 3D Gaussians. Our approach represents the human as a set of 3D Gaussians within a canonical space, whose articulation is defined by extending the skinning of the underlying SMPL geometry to arbitrary locations in the canonical space. To account for pose-dependent effects, we introduce a SE(3) field, which allows us to capture both the location and anisotropy of the Gaussians. Furthermore, we propose the use of a neural color field to provide color regularization and 3D supervision for the precise positioning of these Gaussians. We show that Gaussian splatting provides an interesting alternative to neural rendering based methods by leverging a rasterization primitive without facing any of the non-differentiability and optimization challenges typically faced in such approaches. The rasterization paradigms allows us to leverage forward skinning, and does not suffer from the ambiguities associated with inverse skinning and warping. We show compelling results on the ZJU MoCap and People Snapshot datasets, which underscore the effectiveness of our method for controllable human synthesis.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.10812.pdf) |  [🌐 Project Page](https://jenaroh.it/splatarmor/) | [💻 Code (not yet)](https://github.com/rohitrango/splatarmor)

### 3. Animatable Gaussians: Learning Pose-dependent Gaussian Maps for High-fidelity Human Avatar Modeling 
**Authors**: Zhe Li, Zerong Zheng, Lizhen Wang, Yebin Liu 
<details span>
<summary><b>Abstract</b></summary>
Modeling animatable human avatars from RGB videos is a long-standing and challenging problem. Recent works usually adopt MLP-based neural radiance fields (NeRF) to represent 3D humans, but it remains difficult for pure MLPs to regress pose-dependent garment details. To this end, we introduce Animatable Gaussians, a new avatar representation that leverages powerful 2D CNNs and 3D Gaussian splatting to create high-fidelity avatars. To associate 3D Gaussians with the animatable avatar, we learn a parametric template from the input videos, and then parameterize the template on two front & back canonical Gaussian maps where each pixel represents a 3D Gaussian. The learned template is adaptive to the wearing garments for modeling looser clothes like dresses. Such template-guided 2D parameterization enables us to employ a powerful StyleGAN-based CNN to learn the pose-dependent Gaussian maps for modeling detailed dynamic appearances. Furthermore, we introduce a pose projection strategy for better generalization given novel poses. Overall, our method can create lifelike avatars with dynamic, realistic and generalized appearances. Experiments show that our method outperforms other state-of-the-art approaches. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.16096.pdf) | [🌐 Project Page](https://animatable-gaussians.github.io/) | [💻 Code (not yet)](https://github.com/lizhe00/AnimatableGaussians)

### 4. GART: Gaussian Articulated Template Models 
**Authors**: Jiahui Lei, Yufu Wang, Georgios Pavlakos, Lingjie Liu, Kostas Daniilidis 
<details span>
<summary><b>Abstract</b></summary>
We introduce Gaussian Articulated Template Model GART, an explicit, efficient, and expressive representation for non-rigid articulated subject capturing and rendering from monocular videos. GART utilizes a mixture of moving 3D Gaussians to explicitly approximate a deformable subject's geometry and appearance. It takes advantage of a categorical template model prior (SMPL, SMAL, etc.) with learnable forward skinning while further generalizing to more complex non-rigid deformations with novel latent bones. GART can be reconstructed via differentiable rendering from monocular videos in seconds or minutes and rendered in novel poses faster than 150fps.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.16099.pdf) | [🌐 Project Page](https://www.cis.upenn.edu/~leijh/projects/gart/) | [💻 Code](https://github.com/JiahuiLei/GART) | [🎥 Short Presentation](https://www.youtube.com/watch?v=-xYNtIlW4WY)

### 5. Human Gaussian Splatting: Real-time Rendering of Animatable Avatars 
**Authors**: Arthur Moreau, Jifei Song, Helisa Dhamo, Richard Shaw, Yiren Zhou, Eduardo Pérez-Pellitero 
<details span>
<summary><b>Abstract</b></summary>
This work addresses the problem of real-time rendering of photorealistic human body avatars learned from multi-view videos. While the classical approaches to model and render virtual humans generally use a textured mesh, recent research has developed neural body representations that achieve impressive visual quality. However, these models are difficult to render in real-time and their quality degrades when the character is animated with body poses different than the training observations. We propose the first animatable human model based on 3D Gaussian Splatting, that has recently emerged as a very efficient alternative to neural radiance fields. Our body is represented by a set of gaussian primitives in a canonical space which are deformed in a coarse to fine approach that combines forward skinning and local non-rigid refinement. We describe how to learn our Human Gaussian Splatting (\OURS) model in an end-to-end fashion from multi-view observations, and evaluate it against the state-of-the-art approaches for novel pose synthesis of clothed body. Our method presents a PSNR 1.5dbB better than the state-of-the-art on THuman4 dataset while being able to render at 20fps or more. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17113.pdf) 

### 6. HUGS: Human Gaussian Splats 
**Authors**: Muhammed Kocabas, Jen-Hao Rick Chang, James Gabriel, Oncel Tuzel, Anurag Ranjan 
<details span>
<summary><b>Abstract</b></summary>
Recent advances in neural rendering have improved both training and rendering times by orders of magnitude. While these methods demonstrate state-of-the-art quality and speed, they are designed for photogrammetry of static scenes and do not generalize well to freely moving humans in the environment. In this work, we introduce Human Gaussian Splats (HUGS) that represents an animatable human together with the scene using 3D Gaussian Splatting (3DGS). Our method takes only a monocular video with a small number of (50-100) frames, and it automatically learns to disentangle the static scene and a fully animatable human avatar within 30 minutes. We utilize the SMPL body model to initialize the human Gaussians. To capture details that are not modeled by SMPL (e.g. cloth, hairs), we allow the 3D Gaussians to deviate from the human body model. Utilizing 3D Gaussians for animated humans brings new challenges, including the artifacts created when articulating the Gaussians. We propose to jointly optimize the linear blend skinning weights to coordinate the movements of individual Gaussians during animation. Our approach enables novel-pose synthesis of human and novel view synthesis of both the human and the scene. We achieve state-of-the-art rendering quality with a rendering speed of 60 FPS while being ~100x faster to train over previous work.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17910.pdf) | [🌐 Project Page](https://machinelearning.apple.com/research/hugs) | [💻 Code (not yet)](https://github.com/apple/ml-hugs)

### 7. Gaussian Shell Maps for Efficient 3D Human Generation
**Authors**: Rameen Abdal, Wang Yifan, Zifan Shi, Yinghao Xu, Ryan Po, Zhengfei Kuang, Qifeng Chen, Dit-Yan Yeung, Gordon Wetzstein
<details span>
<summary><b>Abstract</b></summary>
Efficient generation of 3D digital humans is important in several industries, including virtual reality, social media, and cinematic production. 3D generative adversarial networks (GANs) have demonstrated state-of-the-art (SOTA) quality and diversity for generated assets. Current 3D GAN architectures, however, typically rely on volume representations, which are slow to render, thereby hampering the GAN training and requiring multi-view-inconsistent 2D upsamplers. Here, we introduce Gaussian Shell Maps (GSMs) as a framework that connects SOTA generator network architectures with emerging 3D Gaussian rendering primitives using an articulable multi shell–based scaffold. In this setting, a CNN generates a 3D texture stack with features that are mapped to the shells. The latter represent inflated and deflated versions of a template surface of a digital human in a canonical body pose. Instead of rasterizing the shells directly, we sample 3D Gaussians on the shells whose attributes are encoded in the texture features. These Gaussians are efficiently and differentiably rendered. The ability to articulate the shells is important during GAN training and, at inference time, to deform a body into arbitrary userdefined poses. Our efficient rendering scheme bypasses the need for view-inconsistent upsamplers and achieves highquality multi-view consistent renderings at a native resolution of 512 × 512 pixels. We demonstrate that GSMs successfully generate 3D humans when trained on single-view datasets, including SHHQ and DeepFashion.
</details>

  [📄 Paper](https://arxiv.org/abs/2311.17857) | [🌐 Project Page](https://rameenabdal.github.io/GaussianShellMaps/) | [💻 Code](https://github.com/computational-imaging/GSM)

### 8. GaussianHead: High-fidelity Head Avatars with Learnable Gaussian Derivation
**Authors**: Jie Wang, Jiu-Cheng Xie, Xianyan Li, Chi-Man Pun, Feng Xu, Hao Gao

<details span>
<summary><b>Abstract</b></summary>
Constructing vivid 3D head avatars for given subjects and realizing a series of animations on them is valuable yet challenging. This paper presents GaussianHead, which models the actional human head with anisotropic 3D Gaussians. In our framework, a motion deformation field and multi-resolution tri-plane are constructed respectively to deal with the head's dynamic geometry and complex texture. Notably, we impose an exclusive derivation scheme on each Gaussian, which generates its multiple doppelgangers through a set of learnable parameters for position transformation. With this design, we can compactly and accurately encode the appearance information of Gaussians, even those fitting the head's particular components with sophisticated structures. In addition, an inherited derivation strategy for newly added Gaussians is adopted to facilitate training acceleration. Extensive experiments show that our method can produce high-fidelity renderings, outperforming state-of-the-art approaches in reconstruction, cross-identity reenactment, and novel view synthesis tasks.
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.01632.pdf) | [🌐 Project Page](https://chiehwangs.github.io/gaussian-head-page/) | [💻 Code](https://github.com/chiehwangs/gaussian-head)

### 9. GaussianAvatars: Photorealistic Head Avatars with Rigged 3D Gaussians
**Authors**: Shenhan Qian, Tobias Kirschstein, Liam Schoneveld, Davide Davoli, Simon Giebenhain, Matthias Nießner

<details span>
<summary><b>Abstract</b></summary>
We introduce GaussianAvatars, a new method to create photorealistic head avatars that are fully controllable in terms of expression, pose, and viewpoint. The core idea is a dynamic 3D representation based on 3D Gaussian splats that are rigged to a parametric morphable face model. This combination facilitates photorealistic rendering while allowing for precise animation control via the underlying parametric model, e.g., through expression transfer from a driving sequence or by manually changing the morphable model parameters. We parameterize each splat by a local coordinate frame of a triangle and optimize for explicit displacement offset to obtain a more accurate geometric representation. During avatar reconstruction, we jointly optimize for the morphable model parameters and Gaussian splat parameters in an end-to-end fashion. We demonstrate the animation capabilities of our photorealistic avatar in several challenging scenarios. For instance, we show reenactments from a driving video, where our method outperforms existing works by a significant margin.
</details>

 [📄 Paper](https://arxiv.org/abs/2312.02069) | [🌐 Project Page](https://shenhanqian.github.io/gaussian-avatars) | [💻 Code](https://github.com/ShenhanQian/GaussianAvatars) | [🎥 Short Presentation](https://youtu.be/lVEY78RwU_I)

### 10. GPS-Gaussian: Generalizable Pixel-wise 3D Gaussian Splatting for Real-time Human Novel View Synthesis
**Authors**: Shunyuan Zheng, Boyao Zhou, Ruizhi Shao, Boning Liu, Shengping Zhang, Liqiang Nie, Yebin Liu

<details span>
<summary><b>Abstract</b></summary>
We present a new approach, termed GPS-Gaussian, for synthesizing novel views of a character in a real-time manner. The proposed method enables 2K-resolution rendering under a sparse-view camera setting. Unlike the original Gaussian Splatting or neural implicit rendering methods that necessitate per-subject optimizations, we introduce Gaussian parameter maps defined on the source views and regress directly Gaussian Splatting properties for instant novel view synthesis without any fine-tuning or optimization. To this end, we train our Gaussian parameter regression module on a large amount of human scan data, jointly with a depth estimation module to lift 2D parameter maps to 3D space. The proposed framework is fully differentiable and experiments on several datasets demonstrate that our method outperforms state-of-the-art methods while achieving an exceeding rendering speed.
</details>

 [📄 Paper)](https://arxiv.org/pdf/2312.02155.pdf) | [🌐 Project Page](https://github.com/ShunyuanZheng/GPS-Gaussian) | [💻 Code](https://github.com/ShunyuanZheng/GPS-Gaussian) | [🎥 Short Presentation](https://youtu.be/TBIekcqt0j0)

### 11. GauHuman: Articulated Gaussian Splatting from Monocular Human Videos 
**Authors**: Shoukang Hu Ziwei Liu  

<details span>
<summary><b>Abstract</b></summary>
 We present, GauHuman, a 3D human model with Gaussian Splatting for both fast training (1~2 minutes) and real-time rendering (up to 189 FPS), compared with existing NeRF-based implicit representation modelling frameworks demanding hours of training and seconds of rendering per frame. Specifically, GauHuman encodes Gaussian Splatting in the canonical space and transforms 3D Gaussians from canonical space to posed space with linear blend skinning (LBS), in which effective pose and LBS refinement modules are designed to learn fine details of 3D humans under negligible computational cost. Moreover, to enable fast optimization of GauHuman, we initialize and prune 3D Gaussians with 3D human prior, while splitting/cloning via KL divergence guidance, along with a novel merge operation for further speeding up. Extensive experiments on ZJU_Mocap and MonoCap datasets demonstrate that GauHuman achieves state-of-the-art performance quantitatively and qualitatively with fast training and real-time rendering speed. Notably, without sacrificing rendering quality, GauHuman can fast model the 3D human performer with ~13k 3D Gaussians.
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.02973.pdf) | [🌐 Project Page](https://skhu101.github.io/GauHuman/) | [💻 Code](https://github.com/skhu101/GauHuman) | [🎥 Short Presentation](https://www.youtube.com/embed/47772bgt5Xo)

### 12. HeadGaS: Real-Time Animatable Head Avatars via 3D Gaussian Splatting 
**Authors**: Helisa Dhamo, Yinyu Nie, Arthur Moreau, Jifei Song, Richard Shaw, Yiren Zhou, Eduardo Pérez-Pellitero  

<details span>
<summary><b>Abstract</b></summary>
3D head animation has seen major quality and runtime improvements over the last few years, particularly empowered by the advances in differentiable rendering and neural radiance fields. Real-time rendering is a highly desirable goal for real-world applications. We propose HeadGaS, the first model to use 3D Gaussian Splats (3DGS) for 3D head reconstruction and animation. In this paper we introduce a hybrid model that extends the explicit representation from 3DGS with a base of learnable latent features, which can be linearly blended with low-dimensional parameters from parametric head models to obtain expression-dependent final color and opacity values. We demonstrate that HeadGaS delivers state-of-the-art results in real-time inference frame rates, which surpasses baselines by up to ~2dB, while accelerating rendering speed by over x10. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.02902.pdf)

### 13. HiFi4G: High-Fidelity Human Performance Rendering via Compact Gaussian Splatting
**Authors**: Yuheng Jiang, Zhehao Shen, Penghao Wang, Zhuo Su, Yu Hong, Yingliang Zhang, Jingyi Yu, Lan Xu  

<details span>
<summary><b>Abstract</b></summary>
We have recently seen tremendous progress in photo-real human modeling and rendering. Yet, efficiently rendering realistic human performance and integrating it into the rasterization pipeline remains challenging. In this paper, we present HiFi4G, an explicit and compact Gaussian-based approach for high-fidelity human performance rendering from dense footage. Our core intuition is to marry the 3D Gaussian representation with non-rigid tracking, achieving a compact and compression-friendly representation. We first propose a dual-graph mechanism to obtain motion priors, with a coarse deformation graph for effective initialization and a fine-grained Gaussian graph to enforce subsequent constraints. Then, we utilize a 4D Gaussian optimization scheme with adaptive spatial-temporal regularizers to effectively balance the non-rigid prior and Gaussian updating. We also present a companion compression scheme with residual compensation for immersive experiences on various platforms. It achieves a substantial compression rate of approximately 25 times, with less than 2MB of storage per frame. Extensive experiments demonstrate the effectiveness of our approach, which significantly outperforms existing approaches in terms of optimization speed, rendering quality, and storage overhead. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.03461.pdf) | [🌐 Project Page](https://nowheretrix.github.io/HiFi4G/) | [🎥 Short Presentation](https://youtu.be/917WVr2EHh4)

### 14. GaussianAvatar: Towards Realistic Human Avatar Modeling from a Single Video via Animatable 3D Gaussians  
**Authors**: Liangxiao Hu, Hongwen Zhang, Yuxiang Zhang, Boyao Zhou, Boning Liu, Shengping Zhang, Liqiang Nie  

<details span>
<summary><b>Abstract</b></summary>
We present GaussianAvatar, an efficient approach to creating realistic human avatars with dynamic 3D appearances from a single video. We start by introducing animatable 3D Gaussians to explicitly represent humans in various poses and clothing styles. Such an explicit and animatable representation can fuse 3D appearances more efficiently and consistently from 2D observations. Our representation is further augmented with dynamic properties to support pose-dependent appearance modeling, where a dynamic appearance network along with an optimizable feature tensor is designed to learn the motion-to-appearance mapping. Moreover, by leveraging the differentiable motion condition, our method enables a joint optimization of motions and appearances during avatar modeling, which helps to tackle the long-standing issue of inaccurate motion estimation in monocular settings. The efficacy of GaussianAvatar is validated on both the public dataset and our collected dataset, demonstrating its superior performances in terms of appearance quality and rendering efficiency. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.02134.pdf) | [🌐 Project Page](https://huliangxiao.github.io/GaussianAvatar) | [💻 Code](https://github.com/huliangxiao/GaussianAvatar) | [🎥 Short Presentation](https://www.youtube.com/watch?v=a4g8Z9nCF-k&t=1s)

### 15. FlashAvatar: High-Fidelity Digital Avatar Rendering at 300FPS  
**Authors**: Jun Xiang, Xuan Gao, Yudong Guo, Juyong Zhang  

<details span>
<summary><b>Abstract</b></summary>
We propose FlashAvatar, a novel and lightweight 3D animatable avatar representation that could reconstruct a digital avatar from a short monocular video sequence in minutes and render high-fidelity photo-realistic images at 300FPS on a consumer-grade GPU. To achieve this, we maintain a uniform 3D Gaussian field embedded in the surface of a parametric face model and learn extra spatial offset to model non-surface regions and subtle facial details. While full use of geometric priors can capture high-frequency facial details and preserve exaggerated expressions, proper initialization can help reduce the number of Gaussians, thus enabling super-fast rendering speed. Extensive experimental results demonstrate that FlashAvatar outperforms existing works regarding visual quality and personalized details and is almost an order of magnitude faster in rendering speed.
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.02134.pdf) | [🌐 Project Page](https://ustc3dv.github.io/FlashAvatar/) | [💻 Code (not yet)]()

### 16. Relightable Gaussian Codec Avatars 
**Authors**: Shunsuke Saito, Gabriel Schwartz, Tomas Simon, Junxuan Li, Giljoo Nam  

<details span>
<summary><b>Abstract</b></summary>
The fidelity of relighting is bounded by both geometry and appearance representations. For geometry, both mesh and volumetric approaches have difficulty modeling intricate structures like 3D hair geometry. For appearance, existing relighting models are limited in fidelity and often too slow to render in real-time with high-resolution continuous environments. In this work, we present Relightable Gaussian Codec Avatars, a method to build high-fidelity relightable head avatars that can be animated to generate novel expressions. Our geometry model based on 3D Gaussians can capture 3D-consistent sub-millimeter details such as hair strands and pores on dynamic face sequences. To support diverse materials of human heads such as the eyes, skin, and hair in a unified manner, we present a novel relightable appearance model based on learnable radiance transfer. Together with global illumination-aware spherical harmonics for the diffuse components, we achieve real-time relighting with spatially all-frequency reflections using spherical Gaussians. This appearance model can be efficiently relit under both point light and continuous illumination. We further improve the fidelity of eye reflections and enable explicit gaze control by introducing relightable explicit eye models. Our method outperforms existing approaches without compromising real-time performance. We also demonstrate real-time relighting of avatars on a tethered consumer VR headset, showcasing the efficiency and fidelity of our avatars. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.03704.pdf) | [🌐 Project Page](https://shunsukesaito.github.io/rgca/)

### 17. MonoGaussianAvatar: Monocular Gaussian Point-based Head Avatar 
**Authors**: Yufan Chen, Lizhen Wang, Qijing Li, Hongjiang Xiao, Shengping Zhang, Hongxun Yao, Yebin Liu  

<details span>
<summary><b>Abstract</b></summary>
The ability to animate photo-realistic head avatars reconstructed from monocular portrait video sequences represents a crucial step in bridging the gap between the virtual and real worlds. Recent advancements in head avatar techniques, including explicit 3D morphable meshes (3DMM), point clouds, and neural implicit representation have been exploited for this ongoing research. However, 3DMM-based methods are constrained by their fixed topologies, point-based approaches suffer from a heavy training burden due to the extensive quantity of points involved, and the last ones suffer from limitations in deformation flexibility and rendering efficiency. In response to these challenges, we propose MonoGaussianAvatar (Monocular Gaussian Point-based Head Avatar), a novel approach that harnesses 3D Gaussian point representation coupled with a Gaussian deformation field to learn explicit head avatars from monocular portrait videos. We define our head avatars with Gaussian points characterized by adaptable shapes, enabling flexible topology. These points exhibit movement with a Gaussian deformation field in alignment with the target pose and expression of a person, facilitating efficient deformation. Additionally, the Gaussian points have controllable shape, size, color, and opacity combined with Gaussian splatting, allowing for efficient training and rendering. Experiments demonstrate the superior performance of our method, which achieves state-of-the-art results among previous methods. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.04558.pdf) | [🌐 Project Page](https://yufan1012.github.io/MonoGaussianAvatar) | [💻 Code (not yet)](https://github.com/yufan1012/MonoGaussianAvatar) | [🎥 Short Presentation](https://youtu.be/3UvBkyPc-oc?si=SbveQKBLJh5GuhIY)

### 18. ASH: Animatable Gaussian Splats for Efficient and Photoreal Human Rendering  
**Authors**: Haokai Pang, Heming Zhu, Adam Kortylewski, Christian Theobalt, Marc Habermann 

<details span>
<summary><b>Abstract</b></summary>
Real-time rendering of photorealistic and controllable human avatars stands as a cornerstone in Computer Vision and Graphics. While recent advances in neural implicit rendering have unlocked unprecedented photorealism for digital avatars, real-time performance has mostly been demonstrated for static scenes only. To address this, we propose ASH, an animatable Gaussian splatting approach for photorealistic rendering of dynamic humans in real-time. We parameterize the clothed human as animatable 3D Gaussians, which can be efficiently splatted into image space to generate the final rendering. However, naively learning the Gaussian parameters in 3D space poses a severe challenge in terms of compute. Instead, we attach the Gaussians onto a deformable character model, and learn their parameters in 2D texture space, which allows leveraging efficient 2D convolutional architectures that easily scale with the required number of Gaussians. We benchmark ASH with competing methods on pose-controllable avatars, demonstrating that our method outperforms existing real-time methods by a large margin and shows comparable or even better results than offline methods. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.05941.pdf) | [🌐 Project Page](https://vcai.mpi-inf.mpg.de/projects/ash/) | [💻 Code (not yet)]() | [🎥 Short Presentation](https://vcai.mpi-inf.mpg.de/projects/ash/videos/video_for_page.mp4)

### 19. 3DGS-Avatar: Animatable Avatars via Deformable 3D Gaussian Splatting  
**Authors**: Zhiyin Qian, Shaofei Wang, Marko Mihajlovic, Andreas Geiger, Siyu Tang 

<details span>
<summary><b>Abstract</b></summary>
We introduce an approach that creates animatable human avatars from monocular videos using 3D Gaussian Splatting (3DGS). Existing methods based on neural radiance fields (NeRFs) achieve high-quality novel-view/novel-pose image synthesis but often require days of training, and are extremely slow at inference time. Recently, the community has explored fast grid structures for efficient training of clothed avatars. Albeit being extremely fast at training, these methods can barely achieve an interactive rendering frame rate with around 15 FPS. In this paper, we use 3D Gaussian Splatting and learn a non-rigid deformation network to reconstruct animatable clothed human avatars that can be trained within 30 minutes and rendered at real-time frame rates (50+ FPS). Given the explicit nature of our representation, we further introduce as-isometric-as-possible regularizations on both the Gaussian mean vectors and the covariance matrices, enhancing the generalization of our model on highly articulated unseen poses. Experimental results show that our method achieves comparable and even better performance compared to state-of-the-art approaches on animatable avatar creation from a monocular input, while being 400x and 250x faster in training and inference, respectively. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.09228.pdf) | [🌐 Project Page](https://neuralbodies.github.io/3DGS-Avatar/index.html) | [💻 Code](https://github.com/mikeqzy/3dgs-avatar-release) | [🎥 Short Presentation](https://youtu.be/FJ29U9OkmmU?si=5ua2mtpv5ei2n28Z)

### 20. GAvatar: Animatable 3D Gaussian Avatars with Implicit Mesh Learning  
**Authors**: Ye Yuan, Xueting Li, Yangyi Huang, Shalini De Mello, Koki Nagano, Jan Kautz, Umar Iqbal 

<details span>
<summary><b>Abstract</b></summary>
 Gaussian splatting has emerged as a powerful 3D representation that harnesses the advantages of both explicit (mesh) and implicit (NeRF) 3D representations. In this paper, we seek to leverage Gaussian splatting to generate realistic animatable avatars from textual descriptions, addressing the limitations (e.g., flexibility and efficiency) imposed by mesh or NeRF-based representations. However, a naive application of Gaussian splatting cannot generate high-quality animatable avatars and suffers from learning instability; it also cannot capture fine avatar geometries and often leads to degenerate body parts. To tackle these problems, we first propose a primitive-based 3D Gaussian representation where Gaussians are defined inside pose-driven primitives to facilitate animation. Second, to stabilize and amortize the learning of millions of Gaussians, we propose to use neural implicit fields to predict the Gaussian attributes (e.g., colors). Finally, to capture fine avatar geometries and extract detailed meshes, we propose a novel SDF-based implicit mesh learning approach for 3D Gaussians that regularizes the underlying geometries and extracts highly detailed textured meshes. Our proposed method, GAvatar, enables the large-scale generation of diverse animatable avatars using only text prompts. GAvatar significantly surpasses existing methods in terms of both appearance and geometry quality, and achieves extremely fast rendering (100 fps) at 1K resolution.
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.11461.pdf) | [🌐 Project Page](https://nvlabs.github.io/GAvatar/) | [🎥 Short Presentation](https://www.youtube.com/watch?v=PbCF1HzrKrs)

### 21. Deformable 3D Gaussian Splatting for Animatable Human Avatars 
**Authors**: HyunJun Jung, Nikolas Brasch, Jifei Song, Eduardo Perez-Pellitero, Yiren Zhou, Zhihao Li, Nassir Navab, Benjamin Busam 

<details span>
<summary><b>Abstract</b></summary>
Recent advances in neural radiance fields enable novel view synthesis of photo-realistic images in dynamic settings, which can be applied to scenarios with human animation. Commonly used implicit backbones to establish accurate models, however, require many input views and additional annotations such as human masks, UV maps and depth maps. In this work, we propose ParDy-Human (Parameterized Dynamic Human Avatar), a fully explicit approach to construct a digital avatar from as little as a single monocular sequence. ParDy-Human introduces parameter-driven dynamics into 3D Gaussian Splatting where 3D Gaussians are deformed by a human pose model to animate the avatar. Our method is composed of two parts: A first module that deforms canonical 3D Gaussians according to SMPL vertices and a consecutive module that further takes their designed joint encodings and predicts per Gaussian deformations to deal with dynamics beyond SMPL vertex deformations. Images are then synthesized by a rasterizer. ParDy-Human constitutes an explicit model for realistic dynamic human avatars which requires significantly fewer training views and images. Our avatars learning is free of additional annotations such as masks and can be trained with variable backgrounds while inferring full-resolution images efficiently even on consumer hardware. We provide experimental evidence to show that ParDy-Human outperforms state-of-the-art methods on ZJU-MoCap and THUman4.0 datasets both quantitatively and visually. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.15059.pdf) 

### 22. Human101: Training 100+FPS Human Gaussians in 100s from 1 View  
**Authors**: Mingwei Li, Jiachen Tao, Zongxin Yang, Yi Yang 

<details span>
<summary><b>Abstract</b></summary>
Reconstructing the human body from single-view videos plays a pivotal role in the virtual reality domain. One prevalent application scenario necessitates the rapid reconstruction of high-fidelity 3D digital humans while simultaneously ensuring real-time rendering and interaction. Existing methods often struggle to fulfill both requirements. In this paper, we introduce Human101, a novel framework adept at producing high-fidelity dynamic 3D human reconstructions from 1-view videos by training 3D Gaussians in 100 seconds and rendering in 100+ FPS. Our method leverages the strengths of 3D Gaussian Splatting, which provides an explicit and efficient representation of 3D humans. Standing apart from prior NeRF-based pipelines, Human101 ingeniously applies a Human-centric Forward Gaussian Animation method to deform the parameters of 3D Gaussians, thereby enhancing rendering speed (i.e., rendering 1024-resolution images at an impressive 60+ FPS and rendering 512-resolution images at 100+ FPS). Experimental results indicate that our approach substantially eclipses current methods, clocking up to a 10 times surge in frames per second and delivering comparable or superior rendering quality.
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.15258.pdf) | [🌐 Project Page](https://longxiang-ai.github.io/Human101/) | [💻 Code (not yet)](https://github.com/longxiang-ai/Human101) 

### 23. Gaussian Head Avatar: Ultra High-fidelity Head Avatar via Dynamic Gaussians  
**Authors**: Yuelang Xu, Benwang Chen, Zhe Li, Hongwen Zhang, Lizhen Wang, Zerong Zheng, Yebin Liu 

<details span>
<summary><b>Abstract</b></summary>
Creating high-fidelity 3D head avatars has always been a research hotspot, but there remains a great challenge under lightweight sparse view setups. In this paper, we propose Gaussian Head Avatar represented by controllable 3D Gaussians for high-fidelity head avatar modeling. We optimize the neutral 3D Gaussians and a fully learned MLP-based deformation field to capture complex expressions. The two parts benefit each other, thereby our method can model fine-grained dynamic details while ensuring expression accuracy. Furthermore, we devise a well-designed geometry-guided initialization strategy based on implicit SDF and Deep Marching Tetrahedra for the stability and convergence of the training procedure. Experiments show our approach outperforms other state-of-the-art sparse-view methods, achieving ultra high-fidelity rendering quality at 2K resolution even under exaggerated expressions. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.03029.pdf) | [🌐 Project Page](https://yuelangx.github.io/gaussianheadavatar/) | | [💻 Code (not yet)](https://github.com/YuelangX/Gaussian-Head-Avatar) | [🎥 Short Presentation](https://www.youtube.com/watch?v=kvrrI3EoM5g)

<br>

## Classic work:
### 1. A Generalization of Algebraic Surface Drawing
**Authors**: James F. Blinn

 ***Comment:***: First paper rendering 3D gaussians.

<details span>
<summary><b>Abstract</b></summary>
The mathematical description of three-dimensional surfaces usually falls into one of two classifications: 
parametric and implicit. An implicit surface is defined to be all points which satisfy some
equation F (x, y, z) = 0. This form is ideally suited for image space shaded picture drawing; the pixel
coordinates are substituted for x and y, and the equation is solved for z. Algorithms for drawing such
objects have been developed primarily for first- and second-order polynomial functions, a subcategory
known as algebraic surfaces. This paper presents a new algorithm applicable to other functional
forms, in particular to the summation of several Gaussian density distributions. The algorithm was
created to model electron density maps of molecular structures, but it can be used for other artistically
interesting shapes.
</details>

[📄 Paper](https://dl.acm.org/doi/pdf/10.1145/357306.357310) 

### 2. Approximate Differentiable Rendering with Algebraic Surfaces
**Authors**: Leonid Keselman and Martial Hebert

 ***Comment:***: First paper to do differentiable rendering optimization of 3D gaussians.

<details span>
<summary><b>Abstract</b></summary>
Differentiable renderers provide a direct mathematical link
between an object’s 3D representation and images of that object. In
this work, we develop an approximate differentiable renderer for a compact, interpretable representation, which we call Fuzzy Metaballs. Our
approximate renderer focuses on rendering shapes via depth maps and
silhouettes. It sacrifices fidelity for utility, producing fast runtimes and
high-quality gradient information that can be used to solve vision tasks.
Compared to mesh-based differentiable renderers, our method has forward passes that are 5x faster and backwards passes that are 30x faster.
The depth maps and silhouette images generated by our method are
smooth and defined everywhere. In our evaluation of differentiable renderers for pose estimation, we show that our method is the only one
comparable to classic techniques. In shape from silhouette, our method
performs well using only gradient descent and a per-pixel loss, without
any surrogate losses or regularization. These reconstructions work well
even on natural video sequences with segmentation artifacts.
</details>

[📄 Paper](https://arxiv.org/pdf/2207.10606.pdf) | [🌐 Project Page](https://leonidk.com/fuzzy-metaballs/) | [💻 Code](https://github.com/leonidk/fuzzy-metaballs) | [🎥 Short Presentation](https://www.youtube.com/watch?v=Ec7cxEc9eOU) 

### 3. Unbiased Gradient Estimation for Differentiable Surface Splatting via Poisson Sampling
**Authors**: Jan U. Müller, Michael Weinmann, Reinhard Klein

***Comment:*** Builds 2D screen-space gaussians from underlying 3D representations.

<details span>
<summary><b>Abstract</b></summary>
We propose an efficient and GPU-accelerated sampling framework which enables unbiased gradient approximation for differentiable point cloud rendering based on surface splatting. Our framework models the contribution of a point to the rendered image as a probability distribution. We derive an unbiased approximative gradient for the rendering function within this model. To efficiently evaluate the proposed sample estimate, we introduce a tree-based data-structure which employs multi-pole methods to draw samples in near linear time. Our gradient estimator allows us to avoid regularization required by previous methods, leading to a more faithful shape recovery from images. Furthermore, we validate that these improvements are applicable to real-world applications by refining the camera poses and point cloud obtained from a real-time SLAM system. Finally, employing our framework in a neural rendering setting optimizes both the point cloud and network parameters, highlighting the framework’s ability to enhance data driven approaches.
</details>

[📄 Paper](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136930276.pdf) [💻 Code](https://github.com/muellerju/unbiased-differentiable-splatting) 

### 4. Generating and Real-Time Rendering of Clouds
**Authors**: Petr Man

***Comment:*** Splatting of anisotropic gaussians. Basically a non-differentiable implementation of 3DGS.

<details span>
<summary><b>Abstract</b></summary>
This paper presents a method for generation and real-time
rendering of static clouds. Perlin noise function generates
three dimensional map of a cloud. We also present a twopass rendering algorithm that performs physically based
approximation. In the first preprocessed phase it computes
multiple forward scattering. In the second phase first order
anisotropic scattering at runtime is evaluated.
The generated map is stored as voxels and is unsuitable
for the real-time rendering. We introduce a more suitable
inner representation of cloud that approximates the original map and contains much less information. The cloud is
then represented by a set of metaballs (spheres) with parameters such as center positions, radii and density values.
The main contribution of this paper is to propose a
method, that transforms the original cloud map to the inner
representation. This method uses the Radial Basis Function (RBF) neural network.
</details>

[📄 Paper](https://old.cescg.org/CESCG-2006/papers/Prague-Man-Petr.pdf) 

<br>

## Compression:
## 2024:
### 1. Compressed 3D Gaussian Splatting for Accelerated Novel View Synthesis 
**Authors**: Simon Niedermayr, Josef Stumpfegger, Rüdiger Westermann 
<details span>
<summary><b>Abstract</b></summary>
Recently, high-fidelity scene reconstruction with an optimized 3D Gaussian splat representation has been introduced for novel view synthesis from sparse image sets. Making such representations suitable for applications like network streaming and rendering on low-power devices requires significantly reduced memory consumption as well as improved rendering efficiency. We propose a compressed 3D Gaussian splat representation that utilizes sensitivity-aware vector clustering with quantization-aware training to compress directional colors and Gaussian parameters. The learned codebooks have low bitrates and achieve a compression rate of up to 31× on real-world scenes with only minimal degradation of visual quality. We demonstrate that the compressed splat representation can be efficiently rendered with hardware rasterization on lightweight GPUs at up to 4× higher framerates than reported via an optimized GPU compute pipeline. Extensive experiments across multiple datasets demonstrate the robustness and rendering speed of the proposed approach. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.02436.pdf) | [🌐 Project Page](https://keksboter.github.io/c3dgs/) | [💻 Code](https://github.com/KeKsBoTer/c3dgs) 

## 2023:
### 1. LightGaussian: Unbounded 3D Gaussian Compression with 15x Reduction and 200+ FPS 
**Authors**: Zhiwen Fan, Kevin Wang, Kairun Wen, Zehao Zhu, Dejia Xu, Zhangyang Wang 
<details span>
<summary><b>Abstract</b></summary>
Recent advancements in real-time neural rendering using point-based techniques have paved the way for the widespread adoption of 3D representations. However, foundational approaches like 3D Gaussian Splatting come with a substantial storage overhead caused by growing the SfM points to millions, often demanding gigabyte-level disk space for a single unbounded scene, posing significant scalability challenges and hindering the splatting efficiency.
To address this challenge, we introduce LightGaussian, a novel method designed to transform 3D Gaussians into a more efficient and compact format. Drawing inspiration from the concept of Network Pruning, LightGaussian identifies Gaussians that are insignificant in contributing to the scene reconstruction and adopts a pruning and recovery process, effectively reducing redundancy in Gaussian counts while preserving visual effects. Additionally, LightGaussian employs distillation and pseudo-view augmentation to distill spherical harmonics to a lower degree, allowing knowledge transfer to more compact representations while maintaining reflectance. Furthermore, we propose a hybrid scheme, VecTree Quantization, to quantize all attributes, resulting in lower bitwidth representations with minimal accuracy losses.
In summary, LightGaussian achieves an averaged compression rate over 15x while boosting the FPS from 139 to 215, enabling an efficient representation of complex scenes on Mip-NeRF 360, Tank and Temple datasets. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17245.pdf) | [🌐 Project Page](https://lightgaussian.github.io/) | [💻 Code](https://github.com/VITA-Group/LightGaussian) | [🎥 Short Presentation](https://youtu.be/470hul75bSM?si=EKm-UaBaTs9qJH6K)

### 2. Compact3D: Compressing Gaussian Splat Radiance Field Models with Vector Quantization 
**Authors**: KL Navaneet, Kossar Pourahmadi Meibodi, Soroush Abbasi Koohpayegani, Hamed Pirsiavash 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian Splatting is a new method for modeling and rendering 3D radiance fields that achieves much faster learning and rendering time compared to SOTA NeRF methods. However, it comes with a drawback in the much larger storage demand compared to NeRF methods since it needs to store the parameters for several 3D Gaussians. We notice that many Gaussians may share similar parameters, so we introduce a simple vector quantization method based on \kmeans algorithm to quantize the Gaussian parameters. Then, we store the small codebook along with the index of the code for each Gaussian. Moreover, we compress the indices further by sorting them and using a method similar to run-length encoding. We do extensive experiments on standard benchmarks as well as a new benchmark which is an order of magnitude larger than the standard benchmarks. We show that our simple yet effective method can reduce the storage cost for the original 3D Gaussian Splatting method by a factor of almost 20× with a very small drop in the quality of rendered images. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.18159.pdf) | [💻 Code](https://github.com/UCDvision/compact3d)

### 3. Compact 3D Gaussian Representation for Radiance Field 
**Authors**: Joo Chan Lee, Daniel Rho, Xiangyu Sun, Jong Hwan Ko, Eunbyung Park 
<details span>
<summary><b>Abstract</b></summary>
Neural Radiance Fields (NeRFs) have demonstrated remarkable potential in capturing complex 3D scenes with high fidelity. However, one persistent challenge that hinders the widespread adoption of NeRFs is the computational bottleneck due to the volumetric rendering. On the other hand, 3D Gaussian splatting (3DGS) has recently emerged as an alternative representation that leverages a 3D Gaussisan-based representation and adopts the rasterization pipeline to render the images rather than volumetric rendering, achieving very fast rendering speed and promising image quality. However, a significant drawback arises as 3DGS entails a substantial number of 3D Gaussians to maintain the high fidelity of the rendered images, which requires a large amount of memory and storage. To address this critical issue, we place a specific emphasis on two key objectives: reducing the number of Gaussian points without sacrificing performance and compressing the Gaussian attributes, such as view-dependent color and covariance. To this end, we propose a learnable mask strategy that significantly reduces the number of Gaussians while preserving high performance. In addition, we propose a compact but effective representation of view-dependent color by employing a grid-based neural field rather than relying on spherical harmonics. Finally, we learn codebooks to compactly represent the geometric attributes of Gaussian by vector quantization. In our extensive experiments, we consistently show over 10× reduced storage and enhanced rendering speed, while maintaining the quality of the scene representation, compared to 3DGS. Our work provides a comprehensive framework for 3D scene representation, achieving high performance, fast training, compactness, and real-time rendering.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.13681.pdf) | [🌐 Project Page](https://maincold2.github.io/c3dgs/) | [💻 Code ](https://github.com/maincold2/Compact-3DGS) 

### 4. Compact 3D Scene Representation via Self-Organizing Gaussian Grids 
**Authors**: Wieland Morgenstern, Florian Barthel, Anna Hilsmann, Peter Eisert 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian Splatting has recently emerged as a highly promising technique for modeling of static 3D scenes. In contrast to Neural Radiance Fields, it utilizes efficient rasterization allowing for very fast rendering at high-quality. However, the storage size is significantly higher, which hinders practical deployment, e.g.~on resource constrained devices. In this paper, we introduce a compact scene representation organizing the parameters of 3D Gaussian Splatting (3DGS) into a 2D grid with local homogeneity, ensuring a drastic reduction in storage requirements without compromising visual quality during rendering. Central to our idea is the explicit exploitation of perceptual redundancies present in natural scenes. In essence, the inherent nature of a scene allows for numerous permutations of Gaussian parameters to equivalently represent it. To this end, we propose a novel highly parallel algorithm that regularly arranges the high-dimensional Gaussian parameters into a 2D grid while preserving their neighborhood structure. During training, we further enforce local smoothness between the sorted parameters in the grid. The uncompressed Gaussians use the same structure as 3DGS, ensuring a seamless integration with established renderers. Our method achieves a reduction factor of 8x to 26x in size for complex scenes with no increase in training time, marking a substantial leap forward in the domain of 3D scene distribution and consumption. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.13299.pdf) | [🌐 Project Page](https://fraunhoferhhi.github.io/Self-Organizing-Gaussians/) | [💻 Code (not yet)](https://github.com/fraunhoferhhi/Self-Organizing-Gaussians) 

<br>

## Diffusion:
## 2024:
### 1. AGG: Amortized Generative 3D Gaussians for Single Image to 3D 
**Authors**: Dejia Xu, Ye Yuan, Morteza Mardani, Sifei Liu, Jiaming Song, Zhangyang Wang, Arash Vahdat 

<details span>
<summary><b>Abstract</b></summary>
Given the growing need for automatic 3D content creation pipelines, various 3D representations have been studied to generate 3D objects from a single image. Due to its superior rendering efficiency, 3D Gaussian splatting-based models have recently excelled in both 3D reconstruction and generation. 3D Gaussian splatting approaches for image to 3D generation are often optimization-based, requiring many computationally expensive score-distillation steps. To overcome these challenges, we introduce an Amortized Generative 3D Gaussian framework (AGG) that instantly produces 3D Gaussians from a single image, eliminating the need for per-instance optimization. Utilizing an intermediate hybrid representation, AGG decomposes the generation of 3D Gaussian locations and other appearance attributes for joint optimization. Moreover, we propose a cascaded pipeline that first generates a coarse representation of the 3D data and later upsamples it with a 3D Gaussian super-resolution module. Our method is evaluated against existing optimization-based 3D Gaussian frameworks and sampling-based pipelines utilizing other 3D representations, where AGG showcases competitive generation abilities both qualitatively and quantitatively while being several orders of magnitude faster. 
</details>

[📄 Paper](https://arxiv.org/pdf/2401.04099.pdf) | [🌐 Project Page](https://ir1d.github.io/AGG/)| [🎥 Short Presentation](https://youtu.be/jkwmp2UH0Ug?si=lBXjme-d9bVrXTNf)

### 2. Fast Dynamic 3D Object Generation from a Single-view Video 
**Authors**: Zijie Pan, Zeyu Yang, Xiatian Zhu, Li Zhang 

<details span>
<summary><b>Abstract</b></summary>
Generating dynamic three-dimensional (3D) object from a single-view video is challenging due to the lack of 4D labeled data. Existing methods extend text-to-3D pipelines by transferring off-the-shelf image generation models such as score distillation sampling, but they are slow and expensive to scale (e.g., 150 minutes per object) due to the need for back-propagating the information-limited supervision signals through a large pretrained model. To address this limitation, we propose an efficient video-to-4D object generation framework called Efficient4D. It generates high-quality spacetime-consistent images under different camera views, and then uses them as labeled data to directly train a novel 4D Gaussian splatting model with explicit point cloud geometry, enabling real-time rendering under continuous camera trajectories. Extensive experiments on synthetic and real videos show that Efficient4D offers a remarkable 10-fold increase in speed when compared to prior art alternatives while preserving the same level of innovative view synthesis quality. For example, Efficient4D takes only 14 minutes to model a dynamic object. 
</details>

[📄 Paper](https://arxiv.org/pdf/2401.08742.pdf) | [🌐 Project Page](https://fudan-zvg.github.io/Efficient4D/) | [💻 Code](https://github.com/fudan-zvg/Efficient4D) | [🎥 Short Presentation](https://fudan-zvg.github.io/Efficient4D/assets/video/demo.mp4)

### 3. GaussianObject: Just Taking Four Images to Get A High-Quality 3D Object with Gaussian Splatting
**Authors**: Chen Yang, Sikuang Li, Jiemin Fang, Ruofan Liang, Lingxi Xie, Xiaopeng Zhang, Wei Shen, Qi Tian  

<details span>
<summary><b>Abstract</b></summary>
Reconstructing and rendering 3D objects from highly sparse views is of critical importance for promoting applications of 3D vision techniques and improving user experience. However, images from sparse views only contain very limited 3D information, leading to two significant challenges: 1) Difficulty in building multi-view consistency as images for matching are too few; 2) Partially omitted or highly compressed object information as view coverage is insufficient. To tackle these challenges, we propose GaussianObject, a framework to represent and render the 3D object with Gaussian splatting, that achieves high rendering quality with only 4 input images. We first introduce techniques of visual hull and floater elimination which explicitly inject structure priors into the initial optimization process for helping build multi-view consistency, yielding a coarse 3D Gaussian representation. Then we construct a Gaussian repair model based on diffusion models to supplement the omitted object information, where Gaussians are further refined. We design a self-generating strategy to obtain image pairs for training the repair model. Our GaussianObject is evaluated on several challenging datasets, including MipNeRF360, OmniObject3D, and OpenIllumination, achieving strong reconstruction results from only 4 views and significantly outperforming previous state-of-the-art methods. 
</details>

[📄 Paper](https://arxiv.org/pdf/2402.10259.pdf) | [🌐 Project Page](https://gaussianobject.github.io/) | [💻 Code](https://github.com/GaussianObject/GaussianObject) | [🎥 Short Presentation](https://youtu.be/ozoI0tmW3r0?si=KcaHtvVnrexqaf58) 

### 4.LGM: Large Multi-View Gaussian Model for High-Resolution 3D Content Creation 
**Authors**: Chen Yang, Sikuang Li, Jiemin Fang, Ruofan Liang, Lingxi Xie, Xiaopeng Zhang, Wei Shen, Qi Tian  

<details span>
<summary><b>Abstract</b></summary>
Reconstructing and rendering 3D objects from highly sparse views is of critical importance for promoting applications of 3D vision techniques and improving user experience. However, images from sparse views only contain very limited 3D information, leading to two significant challenges: 1) Difficulty in building multi-view consistency as images for matching are too few; 2) Partially omitted or highly compressed object information as view coverage is insufficient. To tackle these challenges, we propose GaussianObject, a framework to represent and render the 3D object with Gaussian splatting, that achieves high rendering quality with only 4 input images. We first introduce techniques of visual hull and floater elimination which explicitly inject structure priors into the initial optimization process for helping build multi-view consistency, yielding a coarse 3D Gaussian representation. Then we construct a Gaussian repair model based on diffusion models to supplement the omitted object information, where Gaussians are further refined. We design a self-generating strategy to obtain image pairs for training the repair model. Our GaussianObject is evaluated on several challenging datasets, including MipNeRF360, OmniObject3D, and OpenIllumination, achieving strong reconstruction results from only 4 views and significantly outperforming previous state-of-the-art methods. 
</details>

[📄 Paper](https://arxiv.org/pdf/2402.05054.pdf) | [🌐 Project Page](https://me.kiui.moe/lgm/) | [💻 Code](https://github.com/3DTopia/LGM) 

### 5. GALA3D: Towards Text-to-3D Complex Scene Generation via Layout-guided Generative Gaussian Splatting 
**Authors**: Xiaoyu Zhou, Xingjian Ran, Yajiao Xiong, Jinlin He, Zhiwei Lin, Yongtao Wang, Deqing Sun, Ming-Hsuan Yang  

<details span>
<summary><b>Abstract</b></summary>
We present GALA3D, generative 3D GAussians with LAyout-guided control, for effective compositional text-to-3D generation. We first utilize large language models (LLMs) to generate the initial layout and introduce a layout-guided 3D Gaussian representation for 3D content generation with adaptive geometric constraints. We then propose an object-scene compositional optimization mechanism with conditioned diffusion to collaboratively generate realistic 3D scenes with consistent geometry, texture, scale, and accurate interactions among multiple objects while simultaneously adjusting the coarse layout priors extracted from the LLMs to align with the generated scene. Experiments show that GALA3D is a user-friendly, end-to-end framework for state-of-the-art scene-level 3D content generation and controllable editing while ensuring the high fidelity of object-level entities within the scene.
</details>

[📄 Paper](https://arxiv.org/pdf/2402.07207.pdf) | [🌐 Project Page](https://gala3d.github.io/) | [💻 Code (not yet)](https://github.com/VDIGPKU/GALA3D)

### 6. IM-3D: Iterative Multiview Diffusion and Reconstruction for High-Quality 3D Generation  
**Authors**: Luke Melas-Kyriazi, Iro Laina, Christian Rupprecht, Natalia Neverova, Andrea Vedaldi, Oran Gafni, Filippos Kokkinos 

<details span>
<summary><b>Abstract</b></summary>
Most text-to-3D generators build upon off-the-shelf text-to-image models trained on billions of images. They use variants of Score Distillation Sampling (SDS), which is slow, somewhat unstable, and prone to artifacts. A mitigation is to fine-tune the 2D generator to be multi-view aware, which can help distillation or can be combined with reconstruction networks to output 3D objects directly. In this paper, we further explore the design space of text-to-3D models. We significantly improve multi-view generation by considering video instead of image generators. Combined with a 3D reconstruction algorithm which, by using Gaussian splatting, can optimize a robust image-based loss, we directly produce high-quality 3D outputs from the generated views. Our new method, IM-3D, reduces the number of evaluations of the 2D generator network 10-100x, resulting in a much more efficient pipeline, better quality, fewer geometric inconsistencies, and higher yield of usable 3D assets. 
</details>

[📄 Paper](https://arxiv.org/pdf/2402.08682.pdf) 

## 2023:
### 1. Text-to-3D using Gaussian Splatting
**Authors**: Zilong Chen, Feng Wang, Huaping Liu

<details span>
<summary><b>Abstract</b></summary>
In this paper, we present Gaussian Splatting based text-to-3D generation (GSGEN), a novel approach for generating high-quality 3D objects. Previous methods suffer from inaccurate geometry and limited fidelity due to the absence of 3D prior and proper representation. We leverage 3D Gaussian Splatting, a recent state-of-the-art representation, to address existing shortcomings by exploiting the explicit nature that enables the incorporation of 3D prior. Specifically, our method adopts a pro- gressive optimization strategy, which includes a geometry optimization stage and an appearance refinement stage. In geometry optimization, a coarse representation is established under a 3D geometry prior along with the ordinary 2D SDS loss, ensuring a sensible and 3D-consistent rough shape. Subsequently, the obtained Gaussians undergo an iterative refinement to enrich details. In this stage, we increase the number of Gaussians by compactness-based densification to enhance continuity and improve fidelity. With these designs, our approach can generate 3D content with delicate details and more accurate geometry. Extensive evaluations demonstrate the effectiveness of our method, especially for capturing high-frequency components.
</details>

[📄 Paper](https://arxiv.org/pdf/2309.16585.pdf) | [🌐 Project Page](https://gsgen3d.github.io/) | [💻 Code](https://github.com/gsgen3d/gsgen) | [🎥 Short Presentation](https://streamable.com/28snte) | [🎥 Explanation Video](https://www.youtube.com/live/l956ye13F8M?si=ZkvFL_lsY5OQUB7e)

### 2. DreamGaussian: Generative Gaussian Splatting for Efficient 3D Content Creation
**Authors**: Jiaxiang Tang, Jiawei Ren, Hang Zhou, Ziwei Liu, Gang Zeng

<details span>
<summary><b>Abstract</b></summary>
Recent advances in 3D content creation mostly leverage optimization-based 3D generation via score distillation sampling (SDS). Though promising results have been exhibited, these methods often suffer from slow per-sample optimization, limiting their practical usage. In this paper, we propose DreamGaussian, a novel 3D content generation framework that achieves both efficiency and quality simultaneously. Our key insight is to design a generative 3D Gaussian Splatting model with companioned mesh extraction and texture refinement in UV space. In contrast to the occupancy pruning used in Neural Radiance Fields, we demonstrate that the progressive densification of 3D Gaussians converges significantly faster for 3D generative tasks. To further enhance the texture quality and facilitate downstream applications, we introduce an efficient algorithm to convert 3D Gaussians into textured meshes and apply a fine-tuning stage to refine the details. Extensive experiments demonstrate the superior efficiency and competitive generation quality of our proposed approach. Notably, DreamGaussian produces high-quality textured meshes in just 2 minutes from a single-view image, achieving approximately 10 times acceleration compared to existing methods.
</details>

  [📄 Paper](https://arxiv.org/pdf/2309.16653.pdf) | [🌐 Project Page](https://dreamgaussian.github.io/) | [💻 Code](https://github.com/dreamgaussian/dreamgaussian) | [🎥 Explanation Video](https://www.youtube.com/live/l956ye13F8M?si=ZkvFL_lsY5OQUB7e)

### 3. GaussianDreamer: Fast Generation from Text to 3D Gaussian Splatting with Point Cloud Priors
**Authors**:  Taoran Yi1, Jiemin Fang, Guanjun Wu1, Lingxi Xie, Xiaopeng Zhang,
Wenyu Liu, Tian Qi, Xinggang Wang 
<details span>
<summary><b>Abstract</b></summary>
In recent times, the generation of 3D assets from text prompts has shown impressive results. Both 2D and 3D diffusion models can generate decent 3D objects based on prompts. 3D diffusion models have good 3D consistency, but their quality and generalization are limited as trainable  3D data is expensive and hard to obtain. 2D diffusion models enjoy strong abilities of generalization and fine generation, but the 3D consistency is hard to guarantee. This paper attempts to bridge the power from the two types of diffusion models via the recent explicit and efficient 3D Gaussian splatting representation. A fast 3D generation framework, named as GaussianDreamer, is proposed, where the 3D diffusion model provides point cloud priors for initialization and the 2D diffusion model enriches the geometry and appearance. Operations of noisy point growing and color perturbation are introduced to enhance the initialized Gaussians. Our GaussianDreamer can generate a high-quality 3D instance within 25 minutes on one GPU, much faster than previous methods, while the generated instances can be directly rendered in real time.
</details>

  [📄 Paper](https://arxiv.org/pdf/2310.08529.pdf) | [🌐 Project Page](https://taoranyi.com/gaussiandreamer/) | [💻 Code](https://github.com/hustvl/GaussianDreamer) 

### 4. GaussianDiffusion: 3D Gaussian Splatting for Denoising Diffusion Probabilistic Models with Structured Noise  
 Xinhai Li, Huaibin Wang, Kuo-Kun Tseng
<details span>
<summary><b>Abstract</b></summary>
 Text-to-3D, known for its efficient generation methods and expansive creative potential, has garnered significant attention in the AIGC domain. However, the amalgamation of Nerf and 2D diffusion models frequently yields oversaturated images, posing severe limitations on downstream industrial applications due to the constraints of pixelwise rendering method. Gaussian splatting has recently superseded the traditional pointwise sampling technique prevalent in NeRF-based methodologies, revolutionizing various aspects of 3D reconstruction. This paper introduces a novel text to 3D content generation framework based on Gaussian splatting, enabling fine control over image saturation through individual Gaussian sphere transparencies, thereby producing more realistic images. The challenge of achieving multi-view consistency in 3D generation significantly impedes modeling complexity and accuracy. Taking inspiration from SJC, we explore employing multi-view noise distributions to perturb images generated by 3D Gaussian splatting, aiming to rectify inconsistencies in multi-view geometry. We ingeniously devise an efficient method to generate noise that produces Gaussian noise from diverse viewpoints, all originating from a shared noise source. Furthermore, vanilla 3D Gaussian-based generation tends to trap models in local minima, causing artifacts like floaters, burrs, or proliferative elements. To mitigate these issues, we propose the variational Gaussian splatting technique to enhance the quality and stability of 3D appearance. To our knowledge, our approach represents the first comprehensive utilization of Gaussian splatting across the entire spectrum of 3D content generation processes.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.11221.pdf)  

### 5. LucidDreamer: Towards High-Fidelity Text-to-3D Generation via Interval Score Matching  
Yixun Liang, Xin Yang, Jiantao Lin, Haodong Li, Xiaogang Xu, Yingcong Chen
<details span>
<summary><b>Abstract</b></summary>
The recent advancements in text-to-3D generation mark a significant milestone in generative models, unlocking new possibilities for creating imaginative 3D assets across various real-world scenarios. While recent advancements in text-to-3D generation have shown promise, they often fall short in rendering detailed and high-quality 3D models. This problem is especially prevalent as many methods base themselves on Score Distillation Sampling (SDS). This paper identifies a notable deficiency in SDS, that it brings inconsistent and low-quality updating direction for the 3D model, causing the over-smoothing effect. To address this, we propose a novel approach called Interval Score Matching (ISM). ISM employs deterministic diffusing trajectories and utilizes interval-based score matching to counteract over-smoothing. Furthermore, we incorporate 3D Gaussian Splatting into our text-to-3D generation pipeline. Extensive experiments show that our model largely outperforms the state-of-the-art in quality and training efficiency.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.11284.pdf) | [💻 Code](https://github.com/EnVision-Research/LucidDreamer) 

### 6. LucidDreamer: Domain-free Generation of 3D Gaussian Splatting Scenes
Jaeyoung Chung, Suyoung Lee, Hyeongjin Nam, Jaerin Lee, Kyoung Mu Lee
<details span>
<summary><b>Abstract</b></summary>
With the widespread usage of VR devices and contents, demands for 3D scene generation techniques become more popular. Existing 3D scene generation models, however, limit the target scene to specific domain, primarily due to their training strategies using 3D scan dataset that is far from the real-world. To address such limitation, we propose LucidDreamer, a domain-free scene generation pipeline by fully leveraging the power of existing large-scale diffusion-based generative model. Our LucidDreamer has two alternate steps: Dreaming and Alignment. First, to generate multi-view consistent images from inputs, we set the point cloud as a geometrical guideline for each image generation. Specifically, we project a portion of point cloud to the desired view and provide the projection as a guidance for inpainting using the generative model. The inpainted images are lifted to 3D space with estimated depth maps, composing a new points. Second, to aggregate the new points into the 3D scene, we propose an aligning algorithm which harmoniously integrates the portions of newly generated 3D scenes. The finally obtained 3D scene serves as initial points for optimizing Gaussian splats. LucidDreamer produces Gaussian splats that are highly-detailed compared to the previous 3D scene generation methods, with no constraint on domain of the target scene. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.13384.pdf) | [🌐 Project Page](https://luciddreamer-cvlab.github.io/) | [💻 Code](https://github.com/anonymous-luciddreamer/LucidDreamer) 

### 7. HumanGaussian: Text-Driven 3D Human Generation with Gaussian Splatting  
Xian Liu, Xiaohang Zhan, Jiaxiang Tang, Ying Shan, Gang Zeng, Dahua Lin, Xihui Liu, Ziwei Liu
<details span>
<summary><b>Abstract</b></summary>
Realistic 3D human generation from text prompts is a desirable yet challenging task. Existing methods optimize 3D representations like mesh or neural fields via score distillation sampling (SDS), which suffers from inadequate fine details or excessive training time. In this paper, we propose an efficient yet effective framework, HumanGaussian, that generates high-quality 3D humans with fine-grained geometry and realistic appearance. Our key insight is that 3D Gaussian Splatting is an efficient renderer with periodic Gaussian shrinkage or growing, where such adaptive density control can be naturally guided by intrinsic human structures. Specifically, 1) we first propose a Structure-Aware SDS that simultaneously optimizes human appearance and geometry. The multi-modal score function from both RGB and depth space is leveraged to distill the Gaussian densification and pruning process. 2) Moreover, we devise an Annealed Negative Prompt Guidance by decomposing SDS into a noisier generative score and a cleaner classifier score, which well addresses the over-saturation issue. The floating artifacts are further eliminated based on Gaussian size in a prune-only phase to enhance generation smoothness. Extensive experiments demonstrate the superior efficiency and competitive quality of our framework, rendering vivid 3D humans under diverse scenarios.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17061.pdf) | [🌐 Project Page](https://alvinliu0.github.io/projects/HumanGaussian) | [💻 Code](https://github.com/alvinliu0/HumanGaussian) | [🎥 Short Presentation](https://www.youtube.com/watch?v=S3djzHoqPKY)

### 8. CG3D: Compositional Generation for Text-to-3D
Alexander Vilesov, Pradyumna Chari, Achuta Kadambi
<details span>
<summary><b>Abstract</b></summary>
With the onset of diffusion-based generative models and their ability to generate text-conditioned images, content generation has received a massive invigoration. Recently, these models have been shown to provide useful guidance for the generation of 3D graphics assets. However, existing work in text-conditioned 3D generation faces fundamental constraints: (i) inability to generate detailed, multi-object scenes, (ii) inability to textually control multi-object configurations, and (iii) physically realistic scene composition. In this work, we propose CG3D, a method for compositionally generating scalable 3D assets that resolves these constraints. We find that explicit Gaussian radiance fields, parameterized to allow for compositions of objects, possess the capability to enable semantically and physically consistent scenes. By utilizing a guidance framework built around this explicit representation, we show state of the art results, capable of even exceeding the guiding diffusion model in terms of object combinations and physics accuracy.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17907.pdf) | [🌐 Project Page](https://asvilesov.github.io/CG3D/) | | [🎥 Short Presentation](https://www.youtube.com/watch?v=FMAVeolsE7s)


### 9. Learn to Optimize Denoising Scores for 3D Generation - A Unified and Improved Diffusion Prior on NeRF and 3D Gaussian Splatting 
Xiaofeng Yang, Yiwen Chen, Cheng Chen, Chi Zhang, Yi Xu, Xulei Yang, Fayao Liu and Guosheng Lin
<details span>
<summary><b>Abstract</b></summary>
We propose a unified framework aimed at enhancing the diffusion priors for 3D generation tasks. Despite the critical importance of these tasks, existing methodologies often struggle to generate high-caliber results. We begin by examining the inherent limitations in previous diffusion priors. We identify a divergence between the diffusion priors and the training procedures of diffusion models that substantially impairs the quality of 3D generation. To address this issue, we propose a novel, unified framework that iteratively optimizes both the 3D model and the diffusion prior. Leveraging the different learnable parameters of the diffusion prior, our approach offers multiple configurations, affording various trade-offs between performance and implementation complexity. Notably, our experimental results demonstrate that our method markedly surpasses existing techniques, establishing new state-of-the-art in the realm of text-to-3D generation. Furthermore, our approach exhibits impressive performance on both NeRF and the newly introduced 3D Gaussian Splatting backbones. Additionally, our framework yields insightful contributions to the understanding of recent score distillation methods, such as the VSD and DDS loss. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.04820.pdf) | [🌐 Project Page](https://yangxiaofeng.github.io/demo_diffusion_prior/) | [💻 Code](https://github.com/yangxiaofeng/LODS)


### 10. Align Your Gaussians: Text-to-4D with Dynamic 3D Gaussians and Composed Diffusion Models 
Andreas Blattmann, Robin Rombach, Huan Ling, Tim Dockhorn, Seung Wook Kim, Sanja Fidler, Karsten Kreis
<details span>
<summary><b>Abstract</b></summary>
Recent advancements in 3D reconstruction from single images have been driven by the evolution of generative models. Prominent among these are methods based on Score Distillation Sampling (SDS) and the adaptation of diffusion models in the 3D domain. Despite their progress, these techniques often face limitations due to slow optimization or rendering processes, leading to extensive training and optimization times. In this paper, we introduce a novel approach for single-view reconstruction that efficiently generates a 3D model from a single image via feed-forward inference. Our method utilizes two transformer-based networks, namely a point decoder and a triplane decoder, to reconstruct 3D objects using a hybrid Triplane-Gaussian intermediate representation. This hybrid representation strikes a balance, achieving a faster rendering speed compared to implicit representations while simultaneously delivering superior rendering quality than explicit representations. The point decoder is designed for generating point clouds from single images, offering an explicit representation which is then utilized by the triplane decoder to query Gaussian features for each point. This design choice addresses the challenges associated with directly regressing explicit 3D Gaussian attributes characterized by their non-structural nature. Subsequently, the 3D Gaussians are decoded by an MLP to enable rapid rendering through splatting. Both decoders are built upon a scalable, transformer-based architecture and have been efficiently trained on large-scale 3D datasets. The evaluations conducted on both synthetic datasets and real-world images demonstrate that our method not only achieves higher quality but also ensures a faster runtime in comparison to previous state-of-the-art techniques.
</details>

  [📄 Paper](https://arxiv.org/pdf/2304.08818.pdf) | [🌐 Project Page](https://research.nvidia.com/labs/toronto-ai/AlignYourGaussians/)

### 11. DreamGaussian4D: Generative 4D Gaussian Splatting 
**Authors**: Jiawei Ren, Liang Pan, Jiaxiang Tang, Chi Zhang, Ang Cao, Gang Zeng, Ziwei Liu 

<details span>
<summary><b>Abstract</b></summary>
Remarkable progress has been made in 4D content generation recently. However, existing methods suffer from long optimization time, lack of motion controllability, and a low level of detail. In this paper, we introduce DreamGaussian4D, an efficient 4D generation framework that builds on 4D Gaussian Splatting representation. Our key insight is that the explicit modeling of spatial transformations in Gaussian Splatting makes it more suitable for the 4D generation setting compared with implicit representations. DreamGaussian4D reduces the optimization time from several hours to just a few minutes, allows flexible control of the generated 3D motion, and produces animated meshes that can be efficiently rendered in 3D engines. 
</details>

[📄 Paper](https://arxiv.org/pdf/2312.17142.pdf) | [🌐 Project Page](https://jiawei-ren.github.io/projects/dreamgaussian4d/) | [💻 Code](https://github.com/jiawei-ren/dreamgaussian4d) 

### 12. 4DGen: Grounded 4D Content Generation with Spatial-temporal Consistency 
**Authors**: Yuyang Yin, Dejia Xu, Zhangyang Wang, Yao Zhao, Yunchao Wei 

<details span>
<summary><b>Abstract</b></summary>
Aided by text-to-image and text-to-video diffusion models, existing 4D content creation pipelines utilize score distillation sampling to optimize entire dynamic 3D scene. However, as these pipelines generate 4D content from text or image inputs, they incur significant time and effort in prompt engineering through trial and error. This work introduces 4DGen, a novel, holistic framework for grounded 4D content generation that decomposes the 4D generation task into multiple stages. We identify static 3D assets and monocular video sequences as key components in constructing the 4D content. Our pipeline facilitates conditional 4D generation, enabling users to specify geometry (3D assets) and motion (monocular videos), thus offering superior control over content creation. Furthermore, we construct our 4D representation using dynamic 3D Gaussians, which permits efficient, high-resolution supervision through rendering during training, thereby facilitating high-quality 4D generation. Additionally, we employ spatial-temporal pseudo labels on anchor frames, along with seamless consistency priors implemented through 3D-aware score distillation sampling and smoothness regularizations. Compared to existing baselines, our approach yields competitive results in faithfully reconstructing input signals and realistically inferring renderings from novel viewpoints and timesteps. Most importantly, our method supports grounded generation, offering users enhanced control, a feature difficult to achieve with previous methods.
</details>

[📄 Paper](https://arxiv.org/pdf/2312.17225.pdf) | [🌐 Project Page](https://vita-group.github.io/4DGen/) | [💻 Code](https://github.com/VITA-Group/4DGen) | [🎥 Short Presentation](https://www.youtube.com/watch?v=-bXyBKdpQ1o) 

### 13. Text2Immersion: Generative Immersive Scene with 3D Gaussian 
**Authors**: Hao Ouyang, Kathryn Heal, Stephen Lombardi, Tiancheng Sun 

<details span>
<summary><b>Abstract</b></summary>
We introduce Text2Immersion, an elegant method for producing high-quality 3D immersive scenes from text prompts. Our proposed pipeline initiates by progressively generating a Gaussian cloud using pre-trained 2D diffusion and depth estimation models. This is followed by a refining stage on the Gaussian cloud, interpolating and refining it to enhance the details of the generated scene. Distinct from prevalent methods that focus on single object or indoor scenes, or employ zoom-out trajectories, our approach generates diverse scenes with various objects, even extending to the creation of imaginary scenes. Consequently, Text2Immersion can have wide-ranging implications for various applications such as virtual reality, game development, and automated content creation. Extensive evaluations demonstrate that our system surpasses other methods in rendering quality and diversity, further progressing towards text-driven 3D scene generation.
</details>

[📄 Paper](https://arxiv.org/pdf/2312.09242.pdf) | [🌐 Project Page](https://ken-ouyang.github.io/text2immersion/index.html) | [💻 Code (not yet)]() 

### 14. Repaint123: Fast and High-quality One Image to 3D Generation with Progressive Controllable 2D Repainting 
**Authors**: Junwu Zhang, Zhenyu Tang, Yatian Pang, Xinhua Cheng, Peng Jin, Yida Wei, Munan Ning, Li Yuan 

<details span>
<summary><b>Abstract</b></summary>
Recent one image to 3D generation methods commonly adopt Score Distillation Sampling (SDS). Despite the impressive results, there are multiple deficiencies including multi-view inconsistency, over-saturated and over-smoothed textures, as well as the slow generation speed. To address these deficiencies, we present Repaint123 to alleviate multi-view bias as well as texture degradation and speed up the generation process. The core idea is to combine the powerful image generation capability of the 2D diffusion model and the texture alignment ability of the repainting strategy for generating high-quality multi-view images with consistency. We further propose visibility-aware adaptive repainting strength for overlap regions to enhance the generated image quality in the repainting process. The generated high-quality and multi-view consistent images enable the use of simple Mean Square Error (MSE) loss for fast 3D content generation. We conduct extensive experiments and show that our method has a superior ability to generate high-quality 3D content with multi-view consistency and fine textures in 2 minutes from scratch.
</details>

[📄 Paper](https://arxiv.org/pdf/2312.13271.pdf) | [🌐 Project Page](https://pku-yuangroup.github.io/repaint123/) | [💻 Code (not yet)](https://github.com/PKU-YuanGroup/repaint123) 

<br>

## Dynamics and Deformation:
## 2024:
### 1. 4D Gaussian Splatting: Towards Efficient Novel View Synthesis for Dynamic Scenes 
**Authors**: Yuanxing Duan, Fangyin Wei, Qiyu Dai, Yuhang He, Wenzheng Chen, Baoquan Chen 

<details span>
<summary><b>Abstract</b></summary>
We consider the problem of novel view synthesis (NVS) for dynamic scenes. Recent neural approaches have accomplished exceptional NVS results for static 3D scenes, but extensions to 4D time-varying scenes remain non-trivial. Prior efforts often encode dynamics by learning a canonical space plus implicit or explicit deformation fields, which struggle in challenging scenarios like sudden movements or capturing high-fidelity renderings. In this paper, we introduce 4D Gaussian Splatting (4DGS), a novel method that represents dynamic scenes with anisotropic 4D XYZT Gaussians, inspired by the success of 3D Gaussian Splatting in static scenes. We model dynamics at each timestamp by temporally slicing the 4D Gaussians, which naturally compose dynamic 3D Gaussians and can be seamlessly projected into images. As an explicit spatial-temporal representation, 4DGS demonstrates powerful capabilities for modeling complicated dynamics and fine details, especially for scenes with abrupt motions. We further implement our temporal slicing and splatting techniques in a highly optimized CUDA acceleration framework, achieving real-time inference rendering speeds of up to 277 FPS on an RTX 3090 GPU and 583 FPS on an RTX 4090 GPU. Rigorous evaluations on scenes with diverse motions showcase the superior efficiency and effectiveness of 4DGS, which consistently outperforms existing methods both quantitatively and qualitatively. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.03307.pdf) 


## 2023:
### 1. Dynamic 3D Gaussians: Tracking by Persistent Dynamic View Synthesis
**Authors**: Jonathon Luiten, Georgios Kopanas, Bastian Leibe, Deva Ramanan

<details span>
<summary><b>Abstract</b></summary>
We present a method that simultaneously addresses the tasks of dynamic scene novel-view synthesis and six degree-of-freedom (6-DOF) tracking of all dense scene elements. We follow an analysis-by-synthesis framework, inspired by recent work that models scenes as a collection of 3D Gaussians which are optimized to reconstruct input images via differentiable rendering. To model dynamic scenes, we allow Gaussians to move and rotate over time while enforcing that they have persistent color, opacity, and size. By regularizing Gaussians’ motion and rotation with local rigidity constraints, we show that our Dynamic 3D Gaussians correctly model the same area of physical space over time, including the rotation of that space. Dense 6-DOF tracking and dynamic reconstruction emerges naturally from persistent dynamic view synthesis, without requiring any correspondence or flow as input. We demonstrate a large number of downstream applications enabled by our representation, including first-person view synthesis, dynamic compositional scene synthesis, and 4D video editing.
</details>

  [📄 Paper](https://dynamic3dgaussians.github.io/paper.pdf) | [🌐 Project Page](https://dynamic3dgaussians.github.io/) | [💻 Code](https://github.com/JonathonLuiten/Dynamic3DGaussians) | [🎥 Explanation Video](https://www.youtube.com/live/hDuy1TgD8I4?si=6oGN0IYnPRxOibpg)

### 2. Deformable 3D Gaussians for High-Fidelity Monocular Dynamic Scene Reconstruction
**Authors**: Ziyi Yang, Xinyu Gao, Wen Zhou, Shaohui Jiao, Yuqing Zhang, Xiaogang Jin 

<details span>
<summary><b>Abstract</b></summary>
Implicit neural representation has opened up new avenues for dynamic scene reconstruction and rendering. Nonetheless, state-of-the-art methods of dynamic neural rendering rely heavily on these implicit representations, which frequently struggle with accurately capturing the intricate details of objects in the scene. Furthermore, implicit methods struggle to achieve real-time rendering in general dynamic scenes, limiting their use in a wide range of tasks. To address the issues, we propose a deformable 3D Gaussians Splatting method that reconstructs scenes using explicit 3D Gaussians and learns Gaussians in canonical space with a deformation field to model monocular dynamic scenes. We also introduced a smoothing training mechanism with no extra overhead to mitigate the impact of inaccurate poses in real datasets on the smoothness of time interpolation tasks. Through differential gaussian rasterization, the deformable 3D Gaussians not only achieve higher rendering quality but also real-time rendering speed. Experiments show that our method outperforms existing methods significantly in terms of both rendering quality and speed, making it well-suited for tasks such as novel-view synthesis, time synthesis, and real-time rendering. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2309.13101.pdf) | [🌐 Project Page](https://ingra14m.github.io/Deformable-Gaussians/) | [💻 Code](https://github.com/ingra14m/Deformable-3D-Gaussians) 

### 3. 4D Gaussian Splatting for Real-Time Dynamic Scene Rendering
**Authors**: Guanjun Wu, Taoran Yi, Jiemin Fang, Lingxi Xie, Xiaopeng Zhang, Wei Wei, Wenyu Liu, Tian Qi, Xinggang Wang

<details span>
<summary><b>Abstract</b></summary>
Representing and rendering dynamic scenes has been an
important but challenging task. Especially, to accurately
model complex motions, high efficiency is usually hard to
maintain. We introduce the 4D Gaussian Splatting (4D-GS)
to achieve real-time dynamic scene rendering while also
enjoying high training and storage efficiency. An efficient
deformation field is constructed to model both Gaussian
motions and shape deformations. Different adjacent Gaussians
are connected via a HexPlane to produce more accurate
position and shape deformations. Our 4D-GS method
achieves real-time rendering under high resolutions, 70
FPS at a 800×800 resolution on an RTX 3090 GPU, while
maintaining comparable or higher quality than previous
state-of-the-art method.
</details>

  [📄 Paper](https://arxiv.org/pdf/2310.08528.pdf) | [🌐 Project Page](https://guanjunwu.github.io/4dgs/) | [💻 Code](https://github.com/hustvl/4DGaussians)
  
### 4. Real-time Photorealistic Dynamic Scene Representation and Rendering with 4D Gaussian Splatting
**Authors**: Zeyu Yang, Hongye Yang, Zijie Pan, Xiatian Zhu, Li Zhang

<details span>
<summary><b>Abstract</b></summary>
Reconstructing dynamic 3D scenes from 2D images and generating diverse views over time is challenging due to scene complexity and temporal dynamics. Despite advancements in neural implicit models, limitations persist: (i) Inadequate Scene Structure: Existing methods struggle to reveal the spatial and temporal structure of dynamic scenes from directly learning the complex 6D plenoptic function. (ii) Scaling Deformation Modeling: Explicitly modeling scene element deformation becomes impractical for complex dynamics. To address these issues, we consider the spacetime as an entirety and propose to approximate the underlying spatio-temporal 4D volume of a dynamic scene by optimizing a collection of 4D primitives, with explicit geometry and appearance modeling. Learning to optimize the 4D primitives enables us to synthesize novel views at any desired time with our tailored rendering routine. Our model is conceptually simple, consisting of a 4D Gaussian parameterized by anisotropic ellipses that can rotate arbitrarily in space and time, as well as view-dependent and time-evolved appearance represented by the coefficient of 4D spherindrical harmonics. This approach offers simplicity, flexibility for variable-length video and end-to-end training, and efficient real-time rendering, making it suitable for capturing complex dynamic scene motions. Experiments across various benchmarks, including monocular and multi-view scenarios, demonstrate our 4DGS model's superior visual quality and efficiency. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2310.10642.pdf) | [💻 Code](https://github.com/fudan-zvg/4d-gaussian-splatting) 

### 5. An Efficient 3D Gaussian Representation for Monocular/Multi-view Dynamic Scenes 
**Authors**: Kai Katsumata, Duc Minh Vo, Hideki Nakayama 

<details span>
<summary><b>Abstract</b></summary>
In novel view synthesis of scenes from multiple input views, 3D Gaussian splatting emerges as a viable alternative to existing radiance field approaches, delivering great visual quality and real-time rendering. While successful in static scenes, the present advancement of 3D Gaussian representation, however, faces challenges in dynamic scenes in terms of memory consumption and the need for numerous observations per time step, due to the onus of storing 3D Gaussian parameters per time step. In this study, we present an efficient 3D Gaussian representation tailored for dynamic scenes in which we define positions and rotations as functions of time while leaving other time-invariant properties of the static 3D Gaussian unchanged. Notably, our representation reduces memory usage, which is consistent regardless of the input sequence length. Additionally, it mitigates the risk of overfitting observed frames by accounting for temporal changes. The optimization of our Gaussian representation based on image and flow reconstruction results in a powerful framework for dynamic scene view synthesis in both monocular and multi-view cases. We obtain the highest rendering speed of 118 frames per second (FPS) at a resolution of 1352×1014 with a single GPU, showing the practical usability and effectiveness of our proposed method in dynamic scene rendering scenarios
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.12897.pdf) | [💻 Code](https://github.com/raven38/EfficientDynamic3DGaussian)

### 6. DynMF: Neural Motion Factorization for Real-time Dynamic View Synthesis with 3D Gaussian Splatting  
**Authors**: Agelos Kratimenos, Jiahui Lei, Kostas Daniilidis 

<details span>
<summary><b>Abstract</b></summary>
Accurately and efficiently modeling dynamic scenes and motions is considered so challenging a task due to temporal dynamics and motion complexity. To address these challenges, we propose DynMF, a compact and efficient representation that decomposes a dynamic scene into a few neural trajectories. We argue that the per-point motions of a dynamic scene can be decomposed into a small set of explicit or learned trajectories. Our carefully designed neural framework consisting of a tiny set of learned basis queried only in time allows for rendering speed similar to 3D Gaussian Splatting, surpassing 120 FPS, while at the same time, requiring only double the storage compared to static scenes. Our neural representation adequately constrains the inherently underconstrained motion field of a dynamic scene leading to effective and fast optimization. This is done by biding each point to motion coefficients that enforce the per-point sharing of basis trajectories. By carefully applying a sparsity loss to the motion coefficients, we are able to disentangle the motions that comprise the scene, independently control them, and generate novel motion combinations that have never been seen before. We can reach state-of-the-art render quality within just 5 minutes of training and in less than half an hour, we can synthesize novel views of dynamic scenes with superior photorealistic quality. Our representation is interpretable, efficient, and expressive enough to offer real-time view synthesis of complex dynamic scene motions, in monocular and multi-view scenarios. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.00112.pdf) | [🌐 Project Page](https://agelosk.github.io/dynmf/) | [💻 Code (not yet)](https://github.com/agelosk/dynmf)

### 7. Control4D: Efficient 4D Portrait Editing with Text 
**Authors**: Ruizhi Shao, Jingxiang Sun, Cheng Peng, Zerong Zheng, Boyao Zhou, Hongwen Zhang, Yebin Liu  

<details span>
<summary><b>Abstract</b></summary>
We introduce Control4D, an innovative framework for editing dynamic 4D portraits using text instructions. Our method addresses the prevalent challenges in 4D editing, notably the inefficiencies of existing 4D representations and the inconsistent editing effect caused by diffusion-based editors. We first propose GaussianPlanes, a novel 4D representation that makes Gaussian Splatting more structured by applying plane-based decomposition in 3D space and time. This enhances both efficiency and robustness in 4D editing. Furthermore, we propose to leverage a 4D generator to learn a more continuous generation space from inconsistent edited images produced by the diffusion-based editor, which effectively improves the consistency and quality of 4D editing. Comprehensive evaluation demonstrates the superiority of Control4D, including significantly reduced training time, high-quality rendering, and spatial-temporal consistency in 4D portrait editing.
</details>

  [📄 Paper](https://arxiv.org/pdf/2305.20082.pdf) | [🌐 Project Page](https://control4darxiv.github.io/) | [💻 Code (not yet)]()

### 8. SC-GS: Sparse-Controlled Gaussian Splatting for Editable Dynamic Scenes 
**Authors**:  Yi-Hua Huang, Yang-Tian Sun, Ziyi Yang, Xiaoyang Lyu, Yan-Pei Cao, Xiaojuan Qi

<details span>
<summary><b>Abstract</b></summary>
Novel view synthesis for dynamic scenes is still a challenging problem in computer vision and graphics. Recently, Gaussian splatting has emerged as a robust technique to represent static scenes and enable high-quality and real-time novel view synthesis. Building upon this technique, we propose a new representation that explicitly decomposes the motion and appearance of dynamic scenes into sparse control points and dense Gaussians, respectively. Our key idea is to use sparse control points, significantly fewer in number than the Gaussians, to learn compact 6 DoF transformation bases, which can be locally interpolated through learned interpolation weights to yield the motion field of 3D Gaussians. We employ a deformation MLP to predict time-varying 6 DoF transformations for each control point, which reduces learning complexities, enhances learning abilities, and facilitates obtaining temporal and spatial coherent motion patterns. Then, we jointly learn the 3D Gaussians, the canonical space locations of control points, and the deformation MLP to reconstruct the appearance, geometry, and dynamics of 3D scenes. During learning, the location and number of control points are adaptively adjusted to accommodate varying motion complexities in different regions, and an ARAP loss following the principle of as rigid as possible is developed to enforce spatial continuity and local rigidity of learned motions. Finally, thanks to the explicit sparse motion representation and its decomposition from appearance, our method can enable user-controlled motion editing while retaining high-fidelity appearances. Extensive experiments demonstrate that our approach outperforms existing approaches on novel view synthesis with a high rendering speed and enables novel appearance-preserved motion editing applications.
</details>

  [📄 Paper](https://yihua7.github.io/SC-GS-web/materials/SC_GS_Arxiv.pdf) | [🌐 Project Page](https://yihua7.github.io/SC-GS-web/) | [💻 Code](https://github.com/yihua7/SC-GS)

### 9. Neural Parametric Gaussians for Monocular Non-Rigid Object Reconstruction
**Authors**: Devikalyan Das, Christopher Wewer, Raza Yunus, Eddy Ilg, Jan Eric Lenssen

<details span>
<summary><b>Abstract</b></summary>
Reconstructing dynamic objects from monocular videos is a severely underconstrained and challenging problem, and recent work has approached it in various directions. However, owing to the ill-posed nature of this problem, there has been no solution that can provide consistent, highquality novel views from camera positions that are significantly different from the training views. In this work, we introduce Neural Parametric Gaussians (NPGs) to take on this challenge by imposing a two-stage approach: first, we fit a low-rank neural deformation model, which then is used as regularization for non-rigid reconstruction in the second stage. The first stage learns the object’s deformations such that it preserves consistency in novel views. The second stage obtains high reconstruction quality by optimizing 3D Gaussians that are driven by the coarse model. To this end, we introduce a local 3D Gaussian representation, where temporally shared Gaussians are anchored in and deformed by local oriented volumes. The resulting combined model can be rendered as radiance fields, resulting in high-quality photo-realistic reconstructions of the non-rigidly deforming objects, maintaining 3D consistency across novel views. We demonstrate that NPGs achieve superior results compared to previous works, especially in challenging scenarios with few multi-view cues. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.01196.pdf)

### 10. Gaussian-Flow: 4D Reconstruction with Dynamic 3D Gaussian Particle
**Authors**: Youtian Lin, Zuozhuo Dai, Siyu Zhu, Yao Yao 

<details span>
<summary><b>Abstract</b></summary>
We introduce Gaussian-Flow, a novel point-based approach for fast dynamic scene reconstruction and real-time rendering from both multi-view and monocular videos. In contrast to the prevalent NeRF-based approaches hampered by slow training and rendering speeds, our approach harnesses recent advancements in point-based 3D Gaussian Splatting (3DGS). Specifically, a novel Dual-Domain Deformation Model (DDDM) is proposed to explicitly model attribute deformations of each Gaussian point, where the time-dependent residual of each attribute is captured by a polynomial fitting in the time domain, and a Fourier series fitting in the frequency domain. The proposed DDDM is capable of modeling complex scene deformations across long video footage, eliminating the need for training separate 3DGS for each frame or introducing an additional implicit neural field to model 3D dynamics. Moreover, the explicit deformation modeling for discretized Gaussian points ensures ultra-fast training and rendering of a 4D scene, which is comparable to the original 3DGS designed for static 3D reconstruction. Our proposed approach showcases a substantial efficiency improvement, achieving a 5× faster training speed compared to the per-frame 3DGS modeling. In addition, quantitative results demonstrate that the proposed Gaussian-Flow significantly outperforms previous leading methods in novel view rendering quality.
</details>

  [📄 Paper](https://arxiv.org/pdf/2310.08528.pdf) | [🌐 Project Page](https://nju-3dv.github.io/projects/Gaussian-Flow) | [💻 Code (not yet)]()

### 11.CoGS: Controllable Gaussian Splatting 
**Authors**: Heng Yu, Joel Julin, Zoltán Á. Milacski, Koichiro Niinuma, László A. Jeni 

<details span>
<summary><b>Abstract</b></summary>
Capturing and re-animating the 3D structure of articulated objects present significant barriers. On one hand, methods requiring extensively calibrated multi-view setups are prohibitively complex and resource-intensive, limiting their practical applicability. On the other hand, while single-camera Neural Radiance Fields (NeRFs) offer a more streamlined approach, they have excessive training and rendering costs. 3D Gaussian Splatting would be a suitable alternative but for two reasons. Firstly, existing methods for 3D dynamic Gaussians require synchronized multi-view cameras, and secondly, the lack of controllability in dynamic scenarios. We present CoGS, a method for Controllable Gaussian Splatting, that enables the direct manipulation of scene elements, offering real-time control of dynamic scenes without the prerequisite of pre-computing control signals. We evaluated CoGS using both synthetic and real-world datasets that include dynamic objects that differ in degree of difficulty. In our evaluations, CoGS consistently outperformed existing dynamic and controllable neural representations in terms of visual fidelity. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.05664.pdf) | [🌐 Project Page](https://cogs2023.github.io/) | [💻 Code (not yet)]()

### 12. GauFRe: Gaussian Deformation Fields for Real-time Dynamic Novel View Synthesis 
**Authors**: Yiqing Liang, Numair Khan, Zhengqin Li, Thu Nguyen-Phuoc, Douglas Lanman, James Tompkin, Lei Xiao 

<details span>
<summary><b>Abstract</b></summary>
We propose a method for dynamic scene reconstruction using deformable 3D Gaussians that is tailored for monocular video. Building upon the efficiency of Gaussian splatting, our approach extends the representation to accommodate dynamic elements via a deformable set of Gaussians residing in a canonical space, and a time-dependent deformation field defined by a multi-layer perceptron (MLP). Moreover, under the assumption that most natural scenes have large regions that remain static, we allow the MLP to focus its representational power by additionally including a static Gaussian point cloud. The concatenated dynamic and static point clouds form the input for the Gaussian Splatting rasterizer, enabling real-time rendering. The differentiable pipeline is optimized end-to-end with a self-supervised rendering loss. Our method achieves results that are comparable to state-of-the-art dynamic neural radiance field methods while allowing much faster optimization and rendering.
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.11458.pdf) | [🌐 Project Page](https://lynl7130.github.io/gaufre/index.html) | [🎥 Short Presentation](https://youtu.be/YweWidWO8rI?si=jMssQdIXQV67kwzS)

### 13. Spacetime Gaussian Feature Splatting for Real-Time Dynamic View Synthesis 
**Authors**: Zhan Li, Zhang Chen, Zhong Li, Yi Xu 

<details span>
<summary><b>Abstract</b></summary>
Novel view synthesis of dynamic scenes has been an intriguing yet challenging problem. Despite recent advancements, simultaneously achieving high-resolution photorealistic results, real-time rendering, and compact storage remains a formidable task. To address these challenges, we propose Spacetime Gaussian Feature Splatting as a novel dynamic scene representation, composed of three pivotal components. First, we formulate expressive Spacetime Gaussians by enhancing 3D Gaussians with temporal opacity and parametric motion/rotation. This enables Spacetime Gaussians to capture static, dynamic, as well as transient content within a scene. Second, we introduce splatted feature rendering, which replaces spherical harmonics with neural features. These features facilitate the modeling of view- and time-dependent appearance while maintaining small size. Third, we leverage the guidance of training error and coarse depth to sample new Gaussians in areas that are challenging to converge with existing pipelines. Experiments on several established real-world datasets demonstrate that our method achieves state-of-the-art rendering quality and speed, while retaining compact storage. At 8K resolution, our lite-version model can render at 60 FPS on an Nvidia RTX 4090 GPU. 
</details>

[📄 Paper](https://arxiv.org/pdf/2312.16812.pdf) | [🌐 Project Page](https://oppo-us-research.github.io/SpacetimeGaussians-website/) | [💻 Code](https://github.com/oppo-us-research/SpacetimeGaussians) | [🎥 Short Presentation](https://www.youtube.com/watch?v=YsPPmf-E6Lg)

### 14. MD-Splatting: Learning Metric Deformation from 4D Gaussians in Highly Deformable Scenes
**Authors**: Bardienus P. Duisterhof, Zhao Mandi, Yunchao Yao, Jia-Wei Liu, Mike Zheng Shou, Shuran Song, Jeffrey Ichnowski

<details span>
<summary><b>Abstract</b></summary>
Accurate 3D tracking in highly deformable scenes with occlusions and shadows can facilitate new applications in robotics, augmented reality, and generative AI. However, tracking under these conditions is extremely challenging due to the ambiguity that arises with large deformations, shadows, and occlusions. We introduce MD-Splatting, an approach for simultaneous 3D tracking and novel view synthesis, using video captures of a dynamic scene from various camera poses. MD-Splatting builds on recent advances in Gaussian splatting, a method that learns the properties of a large number of Gaussians for state-of-the-art and fast novel view synthesis. MD-Splatting learns a deformation function to project a set of Gaussians with non-metric, thus canonical, properties into metric space. The deformation function uses a neural-voxel encoding and a multilayer perceptron (MLP) to infer Gaussian position, rotation, and a shadow scalar. We enforce physics-inspired regularization terms based on local rigidity, conservation of momentum, and isometry, which leads to trajectories with smaller trajectory errors. MD-Splatting achieves high-quality 3D tracking on highly deformable scenes with shadows and occlusions. Compared to state-of-the-art, we improve 3D tracking by an average of 23.9 %, while simultaneously achieving high-quality novel view synthesis. With sufficient texture such as in scene 6, MD-Splatting achieves a median tracking error of 3.39 mm on a cloth of 1 x 1 meters in size
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.00583) | [🌐 Project Page](https://md-splatting.github.io/) | [💻 Code (not released yet)](https://github.com/momentum-robotics-lab/md-splatting) 

### 15. SWAGS: Sampling Windows Adaptively for Dynamic 3D Gaussian Splatting 
**Authors**: Richard Shaw, Jifei Song, Arthur Moreau, Michal Nazarczuk, Sibi Catley-Chandar, Helisa Dhamo, Eduardo Perez-Pellitero 

<details span>
<summary><b>Abstract</b></summary>
Novel view synthesis has shown rapid progress recently, with methods capable of producing evermore photo-realistic results. 3D Gaussian Splatting has emerged as a particularly promising method, producing high-quality renderings of static scenes and enabling interactive viewing at real-time frame rates. However, it is currently limited to static scenes only. In this work, we extend 3D Gaussian Splatting to reconstruct dynamic scenes. We model the dynamics of a scene using a tunable MLP, which learns the deformation field from a canonical space to a set of 3D Gaussians per frame. To disentangle the static and dynamic parts of the scene, we learn a tuneable parameter for each Gaussian, which weighs the respective MLP parameters to focus attention on the dynamic parts. This improves the model's ability to capture dynamics in scenes with an imbalance of static to dynamic regions. To handle scenes of arbitrary length whilst maintaining high rendering quality, we introduce an adaptive window sampling strategy to partition the sequence into windows based on the amount of movement in the sequence. We train a separate dynamic Gaussian Splatting model for each window, allowing the canonical representation to change, thus enabling the reconstruction of scenes with significant geometric or topological changes. Temporal consistency is enforced using a fine-tuning step with self-supervising consistency loss on randomly sampled novel views. As a result, our method produces high-quality renderings of general dynamic scenes with competitive quantitative performance, which can be viewed in real-time with our dynamic interactive viewer
</details>

[📄 Paper](https://arxiv.org/pdf/2312.13308.pdf) 

### 16. 3DGStream: On-the-Fly Training of 3D Gaussians for Efficient Streaming of Photo-Realistic Free-Viewpoint Videos 
**Authors**: Jiakai Sun, Han Jiao, Guangyuan Li, Zhanjie Zhang, Lei Zhao, Wei Xing 

<details span>
<summary><b>Abstract</b></summary>
Constructing photo-realistic Free-Viewpoint Videos (FVVs) of dynamic scenes from multi-view videos remains a challenging endeavor. Despite the remarkable advancements achieved by current neural rendering techniques, these methods generally require complete video sequences for offline training and are not capable of real-time rendering. To address these constraints, we introduce 3DGStream, a method designed for efficient FVV streaming of real-world dynamic scenes. Our method achieves fast on-the-fly per-frame reconstruction within 12 seconds and real-time rendering at 200 FPS. Specifically, we utilize 3D Gaussians (3DGs) to represent the scene. Instead of the naïve approach of directly optimizing 3DGs per-frame, we employ a compact Neural Transformation Cache (NTC) to model the translations and rotations of 3DGs, markedly reducing the training time and storage required for each FVV frame. Furthermore, we propose an adaptive 3DG addition strategy to handle emerging objects in dynamic scenes. Experiments demonstrate that 3DGStream achieves competitive performance in terms of rendering speed, image quality, training time, and model storage when compared with state-of-the-art methods. 
</details>

[📄 Paper](https://arxiv.org/pdf/2403.01444.pdf) | [🌐 Project Page](https://sjojok.github.io/3dgstream/)

<br>

## Editing:
## 2024:
### 1. CoSSegGaussians: Compact and Swift Scene Segmenting 3D Gaussians
**Authors**: Bin Dou, Tianyu Zhang, Yongjia Ma, Zhaohui Wang, Zejian Yuan
<details span>
<summary><b>Abstract</b></summary>
We propose Compact and Swift Segmenting 3D Gaussians(CoSSegGaussians), a method for compact 3D-consistent scene segmentation at fast rendering speed with only RGB images input. Previous NeRF-based 3D segmentation methods have relied on implicit or voxel neural scene representation and ray-marching volume rendering which are time consuming. Recent 3D Gaussian Splatting significantly improves the rendering speed, however, existing Gaussians-based segmentation methods(eg: Gaussian Grouping) fail to provide compact segmentation masks especially in zero-shot segmentation, which is mainly caused by the lack of robustness and compactness for straightforwardly assigning learnable parameters to each Gaussian when encountering inconsistent 2D machine-generated labels. Our method aims to achieve compact and reliable zero-shot scene segmentation swiftly by mapping fused spatial and semantically meaningful features for each Gaussian
point with a shallow decoding network. Specifically, our method firstly optimizes Gaussian points’ position, convariance and color attributes under the supervision of RGB images. After Gaussian Locating, we distill multi-scale DINO features extracted from images through unprojection to each Gaussian, which is then incorporated with spatial features from the fast point features processing network, i.e. RandLA-Net. Then the shallow decoding MLP is applied to the multi-scale fused features to obtain compact segmentation. Experimental results show that our model can perform high-quality zero-shot scene segmentation, as our model outperforms other segmentation methods on both semantic and panoptic segmentation task, meanwhile consumes approximately only 10% segmenting time compared to NeRF-based segmentation.
</details

 [📄 Paper](https://arxiv.org/pdf/2401.05925.pdf) | [🌐 Project Page](https://david-dou.github.io/CoSSegGaussians/) | [💻 Code (not yet)](https://DavidDou.github.io/CoSSegGaussians)

### 2. TIP-Editor: An Accurate 3D Editor Following Both Text-Prompts And Image-Prompts 
**Authors**: Jingyu Zhuang, Di Kang, Yan-Pei Cao, Guanbin Li, Liang Lin, Ying Shan 
<details span>
<summary><b>Abstract</b></summary>
Text-driven 3D scene editing has gained significant attention owing to its convenience and user-friendliness. However, existing methods still lack accurate control of the specified appearance and location of the editing result due to the inherent limitations of the text description. To this end, we propose a 3D scene editing framework, TIPEditor, that accepts both text and image prompts and a 3D bounding box to specify the editing region. With the image prompt, users can conveniently specify the detailed appearance/style of the target content in complement to the text description, enabling accurate control of the appearance. Specifically, TIP-Editor employs a stepwise 2D personalization strategy to better learn the representation of the existing scene and the reference image, in which a localization loss is proposed to encourage correct object placement as specified by the bounding box. Additionally, TIPEditor utilizes explicit and flexible 3D Gaussian splatting as the 3D representation to facilitate local editing while keeping the background unchanged. Extensive experiments have demonstrated that TIP-Editor conducts accurate editing following the text and image prompts in the specified bounding box region, consistently outperforming the baselines in editing quality, and the alignment to the prompts, qualitatively and quantitatively. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.14828.pdf) | [🌐 Project Page](https://zjy526223908.github.io/TIP-Editor/)

### 3. Segment Anything in 3D Gaussians 
**Authors**: Xu Hu, Yuxi Wang, Lue Fan, Junsong Fan, Junran Peng, Zhen Lei, Qing Li, Zhaoxiang Zhang 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian Splatting has emerged as an alternative 3D representation of Neural Radiance Fields (NeRFs), benefiting from its high-quality rendering results and real-time rendering speed. Considering the 3D Gaussian representation remains unparsed, it is necessary first to execute object segmentation within this domain. Subsequently, scene editing and collision detection can be performed, proving vital to a multitude of applications, such as virtual reality (VR), augmented reality (AR), game/movie production, etc. In this paper, we propose a novel approach to achieve object segmentation in 3D Gaussian via an interactive procedure without any training process and learned parameters. We refer to the proposed method as SA-GS, for Segment Anything in 3D Gaussians. Given a set of clicked points in a single input view, SA-GS can generalize SAM to achieve 3D consistent segmentation via the proposed multi-view mask generation and view-wise label assignment methods. We also propose a cross-view label-voting approach to assign labels from different views. In addition, in order to address the boundary roughness issue of segmented objects resulting from the non-negligible spatial sizes of 3D Gaussian located at the boundary, SA-GS incorporates the simple but effective Gaussian Decomposition scheme. Extensive experiments demonstrate that SA-GS achieves high-quality 3D segmentation results, which can also be easily applied for scene editing and collision detection tasks.
</details>

  [📄 Paper](https://browse.arxiv.org/pdf/2401.17857.pdf) 

## 2023:
### 1. GaussianEditor: Swift and Controllable 3D Editing with Gaussian Splatting 
**Authors**: Yiwen Chen, Zilong Chen, Chi Zhang, Feng Wang, Xiaofeng Yang, Yikai Wang, Zhongang Cai, Lei Yang, Huaping Liu, Guosheng Lin
<details span>
<summary><b>Abstract</b></summary>
3D editing plays a crucial role in many areas such as gaming and virtual reality. Traditional 3D editing methods, which rely on representations like meshes and point clouds, often fall short in realistically depicting complex scenes.
On the other hand, methods based on implicit 3D representations, like Neural Radiance Field (NeRF), render complex scenes effectively but suffer from slow processing speeds and limited control over specific scene areas. In response to these challenges, our paper presents GaussianEditor, an innovative and efficient 3D editing algorithm based on Gaussian Splatting (GS), a novel 3D representation technique.
GaussianEditor enhances precision and control in editing through our proposed Gaussian Semantic Tracing, which traces the editing target throughout the training process. Additionally, we propose hierarchical Gaussian splatting (HGS) to achieve stabilized and fine results under stochastic generative guidance from 2D diffusion models. We also develop editing strategies for efficient object removal and integration, a challenging task for existing methods. Our comprehensive experiments demonstrate GaussianEditor's superior control, efficacy, and rapid performance, marking a significant advancement in 3D editing.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.14521.pdf) | [🌐 Project Page](https://buaacyw.github.io/gaussian-editor/) | [💻 Code](https://github.com/buaacyw/GaussianEditor) | [🎥 Short Presentation](https://youtu.be/TdZIICSFqsU?si=-U4tyOvaAPqIROYn)

### 2. GaussianEditor: Editing 3D Gaussians Delicately with Text Instructions 
**Authors**: Jiemin Fang, Junjie Wang, Xiaopeng Zhang, Lingxi Xie, Qi Tian 
<details span>
<summary><b>Abstract</b></summary>
Recently, impressive results have been achieved in 3D scene editing with text instructions based on a 2D diffusion model. However, current diffusion models primarily generate images by predicting noise in the latent space, and the editing is usually applied to the whole image, which makes it challenging to perform delicate, especially localized, editing for 3D scenes. Inspired by recent 3D Gaussian splatting, we propose a systematic framework, named GaussianEditor, to edit 3D scenes delicately via 3D Gaussians with text instructions. Benefiting from the explicit property of 3D Gaussians, we design a series of techniques to achieve delicate editing. Specifically, we first extract the region of interest (RoI) corresponding to the text instruction, aligning it to 3D Gaussians. The Gaussian RoI is further used to control the editing process. Our framework can achieve more delicate and precise editing of 3D scenes than previous methods while enjoying much faster training speed, i.e. within 20 minutes on a single V100 GPU, more than twice as fast as Instruct-NeRF2NeRF (45 minutes -- 2 hours)
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.16037.pdf) | [🌐 Project Page](https://gaussianeditor.github.io/) | [💻 Code (not yet)]() | [🎥 Short Presentation](https://youtu.be/KWtALsigR3k?si=h6-A44brd5rm3_CM)

### 3. Point'n Move: Interactive Scene Object Manipulation on Gaussian Splatting Radiance Fields 
**Authors**: Jiajun Huang, Hongchuan Yu 
<details span>
<summary><b>Abstract</b></summary>
We propose Point'n Move, a method that achieves interactive scene object manipulation with exposed region inpainting. Interactivity here further comes from intuitive object selection and real-time editing. To achieve this, we adopt Gaussian Splatting Radiance Field as the scene representation and fully leverage its explicit nature and speed advantage. Its explicit representation formulation allows us to devise a 2D prompt points to 3D mask dual-stage self-prompting segmentation algorithm, perform mask refinement and merging, minimize change as well as provide good initialization for scene inpainting and perform editing in real-time without per-editing training, all leads to superior quality and performance. We test our method by performing editing on both forward-facing and 360 scenes. We also compare our method against existing scene object removal methods, showing superior quality despite being more capable and having a speed advantage. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.16737.pdf)

### 4. Gaussian Grouping: Segment and Edit Anything in 3D Scenes 
**Authors**: Mingqiao Ye, Martin Danelljan, Fisher Yu, Lei Ke 
<details span>
<summary><b>Abstract</b></summary>
The recent Gaussian Splatting achieves high-quality and real-time novel-view synthesis of the 3D scenes. However, it is solely concentrated on the appearance and geometry modeling, while lacking in fine-grained object-level scene understanding. To address this issue, we propose Gaussian Grouping, which extends Gaussian Splatting to jointly reconstruct and segment anything in open-world 3D scenes. We augment each Gaussian with a compact Identity Encoding, allowing the Gaussians to be grouped according to their object instance or stuff membership in the 3D scene. Instead of resorting to expensive 3D labels, we supervise the Identity Encodings during the differentiable rendering by leveraging the 2D mask predictions by SAM, along with introduced 3D spatial consistency regularization. Comparing to the implicit NeRF representation, we show that the discrete and grouped 3D Gaussians can reconstruct, segment and edit anything in 3D with high visual quality, fine granularity and efficiency. Based on Gaussian Grouping, we further propose a local Gaussian Editing scheme, which shows efficacy in versatile scene editing applications, including 3D object removal, inpainting, colorization and scene recomposition. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.00732.pdf) | [💻 Code](https://github.com/lkeab/gaussian-grouping) 

### 5. Segment Any 3D Gaussians
**Authors**: Jiazhong Cen, Jiemin Fang, Chen Yang, Lingxi Xie, Xiaopeng Zhang, Wei Shen, Qi Tian

<details span>
<summary><b>Abstract</b></summary>
Interactive 3D segmentation in radiance fields is an appealing task since its importance in 3D scene understanding and manipulation. However, existing methods face challenges in either achieving fine-grained, multi-granularity segmentation or contending with substantial computational overhead, inhibiting real-time interaction. In this paper, we introduce Segment Any 3D GAussians (SAGA), a novel 3D interactive segmentation approach that seamlessly blends a 2D segmentation foundation model with 3D Gaussian Splatting (3DGS), a recent breakthrough of radiance fields. SAGA efficiently embeds multi-granularity 2D segmentation results generated by the segmentation foundation model into 3D Gaussian point features through well-designed contrastive training. Evaluation on existing benchmarks demonstrates that SAGA can achieve competitive performance with state-of-the-art methods. Moreover, SAGA achieves multi-granularity segmentation and accommodates various prompts, including points, scribbles, and 2D masks. Notably, SAGA can finish the 3D segmentation within milliseconds, achieving nearly 1000× acceleration1 compared to previous SOTA.
</details>

  [📄 Paper](https://jumpat.github.io/SAGA/SAGA_paper.pdf) | [🌐 Project Page](https://jumpat.github.io/SAGA/) | [💻 Code](https://github.com/Jumpat/SegAnyGAussians)

### 6. Feature 3DGS: Supercharging 3D Gaussian Splatting to Enable Distilled Feature Fields
**Authors**: Shijie Zhou, Haoran Chang, Sicheng Jiang, Zhiwen Fan, Zehao Zhu, Dejia Xu, Pradyumna Chari, Suya You, Zhangyang Wang, Achuta Kadambi 

<details span>
<summary><b>Abstract</b></summary>
3D scene representations have gained immense popularity in recent years. Methods that use Neural Radiance fields are versatile for traditional tasks such as novel view synthesis. In recent times, some work has emerged that aims to extend the functionality of NeRF beyond view synthesis, for semantically aware tasks such as editing and segmentation using 3D feature field distillation from 2D foundation models. However, these methods have two major limitations: (a) they are limited by the rendering speed of NeRF pipelines, and (b) implicitly represented feature fields suffer from continuity artifacts reducing feature quality. Recently, 3D Gaussian Splatting has shown state-of-the-art performance on real-time radiance field rendering. In this work, we go one step further: in addition to radiance field rendering, we enable 3D Gaussian splatting on arbitrary-dimension semantic features via 2D foundation model distillation. This translation is not straightforward: naively incorporating feature fields in the 3DGS framework leads to warp-level divergence. We propose architectural and training changes to efficiently avert this problem. Our proposed method is general, and our experiments showcase novel view semantic segmentation, language-guided editing and segment anything through learning feature fields from state-of-the-art 2D foundation models such as SAM and CLIP-LSeg. Across experiments, our distillation method is able to provide comparable or better results, while being significantly faster to both train and render. Additionally, to the best of our knowledge, we are the first method to enable point and bounding-box prompting for radiance field manipulation, by leveraging the SAM model. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.03203.pdf) | [🌐 Project Page](https://feature-3dgs.github.io/) | [💻 Code (not yet)]() | [🎥 Short Presentation](https://www.youtube.com/watch?v=YWZiF-WvMN4&t=4s)

### 7. 2D-Guided 3D Gaussian Segmentation 
**Authors**: Kun Lan, Haoran Li, Haolin Shi, Wenjun Wu, Yong Liao, Lin Wang, Pengyuan Zhou 

<details span>
<summary><b>Abstract</b></summary>
Recently, 3D Gaussian, as an explicit 3D representation method, has demonstrated strong competitiveness over NeRF (Neural Radiance Fields) in terms of expressing complex scenes and training duration. These advantages signal a wide range of applications for 3D Gaussians in 3D understanding and editing. Meanwhile, the segmentation of 3D Gaussians is still in its infancy. The existing segmentation methods are not only cumbersome but also incapable of segmenting multiple objects simultaneously in a short amount of time. In response, this paper introduces a 3D Gaussian segmentation method implemented with 2D segmentation as supervision. This approach uses input 2D segmentation maps to guide the learning of the added 3D Gaussian semantic information, while nearest neighbor clustering and statistical filtering refine the segmentation results. Experiments show that our concise method can achieve comparable performances on mIOU and mAcc for multi-object segmentation as previous single-object segmentation methods. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.16047.pdf) 

<br>

## Language Embedding:
## 2023:
### 1. Language Embedded 3D Gaussians for Open-Vocabulary Scene Understanding 
**Authors**: Jin-Chuan Shi, Miao Wang, Hao-Bin Duan, Shao-Hua Guan 
<details span>
<summary><b>Abstract</b></summary>
Open-vocabulary querying in 3D space is challenging but essential for scene understanding tasks such as object localization and segmentation. Language-embedded scene representations have made progress by incorporating language features into 3D spaces. However, their efficacy heavily depends on neural networks that are resource-intensive in training and rendering. Although recent 3D Gaussians offer efficient and high-quality novel view synthesis, directly embedding language features in them leads to prohibitive memory usage and decreased performance. In this work, we introduce Language Embedded 3D Gaussians, a novel scene representation for open-vocabulary query tasks. Instead of embedding high-dimensional raw semantic features on 3D Gaussians, we propose a dedicated quantization scheme that drastically alleviates the memory requirement, and a novel embedding procedure that achieves smoother yet high accuracy query, countering the multi-view feature inconsistencies and the high-frequency inductive bias in point-based representations. Our comprehensive experiments show that our representation achieves the best visual quality and language querying accuracy across current language-embedded representations, while maintaining real-time rendering frame rates on a single desktop GPU. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.18482.pdf) | [🌐 Project Page](https://buaavrcg.github.io/LEGaussians/) | [💻 Code (not yet)]()

### 2. LangSplat: 3D Language Gaussian Splatting 
**Authors**: Minghan Qin, Wanhua Li, Jiawei Zhou, Haoqian Wang, Hanspeter Pfister 
<details span>
<summary><b>Abstract</b></summary>
Human lives in a 3D world and commonly uses natural language to interact with a 3D scene. Modeling a 3D language field to support open-ended language queries in 3D has gained increasing attention recently. This paper introduces LangSplat, which constructs a 3D language field that enables precise and efficient open-vocabulary querying within 3D spaces. Unlike existing methods that ground CLIP language embeddings in a NeRF model, LangSplat advances the field by utilizing a collection of 3D Gaussians, each encoding language features distilled from CLIP, to represent the language field. By employing a tile-based splatting technique for rendering language features, we circumvent the costly rendering process inherent in NeRF. Instead of directly learning CLIP embeddings, LangSplat first trains a scene-wise language autoencoder and then learns language features on the scene-specific latent space, thereby alleviating substantial memory demands imposed by explicit modeling. Existing methods struggle with imprecise and vague 3D language fields, which fail to discern clear boundaries between objects. We delve into this issue and propose to learn hierarchical semantics using SAM, thereby eliminating the need for extensively querying the language field across various scales and the regularization of DINO features. Extensive experiments on open-vocabulary 3D object localization and semantic segmentation demonstrate that LangSplat significantly outperforms the previous state-of-the-art method LERF by a large margin. Notably, LangSplat is extremely efficient, achieving a {\speed} × speedup compared to LERF at the resolution of 1440 × 1080.
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.16084.pdf) | [🌐 Project Page](https://langsplat.github.io/) | [💻 Code](https://github.com/minghanqin/LangSplat) | [🎥 Short Presentation](https://www.youtube.com/watch?v=XMlyjsei-Es)

### 3. FMGS: Foundation Model Embedded 3D Gaussian Splatting for Holistic 3D Scene Understanding 
**Authors**: Xingxing Zuo, Pouya Samangouei, Yunwen Zhou, Yan Di, Mingyang Li 
<details span>
<summary><b>Abstract</b></summary>
Precisely perceiving the geometric and semantic properties of real-world 3D objects is crucial for the continued evolution of augmented reality and robotic applications. To this end, we present \algfull{} (\algname{}), which incorporates vision-language embeddings of foundation models into 3D Gaussian Splatting (GS). The key contribution of this work is an efficient method to reconstruct and represent 3D vision-language models. This is achieved by distilling feature maps generated from image-based foundation models into those rendered from our 3D model. To ensure high-quality rendering and fast training, we introduce a novel scene representation by integrating strengths from both GS and multi-resolution hash encodings (MHE). Our effective training procedure also introduces a pixel alignment loss that makes the rendered feature distance of same semantic entities close, following the pixel-level semantic boundaries. Our results demonstrate remarkable multi-view semantic consistency, facilitating diverse downstream tasks, beating state-of-the-art methods by 10.2 percent on open-vocabulary language-based object detection, despite that we are 851× faster for inference. This research explores the intersection of vision, language, and 3D scene representation, paving the way for enhanced scene understanding in uncontrolled real-world environments.
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.01970.pdf) 

<br>

## Mesh Extraction and Physics: 
## 2024:
### 1. Gaussian Splashing: Dynamic Fluid Synthesis with Gaussian Splatting 
**Authors**: Yutao Feng, Xiang Feng, Yintong Shang, Ying Jiang, Chang Yu, Zeshun Zong, Tianjia Shao, Hongzhi Wu, Kun Zhou, Chenfanfu Jiang, Yin Yang 

<details span>
<summary><b>Abstract</b></summary>
We demonstrate the feasibility of integrating physics-based animations of solids and fluids with 3D Gaussian Splatting (3DGS) to create novel effects in virtual scenes reconstructed using 3DGS. Leveraging the coherence of the Gaussian splatting and position-based dynamics (PBD) in the underlying representation, we manage rendering, view synthesis, and the dynamics of solids and fluids in a cohesive manner. Similar to Gaussian shader, we enhance each Gaussian kernel with an added normal, aligning the kernel's orientation with the surface normal to refine the PBD simulation. This approach effectively eliminates spiky noises that arise from rotational deformation in solids. It also allows us to integrate physically based rendering to augment the dynamic surface reflections on fluids. Consequently, our framework is capable of realistically reproducing surface highlights on dynamic fluids and facilitating interactions between scene objects and fluids from new views. 
</details>

  [📄 Paper](https://browse.arxiv.org/pdf/2401.15318.pdf) | [🌐 Project Page](https://amysteriouscat.github.io/GaussianSplashing/) | [💻 Code (not released yet)]() | [🎥 Short Presentation](https://www.youtube.com/watch?v=KgaR1ni-Egg&t)

### 2. GaMeS: Mesh-Based Adapting and Modification of Gaussian Splatting 
**Authors**: Joanna Waczyńska, Piotr Borycki, Sławomir Tadeja, Jacek Tabor, Przemysław Spurek 

<details span>
<summary><b>Abstract</b></summary>
In recent years, a range of neural network-based methods for image rendering have been introduced. For instance, widely-researched neural radiance fields (NeRF) rely on a neural network to represent 3D scenes, allowing for realistic view synthesis from a small number of 2D images. However, most NeRF models are constrained by long training and inference times. In comparison, Gaussian Splatting (GS) is a novel, state-of-theart technique for rendering points in a 3D scene by approximating their contribution to image pixels through Gaussian distributions, warranting fast training and swift, real-time rendering. A drawback of GS is the absence of a well-defined approach for its conditioning due to the necessity to condition several hundred thousand Gaussian components. To solve this, we introduce Gaussian Mesh Splatting (GaMeS) model, a hybrid of mesh and a Gaussian distribution, that pin all Gaussians splats on the object surface (mesh). The unique contribution of our methods is defining Gaussian splats solely based on their location on the mesh, allowing for automatic adjustments in position, scale, and rotation during animation. As a result, we obtain high-quality renders in the real-time generation of high-quality views. Furthermore, we demonstrate that in the absence of a predefined mesh, it is possible to fine-tune the initial mesh during the learning process. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.01459.pdf) | [💻 Code](https://github.com/waczjoan/gaussian-mesh-splatting) 

### 3. Mesh-based Gaussian Splatting for Real-time Large-scale Deformation 
**Authors**: Lin Gao, Jie Yang, Bo-Tao Zhang, Jia-Mu Sun, Yu-Jie Yuan, Hongbo Fu, Yu-Kun Lai 

<details span>
<summary><b>Abstract</b></summary>
Neural implicit representations, including Neural Distance Fields and Neural Radiance Fields, have demonstrated significant capabilities for reconstructing surfaces with complicated geometry and topology, and generating novel views of a scene. Nevertheless, it is challenging for users to directly deform or manipulate these implicit representations with large deformations in the real-time fashion. Gaussian Splatting(GS) has recently become a promising method with explicit geometry for representing static scenes and facilitating high-quality and real-time synthesis of novel views. However,it cannot be easily deformed due to the use of discrete Gaussians and lack of explicit topology. To address this, we develop a novel GS-based method that enables interactive deformation. Our key idea is to design an innovative mesh-based GS representation, which is integrated into Gaussian learning and manipulation. 3D Gaussians are defined over an explicit mesh, and they are bound with each other: the rendering of 3D Gaussians guides the mesh face split for adaptive refinement, and the mesh face split directs the splitting of 3D Gaussians. Moreover, the explicit mesh constraints help regularize the Gaussian distribution, suppressing poor-quality Gaussians(e.g. misaligned Gaussians,long-narrow shaped Gaussians), thus enhancing visual quality and avoiding artifacts during deformation. Based on this representation, we further introduce a large-scale Gaussian deformation technique to enable deformable GS, which alters the parameters of 3D Gaussians according to the manipulation of the associated mesh. Our method benefits from existing mesh deformation datasets for more realistic data-driven Gaussian deformation. Extensive experiments show that our approach achieves high-quality reconstruction and effective deformation, while maintaining the promising rendering results at a high frame rate(65 FPS on average). 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.04796.pdf) 

## 2023:
### 1. PhysGaussian: Physics-Integrated 3D Gaussians for Generative Dynamics
**Authors**: Tianyi Xie, Zeshun Zong, Yuxin Qiu, Xuan Li, Yutao Feng, Yin Yang, Chenfanfu Jiang

<details span>
<summary><b>Abstract</b></summary>
We introduce PhysGaussian, a new method that seamlessly integrates physically grounded Newtonian dynamics within 3D Gaussians to achieve high-quality novel motion synthesis. Employing a custom Material Point Method (MPM), our approach enriches 3D Gaussian kernels with physically meaningful kinematic deformation and mechanical stress attributes, all evolved in line with continuum mechanics principles. A defining characteristic of our method is the seamless integration between physical simulation and visual rendering: both components utilize the same 3D Gaussian kernels as their discrete representations. This negates the necessity for triangle/tetrahedron meshing, marching cubes, "cage meshes," or any other geometry embedding, highlighting the principle of "what you see is what you simulate (WS2)." Our method demonstrates exceptional versatility across a wide variety of materials--including elastic entities, metals, non-Newtonian fluids, and granular materials--showcasing its strong capabilities in creating diverse visual content with novel viewpoints and movements. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.12198.pdf) | [🌐 Project Page](https://xpandora.github.io/PhysGaussian/) | [💻 Code](https://github.com/XPandora/PhysGaussian) | [🎥 Short Presentation](https://drive.google.com/file/d/1eh7vxRxer7gfvPhs8jDE56oRjayBc9oe/view)

### 2. SuGaR: Surface-Aligned Gaussian Splatting for Efficient 3D Mesh Reconstruction and High-Quality Mesh Rendering
**Authors**: Antoine Guédon, Vincent Lepetit

<details span>
<summary><b>Abstract</b></summary>
We propose a method to allow precise and extremely fast mesh extraction from 3D Gaussian Splatting. Gaussian Splatting has recently become very popular as it yields realistic rendering while being significantly faster to train than NeRFs. It is however challenging to extract a mesh from the millions of tiny 3D gaussians as these gaussians tend to be unorganized after optimization and no method has been proposed so far. Our first key contribution is a regularization term that encourages the gaussians to align well with the surface of the scene. We then introduce a method that exploits this alignment to sample points on the real surface of the scene and extract a mesh from the Gaussians using Poisson reconstruction, which is fast, scalable, and preserves details, in contrast to the Marching Cubes algorithm usually applied to extract meshes from Neural SDFs. Finally, we introduce an optional refinement strategy that binds gaussians to the surface of the mesh, and jointly optimizes these Gaussians and the mesh through Gaussian splatting rendering. This enables easy editing, sculpting, rigging, animating, compositing and relighting of the Gaussians using traditional softwares by manipulating the mesh instead of the gaussians themselves. Retrieving such an editable mesh for realistic rendering is done within minutes with our method, compared to hours with the state-of-the-art methods on neural SDFs, while providing a better rendering quality. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.12775.pdf) | [🌐 Project Page](https://imagine.enpc.fr/~guedona/sugar/) | [💻 Code](https://github.com/Anttwo/SuGaR) | [🎥 Short Presentation](https://www.youtube.com/watch?v=MAkFyWfiBQo.&t)

### 3. NeuSG: Neural Implicit Surface Reconstruction with 3D Gaussian Splatting Guidance
**Authors**: Hanlin Chen, Chen Li, Gim Hee Lee

<details span>
<summary><b>Abstract</b></summary>
Existing neural implicit surface reconstruction methods have achieved impressive performance in multi-view 3D reconstruction by leveraging explicit geometry priors such as depth maps or point clouds as regularization. However, the reconstruction results still lack fine details because of the over-smoothed depth map or sparse point cloud. In this work, we propose a neural implicit surface reconstruction pipeline with guidance from 3D Gaussian Splatting to recover highly detailed surfaces. The advantage of 3D Gaussian Splatting is that it can generate dense point clouds with detailed structure. Nonetheless, a naive adoption of 3D Gaussian Splatting can fail since the generated points are the centers of 3D Gaussians that do not necessarily lie on the surface. We thus introduce a scale regularizer to pull the centers close to the surface by enforcing the 3D Gaussians to be extremely thin. Moreover, we propose to refine the point cloud from 3D Gaussians Splatting with the normal priors from the surface predicted by neural implicit models instead of using a fixed set of points as guidance. Consequently, the quality of surface reconstruction improves from the guidance of the more accurate 3D Gaussian splatting. By jointly optimizing the 3D Gaussian Splatting and the neural implicit model, our approach benefits from both representations and generates complete surfaces with intricate details. Experiments on Tanks and Temples verify the effectiveness of our proposed method.
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.00846.pdf)

<br>

## Misc:
## 2024:
### 1. Characterizing Satellite Geometry via Accelerated 3D Gaussian Splatting 
**Authors**: Van Minh Nguyen, Emma Sandidge, Trupti Mahendrakar, Ryan T. White 
<details span>
<summary><b>Abstract</b></summary>
The accelerating deployment of spacecraft in orbit have generated interest in on-orbit servicing (OOS), inspection of spacecraft, and active debris removal (ADR). Such missions require precise rendezvous and proximity operations in the vicinity of non-cooperative, possible unknown, resident space objects. Safety concerns with manned missions and lag times with ground-based control necessitate complete autonomy. This requires robust characterization of the target's geometry. In this article, we present an approach for mapping geometries of satellites on orbit based on 3D Gaussian Splatting that can run on computing resources available on current spaceflight hardware. We demonstrate model training and 3D rendering performance on a hardware-in-the-loop satellite mock-up under several realistic lighting and motion conditions. Our model is shown to be capable of training on-board and rendering higher quality novel views of an unknown satellite nearly 2 orders of magnitude faster than previous NeRF-based algorithms. Such on-board capabilities are critical to enable downstream machine intelligence tasks necessary for autonomous guidance, navigation, and control tasks. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.02588.pdf)

### 2. TRIPS: Trilinear Point Splatting for Real-Time Radiance Field Rendering
**Authors**: Linus Franke, Darius Rückert, Laura Fink, Marc Stamminger
<details span>
<summary><b>Abstract</b></summary>
Point-based radiance field rendering has demonstrated impressive results for novel view synthesis, offering a compelling blend of rendering quality and computational efficiency. However, also latest approaches in this domain are not without their shortcomings. 3D Gaussian Splatting [Kerbl and Kopanas et al. 2023] struggles when tasked with rendering highly detailed scenes, due to blurring and cloudy artifacts. On the other hand, ADOP [Rückert et al. 2022] can accommodate crisper images, but the neural reconstruction network decreases performance, it grapples with temporal instability and it is unable to effectively address large gaps in the point cloud. In this paper, we present TRIPS (Trilinear Point Splatting), an approach that combines ideas from both Gaussian Splatting and ADOP. The fundamental concept behind our novel technique involves rasterizing points into a screen-space image pyramid, with the selection of the pyramid layer determined by the projected point size. This approach allows rendering arbitrarily large points using a single trilinear write. A lightweight neural network is then used to reconstruct a hole-free image including detail beyond splat resolution. Importantly, our render pipeline is entirely differentiable, allowing for automatic optimization of both point sizes and positions. Our evaluation demonstrate that TRIPS surpasses existing state-of-the-art methods in terms of rendering quality while maintaining a real-time frame rate of 60 frames per second on readily available hardware. This performance extends to challenging scenarios, such as scenes featuring intricate geometry, expansive landscapes, and auto-exposed footage.
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.06003.pdf) | [🌐 Project Page](https://lfranke.github.io/trips/) | [💻 Code](https://github.com/lfranke/trips) 

### 3. EndoGS: Deformable Endoscopic Tissues Reconstruction with Gaussian Splatting
**Authors**: Lingting Zhu, Zhao Wang, Jiahao Cui, Zhenchao Jin, Guying Lin, Lequan Yu
<details span>
<summary><b>Abstract</b></summary>
Surgical 3D reconstruction is a critical area of research in robotic surgery, with recent works adopting variants of dynamic radiance fields to achieve success in 3D reconstruction of deformable tissues from single-viewpoint videos. However, these methods often suffer from time-consuming optimization or inferior quality, limiting their adoption in downstream tasks. Inspired by 3D Gaussian Splatting, a recent trending 3D representation, we present EndoGS, applying Gaussian Splatting for deformable endoscopic tissue reconstruction. Specifically, our approach incorporates deformation fields to handle dynamic scenes, depth-guided supervision with spatial-temporal weight masks to optimize 3D targets with tool occlusion from a single viewpoint, and surface-aligned regularization terms to capture the much better geometry. As a result, EndoGS reconstructs and renders high-quality deformable endoscopic tissues from a single-viewpoint video, estimated depth maps, and labeled tool masks. Experiments on DaVinci robotic surgery videos demonstrate that EndoGS achieves superior rendering quality.
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.11535.pdf) | [💻 Code](https://github.com/HKU-MedAI/EndoGS)

### 4. EndoGaussian: Gaussian Splatting for Deformable Surgical Scene Reconstruction 
**Authors**: Yifan Liu, Chenxin Li, Chen Yang, Yixuan Yuan 
<details span>
<summary><b>Abstract</b></summary>
Reconstructing deformable tissues from endoscopic stereo videos is essential in many downstream surgical applications. However, existing methods suffer from slow inference speed, which greatly limits their practical use. In this paper, we introduce EndoGaussian, a real-time surgical scene reconstruction framework that builds on 3D Gaussian Splatting. Our framework represents dynamic surgical scenes as canonical Gaussians and a time-dependent deformation field, which predicts Gaussian deformations at novel timestamps. Due to the efficient Gaussian representation and parallel rendering pipeline, our framework significantly accelerates the rendering speed compared to previous methods. In addition, we design the deformation field as the combination of a lightweight encoding voxel and an extremely tiny MLP, allowing for efficient Gaussian tracking with a minor rendering burden. Furthermore, we design a holistic Gaussian initialization method to fully leverage the surface distribution prior, achieved by searching informative points from across the input image sequence. Experiments on public endoscope datasets demonstrate that our method can achieve real-time rendering speed (195 FPS real-time, 100× gain) while maintaining the state-of-the-art reconstruction quality (35.925 PSNR) and the fastest training speed (within 2 min/scene), showing significant promise for intraoperative surgery applications. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.12561.pdf) | [🌐 Project Page](https://yifliu3.github.io/EndoGaussian/) | [💻 Code](https://github.com/yifliu3/EndoGaussian)

### 5. GauU-Scene: A Scene Reconstruction Benchmark on Large Scale 3D Reconstruction Dataset Using Gaussian Splatting 
**Authors**: Butian Xiong, Zhuo Li, Zhen Li 
<details span>
<summary><b>Abstract</b></summary>
We introduce a novel large-scale scene reconstruction benchmark using the newly developed 3D representation approach, Gaussian Splatting, on our expansive U-Scene dataset. U-Scene encompasses over one and a half square kilometres, featuring a comprehensive RGB dataset coupled with LiDAR ground truth. For data acquisition, we employed the Matrix 300 drone equipped with the high-accuracy Zenmuse L1 LiDAR, enabling precise rooftop data collection. This dataset, offers a unique blend of urban and academic environments for advanced spatial analysis convers more than 1.5 km2. Our evaluation of U-Scene with Gaussian Splatting includes a detailed analysis across various novel viewpoints. We also juxtapose these results with those derived from our accurate point cloud dataset, highlighting significant differences that underscore the importance of combine multi-modal information 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.14032.pdf)

### 6. LIV-GaussMap: LiDAR-Inertial-Visual Fusion for Real-time 3D Radiance Field Map Rendering 
**Authors**: Sheng Hong, Junjie He, Xinhu Zheng, Hesheng Wang, Hao Fang, Kangcheng Liu, Chunran Zheng, Shaojie Shen 
<details span>
<summary><b>Abstract</b></summary>
We introduce an integrated precise LiDAR, Inertial, and Visual (LIV) multi-modal sensor fused mapping system that builds on the differentiable surface splatting to improve the mapping fidelity, quality, and structural accuracy. Notably, this is also a novel form of tightly coupled map for LiDAR-visual-inertial sensor fusion.
This system leverages the complementary characteristics of LiDAR and visual data to capture the geometric structures of large-scale 3D scenes and restore their visual surface information with high fidelity. The initial poses for surface Gaussian scenes are obtained using a LiDAR-inertial system with size-adaptive voxels. Then, we optimized and refined the Gaussians by visual-derived photometric gradients to optimize the quality and density of LiDAR measurements.
Our method is compatible with various types of LiDAR, including solid-state and mechanical LiDAR, supporting both repetitive and non-repetitive scanning modes. bolstering structure construction through LiDAR and facilitating real-time generation of photorealistic renderings across diverse LIV datasets. It showcases notable resilience and versatility in generating real-time photorealistic scenes potentially for digital twins and virtual reality while also holding potential applicability in real-time SLAM and robotics domains. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.14857.pdf) | [💻 Code (not yet)](https://github.com/sheng00125/LIV-GaussMap)

### 7. VR-GS: A Physical Dynamics-Aware Interactive Gaussian Splatting System in Virtual Reality 
**Authors**: Ying Jiang, Chang Yu, Tianyi Xie, Xuan Li, Yutao Feng, Huamin Wang, Minchen Li, Henry Lau, Feng Gao, Yin Yang, Chenfanfu Jiang 
<details span>
<summary><b>Abstract</b></summary>
As consumer Virtual Reality (VR) and Mixed Reality (MR) technologies gain momentum, there's a growing focus on the development of engagements with 3D virtual content. Unfortunately, traditional techniques for content creation, editing, and interaction within these virtual spaces are fraught with difficulties. They tend to be not only engineering-intensive but also require extensive expertise, which adds to the frustration and inefficiency in virtual object manipulation. Our proposed VR-GS system represents a leap forward in human-centered 3D content interaction, offering a seamless and intuitive user experience. By developing a physical dynamics-aware interactive Gaussian Splatting in a Virtual Reality setting, and constructing a highly efficient two-level embedding strategy alongside deformable body simulations, VR-GS ensures real-time execution with highly realistic dynamic responses. The components of our Virtual Reality system are designed for high efficiency and effectiveness, starting from detailed scene reconstruction and object segmentation, advancing through multi-view image in-painting, and extending to interactive physics-based editing. The system also incorporates real-time deformation embedding and dynamic shadow casting, ensuring a comprehensive and engaging virtual experience.
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.16663.pdf) | [🌐 Project Page](https://yingjiang96.github.io/VR-GS/) 

### 8. Splat-Nav: Safe Real-Time Robot Navigation in Gaussian Splatting Maps 
**Authors**: Timothy Chen, Ola Shorinwa, Weijia Zeng, Joseph Bruno, Philip Dames, Mac Schwager 
<details span>
<summary><b>Abstract</b></summary>
We present Splat-Nav, a navigation pipeline that consists of a real-time safe planning module and a robust state estimation module designed to operate in the Gaussian Splatting (GSplat) environment representation, a popular emerging 3D scene representation from computer vision. We formulate rigorous collision constraints that can be computed quickly to build a guaranteed-safe polytope corridor through the map. We then optimize a B-spline trajectory through this corridor. We also develop a real-time, robust state estimation module by interpreting the GSplat representation as a point cloud. The module enables the robot to localize its global pose with zero prior knowledge from RGB-D images using point cloud alignment, and then track its own pose as it moves through the scene from RGB images using image-to-point cloud localization. We also incorporate semantics into the GSplat in order to obtain better images for localization. All of these modules operate mainly on CPU, freeing up GPU resources for tasks like real-time scene reconstruction. We demonstrate the safety and robustness of our pipeline in both simulation and hardware, where we show re-planning at 5 Hz and pose estimation at 20 Hz, an order of magnitude faster than Neural Radiance Field (NeRF)-based navigation methods, thereby enabling real-time navigation. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2403.02751.pdf)

## 2023:
### 1. FisherRF: Active View Selection and Uncertainty Quantification for Radiance Fields using Fisher Information  
**Authors**: Wen Jiang, Boshu Lei, Kostas Daniilidis 
<details span>
<summary><b>Abstract</b></summary>
This study addresses the challenging problem of active view selection and uncertainty quantification within the domain of Radiance Fields. Neural Radiance Fields (NeRF) have greatly advanced image rendering and reconstruction, but the limited availability of 2D images poses uncertainties stemming from occlusions, depth ambiguities, and imaging errors. Efficiently selecting informative views becomes crucial, and quantifying NeRF model uncertainty presents intricate challenges. Existing approaches either depend on model architecture or are based on assumptions regarding density distributions that are not generally applicable. By leveraging Fisher Information, we efficiently quantify observed information within Radiance Fields without ground truth data. This can be used for the next best view selection and pixel-wise uncertainty quantification. Our method overcomes existing limitations on model architecture and effectiveness, achieving state-of-the-art results in both view selection and uncertainty quantification, demonstrating its potential to advance the field of Radiance Fields. Our method with the 3D Gaussian Splatting backend could perform view selections at 70 fps. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17874.pdf) | [🌐 Project Page](https://jiangwenpl.github.io/FisherRF/) | [💻 Code](https://github.com/JiangWenPL/FisherRF) 

### 2. Periodic Vibration Gaussian: Dynamic Urban Scene Reconstruction and Real-time Rendering 
**Authors**: Yurui Chen, Chun Gu, Junzhe Jiang, Xiatian Zhu, Li Zhang 
<details span>
<summary><b>Abstract</b></summary>
Modeling dynamic, large-scale urban scenes is challenging due to their highly intricate geometric structures and unconstrained dynamics in both space and time. Prior methods often employ high-level architectural priors, separating static and dynamic elements, resulting in suboptimal capture of their synergistic interactions. To address this challenge, we present a unified representation model, called Periodic Vibration Gaussian (PVG). PVG builds upon the efficient 3D Gaussian splatting technique, originally designed for static scene representation, by introducing periodic vibration-based temporal dynamics. This innovation enables PVG to elegantly and uniformly represent the characteristics of various objects and elements in dynamic urban scenes. To enhance temporally coherent representation learning with sparse training data, we introduce a novel flow-based temporal smoothing mechanism and a position-aware adaptive control strategy. Extensive experiments on Waymo Open Dataset and KITTI benchmarks demonstrate that PVG surpasses state-of-the-art alternatives in both reconstruction and novel view synthesis for both dynamic and static scenes. Notably, PVG achieves this without relying on manually labeled object bounding boxes or expensive optical flow estimation. Moreover, PVG exhibits 50/6000-fold acceleration in training/rendering over the best alternative. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.18561.pdf) | [🌐 Project Page](https://fudan-zvg.github.io/PVG/) | [💻 Code (not yet)](https://github.com/fudan-zvg/PVG) 

### 3. MANUS: Markerless Hand-Object Grasp Capture using Articulated 3D Gaussians
**Authors**: Chandradeep Pokhariya, Ishaan N Shah, Angela Xing, Zekun Li, Kefan Chen, Avinash Sharma, Srinath Sridhar

<details span>
<summary><b>Abstract</b></summary>
Understanding how we grasp objects with our hands has important applications in areas like robotics and mixed reality. However, this challenging problem requires accurate modeling of the contact between hands and objects. To capture grasps, existing methods use skeletons, meshes, or parametric models that can cause misalignments resulting in inaccurate contacts. We present MANUS, a method for Markerless Hand-Object Grasp Capture using Articulated 3D Gaussians. We build a novel articulated 3D Gaussians representation that extends 3D Gaussian splatting for high-fidelity representation of articulating hands. Since our representation uses Gaussian primitives, it enables us to efficiently and accurately estimate contacts between the hand and the object. For the most accurate results, our method requires tens of camera views that current datasets do not provide. We therefore build MANUS-Grasps, a new dataset that contains hand-object grasps viewed from 53 cameras across 30+ scenes, 3 subjects, and comprising over 7M frames. In addition to extensive qualitative results, we also show that our method outperforms others on a quantitative contact evaluation method that uses paint transfer from the object to the hand. 
</details>


  [📄 Paper](https://arxiv.org/pdf/2312.02137.pdf)

### 4. Triplane Meets Gaussian Splatting: Fast and Generalizable Single-View 3D Reconstruction with Transformers 
Alexander Vilesov, Pradyumna Chari, Achuta Kadambi
<details span>
<summary><b>Abstract</b></summary>
Recent advancements in 3D reconstruction from single images have been driven by the evolution of generative models. Prominent among these are methods based on Score Distillation Sampling (SDS) and the adaptation of diffusion models in the 3D domain. Despite their progress, these techniques often face limitations due to slow optimization or rendering processes, leading to extensive training and optimization times. In this paper, we introduce a novel approach for single-view reconstruction that efficiently generates a 3D model from a single image via feed-forward inference. Our method utilizes two transformer-based networks, namely a point decoder and a triplane decoder, to reconstruct 3D objects using a hybrid Triplane-Gaussian intermediate representation. This hybrid representation strikes a balance, achieving a faster rendering speed compared to implicit representations while simultaneously delivering superior rendering quality than explicit representations. The point decoder is designed for generating point clouds from single images, offering an explicit representation which is then utilized by the triplane decoder to query Gaussian features for each point. This design choice addresses the challenges associated with directly regressing explicit 3D Gaussian attributes characterized by their non-structural nature. Subsequently, the 3D Gaussians are decoded by an MLP to enable rapid rendering through splatting. Both decoders are built upon a scalable, transformer-based architecture and have been efficiently trained on large-scale 3D datasets. The evaluations conducted on both synthetic datasets and real-world images demonstrate that our method not only achieves higher quality but also ensures a faster runtime in comparison to previous state-of-the-art techniques.
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.09147.pdf) | [🌐 Project Page](https://zouzx.github.io/TriplaneGaussian/) | [💻 Code](https://github.com/VAST-AI-Research/TriplaneGaussian)

### 5. Mathematical Supplement for the gsplat Library 
**Authors**: Vickie Ye, Angjoo Kanazawa 
This report provides the mathematical details of the gsplat library, a modular toolbox for efficient differentiable Gaussian splatting, as proposed by Kerbl et al. It provides a self-contained reference for the computations involved in the forward and backward passes of differentiable Gaussian splatting. To facilitate practical usage and development, we provide a user friendly Python API that exposes each component of the forward and backward passes in rasterization of [gsplat](https://github.com/nerfstudio-project/gsplat).

<details span>
<summary><b>Abstract</b></summary>
Understanding how we grasp objects with our hands has important applications in areas like robotics and mixed reality. However, this challenging problem requires accurate modeling of the contact between hands and objects. To capture grasps, existing methods use skeletons, meshes, or parametric models that can cause misalignments resulting in inaccurate contacts. We present MANUS, a method for Markerless Hand-Object Grasp Capture using Articulated 3D Gaussians. We build a novel articulated 3D Gaussians representation that extends 3D Gaussian splatting for high-fidelity representation of articulating hands. Since our representation uses Gaussian primitives, it enables us to efficiently and accurately estimate contacts between the hand and the object. For the most accurate results, our method requires tens of camera views that current datasets do not provide. We therefore build MANUS-Grasps, a new dataset that contains hand-object grasps viewed from 53 cameras across 30+ scenes, 3 subjects, and comprising over 7M frames. In addition to extensive qualitative results, we also show that our method outperforms others on a quantitative contact evaluation method that uses paint transfer from the object to the hand. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.02137.pdf)

### 6. PEGASUS: Physically Enhanced Gaussian Splatting Simulation System for 6DOF Object Pose Dataset Generation 
**Authors**: Lukas Meyer, Floris Erich, Yusuke Yoshiyasu, Marc Stamminger, Noriaki Ando, Yukiyasu Domae 
<details span>
<summary><b>Abstract</b></summary>
Modeling dynamic, large-scale urban scenes is challenging due to their highly intricate geometric structures and unconstrained dynamics in both space and time. Prior methods often employ high-level architectural priors, separating static and dynamic elements, resulting in suboptimal capture of their synergistic interactions. To address this challenge, we present a unified representation model, called Periodic Vibration Gaussian (PVG). PVG builds upon the efficient 3D Gaussian splatting technique, originally designed for static scene representation, by introducing periodic vibration-based temporal dynamics. This innovation enables PVG to elegantly and uniformly represent the characteristics of various objects and elements in dynamic urban scenes. To enhance temporally coherent representation learning with sparse training data, we introduce a novel flow-based temporal smoothing mechanism and a position-aware adaptive control strategy. Extensive experiments on Waymo Open Dataset and KITTI benchmarks demonstrate that PVG surpasses state-of-the-art alternatives in both reconstruction and novel view synthesis for both dynamic and static scenes. Notably, PVG achieves this without relying on manually labeled object bounding boxes or expensive optical flow estimation. Moreover, PVG exhibits 50/6000-fold acceleration in training/rendering over the best alternative. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.02281.pdf) | [🌐 Project Page](https://meyerls.github.io/pegasus_web/) | [💻 Code (not yet)](https://github.com/meyerls/PEGASUS) 

<br>

## Regularization and Optimization:
## 2024:
### 1. DISTWAR: Fast Differentiable Rendering on Raster-based Rendering Pipelines
**Authors**: Sankeerth Durvasula, Adrian Zhao, Fan Chen, Ruofan Liang, Pawan Kumar Sanjaya, Nandita Vijaykumar
<details span>
<summary><b>Abstract</b></summary>
Differentiable rendering is a technique used in an important emerging class of visual computing applications that involves representing a 3D scene as a model that is trained from 2D images using gradient descent. Recent works (e.g. 3D Gaussian Splatting) use a rasterization pipeline to enable rendering high quality photo-realistic imagery at high speeds from these learned 3D models. These methods have been demonstrated to be very promising, providing state-of-art quality for many important tasks. However, training a model to represent a scene is still a time-consuming task even when using powerful GPUs. In this work, we observe that the gradient computation phase during training is a significant bottleneck on GPUs due to the large number of atomic operations that need to be processed. These atomic operations overwhelm atomic units in the L2 partitions causing stalls. To address this challenge, we leverage the observations that during the gradient computation: (1) for most warps, all threads atomically update the same memory locations; and (2) warps generate varying amounts of atomic traffic (since some threads may be inactive). We propose DISTWAR, a software-approach to accelerate atomic operations based on two key ideas: First, we enable warp-level reduction of threads at the SM sub-cores using registers to leverage the locality in intra-warp atomic updates. Second, we distribute the atomic computation between the warp-level reduction at the SM and the L2 atomic units to increase the throughput of atomic computation. Warps with many threads performing atomic updates to the same memory locations are scheduled at the SM, and the rest using L2 atomic units. We implement DISTWAR using existing warp-level primitives. We evaluate DISTWAR on widely used raster-based differentiable rendering workloads. We demonstrate significant speedups of 2.44x on average (up to 5.7x).
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.05345.pdf)
  
## 2023:
### 1. Depth-Regularized Optimization for 3D Gaussian Splatting in Few-Shot Images 
**Authors**: Jaeyoung Chung, Jeongtaek Oh, Kyoung Mu Lee 
<details span>
<summary><b>Abstract</b></summary>
In this paper, we present a method to optimize Gaussian splatting with a limited number of images while avoiding overfitting. Representing a 3D scene by combining numerous Gaussian splats has yielded outstanding visual quality. However, it tends to overfit the training views when only a small number of images are available. To address this issue, we introduce a dense depth map as a geometry guide to mitigate overfitting. We obtained the depth map using a pre-trained monocular depth estimation model and aligning the scale and offset using sparse COLMAP feature points. The adjusted depth aids in the color-based optimization of 3D Gaussian splatting, mitigating floating artifacts, and ensuring adherence to geometric constraints. We verify the proposed method on the NeRF-LLFF dataset with varying numbers of few images. Our approach demonstrates robust geometry compared to the original method that relies solely on images. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.13398.pdf) | [🌐 Project Page](https://robot0321.github.io/DepthRegGS/index.html) | [💻 Code ](https://github.com/robot0321/DepthRegularizedGS) 

### 2. EAGLES: Efficient Accelerated 3D Gaussians with Lightweight EncodingS 
**Authors**: Sharath Girish, Kamal Gupta, Abhinav Shrivastava 
<details span>
<summary><b>Abstract</b></summary>
Recently, 3D Gaussian splatting (3D-GS) has gained popularity in novel-view scene synthesis. It addresses the challenges of lengthy training times and slow rendering speeds associated with Neural Radiance Fields (NeRFs). Through rapid, differentiable rasterization of 3D Gaussians, 3D-GS achieves real-time rendering and accelerated training. They, however, demand substantial memory resources for both training and storage, as they require millions of Gaussians in their point cloud representation for each scene. We present a technique utilizing quantized embeddings to significantly reduce memory storage requirements and a coarse-to-fine training strategy for a faster and more stable optimization of the Gaussian point clouds. Our approach results in scene representations with fewer Gaussians and quantized representations, leading to faster training times and rendering speeds for real-time rendering of high resolution scenes. We reduce memory by more than an order of magnitude all while maintaining the reconstruction quality. We validate the effectiveness of our approach on a variety of datasets and scenes preserving the visual quality while consuming 10-20x less memory and faster training/inference speed. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.04564.pdf) | [🌐 Project Page](https://efficientgaussian.github.io/) | [💻 Code ](https://github.com/Sharath-girish/efficientgaussian) 

<br>

### 3. COLMAP-Free 3D Gaussian Splatting 
**Authors**: Yang Fu, Sifei Liu, Amey Kulkarni, Jan Kautz, Alexei A. Efros, Xiaolong Wang 
<details span>
<summary><b>Abstract</b></summary>
While neural rendering has led to impressive advances in scene reconstruction and novel view synthesis, it relies heavily on accurately pre-computed camera poses. To relax this constraint, multiple efforts have been made to train Neural Radiance Fields (NeRFs) without pre-processed camera poses. However, the implicit representations of NeRFs provide extra challenges to optimize the 3D structure and camera poses at the same time. On the other hand, the recently proposed 3D Gaussian Splatting provides new opportunities given its explicit point cloud representations. This paper leverages both the explicit geometric representation and the continuity of the input video stream to perform novel view synthesis without any SfM preprocessing. We process the input frames in a sequential manner and progressively grow the 3D Gaussians set by taking one input frame at a time, without the need to pre-compute the camera poses. Our method significantly improves over previous approaches in view synthesis and camera pose estimation under large motion changes.
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.07504.pdf) | [🌐 Project Page](https://oasisyang.github.io/colmap-free-3dgs/) | [💻 Code (not yet)]() | [🎥 Short Presentation](https://youtu.be/IJtnx4keJvg)

### 4. iComMa: Inverting 3D Gaussians Splatting for Camera Pose Estimation via Comparing and Matching 
**Authors**: Yuan Sun, Xuan Wang, Yunfan Zhang, Jie Zhang, Caigui Jiang, Yu Guo, Fei Wang 
<details span>
<summary><b>Abstract</b></summary>
We present a method named iComMa to address the 6D pose estimation problem in computer vision. The conventional pose estimation methods typically rely on the target's CAD model or necessitate specific network training tailored to particular object classes. Some existing methods address mesh-free 6D pose estimation by employing the inversion of a Neural Radiance Field (NeRF), aiming to overcome the aforementioned constraints. However, it still suffers from adverse initializations. By contrast, we model the pose estimation as the problem of inverting the 3D Gaussian Splatting (3DGS) with both the comparing and matching loss. In detail, a render-and-compare strategy is adopted for the precise estimation of poses. Additionally, a matching module is designed to enhance the model's robustness against adverse initializations by minimizing the distances between 2D keypoints. This framework systematically incorporates the distinctive characteristics and inherent rationale of render-and-compare and matching-based approaches. This comprehensive consideration equips the framework to effectively address a broader range of intricate and challenging scenarios, including instances with substantial angular deviations, all while maintaining a high level of prediction accuracy. Experimental results demonstrate the superior precision and robustness of our proposed jointly optimized framework when evaluated on synthetic and complex real-world data in challenging scenarios. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.09031.pdf) 

<br>

## Rendering:
## 2024:
### 1. Gaussian Shadow Casting for Neural Characters 
**Authors**: Luis Bolanos, Shih-Yang Su, Helge Rhodin
<details span>
<summary><b>Abstract</b></summary>
Neural character models can now reconstruct detailed geometry and texture from video, but they lack explicit shadows and shading, leading to artifacts when generating novel views and poses or during relighting. It is particularly difficult to include shadows as they are a global effect and the required casting of secondary rays is costly. We propose a new shadow model using a Gaussian density proxy that replaces sampling with a simple analytic formula. It supports dynamic motion and is tailored for shadow computation, thereby avoiding the affine projection approximation and sorting required by the closely related Gaussian splatting. Combined with a deferred neural rendering model, our Gaussian shadows enable Lambertian shading and shadow casting with minimal overhead. We demonstrate improved reconstructions, with better separation of albedo, shading, and shadows in challenging outdoor scenes with direct sun light and hard shadows. Our method is able to optimize the light direction without any input from the user. As a result, novel poses have fewer shadow artifacts and relighting in novel scenes is more realistic compared to the state-of-the-art methods, providing new ways to pose neural characters in novel environments, increasing their applicability.
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.06116.pdf)

### 2. Optimal Projection for 3D Gaussian Splatting  
**Authors**: Letian Huang, Jiayang Bai, Jie Guo, Yanwen Guo 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian Splatting has garnered extensive attention and application in real-time neural rendering. Concurrently, concerns have been raised about the limitations of this technology in aspects such as point cloud storage, performance , and robustness in sparse viewpoints , leading to various improvements. However, there has been a notable lack of attention to the projection errors introduced by the local affine approximation inherent in the splatting itself, and the consequential impact of these errors on the quality of photo-realistic rendering. This paper addresses the projection error function of 3D Gaussian Splatting, commencing with the residual error from the first-order Taylor expansion of the projection function ϕ. The analysis establishes a correlation between the error and the Gaussian mean position. Subsequently, leveraging function optimization theory, this paper analyzes the function's minima to provide an optimal projection strategy for Gaussian Splatting referred to Optimal Gaussian Splatting. Experimental validation further confirms that this projection methodology reduces artifacts, resulting in a more convincingly realistic rendering. 
</details>

  [📄 Paper](https://browse.arxiv.org/pdf/2402.00752.pdf)

### 3. 360-GS: Layout-guided Panoramic Gaussian Splatting For Indoor Roaming 
**Authors**: Letian Huang, Jiayang Bai, Jie Guo, Yanwen Guo 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian Splatting (3D-GS) has recently attracted great attention with real-time and photo-realistic renderings. This technique typically takes perspective images as input and optimizes a set of 3D elliptical Gaussians by splatting them onto the image planes, resulting in 2D Gaussians. However, applying 3D-GS to panoramic inputs presents challenges in effectively modeling the projection onto the spherical surface of 360∘ images using 2D Gaussians. In practical applications, input panoramas are often sparse, leading to unreliable initialization of 3D Gaussians and subsequent degradation of 3D-GS quality. In addition, due to the under-constrained geometry of texture-less planes (e.g., walls and floors), 3D-GS struggles to model these flat regions with elliptical Gaussians, resulting in significant floaters in novel views. To address these issues, we propose 360-GS, a novel 360∘ Gaussian splatting for a limited set of panoramic inputs. Instead of splatting 3D Gaussians directly onto the spherical surface, 360-GS projects them onto the tangent plane of the unit sphere and then maps them to the spherical projections. This adaptation enables the representation of the projection using Gaussians. We guide the optimization of 360-GS by exploiting layout priors within panoramas, which are simple to obtain and contain strong structural information about the indoor scene. Our experimental results demonstrate that 360-GS allows panoramic rendering and outperforms state-of-the-art methods with fewer artifacts in novel view synthesis, thus providing immersive roaming in indoor scenarios. 
</details>

  [📄 Paper](https://browse.arxiv.org/pdf/2402.00763.pdf)

### 4. StopThePop: Sorted Gaussian Splatting for View-Consistent Real-time Rendering 
**Authors**: Lukas Radl, Michael Steiner, Mathias Parger, Alexander Weinrauch, Bernhard Kerbl, Markus Steinberger 
<details span>
<summary><b>Abstract</b></summary>
Gaussian Splatting has emerged as a prominent model for constructing 3D representations from images across diverse domains. However, the efficiency of the 3D Gaussian Splatting rendering pipeline relies on several simplifications. Notably, reducing Gaussian to 2D splats with a single view-space depth introduces popping and blending artifacts during view rotation. Addressing this issue requires accurate per-pixel depth computation, yet a full per-pixel sort proves excessively costly compared to a global sort operation. In this paper, we present a novel hierarchical rasterization approach that systematically resorts and culls splats with minimal processing overhead. Our software rasterizer effectively eliminates popping artifacts and view inconsistencies, as demonstrated through both quantitative and qualitative measurements. Simultaneously, our method mitigates the potential for cheating view-dependent effects with popping, ensuring a more authentic representation. Despite the elimination of cheating, our approach achieves comparable quantitative results for test images, while increasing the consistency for novel view synthesis in motion. Due to its design, our hierarchical approach is only 4% slower on average than the original Gaussian Splatting. Notably, enforcing consistency enables a reduction in the number of Gaussians by approximately half with nearly identical quality and view-consistency. Consequently, rendering performance is nearly doubled, making our approach 1.6x faster than the original Gaussian Splatting, with a 50% reduction in memory requirements. 
</details>

  [📄 Paper](arxiv.org/pdf/2402.00525.pdf) | [🎥 Short Presentation](https://youtu.be/RJQlSORNkr0)

### 5. GES: Generalized Exponential Splatting for Efficient Radiance Field Rendering 
**Authors**: Abdullah Hamdi, Luke Melas-Kyriazi, Guocheng Qian, Jinjie Mai, Ruoshi Liu, Carl Vondrick, Bernard Ghanem, Andrea Vedaldi 
<details span>
<summary><b>Abstract</b></summary>
Advancements in 3D Gaussian Splatting have significantly accelerated 3D reconstruction and generation. However, it may require a large number of Gaussians, which creates a substantial memory footprint. This paper introduces GES (Generalized Exponential Splatting), a novel representation that employs Generalized Exponential Function (GEF) to model 3D scenes, requiring far fewer particles to represent a scene and thus significantly outperforming Gaussian Splatting methods in efficiency with a plug-and-play replacement ability for Gaussian-based utilities. GES is validated theoretically and empirically in both principled 1D setup and realistic 3D scenes.
It is shown to represent signals with sharp edges more accurately, which are typically challenging for Gaussians due to their inherent low-pass characteristics. Our empirical analysis demonstrates that GEF outperforms Gaussians in fitting natural-occurring signals (e.g. squares, triangles, and parabolic signals), thereby reducing the need for extensive splitting operations that increase the memory footprint of Gaussian Splatting. With the aid of a frequency-modulated loss, GES achieves competitive performance in novel-view synthesis benchmarks while requiring less than half the memory storage of Gaussian Splatting and increasing the rendering speed by up to 39%.
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.10128.pdf) | [🌐 Project Page](https://abdullahamdi.com/ges/) | [💻 Code](https://github.com/ajhamdi/ges-splatting) | [🎥 Presentation](https://youtu.be/edSvNy3roV8?si=VGncH7op1OfqkEtx) 

### 6. Identifying Unnecessary 3D Gaussians using Clustering for Fast Rendering of 3D Gaussian Splatting
**Authors**: Joongho Jo, Hyeongwon Kim, Jongsun Park 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian splatting (3D-GS) is a new rendering approach that outperforms the neural radiance field (NeRF) in terms of both speed and image quality. 3D-GS represents 3D scenes by utilizing millions of 3D Gaussians and projects these Gaussians onto the 2D image plane for rendering. However, during the rendering process, a substantial number of unnecessary 3D Gaussians exist for the current view direction, resulting in significant computation costs associated with their identification. In this paper, we propose a computational reduction technique that quickly identifies unnecessary 3D Gaussians in real-time for rendering the current view without compromising image quality. This is accomplished through the offline clustering of 3D Gaussians that are close in distance, followed by the projection of these clusters onto a 2D image plane during runtime. Additionally, we analyze the bottleneck associated with the proposed technique when executed on GPUs and propose an efficient hardware architecture that seamlessly supports the proposed scheme. For the Mip-NeRF360 dataset, the proposed technique excludes 63% of 3D Gaussians on average before the 2D image projection, which reduces the overall rendering computation by almost 38.3% without sacrificing peak-signal-to-noise-ratio (PSNR). The proposed accelerator also achieves a speedup of 10.7x compared to a GPU. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.13827.pdf) 

### 7. GaussianPro: 3D Gaussian Splatting with Progressive Propagation 
**Authors**: Kai Cheng, Xiaoxiao Long, Kaizhi Yang, Yao Yao, Wei Yin, Yuexin Ma, Wenping Wang, Xuejin Chen 
<details span>
<summary><b>Abstract</b></summary>
The advent of 3D Gaussian Splatting (3DGS) has recently brought about a revolution in the field of neural rendering, facilitating high-quality renderings at real-time speed. However, 3DGS heavily depends on the initialized point cloud produced by Structure-from-Motion (SfM) techniques. When tackling with large-scale scenes that unavoidably contain texture-less surfaces, the SfM techniques always fail to produce enough points in these surfaces and cannot provide good initialization for 3DGS. As a result, 3DGS suffers from difficult optimization and low-quality renderings. In this paper, inspired by classical multi-view stereo (MVS) techniques, we propose GaussianPro, a novel method that applies a progressive propagation strategy to guide the densification of the 3D Gaussians. Compared to the simple split and clone strategies used in 3DGS, our method leverages the priors of the existing reconstructed geometries of the scene and patch matching techniques to produce new Gaussians with accurate positions and orientations. Experiments on both large-scale and small-scale scenes validate the effectiveness of our method, where our method significantly surpasses 3DGS on the Waymo dataset, exhibiting an improvement of 1.15dB in terms of PSNR. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.14650.pdf) | [🌐 Project Page](https://kcheng1021.github.io/gaussianpro.github.io/) | [💻 Code](https://github.com/kcheng1021/GaussianPro) 

### 8. Spec-Gaussian: Anisotropic View-Dependent Appearance for 3D Gaussian Splatting 
**Authors**: Ziyi Yang, Xinyu Gao, Yangtian Sun, Yihua Huang, Xiaoyang Lyu, Wen Zhou, Shaohui Jiao, Xiaojuan Qi, Xiaogang Jin 
<details span>
<summary><b>Abstract</b></summary>
The recent advancements in 3D Gaussian splatting (3D-GS) have not only facilitated real-time rendering through modern GPU rasterization pipelines but have also attained state-of-the-art rendering quality. Nevertheless, despite its exceptional rendering quality and performance on standard datasets, 3D-GS frequently encounters difficulties in accurately modeling specular and anisotropic components. This issue stems from the limited ability of spherical harmonics (SH) to represent high-frequency information. To overcome this challenge, we introduce Spec-Gaussian, an approach that utilizes an anisotropic spherical Gaussian (ASG) appearance field instead of SH for modeling the view-dependent appearance of each 3D Gaussian. Additionally, we have developed a coarse-to-fine training strategy to improve learning efficiency and eliminate floaters caused by overfitting in real-world scenes. Our experimental results demonstrate that our method surpasses existing approaches in terms of rendering quality. Thanks to ASG, we have significantly improved the ability of 3D-GS to model scenes with specular and anisotropic components without increasing the number of 3D Gaussians. This improvement extends the applicability of 3D GS to handle intricate scenarios with specular and anisotropic surfaces. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.15870.pdf) 

### 9. VastGaussian: Vast 3D Gaussians for Large Scene Reconstruction 
**Authors**: Jiaqi Lin, Zhihao Li, Xiao Tang, Jianzhuang Liu, Shiyong Liu, Jiayue Liu, Yangdi Lu, Xiaofei Wu, Songcen Xu, Youliang Yan, Wenming Yang 
<details span>
<summary><b>Abstract</b></summary>
Existing NeRF-based methods for large scene reconstruction often have limitations in visual quality and rendering speed. While the recent 3D Gaussian Splatting works well on small-scale and object-centric scenes, scaling it up to large scenes poses challenges due to limited video memory, long optimization time, and noticeable appearance variations. To address these challenges, we present VastGaussian, the first method for high-quality reconstruction and real-time rendering on large scenes based on 3D Gaussian Splatting. We propose a progressive partitioning strategy to divide a large scene into multiple cells, where the training cameras and point cloud are properly distributed with an airspace-aware visibility criterion. These cells are merged into a complete scene after parallel optimization. We also introduce decoupled appearance modeling into the optimization process to reduce appearance variations in the rendered images. Our approach outperforms existing NeRF-based methods and achieves state-of-the-art results on multiple large scene datasets, enabling fast optimization and high-fidelity real-time rendering. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.17427.pdf) | [🌐 Project Page](https://vastgaussian.github.io/) | [💻 Code (not yet)]() 

### 10. 3D Gaussian Model for Animation and Texturing
**Authors**: Xiangzhi Eric Wang, Zackary P. T. Sin 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian Splatting has made a marked impact on neural rendering by achieving impressive fidelity and performance. Despite this achievement, however, it is not readily applicable to developing interactive applications. Real-time applications like XR apps and games require functions such as animation, UV-mapping, and model editing simultaneously manipulated through the usage of a 3D model. We propose a modeling that is analogous to typical 3D models, which we call 3D Gaussian Model (3DGM); it provides a manipulatable proxy for novel animation and texture transfer. By binding the 3D Gaussians in texture space and re-projecting them back to world space through implicit shell mapping, we show how our 3D modeling can serve as a valid rendering methodology for interactive applications. It is further noted that recently, 3D mesh reconstruction works have been able to produce high-quality mesh for rendering. Our work, on the other hand, only requires an approximated geometry for rendering an object in high fidelity. Applicationwise, we will show that our proxy-based 3DGM is capable of driving novel animation without animated training data and texture transferring via UV mapping of the 3D Gaussians. We believe the result indicates the potential of our work for enabling interactive applications for 3D Gaussian Splatting. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.19441.pdf) 

## 2023:
### 1. Mip-Splatting Alias-free 3D Gaussian Splatting 
**Authors**: Zehao Yu, Anpei Chen, Binbin Huang, Torsten Sattler, Andreas Geiger
<details span>
<summary><b>Abstract</b></summary>
Recently, 3D Gaussian Splatting (3DGS) has demonstrated impressive novel view synthesis results, reaching high fidelity and efficiency. However, strong artifacts can be observed when changing the sampling rate, e.g., by changing focal length or camera distance. We find that the source for this phenomenon can be attributed to the lack of 3D frequency constraints and the usage of a 2D dilation filter. To address this problem, we introduce a 3D smoothing filter which constrains the size of the 3D Gaussian primitives based on the maximal sampling frequency induced by the input views, eliminating high frequency artifacts when zooming in. Moreover, replacing 2D dilation with a 2D Mip filter, which simulates a 2D box filter, effectively mitigates aliasing and dilation issues. Our comprehensive evaluation, including scenarios such as training on single-scale images and testing on multiple scales, validates the effectiveness of our approach. 
</details>

  [📄 Paper](https://drive.google.com/file/d/1Q7KgGbynzcIEyFJV1I17HgrYz6xrOwRJ/view) | [🌐 Project Page](https://niujinshuchong.github.io/mip-splatting/) | [💻 Code](https://github.com/autonomousvision/mip-splatting) 

### 2. Relightable 3D Gaussian: Real-time Point Cloud Relighting with BRDF Decomposition and Ray Tracing 
**Authors**: Jian Gao, Chun Gu, Youtian Lin, Hao Zhu, Xun Cao, Li Zhang, Yao Yao 
<details span>
<summary><b>Abstract</b></summary>
We present a novel differentiable point-based rendering framework for material and lighting decomposition from multi-view images, enabling editing, ray-tracing, and real-time relighting of the 3D point cloud. Specifically, a 3D scene is represented as a set of relightable 3D Gaussian points, where each point is additionally associated with a normal direction, BRDF parameters, and incident lights from different directions. To achieve robust lighting estimation, we further divide incident lights of each point into global and local components, as well as view-dependent visibilities. The 3D scene is optimized through the 3D Gaussian Splatting technique while BRDF and lighting are decomposed by physically-based differentiable rendering. Moreover, we introduce an innovative point-based ray-tracing approach based on the bounding volume hierarchy for efficient visibility baking, enabling real-time rendering and relighting of 3D Gaussian points with accurate shadow effects. Extensive experiments demonstrate improved BRDF estimation and novel view rendering results compared to state-of-the-art material estimation approaches. Our framework showcases the potential to revolutionize the mesh-based graphics pipeline with a relightable, traceable, and editable rendering pipeline solely based on point cloud.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.16043.pdf) | [🌐 Project Page](https://nju-3dv.github.io/projects/Relightable3DGaussian/) | [💻 Code](https://github.com/NJU-3DV/Relightable3DGaussian) 

### 3. GS-IR: 3D Gaussian Splatting for Inverse Rendering 
**Authors**: Zhihao Liang, Qi Zhang, Ying Feng, Ying Shan, Kui Jia 
<details span>
<summary><b>Abstract</b></summary>
We propose GS-IR, a novel inverse rendering approach based on 3D Gaussian Splatting (GS) that leverages forward mapping volume rendering to achieve photorealistic novel view synthesis and relighting results. Unlike previous works that use implicit neural representations and volume rendering (e.g. NeRF), which suffer from low expressive power and high computational complexity, we extend GS, a top-performance representation for novel view synthesis, to estimate scene geometry, surface material, and environment illumination from multi-view images captured under unknown lighting conditions. There are two main problems when introducing GS to inverse rendering: 1) GS does not support producing plausible normal natively; 2) forward mapping (e.g. rasterization and splatting) cannot trace the occlusion like backward mapping (e.g. ray tracing). To address these challenges, our GS-IR proposes an efficient optimization scheme that incorporates a depth-derivation-based regularization for normal estimation and a baking-based occlusion to model indirect lighting. The flexible and expressive GS representation allows us to achieve fast and compact geometry reconstruction, photorealistic novel view synthesis, and effective physically-based rendering. We demonstrate the superiority of our method over baseline methods through qualitative and quantitative evaluations on various challenging scenes. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.16473.pdf) | [🌐 Project Page](https://github.com/lzhnb/GS-IR) | [💻 Code (not yet)](https://github.com/lzhnb/GS-IR) 

### 4. Multi-Scale 3D Gaussian Splatting for Anti-Aliased Rendering  
**Authors**: Zhiwen Yan, Weng Fei Low, Yu Chen, Gim Hee Lee 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussians have recently emerged as a highly efficient representation for 3D reconstruction and rendering. Despite its high rendering quality and speed at high resolutions, they both deteriorate drastically when rendered at lower resolutions or from far away camera position. During low resolution or far away rendering, the pixel size of the image can fall below the Nyquist frequency compared to the screen size of each splatted 3D Gaussian and leads to aliasing effect. The rendering is also drastically slowed down by the sequential alpha blending of more splatted Gaussians per pixel. To address these issues, we propose a multi-scale 3D Gaussian splatting algorithm, which maintains Gaussians at different scales to represent the same scene. Higher-resolution images are rendered with more small Gaussians, and lower-resolution images are rendered with fewer larger Gaussians. With similar training time, our algorithm can achieve 13\%-66\% PSNR and 160\%-2400\% rendering speed improvement at 4×-128× scale rendering on Mip-NeRF360 dataset compared to the single scale 3D Gaussian splatting. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17089.pdf) 

### 5. GaussianShader: 3D Gaussian Splatting with Shading Functions for Reflective Surfaces 
**Authors**: Yingwenqi Jiang, Jiadong Tu, Yuan Liu, Xifeng Gao, Xiaoxiao Long, Wenping Wang, Yuexin Ma 
<details span>
<summary><b>Abstract</b></summary>
The advent of neural 3D Gaussians has recently brought about a revolution in the field of neural rendering, facilitating the generation of high-quality renderings at real-time speeds. However, the explicit and discrete representation encounters challenges when applied to scenes featuring reflective surfaces. In this paper, we present GaussianShader, a novel method that applies a simplified shading function on 3D Gaussians to enhance the neural rendering in scenes with reflective surfaces while preserving the training and rendering efficiency. The main challenge in applying the shading function lies in the accurate normal estimation on discrete 3D Gaussians. Specifically, we proposed a novel normal estimation framework based on the shortest axis directions of 3D Gaussians with a delicately designed loss to make the consistency between the normals and the geometries of Gaussian spheres. Experiments show that GaussianShader strikes a commendable balance between efficiency and visual quality. Our method surpasses Gaussian Splatting in PSNR on specular object datasets, exhibiting an improvement of 1.57dB. When compared to prior works handling reflective surfaces, such as Ref-NeRF, our optimization time is significantly accelerated (23h vs. 0.58h). Please click on our project website to see more results. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17977.pdf) | [🌐 Project Page](https://asparagus15.github.io/GaussianShader.github.io/) | [💻 Code](https://github.com/Asparagus15/GaussianShader) 

### 6. Scaffold-GS: Structured 3D Gaussians for View-Adaptive Rendering  
**Authors**:  Tao Lu, Mulin Yu, Linning Xu, Yuanbo Xiangli, Limin Wang, Dahua Lin, Bo Dai 
<details span>
<summary><b>Abstract</b></summary>
Neural rendering methods have significantly advanced photo-realistic 3D scene rendering in various academic and industrial applications. The recent 3D Gaussian Splatting method has achieved the state-of-the-art rendering quality and speed combining the benefits of both primitive-based representations and volumetric representations. However, it often leads to heavily redundant Gaussians that try to fit every training view, neglecting the underlying scene geometry. Consequently, the resulting model becomes less robust to significant view changes, texture-less area and lighting effects. We introduce Scaffold-GS, which uses anchor points to distribute local 3D Gaussians, and predicts their attributes on-the-fly based on viewing direction and distance within the view frustum. Anchor growing and pruning strategies are developed based on the importance of neural Gaussians to reliably improve the scene coverage. We show that our method effectively reduces redundant Gaussians while delivering high-quality rendering. We also demonstrates an enhanced capability to accommodate scenes with varying levels-of-detail and view-dependent observations, without sacrificing the rendering speed.
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.00109.pdf) | [🌐 Project Page](https://city-super.github.io/scaffold-gs/) | [💻 Code](https://github.com/city-super/Scaffold-GS) 

### 7. Deblurring 3D Gaussian Splatting 
**Authors**: Byeonghyeon Lee, Howoong Lee, Xiangyu Sun, Usman Ali, Eunbyung Park 
<details span>
<summary><b>Abstract</b></summary>
Recent studies in Radiance Fields have paved the robust way for novel view synthesis with their photorealistic rendering quality. Nevertheless, they usually employ neural networks and volumetric rendering, which are costly to train and impede their broad use in various real-time applications due to the lengthy rendering time. Lately 3D Gaussians splatting-based approach has been proposed to model the 3D scene, and it achieves remarkable visual quality while rendering the images in real-time. However, it suffers from severe degradation in the rendering quality if the training images are blurry. Blurriness commonly occurs due to the lens defocusing, object motion, and camera shake, and it inevitably intervenes in clean image acquisition. Several previous studies have attempted to render clean and sharp images from blurry input images using neural fields. The majority of those works, however, are designed only for volumetric rendering-based neural radiance fields and are not straightforwardly applicable to rasterization-based 3D Gaussian splatting methods. Thus, we propose a novel real-time deblurring framework, deblurring 3D Gaussian Splatting, using a small Multi-Layer Perceptron (MLP) that manipulates the covariance of each 3D Gaussian to model the scene blurriness. While deblurring 3D Gaussian Splatting can still enjoy real-time rendering, it can reconstruct fine and sharp details from blurry images. A variety of experiments have been conducted on the benchmark, and the results have revealed the effectiveness of our approach for deblurring.
</details>

  [📄 Paper)](https://arxiv.org/pdf/2401.00834.pdf) | [🌐 Project Page](https://benhenryl.github.io/Deblurring-3D-Gaussian-Splatting/) | [💻 Code (not yet)](https://github.com/benhenryL/Deblurring-3D-Gaussian-Splatting) 

### 8. GIR: 3D Gaussian Inverse Rendering for Relightable Scene Factorization
**Authors**: Yahao Shi, Yanmin Wu, Chenming Wu, Xing Liu, Chen Zhao, Haocheng Feng, Jingtuo Liu, Liangjun Zhang, Jian Zhang, Bin Zhou, Errui Ding, Jingdong Wang
<details span>
<summary><b>Abstract</b></summary>
This paper presents GIR, a 3D Gaussian Inverse Rendering method for relightable scene factorization. Compared to existing methods leveraging discrete meshes or neural implicit fields for inverse rendering, our method utilizes 3D Gaussians to estimate the material properties, illumination, and geometry of an object from multi-view images. Our study is motivated by the evidence showing that 3D Gaussian is a more promising backbone than neural fields in terms of performance, versatility, and efficiency. In this paper, we aim to answer the question: "How can 3D Gaussian be applied to improve the performance of inverse rendering?" To address the complexity of estimating normals based on discrete and often in-homogeneous distributed 3D Gaussian representations, we proposed an efficient self-regularization method that facilitates the modeling of surface normals without the need for additional supervision. To reconstruct indirect illumination, we propose an approach that simulates ray tracing. Extensive experiments demonstrate our proposed GIR's superior performance over existing methods across multiple tasks on a variety of widely used datasets in inverse rendering. This substantiates its efficacy and broad applicability, highlighting its potential as an influential tool in relighting and reconstruction.
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.05133) | [🌐 Project Page](https://3dgir.github.io/) | [💻 Code(not yet)]() 

### 9. Gaussian Splitting Algorithm with Color and Opacity Depended on Viewing Direction 
**Authors**: Dawid Malarz, Weronika Smolak, Jacek Tabor, Sławomir Tadeja, Przemysław Spurek 
<details span>
<summary><b>Abstract</b></summary>
Neural Radiance Fields (NeRFs) have demonstrated the remarkable potential of neural networks to capture the intricacies of 3D objects. By encoding the shape and color information within neural network weights, NeRFs excel at producing strikingly sharp novel views of 3D objects. Recently, numerous generalizations of NeRFs utilizing generative models have emerged, expanding its versatility. In contrast, Gaussian Splatting (GS) offers a similar renders quality with faster training and inference as it does not need neural networks to work. We encode information about the 3D objects in the set of Gaussian distributions that can be rendered in 3D similarly to classical meshes. Unfortunately, GS are difficult to condition since they usually require circa hundred thousand Gaussian components. To mitigate the caveats of both models, we propose a hybrid model that uses GS representation of the 3D object's shape and NeRF-based encoding of color and opacity. Our model uses Gaussian distributions with trainable positions (i.e. means of Gaussian), shape (i.e. covariance of Gaussian), color and opacity, and neural network, which takes parameters of Gaussian and viewing direction to produce changes in color and opacity. Consequently, our model better describes shadows, light reflections, and transparency of 3D objects. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.13729.pdf) | [🌐 Project Page]() | [💻 Code](https://github.com/gmum/ViewingDirectionGaussianSplatting) 
  
<br>

## Reviews:
## 2024:
### 1. Progress and Prospects in 3D Generative AI: A Technical Overview including 3D human 
**Authors**: Song Bai, Jie Li 
<details span>
<summary><b>Abstract</b></summary>
While AI-generated text and 2D images continue to expand its territory, 3D generation has gradually emerged as a trend that cannot be ignored. Since the year 2023 an abundant amount of research papers has emerged in the domain of 3D generation. This growth encompasses not just the creation of 3D objects, but also the rapid development of 3D character and motion generation. Several key factors contribute to this progress. The enhanced fidelity in stable diffusion, coupled with control methods that ensure multi-view consistency, and realistic human models like SMPL-X, contribute synergistically to the production of 3D models with remarkable consistency and near-realistic appearances. The advancements in neural network-based 3D storing and rendering models, such as Neural Radiance Fields (NeRF) and 3D Gaussian Splatting (3DGS), have accelerated the efficiency and realism of neural rendered models. Furthermore, the multimodality capabilities of large language models have enabled language inputs to transcend into human motion outputs. This paper aims to provide a comprehensive overview and summary of the relevant papers published mostly during the latter half year of 2023. It will begin by discussing the AI generated object models in 3D, followed by the generated 3D human models, and finally, the generated 3D human motions, culminating in a conclusive summary and a vision for the future. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.02620.pdf)

### 2. A Survey on 3D Gaussian Splatting 
**Authors**: Guikun Chen, Wenguan Wang
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian splatting (3D GS) has recently emerged as a transformative technique in the explicit radiance field and computer graphics landscape. This innovative approach, characterized by the utilization of millions of 3D Gaussians, represents a significant departure from the neural radiance field (NeRF) methodologies, which predominantly use implicit, coordinate-based models to map spatial coordinates to pixel values. 3D GS, with its explicit scene representations and differentiable rendering algorithms, not only promises real-time rendering capabilities but also introduces unprecedented levels of control and editability. This positions 3D GS as a potential game-changer for the next generation of 3D reconstruction and representation. In the present paper, we provide the first systematic overview of the recent developments and critical contributions in the domain of 3D GS. We begin with a detailed exploration of the underlying principles and the driving forces behind the advent of 3D GS, setting the stage for understanding its significance. A focal point of our discussion is the practical applicability of 3D GS. By facilitating real-time performance, 3D GS opens up a plethora of applications, ranging from virtual reality to interactive media and beyond. This is complemented by a comparative analysis of leading 3D GS models, evaluated across various benchmark tasks to highlight their performance and practical utility. The survey concludes by identifying current challenges and suggesting potential avenues for future research in this domain. Through this survey, we aim to provide a valuable resource for both newcomers and seasoned researchers, fostering further exploration and advancement in applicable and explicit radiance field representation. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.03890.pdf)

### 3. 3D Gaussian as a New Vision Era: A Survey 
**Authors**: Ben Fei, Jingyi Xu, Rui Zhang, Qingyuan Zhou, Weidong Yang, Ying He 
<details span>
<summary><b>Abstract</b></summary>
3D Gaussian Splatting (3D-GS) has emerged as a significant advancement in the field of Computer Graphics, offering explicit scene representation and novel view synthesis without the reliance on neural networks, such as Neural Radiance Fields (NeRF). This technique has found diverse applications in areas such as robotics, urban mapping, autonomous navigation, and virtual reality/augmented reality, just name a few. Given the growing popularity and expanding research in 3D Gaussian Splatting, this paper presents a comprehensive survey of relevant papers from the past year. We organize the survey into taxonomies based on characteristics and applications, providing an introduction to the theoretical underpinnings of 3D Gaussian Splatting. Our goal through this survey is to acquaint new researchers with 3D Gaussian Splatting, serve as a valuable reference for seminal works in the field, and inspire future research directions, as discussed in our concluding section. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.07181.pdf)

### 4. How NeRFs and 3D Gaussian Splatting are Reshaping SLAM: a Survey 
**Authors**: Fabio Tosi, Youmin Zhang, Ziren Gong, Erik Sandström, Stefano Mattoccia, Martin R. Oswald, Matteo Poggi 
<details span>
<summary><b>Abstract</b></summary>
Over the past two decades, research in the field of Simultaneous Localization and Mapping (SLAM) has undergone a significant evolution, highlighting its critical role in enabling autonomous exploration of unknown environments. This evolution ranges from hand-crafted methods, through the era of deep learning, to more recent developments focused on Neural Radiance Fields (NeRFs) and 3D Gaussian Splatting (3DGS) representations. Recognizing the growing body of research and the absence of a comprehensive survey on the topic, this paper aims to provide the first comprehensive overview of SLAM progress through the lens of the latest advancements in radiance fields. It sheds light on the background, evolutionary path, inherent strengths and limitations, and serves as a fundamental reference to highlight the dynamic progress and specific challenges. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.13255.pdf)

<br>

## SLAM:
## 2024:
### 1. SGS-SLAM: Semantic Gaussian Splatting For Neural Dense SLAM 
**Authors**: Mingrui Li, Shuhong Liu, Heng Zhou 
<details span>
<summary><b>Abstract</b></summary>
Semantic understanding plays a crucial role in Dense Simultaneous Localization and Mapping (SLAM), facilitating comprehensive scene interpretation. Recent advancements that integrate Gaussian Splatting into SLAM systems have demonstrated its effectiveness in generating high-quality renderings through the use of explicit 3D Gaussian representations. Building on this progress, we propose SGS-SLAM, the first semantic dense visual SLAM system grounded in 3D Gaussians, which provides precise 3D semantic segmentation alongside high-fidelity reconstructions. Specifically, we propose to employ multi-channel optimization during the mapping process, integrating appearance, geometric, and semantic constraints with key-frame optimization to enhance reconstruction quality. Extensive experiments demonstrate that SGS-SLAM delivers state-of-the-art performance in camera pose estimation, map reconstruction, and semantic segmentation, outperforming existing methods meanwhile preserving real-time rendering ability. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2402.03246.pdf) 
## 2023:
### 1. GS-SLAM: Dense Visual SLAM with 3D Gaussian Splatting
**Authors**: Chi Yan, Delin Qu, Dong Wang, Dan Xu, Zhigang Wang, Bin Zhao, Xuelong Li
<details span>
<summary><b>Abstract</b></summary>
In this paper, we introduce GS-SLAM that first utilizes 3D Gaussian representation in the Simultaneous Localization and Mapping (SLAM) system. It facilitates a better balance between efficiency and accuracy. Compared to recent SLAM methods employing neural implicit representations, our method utilizes a real-time differentiable splatting rendering pipeline that offers significant speedup to map optimization and RGB-D re-rendering. Specifically, we propose an adaptive expansion strategy that adds new or deletes noisy 3D Gaussian in order to efficiently reconstruct new observed scene geometry and improve the mapping of previously observed areas. This strategy is essential to extend 3D Gaussian representation to reconstruct the whole scene rather than synthesize a static object in existing methods. Moreover, in the pose tracking process, an effective coarse-to-fine technique is designed to select reliable 3D Gaussian representations to optimize camera pose, resulting in runtime reduction and robust estimation. Our method achieves competitive performance compared with existing state-of-the-art real-time methods on the Replica, TUM-RGBD datasets. The source code will be released upon acceptance. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.11700.pdf) 

### 2. SplaTAM: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM
**Authors**: Nikhil Keetha, Jay Karhade, Krishna Murthy Jatavallabhula, Gengshan Yang,
Sebastian Scherer, Deva Ramanan, Jonathon Luiten

<details span>
<summary><b>Abstract</b></summary>
Dense simultaneous localization and mapping (SLAM) is pivotal for embodied scene understanding. Recent work has shown that 3D Gaussians enable high-quality reconstruction and real-time rendering of scenes using multiple posed cameras. In this light, we show for the first time that representing a scene by 3D Gaussians can enable dense SLAM using a single unposed monocular RGB-D camera. Our method, SplaTAM, addresses the limitations of prior radiance field-based representations, including fast rendering and optimization, the ability to determine if areas have been previously mapped, and structured map expansion by adding more Gaussians. We employ an online tracking and mapping pipeline while tailoring it to specifically use an underlying Gaussian representation and silhouette-guided optimization via differentiable rendering. Extensive experiments show that SplaTAM achieves up to 2× state-of-theart performance in camera pose estimation, map construction, and novel-view synthesis, demonstrating its superiority over existing approaches, while allowing real-time rendering of a high-resolution dense 3D map.
</details>

 [📄 Paper](https://arxiv.org/pdf/2312.02126.pdf) | [🌐 Project Page](https://spla-tam.github.io/) | [💻 Code](https://github.com/spla-tam/SplaTAM) | [🎥 Explanation Video](https://www.youtube.com/watch?v=35SX8DTdQLs)

### 3. Gaussian Splatting SLAM 
**Authors**: Hidenobu Matsuki, Riku Murai, Paul H. J. Kelly, Andrew J. Davison 

<details span>
<summary><b>Abstract</b></summary>
We present the first application of 3D Gaussian Splatting to incremental 3D reconstruction using a single moving monocular or RGB-D camera. Our Simultaneous Localisation and Mapping (SLAM) method, which runs live at 3fps, utilises Gaussians as the only 3D representation, unifying the required representation for accurate, efficient tracking, mapping, and high-quality rendering.
Several innovations are required to continuously reconstruct 3D scenes with high fidelity from a live camera. First, to move beyond the original 3DGS algorithm, which requires accurate poses from an offline Structure from Motion (SfM) system, we formulate camera tracking for 3DGS using direct optimisation against the 3D Gaussians, and show that this enables fast and robust tracking with a wide basin of convergence. Second, by utilising the explicit nature of the Gaussians, we introduce geometric verification and regularisation to handle the ambiguities occurring in incremental 3D dense reconstruction. Finally, we introduce a full SLAM system which not only achieves state-of-the-art results in novel view synthesis and trajectory estimation, but also reconstruction of tiny and even transparent objects. 
</details>

 [📄 Paper](https://www.imperial.ac.uk/media/imperial-college/research-centres-and-groups/dyson-robotics-lab/hide-et-al_GaussianSplattingSLAM_Dec2023.pdf) | [🌐 Project Page](https://rmurai.co.uk/projects/GaussianSplattingSLAM/) | [💻 Code](https://github.com/muskie82/MonoGS) | [🎥 Short Presentation](https://youtu.be/x604ghp9R_Q?si=fPtz4kgBKFfcnQf3)

### 4. Gaussian-SLAM: Photo-realistic Dense SLAM with Gaussian Splatting 
**Authors**: Vladimir Yugay, Yue Li, Theo Gevers, Martin R. Oswald  

<details span>
<summary><b>Abstract</b></summary>
We present the first neural RGBD SLAM method capable of photorealistically reconstructing real-world scenes.
Despite modern SLAM methods achieving impressive results on synthetic datasets, they still struggle with real-world datasets. Our approach utilizes 3D Gaussians as a primary unit for our scene representation to overcome the limitations of the previous methods. We observe that classical 3D Gaussians are hard to use in a monocular setup: they can't encode accurate geometry and are hard to optimize with single-view sequential supervision. By extending classical 3D Gaussians to encode geometry, and designing a novel scene representation and the means to grow, and optimize it, we propose a SLAM system capable of reconstructing and rendering real-world datasets without compromising on speed and efficiency.
We show that Gaussian-SLAM can reconstruct and photorealistically render real-world scenes. We evaluate our method on common synthetic and real-world datasets and compare it against other state-of-the-art SLAM methods. Finally, we demonstrate, that the final 3D scene representation that we obtain can be rendered in Real-time thanks to the efficient Gaussian Splatting rendering.
</details>

 [📄 Paper](https://ivi.fnwi.uva.nl/cv/paper/GaussianSLAM.pdf) | [🌐 Project Page](https://vladimiryugay.github.io/gaussian_slam/) | [💻 Code (not yet)](https://github.com/VladimirYugay/Gaussian-SLAM) | [🎥 Short Presentation](https://www.youtube.com/watch?v=RZK1o_ija7M)

### 5. Photo-SLAM: Real-time Simultaneous Localization and Photorealistic Mapping for Monocular, Stereo, and RGB-D Cameras  
**Authors**: Huajian Huang, Longwei Li, Hui Cheng, Sai-Kit Yeung  

<details span>
<summary><b>Abstract</b></summary>
The integration of neural rendering and the SLAM system recently showed promising results in joint localization and photorealistic view reconstruction. However, existing methods, fully relying on implicit representations, are so resource-hungry that they cannot run on portable devices, which deviates from the original intention of SLAM. In this paper, we present Photo-SLAM, a novel SLAM framework with a hyper primitives map. Specifically, we simultaneously exploit explicit geometric features for localization and learn implicit photometric features to represent the texture information of the observed environment. In addition to actively densifying hyper primitives based on geometric features, we further introduce a Gaussian-Pyramid-based training method to progressively learn multi-level features, enhancing photorealistic mapping performance. The extensive experiments with monocular, stereo, and RGB-D datasets prove that our proposed system Photo-SLAM significantly outperforms current state-of-the-art SLAM systems for online photorealistic mapping, e.g., PSNR is 30% higher and rendering speed is hundreds of times faster in the Replica dataset. Moreover, the Photo-SLAM can run at real-time speed using an embedded platform such as Jetson AGX Orin, showing the potential of robotics applications. 
</details>

 [📄 Paper](https://arxiv.org/pdf/2311.16728.pdf)

<br>

## Sparse:
## 2023:
### 1. SparseGS: Real-Time 360° Sparse View Synthesis using Gaussian Splatting   
**Authors**: Haolin Xiong, Sairisheek Muttukuru, Rishi Upadhyay, Pradyumna Chari, Achuta Kadambi 
<details span>
<summary><b>Abstract</b></summary>
The problem of novel view synthesis has grown significantly in popularity recently with the introduction of Neural Radiance Fields (NeRFs) and other implicit scene representation methods. A recent advance, 3D Gaussian Splatting (3DGS), leverages an explicit representation to achieve real-time rendering with high-quality results. However, 3DGS still requires an abundance of training views to generate a coherent scene representation. In few shot settings, similar to NeRF, 3DGS tends to overfit to training views, causing background collapse and excessive floaters, especially as the number of training views are reduced. We propose a method to enable training coherent 3DGS-based radiance fields of 360 scenes from sparse training views. We find that using naive depth priors is not sufficient and integrate depth priors with generative and explicit constraints to reduce background collapse, remove floaters, and enhance consistency from unseen viewpoints. Experiments show that our method outperforms base 3DGS by up to 30.5% and NeRF-based methods by up to 15.6% in LPIPS on the MipNeRF-360 dataset with substantially less training and inference cost. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.00206.pdf) | [🌐 Project Page](https://formycat.github.io/SparseGS-Real-Time-360-Sparse-View-Synthesis-using-Gaussian-Splatting/) | [💻 Code (not yet)]() 

### 2. FSGS: Real-Time Few-shot View Synthesis using Gaussian Splatting  
**Authors**: Zehao Zhu, Zhiwen Fan, Yifan Jiang, Zhangyang Wang 
<details span>
<summary><b>Abstract</b></summary>
Novel view synthesis from limited observations remains an important and persistent task. However, high efficiency in existing NeRF-based few-shot view synthesis is often compromised to obtain an accurate 3D representation. To address this challenge, we propose a few-shot view synthesis framework based on 3D Gaussian Splatting that enables real-time and photo-realistic view synthesis with as few as three training views. The proposed method, dubbed FSGS, handles the extremely sparse initialized SfM points with a thoughtfully designed Gaussian Unpooling process. Our method iteratively distributes new Gaussians around the most representative locations, subsequently infilling local details in vacant areas. We also integrate a large-scale pre-trained monocular depth estimator within the Gaussians optimization process, leveraging online augmented views to guide the geometric optimization towards an optimal solution. Starting from sparse points observed from limited input viewpoints, our FSGS can accurately grow into unseen regions, comprehensively covering the scene and boosting the rendering quality of novel views. Overall, FSGS achieves state-of-the-art performance in both accuracy and rendering efficiency across diverse datasets, including LLFF, Mip-NeRF360, and Blender
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.00451.pdf) | [🌐 Project Page](https://zehaozhu.github.io/FSGS/) | [💻 Code](https://github.com/VITA-Group/FSGS) 

### 3. pixelSplat: 3D Gaussian Splats from Image Pairs for Scalable Generalizable 3D Reconstruction 
**Authors**: David Charatan, Sizhe Li, Andrea Tagliasacchi, Vincent Sitzmann 
<details span>
<summary><b>Abstract</b></summary>
We introduce pixelSplat, a feed-forward model that learns to reconstruct 3D radiance fields parameterized by 3D Gaussian primitives from pairs of images. Our model features real-time and memory-efficient rendering for scalable training as well as fast 3D reconstruction at inference time. To overcome local minima inherent to sparse and locally supported representations, we predict a dense probability distribution over 3D and sample Gaussian means from that probability distribution. We make this sampling operation differentiable via a reparameterization trick, allowing us to back-propagate gradients through the Gaussian splatting representation. We benchmark our method on wide-baseline novel view synthesis on the real-world RealEstate10k and ACID datasets, where we outperform state-of-the-art light field transformers and accelerate rendering by 2.5 orders of magnitude while reconstructing an interpretable and editable 3D radiance field. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.12337.pdf) | [🌐 Project Page](https://davidcharatan.com/pixelsplat/) | [💻 Code](https://github.com/dcharatan/pixelsplat) 

### 4. Splatter Image: Ultra-Fast Single-View 3D Reconstruction 
**Authors**: Stanislaw Szymanowicz, Christian Rupprecht, Andrea Vedaldi 
<details span>
<summary><b>Abstract</b></summary>
We introduce the Splatter Image, an ultra-fast approach for monocular 3D object reconstruction which operates at 38 FPS. Splatter Image is based on Gaussian Splatting, which has recently brought real-time rendering, fast training, and excellent scaling to multi-view reconstruction. For the first time, we apply Gaussian Splatting in a monocular reconstruction setting. Our approach is learning-based, and, at test time, reconstruction only requires the feed-forward evaluation of a neural network. The main innovation of Splatter Image is the surprisingly straightforward design: it uses a 2D image-to-image network to map the input image to one 3D Gaussian per pixel. The resulting Gaussians thus have the form of an image, the Splatter Image. We further extend the method to incorporate more than one image as input, which we do by adding cross-view attention. Owning to the speed of the renderer (588 FPS), we can use a single GPU for training while generating entire images at each iteration in order to optimize perceptual metrics like LPIPS. On standard benchmarks, we demonstrate not only fast reconstruction but also better results than recent and much more expensive baselines in terms of PSNR, LPIPS, and other metrics. 
</details>

  [📄 Paper](https://arxiv.org/pdf/2312.13150.pdf) | [🌐 Project Page](https://szymanowiczs.github.io/splatter-image.html) | [💻 Code](https://github.com/szymanowiczs/splatter-image) | [🎥 Short Presentation](https://www.youtube.com/watch?v=pcKTf9SVh4g)

<br>

## Data
- [NERDS 360 Multi-View dataset for Outdoor Scenes](https://zubair-irshad.github.io/projects/neo360.html)

<br>

## Courses
- [MIT Inverse Rendering Lectures (Module 2)](https://www.scenerepresentations.org/courses/inverse-graphics-23/)

<br>

## Open Source Implementations 
### Reference 
- [Gaussian Splatting](https://github.com/graphdeco-inria/gaussian-splatting)

### Unofficial Implementations
- [Taichi 3D Gaussian Splatting](https://github.com/wanmeihuali/taichi_3d_gaussian_splatting)
- [Gaussian Splatting 3D](https://github.com/heheyas/gaussian_splatting_3d)
- [3D Gaussian Splatting](https://github.com/WangFeng18/3d-gaussian-splatting)
- [fast: C++/CUDA](https://github.com/MrNeRF/gaussian-splatting-cuda)
- [nerfstudio: python/CUDA](https://github.com/nerfstudio-project/gsplat)
- [taichi-splatting: pytorch/taichi](https://github.com/uc-vision/taichi-splatting)
- [OpenSplat: C++/CUDA](https://github.com/pierotofy/OpenSplat)

### 2D Gaussian Splatting
- [jupyter notebook 2D GS splatting](https://github.com/OutofAi/2D-Gaussian-Splatting)

### Game Engines 
- [Unity](https://github.com/aras-p/UnityGaussianSplatting)
- [PlayCanvas](https://github.com/playcanvas/engine/tree/main/extras/splat)
- [Unreal](https://github.com/xverse-engine/XV3DGS-UEPlugin)

### Viewers
- [WebGL Viewer 1](https://github.com/antimatter15/splat)
- [WebGL Viewer 2](https://github.com/kishimisu/Gaussian-Splatting-WebGL)
- [WebGL Viewer 3](https://github.com/BladeTransformerLLC/gauzilla)
- [WebGPU Viewer 1](https://github.com/cvlab-epfl/gaussian-splatting-web)
- [WebGPU Viewer 2](https://github.com/MarcusAndreasSvensson/gaussian-splatting-webgpu)
- [Three.js](https://github.com/mkkellogg/GaussianSplats3D)
- [A-Frame](https://github.com/quadjr/aframe-gaussian-splatting)
- [Nerfstudio Unofficial](https://github.com/yzslab/nerfstudio/tree/gaussian_splatting)
- [Nerfstudio Viser](https://github.com/nerfstudio-project/viser)
- [Blender (Editor)](https://github.com/ReshotAI/gaussian-splatting-blender-addon/tree/master)
- [WebRTC viewer](https://github.com/dylanebert/gaussian-viewer)
- [iOS & Metal viewer](https://github.com/laanlabs/metal-splats)
- [jupyter notebook](https://github.com/shumash/gaussian-splatting/blob/mshugrina/interactive/interactive.ipynb)
- [PyOpenGL viewer (also with official CUDA backend)](https://github.com/limacv/GaussianSplattingViewer.git)
- [PlayCanvas Viewer](https://github.com/playcanvas/model-viewer)
- [gsplat.js](https://github.com/dylanebert/gsplat.js)
- [Splatapult](https://github.com/hyperlogic/splatapult) - 3d gaussian splatting renderer in C++ and OpenGL, works with OpenXR for tethered VR
- [VulkanSplatting](https://github.com/shg8/VulkanSplatting) - cross-platform, high performance 3DGS renderer in C++ and Vulkan Compute
- [Gaussian Viewer](https://github.com/Florian-Barthel/gaussian_viewer) - Loads also Compact3D plys.

### Utilities
- [Kapture](https://github.com/naver/kapture) - A unified data format to facilitate visual localization and structure from motion e.g. for bundler to colmap model conversion
- [Kapture image cropper script](https://gist.github.com/jo-chemla/258e6e40d3d6c2220b29518ff3c17c40) - Undistorted image cropper script to remove black borders with included conversion instructions
- [camorph](https://github.com/Fraunhofer-IIS/camorph) - A toolbox for conversion between camera parameter conventions e.g. Reality Capture to colmap model
- [3DGS Converter](https://github.com/francescofugazzi/3dgsconverter) - A tool for converting 3D Gaussian Splatting .ply files into a format suitable for Cloud Compare and vice-versa
- [SuperSplat](https://github.com/playcanvas/super-splat) - Open source browser-based tool to clean/filter, reorient and compress .ply/.splat files
- [SpectacularAI](https://github.com/SpectacularAI/point-cloud-tools) - Conversion scripts for different 3DGS conventions
- [GSOPs](https://github.com/david-rhodes/GSOPs) - GSOPs (Gaussian Splat Operators) for SideFX Houdini. Import, edit, and export models, or generate synthetic training data

### Other
- [My-exp-Gaussians](https://github.com/ingra14m/My-exp-Gaussians) - Enhancing the ability of 3D Gaussians to model complex scenes


## Blog Posts

1. [Gaussian Splatting is pretty cool](https://aras-p.info/blog/2023/09/05/Gaussian-Splatting-is-pretty-cool/)
2. [Making Gaussian Splats smaller](https://aras-p.info/blog/2023/09/13/Making-Gaussian-Splats-smaller/)
3. [Making Gaussian Splats more smaller](https://aras-p.info/blog/2023/09/27/Making-Gaussian-Splats-more-smaller/)
4. [Introduction to 3D Gaussian Splatting](https://huggingface.co/blog/gaussian-splatting)
5. [Very good (technical) intro to 3D Gaussian Splatting](https://medium.com/@AriaLeeNotAriel/numbynum-3d-gaussian-splatting-for-real-time-radiance-field-rendering-kerbl-et-al-60c0b25e5544)
6. [Write up on some mathematical details of the 3DGS implementation](https://github.com/kwea123/gaussian_splatting_notes)
7. [Discussion about gs universal format](https://github.com/mkkellogg/GaussianSplats3D/issues/47#issuecomment-1801360116)
8. [Math explanation to understand 3DGS](https://github.com/chiehwangs/3d-gaussian-theory)
9. [Compressing Gaussian Splats](https://blog.playcanvas.com/compressing-gaussian-splats/)
10. [Comprehensive overview of Gaussian Splatting](https://towardsdatascience.com/a-comprehensive-overview-of-gaussian-splatting-e7d570081362)
11. [Gaussian Head Avatars: A Summary](https://towardsdatascience.com/gaussian-head-avatars-a-summary-2bd17bd48500)
12. [NeRFs vs. 3DGS](https://edwardahn.me/writing/NeRFvs3DGS/)

## Tutorial Videos

1. [Getting Started with 3DGS for Windows](https://youtu.be/UXtuigy_wYc?si=j1vfORNspcocSH-b)
2. [How to view 3DGS Scenes in Unity](https://youtu.be/5_GaPYBHqOo?si=6u9j1HqXwF_5WSUL)
3. [Two-minute explanation of 3DGS](https://youtu.be/HVv_IQKlafQ?si=w5c9XKHfKIBuXDLW)
4. [Jupyter notebook tutorial](https://www.youtube.com/watch?v=OcvA7fmiZYM&t=2s)
5. [Intro to gaussian splatting (and Unity plugin)](https://www.xuanprada.com/blog/2023/10/22/intro-to-gaussian-splatting)

## Credits

- Thanks to [Leonid Keselman](https://github.com/leonidk) for informing me about the release of the paper "Real-time Photorealistic Dynamic Scene Representation and Rendering with 4D Gaussian Splatting".
- Thanks to [Eric Haines](https://github.com/erich666) for suggesting the jupyter notebook viewer, windows tutorial and for fixing text hyphenations and other issues.
- Thanks to [Henry Pearce](https://github.com/henrypearce4D) for maintaining contributions.
