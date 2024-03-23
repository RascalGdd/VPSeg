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
By contrast, we are the first to harness vanishing point (VP) priors for more effective segmentation. The comparisons between different tasks are shown in the following figure.
<p align="center">
    <img src="./figs/git_compare.png" width="1020" height="475"/> <br />
    <em> 
    Figure 1: Qualitative comparison on ACDC.} The yellow box represents the densely partitioned VP region. Our model produces more accurate results for both distant tiny hard samples near the VP and occluded fast-moving close targets.
    </em>
</p>

Due to a lack of appropriate IOC datasets, we present a large-scale dataset IOCfish5K which contains a total of 5,637 high-resolution images and 659,024 annotated center points. Underwater scenes contain many indiscernible objects (Sea Horse, Reef Stonefish, Lionfish, and Leafy Sea Dragon) because of limited visibility and active mimicry. Hence, we focus on underwater scenes for our dataset. 

