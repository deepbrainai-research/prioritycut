---
layout: default
---

# Abstract 

We propose a novel architecture and improved training objectives for non-parallel voice conversion. Our proposed CycleGAN-based model performs a shape-preserving transformation directly on a high frequency-resolution magnitude spectrogram, converting its style (i.e. speaker identity) while preserving the speech content. Throughout the entire conversion process, the model does not resort to compressed intermediate representations of any sort (e.g. mel spectrogram, low resolution spectrogram, decomposed network feature). We propose an efficient axial residual block architecture to support this expensive procedure and various modifications to the CycleGAN losses to stabilize the training process. We demonstrate via experiments that our proposed model outperforms Scyclone and shows a comparable or better performance to that of CycleGAN-VC2 even without employing a neural vocoder.


# Audio Samples 

**Note**: For experimental details please refer to the [**[paper]**](https://arxiv.org/abs/2102.08075).



## VCTK dataset (English)

**Source** is the source speech samples. 
**Target** is the target speech samples.  
They are provided as references. Note that we did not use these data during training.

### Female -> Female (p299, p301)

| Source | Target | Scyclone | CycleGAN-VC2 | Ours | 
|:-------|:-------|:---------|:-------------|:-----|
|<audio src="./assets/audio/ff_p299_to_p301/gt_src/p299_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/ff_p299_to_p301/gt_tgt/p301_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/ff_p299_to_p301/scy/AB_0.wav" controls preload="auto">|<audio src="./assets/audio/ff_p299_to_p301/vc2/001.wav" controls preload="auto">|<audio src="./assets/audio/ff_p299_to_p301/ours/001.wav" controls preload="auto">|

### Female -> Female (p301, p299)

| Source | Target | Scyclone | CycleGAN-VC2 | Ours | 
|:-------|:-------|:---------|:-------------|:-----|
|<audio src="./assets/audio/ff_p301_to_p299/gt_src/p301_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/ff_p301_to_p299/gt_tgt/p299_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/ff_p301_to_p299/scy/BA_0.wav" controls preload="auto">|<audio src="./assets/audio/ff_p301_to_p299/vc2/001.wav" controls preload="auto">|<audio src="./assets/audio/ff_p301_to_p299/ours/001.wav" controls preload="auto">|

### Female -> Male (p299, p311)

| Source | Target | Scyclone | CycleGAN-VC2 | Ours | 
|:-------|:-------|:---------|:-------------|:-----|
|<audio src="./assets/audio/fm_p299_to_p311/gt_src/p299_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/fm_p299_to_p311/gt_tgt/p311_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/fm_p299_to_p311/scy/AB_0.wav" controls preload="auto">|<audio src="./assets/audio/fm_p299_to_p311/vc2/001.wav" controls preload="auto">|<audio src="./assets/audio/fm_p299_to_p311/ours/001.wav" controls preload="auto">|

### Male -> Female (p311, p299)

| Source | Target | Scyclone | CycleGAN-VC2 | Ours | 
|:-------|:-------|:---------|:-------------|:-----|
|<audio src="./assets/audio/fm_p311_to_p299/gt_src/p311_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/fm_p311_to_p299/gt_tgt/p299_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/fm_p311_to_p299/scy/BA_0.wav" controls preload="auto">|<audio src="./assets/audio/fm_p311_to_p299/vc2/001.wav" controls preload="auto">|<audio src="./assets/audio/fm_p311_to_p299/ours/001.wav" controls preload="auto">|

### Male -> Male (p311, p360)

| Source | Target | Scyclone | CycleGAN-VC2 | Ours | 
|:-------|:-------|:---------|:-------------|:-----|
|<audio src="./assets/audio/mm_p311_to_p360/gt_src/p311_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/mm_p311_to_p360/gt_tgt/p360_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/mm_p311_to_p360/scy/001.wav" controls preload="auto">|<audio src="./assets/audio/mm_p311_to_p360/vc2/001.wav" controls preload="auto">|<audio src="./assets/audio/mm_p311_to_p360/ours/001.wav" controls preload="auto">|

### Male -> Male (p360, p311)

| Source | Target | Scyclone | CycleGAN-VC2 | Ours | 
|:-------|:-------|:---------|:-------------|:-----|
|<audio src="./assets/audio/mm_p360_to_p311/gt_src/p360_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/mm_p360_to_p311/gt_tgt/p311_001_mic1.wav" controls preload="auto">|<audio src="./assets/audio/mm_p360_to_p311/scy/BA_0.wav" controls preload="auto">|<audio src="./assets/audio/mm_p360_to_p311/vc2/001.wav" controls preload="auto">|<audio src="./assets/audio/mm_p360_to_p311/ours/001.wav" controls preload="auto">|


## KSS & Internal dataset (Korean)

**Target** is omitted since KSS and our internal datset are non-parallel.

### Female -> Female (JEY, KSS)

| Source | Scyclone | CycleGAN-VC2 | Ours | 
|:-------|:---------|:-------------|:-----|
|<audio src="./assets/audio/ff_JEY_to_KSS/gt_src/100.wav" controls preload="auto">|<audio src="./assets/audio/ff_JEY_to_KSS/scy/KSS_00.wav" controls preload="auto">|<audio src="./assets/audio/ff_JEY_to_KSS/vc2/KSS_00.wav" controls preload="auto">|<audio src="./assets/audio/ff_JEY_to_KSS/ours/KSS_00.wav" controls preload="auto">|
|<audio src="./assets/audio/ff_JEY_to_KSS/gt_src/107.wav" controls preload="auto">|<audio src="./assets/audio/ff_JEY_to_KSS/scy/KSS_07.wav" controls preload="auto">|<audio src="./assets/audio/ff_JEY_to_KSS/vc2/KSS_07.wav" controls preload="auto">|<audio src="./assets/audio/ff_JEY_to_KSS/ours/KSS_07.wav" controls preload="auto">|

### Female -> Female (KSS, JEY)

| Source | Scyclone | CycleGAN-VC2 | Ours |
|:-------|:---------|:-------------|:-----|
|<audio src="./assets/audio/ff_KSS_to_JEY/gt_src/KSS_00.wav" controls preload="auto">|<audio src="./assets/audio/ff_KSS_to_JEY/scy/JEY_00.wav" controls preload="auto">|<audio src="./assets/audio/ff_KSS_to_JEY/vc2/JEY_00.wav" controls preload="auto">|<audio src="./assets/audio/ff_KSS_to_JEY/ours/JEY_00.wav" controls preload="auto">|
|<audio src="./assets/audio/ff_KSS_to_JEY/gt_src/KSS_09.wav" controls preload="auto">|<audio src="./assets/audio/ff_KSS_to_JEY/scy/JEY_09.wav" controls preload="auto">|<audio src="./assets/audio/ff_KSS_to_JEY/vc2/JEY_09.wav" controls preload="auto">|<audio src="./assets/audio/ff_KSS_to_JEY/ours/JEY_09.wav" controls preload="auto">|


# Citation 

```plain
@article{you2021arnvc,
  title={Axial Residual Networks for CycleGAN-based Voice Conversion},
  author={Jaeseong You, Gyuhyeon Nam, Dalhyun Kim, Gyeongsu Chae},
  journal={arXiv preprint arXiv:2102.08075},
  year={2021}
}
```


<!-- # Some Template 

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
``` -->
