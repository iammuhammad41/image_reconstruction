# CT Segmentation & 3D Reconstruction

A lightweight PyTorch pipeline for  
1. 2D semantic segmentation of lung/infection regions in COVID-19 CT scans (U-Net / ResNeXt-U-Net),  
2. Interactive 3D volume rendering with VTK.

## ⚙️ Installation

```bash
git clone https://github.com/you/covid19-seg-3d.git
cd covid19-seg-3d
conda create -n covid19 python=3.8 -y
conda activate covid19
pip install -r requirements.txt
````

## 🚀 Quick Start

1. **Train segmentation**

   ```bash
   python src/train.py --metadata data/metadata.csv --model unet
   ```
2. **Reconstruct & render**

   ```bash
   python src/reconstruct.py \
     --ct-volume data/ct.nii.gz \
     --mask-volume data/mask.nii.gz
   ```

## 📂 Structure

```
src/             # code for dataset, models, training, reconstruction  
data/            # metadata.csv + NIfTI CT & mask volumes  
outputs/         # checkpoints & screenshots  
```
```
