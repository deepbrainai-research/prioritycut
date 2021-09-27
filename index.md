---
layout: default
---


# Abstract 
Image animation generates a video of a source image following the motion of a driving video. State-of-the-art self-supervised image animation approaches warp the source image according to the motion of the driving video and recover the warping artifacts by inpainting. These approaches mostly use vanilla convolution for inpainting, and vanilla convolution does not distinguish between valid and invalid pixels. As a result, visual artifacts are still noticeable after inpainting. CutMix is a state-of-the-art regularization strategy that cuts and mixes patches of images and is widely studied in different computer vision tasks. Among the remaining computer vision tasks, warp-based image animation is one of the fields that the effects of CutMix have yet to be studied. This paper first presents a preliminary study on the effects of CutMix on warp-based image animation. We observed in our study that CutMix helps improve only pixel values, but disturbs the spatial relationships between pixels. Based on such observation, we propose PriorityCut, a novel augmentation approach that uses the top-k percent occluded pixels of the foreground to regularize warp-based image animation. By leveraging the domain knowledge in warp-based image animation, PriorityCut significantly reduces the warping artifacts in state-of-the-art warp-based image animation models on diverse datasets.

# PriorityCut

| Source Image | Driving Image | Generated Image | Occlusion Mask | PriorityCut Mask | Augmented Image |
|---|---|---|---|---|---|
| ![source](https://user-images.githubusercontent.com/64956291/112423728-86134800-8d76-11eb-835c-84182af73dcd.png) | ![driving](https://user-images.githubusercontent.com/64956291/112423788-a2af8000-8d76-11eb-9d1b-e40641d15c29.png) | ![generated](https://user-images.githubusercontent.com/64956291/112423831-b529b980-8d76-11eb-9280-519addf86e8d.png) | ![occlusion](https://user-images.githubusercontent.com/64956291/112423898-d25e8800-8d76-11eb-80a9-4fadc783d8ce.png) | ![mask](https://user-images.githubusercontent.com/64956291/112423935-e1ddd100-8d76-11eb-8b56-8da570f9589b.png) | ![final](https://user-images.githubusercontent.com/64956291/112423968-f1f5b080-8d76-11eb-8132-b52212c98fb8.png) |

Warp-based image animation warps the source image (1st column) based on the driving image (2nd column) and recovers the warping artifacts by inpainting (3rd column). PriorityCut utilizes the occlusion information (4th column) in image animation indicating the locations of warping artifacts (5th column) to regularize discriminator predictions on inpainting. The augmented image (6th column) contains a mixture of patches between the driving and the generated images. For further details, please refer to the [paper](https://arxiv.org/abs/2103.11600).

# Results

## VoxCeleb

<center>
<iframe width="800" height="200"
src="https://user-images.githubusercontent.com/64956291/112410217-332d9680-8d5e-11eb-8c9c-9c8961c85a2a.mp4"
frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
allowfullscreen></iframe>

<iframe width="800" height="200"
src="https://user-images.githubusercontent.com/64956291/112411312-07131500-8d60-11eb-9cf4-69c6180e046e.mp4"
frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
allowfullscreen></iframe>

<iframe width="800" height="200"
src="https://user-images.githubusercontent.com/64956291/112411375-2611a700-8d60-11eb-93cb-e7c6fe0bdfef.mp4"
frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
allowfullscreen></iframe>
</center>

## BAIR

<center>
<iframe width="640" height="200"
src="https://user-images.githubusercontent.com/64956291/112411516-5fe2ad80-8d60-11eb-97b0-3544778d1765.mp4"
frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
allowfullscreen></iframe>

<iframe width="640" height="200"
src="https://user-images.githubusercontent.com/64956291/112411533-6cff9c80-8d60-11eb-91da-7718b3c370ac.mp4"
frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
allowfullscreen></iframe>
</center>

## Tai-Chi-HD

<center>
<iframe width="800" height="200"
src="https://user-images.githubusercontent.com/64956291/112411647-9b7d7780-8d60-11eb-8347-21a8b656ef1a.mp4"
frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
allowfullscreen></iframe>

<iframe width="800" height="200"
src="https://user-images.githubusercontent.com/64956291/112411685-a6d0a300-8d60-11eb-96ca-1566cfbc9b63.mp4"
frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
allowfullscreen></iframe>
</center>

# Citation 

```plain
@misc{cheung2021prioritycut,
      title={PriorityCut: Occlusion-guided Regularization for Warp-based Image Animation},
      author={Wai Ting Cheung and Gyeongsu Chae},
      year={2021},
      eprint={2103.11600},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
