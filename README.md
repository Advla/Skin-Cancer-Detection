# Skin-Cancer-Detection
An attempt to classify skin lesions from the HAM10000 Dataset, using CNNs (Transfer learning on DenseNet201).

Massive Class imbalance (See Data Exploration notebook) was handled using a weighted loss function.

Image preprocessing techniques tested:
- DullRazor algorithm (Hair removal through filtering techniques)
- Otsu's thresholding + Convex Hull (some images contained holes and led to bad segmentation results)

Then we tested the influence of those techniques on the performance of the model.
We found that classification was significantly better (across all metrics used) with DullRazor algorithm.

Then we moved on to test the influence of a simple segmentation technique (Otsu's Thresholding) with DullRazor algorithm applied.
