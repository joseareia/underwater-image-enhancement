# Underwater Image Enhancement

---

<p align="center">
    <img src="Assets/CIIC-FCT.png" width="75%"/>
</p>

---

This repository stores the work made to explores image enhancement methods for underwater imagery.

## Repository Structure
```
underwater-image-enhancement/  
│  
├── 🎨 Assets/                  # Logos and other visual assets  
├── 📓 Notebooks/               # Jupyter notebooks implementing the algorithms  
├── 🧪 Results/                 # Output imagery from tested algorithms  
├── 🙈 .gitignore               # Git ignore file  
├── ⚙️ .gitattributes           # Git attributes file  
├── 📜 README.md                # Project documentation  
├── 🛠️ requirements.txt         # Project dependencies 
```

## Image Enhancement

Image enhancement techniques are used to improve the quality of underwater images, which are often degraded by scattering and absorption effects. These techniques can be broadly categorised into two groups: classical image enhancement algorithms and deep learning-based models.

Classical algorithms are often based on Retinex theory, which aims to restore an image’s original colours by separating its illumination and reflectance components. In contrast, deep learning-based models leverage convolutional neural networks to enhance underwater images.

We evaluate the performance of four image enhancement algorithms using our underwater image dataset, captured in Leixões Bay, Portugal.

### Tested Models

| Model      | Description                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| **MSRCP**  | An image enhancement algorithm that combines multi-scale Retinex processing with colour priors. It effectively improves illumination and colour balance.  |
| **MSRCR**  | A multi-scale Retinex-based method focused on colour restoration. It enhances colour fidelity and sharpness, making it suitable for various applications. |
| **UWCNN**  | A convolutional neural network-based model for enhancing underwater colour images. It leverages deep learning to improve image quality and visibility in underwater environments.  |
| **Waternet**| A deep learning-based model designed to counter underwater image degradation caused by scattering and low light, producing clearer and more visually appealing images. |


### Table of Performance Metrics for Image Enhancement Algorithms

| Model         | UIQM $\uparrow$       | UCIQE $\uparrow$      | CCF $\downarrow$      |
|---------------|-----------------------|-----------------------|-----------------------|
| Original      | 0.40 $\pm$ 0.66       | 18.06 $\pm$ 3.39      | 0.75 $\pm$ 0.30       | 
| **MSRCP**     | **6.56 $\pm$ 1.36**   | 29.30 $\pm$ 0.38      | **0.93 $\pm$ 0.26**   | 
| **MSRCR**     | 6.20 $\pm$ 1.22       | **30.14 $\pm$ 0.50**  | 1.95 $\pm$ 0.11       | 
| **UWCNN**     | 1.74 $\pm$ 0.70       | 22.51 $\pm$ 3.11      | 1.11 $\pm$ 0.36       |
| **Waternet**  | 2.13 $\pm$ 0.68       | 25.32 $\pm$ 0.94      | 1.95 $\pm$ 0.10       |

- **UIQM** (Universal Image Quality Metric).
- **UCIQE** (Universal Color Image Quality Evaluation).
- **CCF** (Colorfulness, Contrast, and Fog Density).

### Key Takeaways

**Quantitative Evaluation (Performance Metrics)**
- MSRCR achieves the best performance in terms of UCIQE and CCF.
- MSRCP performs best in terms of UIQM.
- UWCNN has the worst performance in both UIQM and UCIQE.
- WaterNet and MSRCP demonstrates competitive performance in UCIQE.

**Qualitative Evaluation**
- MSRCP struggles with colour restoration.
- WaterNet produces images that appear more natural and visually appealing.
- UWCNN generates images that lack sharpness and colour fidelity.

## Acknowledgements
This work is partially funded by [FCT - Fundação para a Ciência e a Tecnologia](https://www.fct.pt), I.P., through projects MIT-EXPL/ACC/0057/2021 and UIDB/04524/2020, and under the Scientific Employment Stimulus - Institutional Call - CEE/CINST/00051/2018.
