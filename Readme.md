<img src="https://github.com/chaidosa/AI-535-Final-Project/blob/main/col_sim.gif?raw=true" width="800">


##  Setup

### Prepare Environment
```
conda create -n seine python==3.9.16
conda activate seine
pip install -r requirement.txt
```

### Download SEINE model and T2I base model

Our model is based on Stable diffusion v1.4, you may download [Stable Diffusion v1-4](https://huggingface.co/CompVis/stable-diffusion-v1-4) to the director of ``` pretrained ```
.
Download our model checkpoint (from [google drive](https://drive.google.com/drive/folders/1cWfeDzKJhpb0m6HA5DoMOH0_ItuUY95b?usp=sharing) or [hugging face](https://huggingface.co/xinyuanc91/SEINE/tree/main)) and save to the directory of ```pretrained```


Now under `./pretrained`, you should be able to see the following:
```
├── pretrained
│   ├── seine.pt or checkpoints after training 
│   ├── stable-diffusion-v1-4
│   │   ├── ...
└── └── ├── ...
        ├── ...
```
## Usage
### Inference for Collsion
Run the following command to get the I2V results:
```python
python sample_scripts/with_mask_sample.py --config configs/collision.yaml
```
The generated video will be saved in ```./results/collsion```.

