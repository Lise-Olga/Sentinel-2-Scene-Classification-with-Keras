# Sentinel-2 Scene Classification with Keras
**Classifying Sentinel-2 images (EuroSAT) into 10 land-cover classes with TensorFlow and Keras. Each notebook adapts an official TensorFlow tutorial to satellite images, and explains the concepts for GIS and remote sensing users through ArcGIS tools (rasters, ModelBuilder, Focal Statistics).**

## Notebook
| | Notebook | Model | Test accuracy | Article |
|:-:|---|---|:-:|:-:|
| **01** | [**My first model with TensorFlow**](01_tensorflow_first_model/01_tensorflow_first_model_eurosat.ipynb)<br><sub>The 5 steps of a Keras model: load, build, compile, train, evaluate</sub> | Flatten + Dense | **47%** | [📖 Read](link) |

## Data
All notebooks use EuroSAT (RGB): 27,000 Sentinel-2 images of 64 × 64 pixels, with 10 land-cover classes.
The notebooks download it automatically from Zenodo (about 95 MB).
The data is not stored in this repository.

## How to run
1. Install Python 3.10 or newer.
2. Install the libraries:
```
   pip install -r requirements.txt
   ```
3. Open a notebook in Jupyter and run the cells from top to bottom.
Training runs on a normal computer (CPU). A GPU makes it faster.

## References
- TensorFlow 2 quickstart for beginners: https://www.tensorflow.org/tutorials/quickstart/beginner
- Helber, P., Bischke, B., Dengel, A., & Borth, D. (2019). EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use and Land Cover Classification. IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing, 12(7), 2217–2226.

## Author
Lise Olga Makonga, M.S. student in Geography and Geospatial Sciences.
