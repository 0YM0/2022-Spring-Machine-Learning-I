# Dataset Layout

Place dataset files under a local `data/` directory when running the notebooks.

## Faster R-CNN CSV Format

Expected layout:

```text
data/
└── TrafficSignDataSet/
    ├── train/
    │   ├── _annotations.csv
    │   └── *.jpg
    ├── valid/
    │   ├── _annotations.csv
    │   └── *.jpg
    └── test/
        ├── _annotations.csv
        └── *.jpg
```

Annotation CSV columns used by the notebook:

- `image`
- `xmin`
- `ymin`
- `xmax`
- `ymax`
- `class`

## YOLOv5 Format

Expected layout:

```text
data/
└── train_data/
    ├── images/
    │   ├── train/
    │   ├── val/
    │   └── test/
    └── labels/
        ├── train/
        ├── val/
        └── test/
```

Example YOLOv5 data config:

```yaml
train: ../data/train_data/images/train
val: ../data/train_data/images/val
test: ../data/train_data/images/test

nc: 3
names: ["prohibitory", "mandatory", "danger"]
```
