# AttnFlow

**AttnFlow** is the official implementation of the paper:  
**Conditional Attention Guided Normalizing Flow for Low-light Image Enhancement**

## Acknowledgements

This work is built upon several excellent open-source projects. We extend our sincere gratitude to the contributors of:

- [**BasicSR**](https://github.com/xinntao/BasicSR)  
- [**Glow**](https://github.com/openai/glow)  
- [**SRFlow**](https://github.com/andreas128/SRFlow)  
- [**LLFlow**](https://github.com/wyf0912/LLFlow)


## Getting Started

### 1. Create a Conda Environment

```bash
conda create --name attnflow python=3.8
conda activate attnflow
```


### 2. Install Dependencies

```bash
cd AttnFlow
pip install -r ./code/requirements.txt
```

### 3. Download Datasets

Download the datasets from the following links:

- [LOL](https://daooshee.github.io/BMVC2018website/)
- [LOL-v2](https://github.com/flyywh/CVPR-2020-Semi-Low-Light)

### 4. Configure Paths

Modify the dataset and model paths in the config files located at `./confs/`. Update the following fields:

- `datasets.train.root`
- `datasets.val.root`
- `dataroot_unpaired`
- `dataroot_GT`
- `dataroot_LR`
- `model_path`

---

## Testing

### Paired Test

```bash
cd code
python test.py --opt ./confs/LOL-pc.yml
```

### Unpaired Test

```bash
python test_unpaired.py --opt ./confs/LOL-pc.yml -n results_folder_name
```

---

## Training

```bash
python train.py --opt ./confs/LOL-pc.yml
```
