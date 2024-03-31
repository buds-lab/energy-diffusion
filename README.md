# Creating synthetic energy meter data using conditional diffusion and building metadata

This repository contains all the necessary datasets and Jupyter notebooks used in our research, "Creating synthetic energy meter data using conditional diffusion and building metadata". 

## Research Abstract

Advances in machine learning and increased computational power have driven progress in energy-related research. However, limited access to private energy data from buildings hinders traditional regression models relying on historical data. While generative models offer a solution, previous studies have primarily focused on short-term generation periods (e.g., daily profiles) and a limited number of meters. Thus, the study proposes a conditional diffusion model for generating high-quality synthetic energy data using relevant metadata. Using a dataset comprising 1,828 power meters from various buildings and countries, this model is compared with traditional methods like Conditional Generative Adversarial Networks (CGAN) and Conditional Variational Auto-Encoders (CVAE). It explicitly handles long-term annual consumption profiles, harnessing metadata such as location, weather, building, and meter type to produce coherent synthetic data that closely resembles real-world energy consumption patterns. The results demonstrate the proposed diffusion model's superior performance, with a 36\% reduction in Fr'echet Inception Distance (FID) score and a 13\% decrease in Kullback-Leibler divergence (KL divergence) compared to the following best method. The proposed method successfully generates high-quality energy data through metadata, and its code will be open-sourced, establishing a foundation for a broader array of energy data generation models in the future.

![Research Concept](https://github.com/buds-lab/energy-diffusion/blob/main/research_concept.jpg)

## Proposed conditional diffusion model

Original 1D time series energy data were reshaped into 2D data to capture weekly usage patterns and then integrated into the image-based generative model.
![Diffusion model](https://github.com/buds-lab/energy-diffusion/blob/main/reshaping_illustration.jpg)

We introduce an advanced conditional diffusion Mmodel tailored for synthesizing high-quality, long-term energy data. This model employs a context-dependent U-Net architecture to incorporate metadata about energy consumption patterns. Further enhancing its capabilities, a time-embedding layer is integrated to capture the temporal dependencies prevalent in energy data. Our conditional diffusion model starts with a noise base and progressively denoises it into realistic energy data, which are aligned with encoded metadata attributes. This dual capability of maintaining data integrity while factoring in rich contextual and temporal information makes it particularly well-suited for handling complex but structured energy datasets.
![Diffusion model](https://github.com/buds-lab/energy-diffusion/blob/main/diffusion_illustration.jpg)

## Repository Content

This repository is organized as follows:

1. **Notebooks**: This directory contains all Jupyter notebooks that provide the code implementations of the various techniques used in the research.

2. **Data**: Due to the constraints posed by the Github platform, the dataset used in our research is not provided here. Nevertheless, the energy dataset (including meter data, metadata, and weather data) could be found on [BDG2 Github repository](https://github.com/buds-lab/building-data-genome-project-2).

## License

This project is licensed under the terms of the MIT license.
