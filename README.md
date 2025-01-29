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


## NVIDIA Jetson Orin Nano Super

```bash
sudo apt install nvidia-jetpack
sudo apt-get install firefox
sudo apt-get -y update
sudo apt-get install -y  python3-pip libopenblas-dev;
wget raw.githubusercontent.com/pytorch/pytorch/5c6af2b583709f6176898c017424dc9981023c28/.ci/docker/
common/install_cusparselt.sh
export CUDA_VERSION=12.6
bash ./install_cusparselt.sh
wget https://developer.download.nvidia.com/compute/cusparselt/0.6.3/local_installers/cusparselt-local-tegra-repo-ubuntu2204-0.6.3_1.0-1_arm64.deb
sudo dpkg -i cusparselt-local-tegra-repo-ubuntu2204-0.6.3_1.0-1_arm64.deb
sudo cp /var/cusparselt-local-tegra-repo-ubuntu2204-0.6.3/cusparselt-*-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt-get -y install libcusparselt0 libcusparselt-dev
sudo apt-get install libjpeg-dev libpng-dev libtiff-dev
sudo apt-get install ffmpeg libavutil-dev libavcodec-dev libavformat-dev libavdevice-dev libavfilter-dev libswscale-dev libswresample-dev libswresample-dev libpostproc-dev libjpeg-dev libpng-dev
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/190/d8dfbcf6c4d3c/cupy-14.0.0a1-cp310-cp310-linux_aarch64.whl#sha256=190d8dfbcf6c4d3cda21c7e0a973fc20385fa02e75266456851b48fd15eddae8
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/b60/b3dacbcbf4ab4/cuda_python-12.6.0+0.gb9f40f6.dirty-cp310-cp310-linux_aarch64.whl#sha256=b60b3dacbcbf4ab4391428d33a04aabdf7f7a53a6707a27afca85b453895a02f
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/7a1/7ce289f62d4c2/xformers-0.0.30+56be3b5.d20241230-cp310-cp310-linux_aarch64.whl#sha256=7a17ce289f62d4c28b7707eaf334c65dff39a18f8f184502e1693b961dbad0b2
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/97d/e894e562ead63/pycuda-2024.1.2-cp310-cp310-linux_aarch64.whl#sha256=97de894e562ead63d6fa3aa79d4c947ed7cd9fd75cc8920b712475cc6ff69b7f
pip install http://jetson.webredirect.org/jp6/cu126/+f/5cf/9ed17e35cb752/torch-2.5.0-cp310-cp310-linux_aarch64.whl#sha256=5cf9ed17e35cb7523812aeda9e7d6353c437048c5a6df1dc6617650333049092
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/77c/71332142a20e2/flash_attn-2.7.2.post1-cp310-cp310-linux_aarch64.whl#sha256=77c71332142a20e2e0f20fd54251d530cab544a9ae66ffbe2e0b8eee48484832
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/0c4/18beb3326027d/onnxruntime_gpu-1.20.0-cp310-cp310-linux_aarch64.whl#sha256=0c418beb3326027d83acc283372ae42ebe9df12f71c3a8c2e9743a4e323443a4
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/5f9/67f920de3953f/torchvision-0.20.0-cp310-cp310-linux_aarch64.whl#sha256=5f967f920de3953f2a39d95154b1feffd5ccc06b4589e51540dc070021a9adb9
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/ad5/16a450009ac2e/bitsandbytes-0.45.0-cp310-cp310-linux_aarch64.whl#sha256=ad516a450009ac2e80077ef04cd5bc1c0c204ca09273e6dd07b4b97e9a7d5e3b
sudo apt-get install -y build-essential python3-dev python3-setuptools make cmake
sudo apt-get install -y ffmpeg libavcodec-dev libavfilter-dev libavformat-dev libavutil-dev
pip install timm transformers accelerate --upgrade
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/366/1e00f6d836491/opencv_python-4.10.0-py3-none-any.whl#sha256=3661e00f6d836491b4fdad8ea04bc56999c21345a8dcd5a6eb11c662e6c86f3d
pip install https://pypi.jetson-ai-lab.dev/jp6/cu126/+f/bea/77ef3f9923c70/opencv_contrib_python-4.10.0+6b45caa-cp310-cp310-linux_aarch64.whl#sha256=bea77ef3f9923c708f6f38e85b615ae9b4fc775de9b765f3b42355d7ef5e8e0c
```
