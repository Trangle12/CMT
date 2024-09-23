# Contrastive Mean Teacher for Intra-camera Supervised Person Re-Identification

Official implementation of paper [Contrastive Mean Teacher for Intra-camera Supervised Person Re-Identification](https://ieeexplore.ieee.org/document/10534060).

## Updates
- 2024/06 The code was released at [code](https://gitee.com/swjtugx/classmate/tree/master/OurGroup/CMT).
- 2024/05/17 CMT for ICS-ReID is accepted by TCSVT2024!
## Overview

![pipeline](assets/pipeline.jpg)

### Preparation

**Requirements: Pytorch>=1.1.0 and python>=3.6**
Download the datasets:

For privacy reasons, we don't have the copyright of the dataset. Please contact authors to get this dataset.

```
DukeMTMC-reID/
├── bounding_box_test
├── bounding_box_train
└── query

Market-1501-v15.09.15/
├── bounding_box_test
├── bounding_box_train
├── gt_bbox
├── gt_query
└── query

MSMT17/
├── bounding_box_test
├── bounding_box_train
└── query

```

### Training

Download the datasets and put them into the right place.
Check and run the shell script `train.sh`:

```bash
CUDA_VISIBLE_DEVICES=0 ./train.sh # run on GPU 0
```

### Evaluation

You can run evaluation on any datasets with model weight provided.

```bash
CUDA_VISIBLE_DEVICES=0 python evaluate.py --weight /path/to/model/weight.pth # run on GPU 0
```

## Performance

![perf](assets/perf.png)

### Supervised ReID

##### Market-1501
| Model         | Image Size|Paper | Download |
| :------:      | :------: |:------: |:------: |
| Resnet50      | 384*128 |88.9/95.8 |[model](https://drive.google.com/drive/folders/1boQ_TMP--TCVJydOOmggkMZDwCTS5CL-?usp=drive_link) / [log](https://drive.google.com/drive/folders/1boQ_TMP--TCVJydOOmggkMZDwCTS5CL-?usp=drive_link)|

##### MSMT17
| Model         | Image Size|Paper | Download |
| :------:      | :------: |:------: |:------: |
| Resnet50      | 384*128 |51.4/78.3 |[model](https://drive.google.com/drive/folders/1qIdEnHg5wOKY-yZ7NIkZt7Vlp9ZMNM0o?usp=drive_link) / [log](https://drive.google.com/drive/folders/1qIdEnHg5wOKY-yZ7NIkZt7Vlp9ZMNM0o?usp=drive_link)|


## Acknowledgement

We would like to sincerely thank [Precise-ICS](https://github.com/Terminator8758/Precise-ICS-master), [CCL](https://github.com/alibaba/cluster-contrast-reid) and [MeanTeacher](https://github.com/CuriousAI/mean-teacher) for their insightful ideas and outstanding works!

## Citation

If you feel our work helpful in your research, please cite it like this:

```bibtex
@ARTICLE{10534060,
  author={Gong, Xun and Tan, Xuan and Xiang, Yang},
  journal={IEEE Transactions on Circuits and Systems for Video Technology}, 
  title={Contrastive Mean Teacher for Intra-camera Supervised Person Re-Identification}, 
  year={2024},
  volume={},
  number={},
  pages={1-1},
  keywords={Cameras;Pedestrians;Training;Feature extraction;Computational modeling;Lighting;Data models;Intra-camera supervision;Mean Teacher;Contrastive learning;Person re-identification},
  doi={10.1109/TCSVT.2024.3402533}}
```
