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
> ## 1. Vanishing-Point Guided
The existing object counting tasks include: Generic Object Counting (GOC), and Dense Object Counting (DOC). In this paper, we propose a new challenge termed "Indiscernible Object Counting (IOC)", which focuses on counting foreground objects in indiscernible scenes. The comparisons between different tasks are shown in the following figure.
<p align="center">
    <img src="./figs/intro_new.png" width="520" height="475"/> <br />
    <em> 
    Figure 1: Illustration of different counting tasks. Top left: Generic Object Counting (GOC), which counts objects of various classes in natural scenes. Top right: Dense Object Counting (DOC), which counts objects of a foreground class in scenes packed with instances. Down: Indiscernible Object Counting (IOC), which counts objects of a foreground class in indiscernible scenes. Can you find all fishes in the given examples? For GOC, DOC, and IOC, the images shown are from PASCAL VOC, ShanghaiTech, and the new IOCfish5K dataset, respectively.
    </em>
</p>

Due to a lack of appropriate IOC datasets, we present a large-scale dataset IOCfish5K which contains a total of 5,637 high-resolution images and 659,024 annotated center points. Underwater scenes contain many indiscernible objects (Sea Horse, Reef Stonefish, Lionfish, and Leafy Sea Dragon) because of limited visibility and active mimicry. Hence, we focus on underwater scenes for our dataset. 

