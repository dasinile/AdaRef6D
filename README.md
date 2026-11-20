# AdaRef6D
## Dependencies

```bash
conda create --name AdaRef6D python=3.10.12
conda activate AdaRef6D
pip install torch==2.2.0 torchvision==0.17.0 --index-url https://download.pytorch.org/whl/cu118  # use the correct version of cuda for your system
pip install mmcv==2.2.0 -f https://download.openmmlab.com/mmcv/dist/cu118/torch2.2/index.html # change cuda version if necessary

# Other required packages
pip install -r requirements.txt

# install bop toolkit for evaluation
cd third_party/bop_toolkit
pip install .[eval_gpu]
cd -

# build pointnet2 extension
cd core/AdaRef6D/model/pointnet2/
pip install -e .
cd -

# Install Detectron2 & PyTorch3D
pip install "git+https://github.com/facebookresearch/detectron2.git"
pip install "git+https://github.com/facebookresearch/pytorch3d.git"

# Create output directory
mkdir output
```

## Datasets

Please refer to [UnoPose](https://github.com/shanice-l/UNOPose) for instructions on downloading the dataset files.

## Checkpoints

**Download DINOv2 checkpoint:** Download `'timm_vit_base_patch14_reg4_dinov2_lvd142m.pth'` and place it in `checkpoints/`:

```bash
# export HF_ENDPOINT="https://hf-mirror.com"  # if huggingface.co is not accessible
python core/AdaRef6D/scripts/download_and_save_dinov2_ckpt.py
```

**Download AdaRef6D checkpoint:** .

## Reproduce the results

**Eval**

```bash

```


**Training**

```bash

```


## Acknowledgments

This work is based on [UnoPose](https://github.com/shanice-l/UNOPose). We thank the authors for their insightful work.
