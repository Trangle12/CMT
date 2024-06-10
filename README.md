# Contrastive Mean Teacher for Intra-camera Supervised Person Re-Identification (CMT)

<!-- The code will be available soon. -->

Official implementation of paper [Contrastive Mean Teacher for Intra-camera Supervised Person Re-Identification](https://ieeexplore.ieee.org/document/10534060) (TCSVT 2024).

![pipeline](assets/pipeline.jpg)


### Installation

Clone this repo and extract the files.

We recommand `conda` to create a virtual Python 3.7 environment and install all requirements in it. Extra packages are listed in `requirements.txt` and can be installed by `pip`:

```bash
conda create -n torch1.6 python=3.7
conda activate torch1.6

pip install -r requirements.txt
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
