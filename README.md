# PriorityCut: Occlusion-guided Regularization for Warp-based Image Animation

<a href="https://arxiv.org/abs/2103.11600"><img src="https://img.shields.io/badge/arXiv-2103.11600-b31b1b.svg"></a>


## Abstract

Image animation generates a video of a source image following the motion of a driving video. State-of-the-art self-supervised image animation approaches warp the source image according to the motion of the driving video and recover the warping artifacts by inpainting. These approaches mostly use vanilla convolution for inpainting, and vanilla convolution does not distinguish between valid and invalid pixels. As a result, visual artifacts are still noticeable after inpainting. CutMix is a state-of-the-art regularization strategy that cuts and mixes patches of images and is widely studied in different computer vision tasks. Among the remaining computer vision tasks, warp-based image animation is one of the fields that the effects of CutMix have yet to be studied. This paper first presents a preliminary study on the effects of CutMix on warp-based image animation. We observed in our study that CutMix helps improve only pixel values, but disturbs the spatial relationships between pixels. Based on such observation, we propose PriorityCut, a novel augmentation approach that uses the top-k percent occluded pixels of the foreground to regularize warp-based image animation. By leveraging the domain knowledge in warp-based image animation, PriorityCut significantly reduces the warping artifacts in state-of-the-art warp-based image animation models on diverse datasets.

## PriorityCut

![teaser](https://user-images.githubusercontent.com/64956291/112425285-279b9900-8d79-11eb-9199-22b0e76d7393.png)

Warp-based image animation warps the source image (1st column) based on the driving image (2nd column) and recovers the warping artifacts by inpainting (3rd column). PriorityCut utilizes the occlusion information (4th column) in image animation indicating the locations of warping artifacts (5th column) to regularize discriminator predictions on inpainting. The augmented image (6th column) contains a mixture of patches between the driving and the generated images. For further details, please refer to the [paper](https://arxiv.org/abs/2103.11600).

## Citation

```plain
@article{cheung2021prioritycut,
      title={PriorityCut: Occlusion-guided Regularization for Warp-based Image Animation}, 
      author={Wai Ting Cheung and Gyeongsu Chae},
      year={2021},
      eprint={2103.11600},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
