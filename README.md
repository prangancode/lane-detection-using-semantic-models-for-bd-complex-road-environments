# Enhancing Lane Detection in Autonomous Driving: A Comparative Study of Semantic Segmentation Models in Challenging Environments

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19431573.svg)](https://doi.org/10.5281/zenodo.19431573)
[![Dataset: Kaggle](https://img.shields.io/badge/Dataset-RSUD20K-blue.svg)](https://www.kaggle.com/datasets/hasibzunair/rsud20k-bangladesh-road-scene-understanding)

This repository contains the official open-source code, implementation details, and evaluation scripts for our manuscript submitted to *The Visual Computer*. It provides a comprehensive comparative analysis of six semantic segmentation models optimized for lane detection under the complex, non-standardized road scenarios characteristic of Bangladesh.

## 📌 Related Publication & Citation
**This code is directly related to our manuscript currently under review at *The Visual Computer*.** To enhance transparency and reproducibility, all experimental setups are provided here. If you utilize this code, the key algorithmic implementations, or our evaluation framework in your research, we strongly encourage you to cite our work:

> Sen, P., Dey, S., Sakib, S., Akhter, K. T., Hasib, M., & Chowdhury, M. R. (2026). "Enhancing Lane Detection in Autonomous Driving: A Comparative Study of Semantic Segmentation Models in Challenging Environments." *The Visual Computer* (Under Review).

---

## 📂 Repository Structure
The codebase is structured into self-contained Jupyter Notebooks to ensure that each model's pipeline (data loading, training, evaluation, and visualization) is transparent, distinct, and easily reproducible.

* `UNet_CustomUNet_lane_detection.ipynb`: Implementation of the baseline U-Net alongside our highly accurate **Custom U-Net** architecture.
* `FCN_lane_detection.ipynb`: Implementation of the **FCN-ResNet50** model, optimized for a balance of accuracy and rapid inference time.
* `Deeplabv3_lane_detection.ipynb`: Implementation of the DeepLabV3+ model utilizing atrous spatial pyramid pooling.
* `SegNet_lane_detection.ipynb`: Implementation of the SegNet encoder-decoder architecture.
* `YOLOP_lane_detection.ipynb`: Implementation and fine-tuning of the YOLOP model for panoptic driving perception.
* `Utilities.ipynb`: Comprehensive usage guidelines and helper functions for data preprocessing, augmentation, mask generation, and calculating evaluation metrics (Accuracy, F1-score, IoU).
* `Model_graphs_&_visualization.ipynb`: Scripts for replicating the experimental results, generating performance comparison graphs, and outputting visual semantic masks.

---

## 📊 Dataset: RSUD20K
The models were trained and evaluated on the **RSUD20K Dataset**, a custom dataset specifically designed to capture the unique challenges of Bangladeshi road environments (non-standardized markings, narrow roads, frequent obstructions, and adverse weather).

* **Access the Dataset:** The official dataset is publicly available on Kaggle: [RSUD20K Bangladesh Road Scene Understanding](https://www.kaggle.com/datasets/hasibzunair/rsud20k-bangladesh-road-scene-understanding)
* **Setup:** Download the dataset from Kaggle and extract it into a local `data/` directory. Ensure the directory structure matches the paths specified in the `Utilities.ipynb` notebook before running the model training scripts.

---

## ⚙️ Dependencies and Requirements
To replicate these experiments, ensure your environment meets the following requirements. 

**Prerequisites:**
* Python 3.8+
* Jupyter Notebook or JupyterLab
* CUDA-enabled GPU (Highly Recommended for training)

**Core Libraries:**
You can install the necessary dependencies via pip:
```bash
pip install torch torchvision torchaudio
pip install opencv-python matplotlib numpy pandas scikit-learn
pip install jupyterlab
