# AI-Maps: Geospatial Deep Learning for Urban Deprivation

Welcome to the training repository for **AI-Maps**, a framework for mapping informal settlements and urban deprivation using deep learning and Earth Observation data. This site accompanies our hands-on workshops and research documentation.

## 🎯 Objective
This training aims to bridge the gap between satellite remote sensing and socio-economic analysis. By the end of this course, participants will be able to:
- Preprocess multi-source satellite imagery using [PyTorch/GDAL/GeoPandas].
- Implement building detection and super-resolution models.
- Quantify uncertainty in urban morphology mapping.
- Transition from local development to HPC-scale training.

## 📚 Curriculum
The training is organized into modular labs:
- **[Introduction & Setup](https://bedruzaman.github.io/ai-maps-dua/setup.html):** Preparing your environment and accessing datasets.
- **[Lab I: Data Curation](https://bedruzaman.github.io/ai-maps-dua/lab1.html):** Handling 32-bit float tensors and patch extraction.
- **[Lab II: Model Training](https://bedruzaman.github.io/ai-maps-dua/lab2.html):** PyTorch Lightning frameworks and model checkpoints.
- **[Lab III: Inference & Scaling](https://bedruzaman.github.io/ai-maps-dua/lab3.html):** Deploying models on HPC infrastructure.

## 🛠 Prerequisites
- Basic proficiency in Python and familiarity with the geospatial stack (`rasterio`, `GeoPandas`, `torchgeo`).
- Access to the University of Twente HPC cluster for full-scale model training.

## 🤝 Contributing
We welcome contributions to this training material! If you find a bug in the code or want to clarify a technical explanation:
1. **Fork** the repository.
2. **Create** a new branch.
3. **Submit** a Pull Request using our [standard template](https://github.com/bedruzaman/ai-maps-dua/blob/main/.github/pull_request_template.md).

## 🙋 License
This project is dual-licensed:
- **Code:** [MIT License](LICENSE)
- **Content:** [Creative Commons Attribution 4.0 International](LICENSE-CC)

---
*Developed by Bedru [Your Last Name/Affiliation] at ITC, University of Twente.*
