# Underwater Image Improvement

---

<p align="center">
    <img src="Assets/CIIC-FCT.png" width="75%"/>
</p>

---

This repository stores the preliminary work made to explores image enhancement methods for underwater imagery. 

## 1. Image Enhancement

Image enhancement techniques are used to improve the quality of underwater images, which are often degraded by scattering and absorption effects. These techniques can be broadly categorised into two groups: classical image enhancement algorithms and deep learning-based models.

Classical algorithms are often based on Retinex theory, which aims to restore an image’s original colours by separating its illumination and reflectance components. In contrast, deep learning-based models leverage convolutional neural networks to enhance underwater images.

We evaluate the performance of four image enhancement algorithms using our underwater image dataset, captured in Leixões Bay, Portugal.

### 1.1. Tested Models

| Model      | Description                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| **MSRCP**  | An image enhancement algorithm that combines multi-scale Retinex processing with colour priors. It effectively improves illumination and colour balance.  |
| **MSRCR**  | A multi-scale Retinex-based method focused on colour restoration. It enhances colour fidelity and sharpness, making it suitable for various applications. |
| **UWCNN**  | A convolutional neural network-based model for enhancing underwater colour images. It leverages deep learning to improve image quality and visibility in underwater environments.  |
| **Waternet**| A deep learning-based model designed to counter underwater image degradation caused by scattering and low light, producing clearer and more visually appealing images. |


### 1.2. Table of Performance Metrics for Image Enhancement Algorithms

| Model         | UIQM                  | UCIQE                 |
|---------------|-----------------------|-----------------------|
| Original      | 0.75 $\pm$ 0.66       | 18.06 $\pm$ 3.39      | 
| **MSRCP**     | **6.56 $\pm$ 1.36**   | 29.30 $\pm$ 0.38      | 
| **MSRCR**     | 6.20 $\pm$ 1.22       | **30.14 $\pm$ 0.50**  | 
| **UWCNN**     | 1.74 $\pm$ 0.70       | 22.51 $\pm$ 3.11      | 
| **Waternet**  | 2.13 $\pm$ 0.68       | 25.32 $\pm$ 0.94      |

- **UIQM** (Universal Image Quality Metric).
- **UCIQE** (Universal Color Image Quality Evaluation) 

### 1.3. Key Takeaways

**Quantitative Evaluation (Performance Metrics)**
- MSRCR achieves the best performance in terms of UCIQE.
- MSRCP performs best in terms of UIQM.
- UWCNN has the worst performance in both UIQM and UCIQE.
- WaterNet demonstrates competitive performance in UCIQE.

**Qualitative Evaluation**
- MSRCP struggles with colour restoration.
- WaterNet produces images that appear more natural and visually appealing.
- UWCNN generates images that lack sharpness and colour fidelity.

## Acknowledgements
This work is partially funded by [FCT - Fundação para a Ciência e a Tecnologia](https://www.fct.pt), I.P., through projects MIT-EXPL/ACC/0057/2021 and UIDB/04524/2020, and under the Scientific Employment Stimulus - Institutional Call - CEE/CINST/00051/2018.
