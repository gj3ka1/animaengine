---
license: mit
datasets:
- trojblue/test-HunyuanVideo-anime-stills
base_model:
- tencent/HunyuanVideo
pipeline_tag: text-to-video
tags:
- hunyuan-video
- text-to-video
- lora
- diffusers
- template:diffusion-lora
instance_prompt: anime
---

# **AnimaEngine**

![Sample 1](samples/ComfyUI_00017_.webp)
![Sample 2](samples/ComfyUI_00024_.webp)
![Sample 3](samples/ComfyUI_00068_.webp)
![Sample 4](samples/ComfyUI_00071_.webp)

[v0.1 - Testing Version]



An anime-style lora trained on anime screencaps and illustrations, aimed to create vibrant, bright and colorful anime style motions. It's good at generating single person motions (and girls better than boys).



## Usage

To use the lora (and to use HunyuanVideo in general) in ComfyUI, it's recommended to install the [VideoHelperSuite](https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite), and update to torch 2.5.1+cu124:

```
pip install -U torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu124
```



## Prompting

Use prompts in the format of `anime <subject> <description>` to get the best results, use resolution `544x960` (and usually horizontal works a little bit better than vertical). for example:



- anime girl with pink twin tails and green eyes, wearing a school uniform, holding a stack of books in a bustling library filled with sunlight streaming through tall windows.
- anime boy with silver hair and blue eyes, wearing a casual hoodie, sitting on a park bench, feeding pigeons with a gentle smile.
- anime girl 1girl, alcohol carton, blush, braid, bridge, crosswalk, dress, green dress, holding carton, long hair, long sleeves, multiple girls, night, open mouth, outdoors, pedestrian bridge, purple eyes, red hair, single braid, solo focus, spaghetti strap

## Limitations

It's trained as a test model so sometimes when body movements are large it gets disconnected. Also some concepts are less anime-like compared to others. I do plan to update the model later with more training time and dataset.
