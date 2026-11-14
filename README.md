# Pet Segmentation: U-Net Experiments

An image-segmentation experiment using Pascal VOC 2012. The notebook trains and compares a baseline small U-Net with a modified U-Net whose bottleneck uses dilated convolutions.

## Experiment

- Dataset: Pascal VOC 2012 segmentation
- Input resolution: 160 x 160
- Task: foreground (pet) versus background segmentation, with unlabeled pixels ignored
- Models: baseline bottleneck dilation of 1 and modified bottleneck dilation of 2
- Evaluation: background IoU, pet IoU, mean IoU, trainable parameter count, and inference latency
- Reproducibility: the notebook sets a random seed and reports the runtime device and library versions

The notebook is the runnable source of truth; metrics and plots are produced when its cells are run and may vary with the hardware and software environment.

## Run the notebook

The notebook is designed for Google Colab and uses a GPU when available.

1. Open `Pet_Segmentation_Experiment_(1) (1).ipynb` in Google Colab.
2. Select a Python runtime (a GPU runtime is recommended).
3. Run the cells in order. The notebook downloads the Pascal VOC training data and saves model checkpoints and evaluation artifacts in the runtime.

The notebook uses PyTorch, Torchvision, NumPy, Matplotlib, and Pandas. Google Colab-specific download cells will need adjustment to run outside Colab.

## Repository contents

- `Pet_Segmentation_Experiment_(1) (1).ipynb` - data preparation, model training, evaluation, and comparison.
- `README.md` - project overview and run instructions.

Dataset files, trained checkpoints, and generated outputs are not included in this repository.
