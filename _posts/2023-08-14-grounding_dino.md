---
date : 2023-08-14
title : "[AI] 🦕 Grounding DINO"
comments : true
categories : 
    - AI
---

* 공식 깃허브 링크 : [Grounding DINO Github](https://github.com/IDEA-Research/GroundingDINO)

<br>

```python
import os
HOME = os.getcwd()
print(HOME)

%cd {HOME}
!git clone -q https://github.com/IDEA-Research/GroundingDINO.git
%cd {HOME}/GroundingDINO
!pip install -q -e .
!pip install -q roboflow

CONFIG_PATH = os.path.join(HOME, "GroundingDINO/groundingdino/config/GroundingDINO_SwinT_OGC.py")
print(CONFIG_PATH, "; exist:", os.path.isfile(CONFIG_PATH))
```

```python
%cd {HOME}
!mkdir {HOME}/weights
%cd {HOME}/weights
!wget -q https://github.com/IDEA-Research/GroundingDINO/releases/download/v0.1.0-alpha/groundingdino_swint_ogc.pth

WEIGHTS_NAME = "groundingdino_swint_ogc.pth"
WEIGHTS_PATH = os.path.join(HOME, "weights", WEIGHTS_NAME)
print(WEIGHTS_PATH, "; exist:", os.path.isfile(WEIGHTS_PATH))
```

```python
%cd {HOME}
!mkdir {HOME}/data
%cd {HOME}/data

!wget -q https://media.roboflow.com/notebooks/examples/dog.jpeg
!wget -q https://media.roboflow.com/notebooks/examples/dog-2.jpeg
!wget -q https://media.roboflow.com/notebooks/examples/dog-3.jpeg
!wget -q https://media.roboflow.com/notebooks/examples/dog-4.jpeg
```

```python
%cd {HOME}/GroundingDINO

from groundingdino.util.inference import load_model, load_image, predict, annotate

model = load_model(CONFIG_PATH, WEIGHTS_PATH)
```

```python
import numpy as np
from PIL import Image
import groundingdino.datasets.transforms as T

def inference(img, prompt, box_threshold=0.35, text_threshold=0.25):
    transform = T.Compose([
        T.RandomResize([800], max_size=1333),
        T.ToTensor(),
        T.Normalize([0.485, 0.456, 0.406], [0.229, 0.224, 0.225]),
    ])

    image_transformed, _ = transform(Image.fromarray(img), None)

    boxes, logits, phrases = predict(
        model=model,
        image=image_transformed,
        caption=prompt,
        box_threshold=box_threshold,
        text_threshold=text_threshold
    )

    annotated_frame = annotate(image_source=img, boxes=boxes, logits=logits, phrases=phrases)

    return annotated_frame
```

```python
TEXT_PROMPT = "chair, dog, table, shoe, light bulb, coffee, hat, glasses, car, tail, umbrella"

result_img = inference(img, TEXT_PROMPT)

plt.figure(figsize=(16, 16))
plt.imshow(result_img[:, :, ::-1])
plt.axis("off")
plt.show()
```

![Unknown](https://github.com/Byeooon/Byeooon/assets/55019557/52309b49-8b50-4925-9977-59e20fa9ac8b)


```python
TEXT_PROMPT = "black car"

result_img = inference(img, TEXT_PROMPT)

plt.figure(figsize=(16, 16))
plt.imshow(result_img[:, :, ::-1])
plt.axis("off")
plt.show()
```

![Unknown-2](https://github.com/Byeooon/Byeooon/assets/55019557/66d066b4-807d-4566-bccf-16849fc04834)