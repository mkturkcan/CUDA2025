# CUDA 2025
Installation instructions for Pytorch+CUDA for 2025 January.

## Linux (RTX 4090/5090)

### Pruning-Capable Environment
```bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
source ~/miniconda3/bin/activate
conda init --all
conda create -n ai python=3.11
conda activate ai
conda install cuda-toolkit=12.6 -c pytorch -c nvidia
pip3 install torch torchvision torchaudio
pip install transformers==4.46.2 accelerate==1.1.1 datasets torch-pruning==1.5.1
```

### Training Environment
```bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
source ~/miniconda3/bin/activate
conda init --all
conda create -n ai python=3.11
conda activate ai
conda install cuda-toolkit=12.6 -c pytorch -c nvidia
pip3 install torch torchvision torchaudio
pip install transformers accelerate datasets
```

## Windows (RTX 4090/5090)


## NVIDIA Jetson Nano Super

