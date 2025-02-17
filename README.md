# gan-anime-sceneries
A FastGAN architecture for unconditional image creation.
This project is based on the research outlined in the paper "Towards Faster and Stabilized GAN Training for High-fidelity Few-shot Image Synthesis". The original paper can be found at [original paper](https://arxiv.org/abs/2101.04775). 

The model was trained using the FastGAN implementation from the [parent FastGAN Repository](https://github.com/odegeasslbc/FastGAN-pytorch/tree/main).

## Dataset:
The dataset used in this project is available on the Hugging Face dataset hub at the following link: [anime-sceneries](https://huggingface.co/datasets/sulpha/anime-sceneries). Users can download the dataset from the link and use it in their own projects. Alternatively, users can download the dataset using the following code:
```py
from datasets import load_dataset

dataset = load_dataset("sulpha/anime-sceneries")
```

## Training:
The model was trained for 8 hours on a P100 GPU. *(See parent repository for training details)*.

## Usage:
The model weights can be downloaded from [here](https://drive.google.com/file/d/1B9P5BhD4fnbsFYYZOTGhB5yghShiE66I/view?usp=sharing)
Download the weights to the same root directory as ```eval.py```

Example execution:
```
python eval.py --n_sample 2
```
where the n_samples is the number of images to be generated (>1 only). The script is modified to run on CPU *only*.

![rec_40000](https://github.com/user-attachments/assets/e50252fa-c68b-4b5b-986d-2e84b50579d4)

