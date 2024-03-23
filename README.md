# Vanishing-Point-Guided Video Semantic Segmentation of Driving Scenes (CVPR2024)
> [Paper](https://arxiv.org/pdf/2401.15261.pdf)
> 
> Authors:
> [Diandian Guo](), 
> [Deng-Ping Fan](https://dengpingfan.github.io/),
> [Tongyu Lu](),
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

### 5.2. Visualization Results
Visualization of detail attention maps O with N motion attention layers in CMA. As N increases, the detail attention map interacts more heavily with the dynamic features, and the weights gradually decrease in closer parts of the scene or on simple semantic categories. The highlighted distant regions near the VP suggest that the final predictions P_f are primarily based on the detail-based predictions P_d and not on P_c for these regions. The VP proximity map serves as a positional prior and assists the model in pinpointing the locations of these distant regions.
<p align="center">
    <img src="./figs/git_vis.png" /> <br />
</p>
