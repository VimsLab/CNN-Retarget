# Feature-Map-Retargeting
Official TensorFlow implementation for [Feature Map Retargeting to Classify Biomedical Journal Figures
](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8635419/). The code has been implemented and tested on the Ubuntu operating system only.

![Alt text](docs/Overview.jpg?raw=true)

## Setup
First, install the [CUDA Toolkit](https://developer.nvidia.com/cuda-toolkit) and the [cuDNN library](https://developer.nvidia.com/rdp/cudnn-archive) matching the version of your Ubuntu operating system. Installation of the [Anaconda Python Distribution](https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh) is required as well. We recommend installing CUDA10.1. Then find the TensorFlow version compatible with your CUDA version [here](https://www.tensorflow.org/install/source#gpu).

Then, run the following commands:
```
conda env create -f config/enviroment.yml
conda activate Retarget
conda install -c conda-forge cudatoolkit=10.1 cudnn=7.6.0
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/
pip install --upgrade pip
pip install tensorflow-gpu==2.2.0
```

## Dataset
Visit the [ImageCLEF2013](https://www.imageclef.org/2013), [ImageCLEF2015](https://www.imageclef.org/2015), and [ImageCLEF2016](https://www.imageclef.org/2016) websites to register and download the datasets.

The datasets follow the directory structure below:
```
├── datasets
│   ├── ImageCLEF13
│   |   ├── train
│   |   ├── test
│   ├── ImageCLEF15
│   ├── ImageCLEF16
```

## Train
```
python train.py
```

## Test
```
python test.py
```
