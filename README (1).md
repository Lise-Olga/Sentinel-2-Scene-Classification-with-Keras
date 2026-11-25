# Sentinel-2 Scene Classification with Keras

Classifying Sentinel-2 images (EuroSAT) into 10 land-cover classes with TensorFlow and Keras, from a simple model to a CNN. Each step is explained for GIS and remote sensing users with ArcGIS tools: **ModelBuilder, Focal Statistics, and Aggregate**.

| My first model: Keras works like ModelBuilder | The CNN: convolution works like Focal Statistics |
|:-:|:-:|
| ![ModelBuilder vs Keras](images/modelbuilder_vs_keras.png) | ![How a CNN processes a satellite image](images/cnn_diagram.png) |

## Notebooks

| | Notebook | Model | Test accuracy | Article |
|:-:|---|---|:-:|:-:|
| **01** | [**My first model with TensorFlow**](01_tensorflow_first_model/01_tensorflow_first_model_eurosat.ipynb)<br><sub>The 5 steps of a Keras model: load, build, compile, train, evaluate</sub> | Flatten + Dense | **47%** | [📖 Read](link) |
| **02** | [**A CNN on Sentinel-2 Images**](02_cnn/02_cnn_eurosat.ipynb)<br><sub>Convolution and pooling, explained with Focal Statistics and Aggregate</sub> | Conv2D + MaxPooling | **80%** | *Coming soon* |

With 10 classes, guessing gives 10%. The CNN recognizes water, buildings, and forests well (94–97%), but vegetation classes remain harder (57–78%).

## How to run

1. Install the libraries: `pip install -r requirements.txt`
2. Open the notebooks in **Jupyter** and run the cells from top to bottom.
3. Run notebook **01** first: it downloads the EuroSAT data from [Zenodo](https://zenodo.org/records/7711810) (about 95 MB).

## References

- TensorFlow tutorials: [beginner quickstart](https://www.tensorflow.org/tutorials/quickstart/beginner) and [CNN](https://www.tensorflow.org/tutorials/images/cnn)
- Helber, P., Bischke, B., Dengel, A., & Borth, D. (2019). EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use and Land Cover Classification. *IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing*, 12(7), 2217–2226.

## Author

**Lise Olga Makonga**, M.S. student in Geography and Geospatial Sciences, South Dakota State University.
