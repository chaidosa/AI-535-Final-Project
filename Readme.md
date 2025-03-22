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
│   ├── seine.pt
│   ├── stable-diffusion-v1-4
│   │   ├── ...
└── └── ├── ...
        ├── ...
```
## Usage
### Inference for I2V 
Run the following command to get the I2V results:
```python
python sample_scripts/with_mask_sample.py --config configs/sample_i2v.yaml
```
The generated video will be saved in ```./results/i2v```.

#### More Details
You may modify ```./configs/sample_i2v.yaml``` to change the generation conditions.
For example:

```ckpt``` is used to specify a model checkpoint.

```text_prompt``` is used to describe the content of the video.

```input_path``` is used to specify the path to the image.

### Inference for Transition
```python
python sample_scripts/with_mask_sample.py --config configs/sample_transition.yaml
```
The generated video will be saved in ```./results/transition```.
