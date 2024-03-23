# Vanishing-Point-Guided Video Semantic Segmentation of Driving Scenes (CVPR2024)
> [Paper](https://arxiv.org/pdf/2401.15261.pdf)
> 
> Authors:
> [Diandian Guo](https://www.linkedin.com/in/diandian-guo-062000228/), 
> [Deng-Ping Fan](https://dengpingfan.github.io/),
> [Tongyu Lu](https://lucainiaoge.github.io/),
> [Christos Sakaridis](https://people.ee.ethz.ch/~csakarid/), 
> [Luc Van Gool](https://ee.ethz.ch/the-department/faculty/professors/person-detail.OTAyMzM=.TGlzdC80MTEsMTA1ODA0MjU5.html).
>
## 1. Vanishing-Point Guided
The estimation of implicit cross-frame correspondences and the high computational cost have long been major challenges in video semantic segmentation (VSS) for driving scenes. 
Prior works utilize keyframes, feature propagation, or cross-frame attention to address these issues.
By contrast, we are the first to harness vanishing point (VP) priors for more effective segmentation. The comparisons between different SOTA methods are shown in the following figure.
<p align="center">
    <img src="./figs/git_compare.png" width="960" height="475"/> <br />
    <em> 
    Figure 1: Qualitative comparison on ACDC.} The yellow box represents the densely partitioned VP region. Our model produces more accurate results for both distant tiny hard samples near the VP and occluded fast-moving close targets.
    </em>
</p>

## 2. Visualization
Visualization of detail attention maps O with N motion attention layers in CMA. As N increases, the detail attention map interacts more heavily with the dynamic features, and the weights gradually decrease in closer parts of the scene or on simple semantic categories. The highlighted distant regions near the VP suggest that the final predictions P_f are primarily based on the detail-based predictions P_d and not on P_c for these regions. The VP proximity map serves as a positional prior and assists the model in pinpointing the locations of these distant regions.
<p align="center">
    <img src="./figs/git_vis2.png" /> <br />
</p>

## 3. Quantitative Results
The results for various methods are shown below.
| Method           | Publication | Val: MAE | Val: MSE | Val: NAE | Test: MAE | Test:MSE | Test:NAE |
|------------------|:-----------:|:--------:|:--------:|:--------:|:---------:|:--------:|:--------:|
| MCNN             |   CVPR'16   |   81.62  |  152.09  |   3.53   |   72.93   |  129.43  |   4.90   |
| CSRNet           |   CVPR'18   |   43.05  |   78.46  |   1.91   |   38.12   |   69.75  |   2.48   |
| LCFCN            |   ECCV'18   |   31.99  |   81.12  |   0.77   |   28.05   |   68.24  |   1.12   |
| CAN              |   CVPR'19   |   47.77  |   83.67  |   2.10   |   42.02   |   74.46  |   2.58   |
| DSSI-Net         |   ICCV'19   |   33.77  |   80.08  |   1.25   |   31.04   |   69.11  |   1.68   |
| BL               |   ICCV'19   |   19.67  |   44.21  |   0.39   |   20.03   |   46.08  |   0.55   |
| NoisyCC          |  NeurIPS'20 |   19.48  |   41.76  |   0.39   |   19.73   |   46.85  |   0.46   |
| DM-Count         |  NeurIPS'20 |   19.65  |   42.56  |   0.42   |   19.52   |   45.52  |   0.55   |
| GL               |   CVPR'21   |   18.13  |   44.57  |   0.33   |   18.80   |   46.19  |   0.47   |
| P2PNet           |   ICCV'21   |   21.38  |   45.12  |   0.39   |   20.74   |   47.90  |   0.48   |
| KDMG             |   TPAMI'22  |   22.79  |   47.32  |   0.90   |   22.79   |   49.94  |   1.17   |
| MPS              |  ICASSP'22  |   34.68  |   59.46  |   2.06   |   33.55   |   55.02  |   2.61   |
| MAN              |   CVPR'22   |   24.36  |   40.65  |   2.39   |   25.82   |   45.82  |   3.16   |
| CLTR             |   ECCV'22   |   17.47  |   37.06  |   0.29   |   18.07   |   41.90  |   0.43   |
| IOCFormer (Ours) |   CVPR'23   |   15.91  |   34.08  |   0.26   |   17.12   |   41.25  |   0.38   |
