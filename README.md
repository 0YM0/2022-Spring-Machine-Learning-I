# 2022 Spring Machine Learning I

Traffic sign object detection project from a Machine Learning I course.

This repository organizes two experiment notebooks:

- Faster R-CNN with TorchVision
- YOLOv5 custom training with Ultralytics YOLOv5

The original backup contained local datasets, Colab outputs, and large zip files. This cleaned version keeps the code and documentation suitable for GitHub, while excluding datasets, model weights, and generated training outputs.

## Poster

[📄 View full poster](assets/2022_Machine_Learning_I_Poster.png)


## Project Structure

```text
.
├── notebooks/
│   ├── faster_rcnn_traffic_sign.ipynb
│   └── yolov5_traffic_sign.ipynb
├── docs/
│   └── dataset.md
├── requirements.txt
└── .gitignore
```

## Dataset

The project uses a traffic sign detection dataset with bounding boxes. The backup dataset had the following structure:

- `TrafficSignDataSet/train`, `valid`, `test` with CSV annotations for Faster R-CNN
- `train_data/images/{train,val,test}` and `train_data/labels/{train,val,test}` in YOLO format

Dataset files are intentionally not committed because the backup includes hundreds of image files and a 100MB+ zip archive. See `docs/dataset.md` for the expected layout.

## Notebooks

### Faster R-CNN

`notebooks/faster_rcnn_traffic_sign.ipynb`

Uses `torchvision.models.detection.fasterrcnn_resnet50_fpn` and replaces the classifier head for the traffic sign classes.

### YOLOv5

`notebooks/yolov5_traffic_sign.ipynb`

Clones Ultralytics YOLOv5 in Colab, prepares a YOLO-format dataset, trains a custom detector, evaluates mAP, and runs inference.

