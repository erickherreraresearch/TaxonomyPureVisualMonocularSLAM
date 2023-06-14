# TaxonomyPureVisualMonocularSLAM
# An Extended Taxonomy for Monocular Visual SLAM, Visual Odometry, and Structure from Motion methods applied to 3D Reconstruction
The monocular pure visual RGB 3D reconstruction challenge is an ill-posed problem that has been widely studied in the past three decades. In particular, the RGB sensor has become the most attractive alternative for Simultaneous Landing and Mapping (SLAM), Visual Odometry (VO), and Structure from Motion (SFM) tasks due to its affordability, lightweight, easy deployment, good outdoor performance, and availability in most handheld devices without requiring additional input devices. In this way, many researchers have proposed multiple alternatives to solve this problem. Early works like (Aqel, Marhaban, Saripan, & Ismail, 2016) have reported classifications like feature-based vs. appearance-based and direct vs. indirect. Nevertheless, there exists a better classification introduced by (Engel, Koltun, & Cremers, 2017) which takes into account the number of points that are projected in the final 3D reconstruction (sparse vs. dense) and the use or absence of preprocessing steps (direct vs. indirect).
### Sparse vs. dense
This classification depends on the number of points projected to represent the geometric scene as point clouds. Those methods that do not recover the majority of pixels of the image are known as sparse, which are primarily focused on recovering specific types of pixel information like edges, corners, or high gradient pixels. On the other hand, dense methods aim to recover most of the pixels and project them as dense point clouds.

### Direct vs. Indirect
Direct vs. indirect classification refers to the existence or absence of preprocessing steps on the pixel information before executing the SLAM, SfM, or VO pipeline. Indirect methods integrate preprocessing steps in their frameworks to select or extract specific pixel information that might be used by their localization or mapping, to reduce computational complexity and prevent the appearance of outliers. On the other hand, direct methods work directly on the pixel information, so they use almost all the information available on each image.

## Extended taxonomy
Due to the impressive advances made in Artificial Intelligence (AI), specifically regarding deep learning and convolutional neural networks, a new classification has emerged to allow researchers to integrate AI techniques to solve the SLAM, SfM, and VO problems. In this way, we propose extending Engel et al.'s taxonomy to include new classifications for these AI-based formulations.
### Claasic vs. Machine Learning
Classic methods, also known as geometric-based, use geometric, probabilistic, and optimization, among other techniques, to build their entire pipeline without requiring machine learning techniques. On the other hand, given the impressive advances in Machine Learning (ML) in recent years, many researchers have made important contributions by fusing classic pipelines with ML techniques to improve the localization or mapping procedures.

Considering all the possible combinations for these three classifications, we can define ten categories for the SLAM, VO, and SfM monocular pure visual algorithms: Classic + Dense + Direct, Classic + Sparse + Direct, Classic + Dense + Indirect, Classic + Sparse + Indirect, Classic + Hybrid, ML + Dense + Direct, ML + Sparse + Direct, ML + Dense + Indirect, ML + Classic + Sparse + Indirect and ML + Hybrid. Figure 1 presents a diagram for the proposed extended taxonomy.

### Figure1. Extended taxonomy
![Alt text](https://github.com/erickherreraresearch/TaxonomyPureVisualMonocularSLAM/blob/main/images/taxonomy.JPG?raw=true "Extended taxonomy for monocular 3D reconstruction methods")

Following the proposed taxonomy, Table 1 presents the most significant proposals for pure visual monocular SLAM, SfM, and VO made from 2000 to 2023.

### Table 1. Classic methods
| Method | Type | Direct or Indirect | Map density | Article | Code |
| Jin et al. (2000)| SfM | Indirect | Sparse | [paper]([https://www.google.com](https://ieeexplore.ieee.org/document/854954)https://ieeexplore.ieee.org/document/854954) | NA |
