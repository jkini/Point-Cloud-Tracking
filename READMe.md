## Installations
```
cuda-11.0
cmake-3.7.2-gcc-6.2.0
pytorch==1.7.1 
torchvision==0.8.2 
torchaudio==0.7.2 
numpy==1.20.3 
open3d==0.9.0.0 
einops==0.3.2 
scikit-learn==1.0.1 
compressai 
argparse
tensorboard
```

## Data Preparation
Download images, annotations, oxts and calibration information from <a href="http://www.cvlibs.net/datasets/kitti/eval_tracking.php">KITTI Tracking website</a>

Run kitti2coco.py in scripts to convert the annotation into COCO format.
```
python scripts/kitti2coco.py
```
It will create tracking_subval_mini.json, tracking_subval.json, tracking_train.json, tracking_subtrain.json, tracking_test.json and similar files with prefix detection- under data/KITTI/anns.


## Training
```
./scripts/train.sh
```

## Testing
```
./scripts/test_eval_exp.sh kitti
