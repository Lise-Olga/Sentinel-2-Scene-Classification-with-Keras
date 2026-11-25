# Sentinel-2 Scene Classification with Keras

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Data](https://img.shields.io/badge/Data-Sentinel--2%20EuroSAT-green)
![Level](https://img.shields.io/badge/Level-Beginner-lightgrey)

Land-cover classification of Sentinel-2 images (EuroSAT) with TensorFlow and Keras: from a simple Dense model (**47%**) to a CNN (**80%**), explained for GIS and remote sensing users.

Each notebook adapts an official TensorFlow tutorial to satellite images and explains every step with tools GIS users already know: **rasters, ModelBuilder, Focal Statistics, and Aggregate**.

![ModelBuilder vs Keras](images/modelbuilder_vs_keras.png)

## What you will learn

- The five steps of every Keras model: **load, build, compile, train, evaluate**
- Why a tensor is a stack of rasters, and Keras works like ModelBuilder
- Why a model can run without errors and still learn nothing (and how to fix it)
- How a convolution works like **Focal Statistics that learns**, and pooling like **Aggregate**
- How to read training curves and spot **overfitting**

## Notebooks

| | Notebook | Model | Test accuracy | Run | Article |
|:-:|---|---|:-:|:-:|:-:|
| **01** | [**My first model with TensorFlow**](01_tensorflow_first_model/01_tensorflow_first_model_eurosat.ipynb)<br><sub>The 5 steps of a Keras model: load, build, compile, train, evaluate</sub> | Flatten + Dense | **47%** | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lise-Olga/Sentinel-2-Scene-Classification-with-Keras/blob/main/01_tensorflow_first_model/01_tensorflow_first_model_eurosat.ipynb) | [📖 Read](link) |
| **02** | [**A CNN on Sentinel-2 Images**](02_cnn/02_cnn_eurosat.ipynb)<br><sub>Convolution and pooling, explained with Focal Statistics and Aggregate</sub> | Conv2D + MaxPooling | **80%** | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lise-Olga/Sentinel-2-Scene-Classification-with-Keras/blob/main/02_cnn/02_cnn_eurosat.ipynb) | *Coming soon* |

## Results

The CNN reached **80%** accuracy on 5,400 test images (chance: 10%). Water, buildings, and forests are easy to recognize. Vegetation classes are harder, because they look alike in red, green, and blue at 10 m.

| How the CNN works | Accuracy by class |
|:-:|:-:|
| ![How a CNN processes a satellite image](images/cnn_diagram.png) | ![Test accuracy by class](images/class_accuracy_cnn.png) |

## Data

**EuroSAT (RGB)**: 27,000 Sentinel-2 images of 64 × 64 pixels, in 10 land-cover classes (AnnualCrop, Forest, HerbaceousVegetation, Highway, Industrial, Pasture, PermanentCrop, Residential, River, SeaLake).

Notebook 01 downloads it from [Zenodo](https://zenodo.org/records/7711810) (about 95 MB) into a folder called `eurosat_data`. Notebook 02 uses the same folder. The data is not stored in this repository.

## How to run

**Option 1: in your browser (nothing to install).** Click an **Open in Colab** button in the table above. Notebook 01 downloads the data by itself. In Colab, each notebook runs separately, so for notebook 02, first copy and run the download cell of notebook 01 (section 2).

**Option 2: on your computer.**

1. Install Python 3.10 or newer.
2. Install the libraries:
   ```
   pip install -r requirements.txt
   ```
3. Run notebook 01 first (it downloads the data), then notebook 02.
4. In each notebook, run the cells **from top to bottom**.

Training runs on a normal computer (CPU). A GPU makes it faster.

## Repository structure

```
├── 01_tensorflow_first_model/   Notebook 01: Flatten + Dense model
├── 02_cnn/                      Notebook 02: CNN
├── images/                      Diagrams and figures
├── requirements.txt             Libraries to install
└── README.md
```

## Next steps

- [ ] Stop training at the best epoch (EarlyStopping)
- [ ] Reduce overfitting with data augmentation (flips and rotations)
- [ ] Add near-infrared and red-edge bands (EuroSAT multispectral) to separate vegetation classes

## References

- TensorFlow 2 quickstart for beginners: https://www.tensorflow.org/tutorials/quickstart/beginner
- TensorFlow CNN tutorial: https://www.tensorflow.org/tutorials/images/cnn
- Helber, P., Bischke, B., Dengel, A., & Borth, D. (2019). EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use and Land Cover Classification. *IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing*, 12(7), 2217–2226.

## Author

**Lise Olga Makonga**, M.S. student in Geography and Geospatial Sciences, South Dakota State University.
GIS and remote sensing, learning deep learning one notebook at a time.
