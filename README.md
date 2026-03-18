# Improve existing online trackers by measuring feature evolution of objects [UAV videos]
## UAV MOT Tracker Comparison

This project evaluates online multi-object tracking on UAV videos using deep ReID appearance features.

## Scope
- Dataset: VisDrone2019-MOT
- Detection source: Ground-truth annotations (no external detector)
- Trackers compared: SORT, DeepSORT, BoT-SORT
- Appearance model: ResNet50-based ReID with 256-d embeddings

## ReID Training (Core Settings)
- Optimizer: Adam
- Learning rate: 0.001
- Batch size: 64
- Weight decay: 5e-4
- Loss: CrossEntropyLoss with label smoothing = 0.1
- Scheduler: StepLR (gamma 0.1, step size 5)
- Input: 256x128
- Augmentations: RandomHorizontalFlip, ColorJitter(0.2), RandomErasing(p=0.5)

## Evaluation Metrics
- MOTA
- IDF1
- IDSW

