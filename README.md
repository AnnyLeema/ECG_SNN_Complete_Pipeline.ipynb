[Uploading README.md…]()
# ECG image classification with a polarity-preserving, lead-aware spiking neural network

Code for the manuscript *Polarity-Preserving Spike Encoding and a Lead-Aware Spiking Neural Network for ECG Image Classification: Cross-Validated Evaluation on a Duplicate-Free Benchmark*.

## Files
| File | Content |
|---|---|
| `ECG_SNN_Extra_Experiments (3).ipynb` | Executed Google Colab notebook (with outputs): set-up, de-duplication, 5-fold cross-validation on 491 distinct images, mixed training with rendered PTB-XL images, S1+ (distillation) experiment and the matched-ANN control |
| `extra_results_cv.zip` | Cross-validation results (predictions and metrics, no model weights) |
| `extra_results_1.zip` | Mixed-training results with PTB-XL images |
| `plus_results.zip` | S1+ experiment results |
| `LICENSE` | MIT licence (code) |

## How to run
1. Open the notebook in Google Colab, choose Runtime > Change runtime type > T4 GPU.
2. Run the cells from top to bottom. Long cells are resumable; a Colab reset deletes the disk, so download the zip files.

## Data
- ECG images: Kaggle `kanishkarathore1604/ecg-image` (CC BY-NC 4.0). Downloaded at run time; not redistributed here. The set contains 3,951 files, of which 491 are distinct after removing byte-identical copies.
- PTB-XL (CC BY 4.0): https://doi.org/10.13026/kfzx-aw45

## Notes
- Energy values are estimates from operation counts (45 nm, E_MAC = 4.6 pJ, E_AC = 0.9 pJ), not hardware measurements.
- Results vary slightly between runs because the augmentation random numbers are not seeded.
- Research prototype; not a medical device.
