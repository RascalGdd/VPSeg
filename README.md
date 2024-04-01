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
    Figure 1: Qualitative comparison on ACDC. The yellow box represents the densely partitioned VP region. Our model produces more accurate results for both distant tiny hard samples near the VP and occluded fast-moving close targets.
    </em>
</p>

## 2. Visualization
Visualization of detail attention maps O with N motion attention layers in CMA. As N increases, the detail attention map interacts more heavily with the dynamic features, and the weights gradually decrease in closer parts of the scene or on simple semantic categories. The highlighted distant regions near the VP suggest that the final predictions P_f are primarily based on the detail-based predictions P_d and not on P_c for these regions. The VP proximity map serves as a positional prior and assists the model in pinpointing the locations of these distant regions.
<p align="center">
    <img src="./figs/git_vis2.png" /> <br />
</p>

## 3. Quantitative Results
The results for various methods are shown below.
| Method           | Publication | Backbone | Params(M)| mIoU (A.)| mIoU (C.) | miIoU(A.)| miIoU(C.)| mIA-IoU  |    VSS   |
|------------------|:-----------:|:--------:|:--------:|:--------:|:---------:|:--------:|:--------:|:--------:|:--------:|
| DeepLabv3+       |   ECCV'18   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &cross; |
| PSPNet           |   CVPR'17   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &cross; |
| OCRNet           |   ECCV'20   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &cross; |
| SeaFormer        |   ICLR'23   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &cross; |
| SegFormer        |   NIPS'21   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &cross; |
| Video K-Net      |   CVPR'22   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |
| ETC              |   ECCV'20   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |
| TCB              |   CVPR'21   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |
| NetWarp          |   ICCV'17   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |
| P2PNet           |   CVPR'24   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |
| CFFM             |   CVPR'24   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |
| MRCFA            |   CVPR'24   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |
| VPSeg (Ours)     |   CVPR'24   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |
| VPSeg (Ours)     |   CVPR'24   |   -----  |  -----   |   ----   |   -----   |  -----   |   ----   |   ----   |  &check; |

## 4. Citations
```bibtex
@inproceedings{guo2024vpseg,
    title={Vanishing-Point-Guided Video Semantic Segmentation of Driving Scenes},
    author={Diandian Guo and Fan, Deng-Ping and Tongyu Lu and Sakaridis, Christos and Van Gool, Luc},
    booktitle={Proceedings of the IEEE/CVF International Conference on Computer Vision and Patern Recognition (CVPR)},
    year={2024}
}
```
## 5. Contact
- Diandian Guo, guodiandian1998@gmail.com
