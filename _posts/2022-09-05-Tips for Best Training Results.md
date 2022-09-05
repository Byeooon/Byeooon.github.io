---
date : 2022-08-31
title : "[YOLO] Yolov5 Tips for Best Training Results"
comments : true
categories : 
    - YOLO
---

* Images per class. ≥ 1500 images per class recommended
* Instances per class. ≥ 10000 instances (labeled objects) per class recommended
* Image variety. Must be representative of deployed environment. For real-world use cases we recommend images from different times of day, different seasons, different weather, different lighting, different angles, different sources (scraped online, collected locally, different cameras) etc.
* Label consistency. All instances of all classes in all images must be labelled. Partial labelling will not work.
* Label accuracy. Labels must closely enclose each object. No space should exist between an object and it's bounding box. No objects should be missing a label.
* Label verification. View train_batch*.jpg on train start to verify your labels appear correct, i.e. see example mosaic.
* Background images. Background images are images with no objects that are added to a dataset to reduce False Positives (FP). We recommend about 0-10% background images to help reduce FPs (COCO has 1000 background images for reference, 1% of the total). No labels are required for background images.

* 출처 : [yolov5.official.github](https://github.com/ultralytics/yolov5/wiki/Tips-for-Best-Training-Results)