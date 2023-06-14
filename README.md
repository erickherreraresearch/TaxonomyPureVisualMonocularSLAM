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
| --- | --- | --- | --- | --- | --- |
| Jin et al. (2000)| SfM | Indirect | Sparse | [paper](https://ieeexplore.ieee.org/document/854954) | NA |
| MonoSLAM (2007) | SfM | Indirect | Sparse | [paper](https://ieeexplore.ieee.org/document/4160954) | [code](https://github.com/marcromani/MonoSLAM) |
| PTAM (2007) | SLAM | Indirect | Sparse | [paper](https://ieeexplore.ieee.org/document/4538852) | [code](https://github.com/Oxford-PTAM/PTAM-GPL) |
| OpenMVG (2013) | SFM | Indirect | Sparse | [paper](https://link.springer.com/chapter/10.1007/978-3-319-56414-2_5) | [code](https://github.com/openMVG/openMVG/tree/v2.0) |
| ORB-SLAM (2015) | SLAM | Indirect | Sparse | [paper](https://ieeexplore.ieee.org/document/7219438) | [code](https://github.com/raulmur/ORB_SLAM) |
| COLMAP (2016) | SFM | Indirect | Sparse | [paper](https://ieeexplore.ieee.org/document/7780814) | [code](https://github.com/colmap/colmap) |
| ORB-SLAM2 (2017) | SLAM | Indirect | Sparse | [paper](https://ieeexplore.ieee.org/document/7946260) | [code](https://github.com/raulmur/ORB_SLAM2) |
| ORB-SLAM3 (2021) | SLAM | Indirect | Sparse | [paper](https://ieeexplore.ieee.org/document/9440682) | [code](https://github.com/UZ-SLAMLab/ORB_SLAM3) |
| Valgaerts et al. (2011) | SFM | Indirect | Dense | [paper](https://link.springer.com/article/10.1007/s11263-011-0466-7) | NA |
| Ranftl et al. (2016) | SFM | Indirect | Dense | [paper](https://ieeexplore.ieee.org/document/7780809) | NA |
|  Stühmer et al. (2010) | SLAM | Indirect | Dense | [paper](https://link.springer.com/chapter/10.1007/978-3-642-15986-2_2) | NA |
|  DTAM (2011) | SLAM | Indirect | Dense | [paper](https://ieeexplore.ieee.org/abstract/document/6126513) | [code](https://github.com/Rintarooo/DTAM_Mapping) |
|  REMODE (2014) | SLAM | Indirect | Dense | [paper](https://ieeexplore.ieee.org/abstract/document/6907233) | [code](https://github.com/uzh-rpg/rpg_open_remode) |
|  LSD-SLAM (2014) | SLAM | Indirect | Dense | [paper](https://link.springer.com/chapter/10.1007/978-3-319-10605-2_54) | [code](https://github.com/tum-vision/lsd_slam) |
|  DSO (2017) | SLAM | Indirect | Dense | [paper](https://ieeexplore.ieee.org/document/7898369) | [code](https://github.com/JakobEngel/dso) |
|  LDSO (2018) | SLAM | Indirect | Dense | [paper](https://ieeexplore.ieee.org/document/8593376) | [code](https://github.com/tum-vision/LDSO) |
|  DSM (2020) | SLAM | Indirect | Dense | [paper](https://ieeexplore.ieee.org/document/9102352) | [code](https://github.com/jzubizarreta/dsm) |
|  SVO (2014) | SLAM | Hybrid | Sparse | [paper](https://ieeexplore.ieee.org/document/6906584) | [code](https://github.com/uzh-rpg/rpg_svo) |

# References
1. Aqel, M. O. A., Marhaban, M. H., Saripan, M. I., & Ismail, N. B. (2016). Review of visual odometry: types, approaches, challenges, and applications. SpringerPlus 2016 5:1, 5(1), 1–26. https://doi.org/10.1186/S40064-016-3573-7
2. Engel, J., Koltun, V., & Cremers, D. (2017). Direct Sparse Odometry. IEEE Transactions on Pattern Analysis and Machine Intelligence, 40(3), 611–625. https://doi.org/10.1109/TPAMI.2017.2658577
