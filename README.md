# Data Science & Machine Learning — Master’s in Physics (PHYMSCFUN02)

This repository hosts all teaching materials, notebooks, dataset pointers, and reproducible workflows for the course **“Data Science and Machine Learning”** (Master’s in Physics with a focus on Fundamental Physics, second semester 2025). It follows the official syllabus covering statistics, time series & image analysis, Fourier/Monte Carlo methods, modern ML (CNNs, AEs, VAEs/GANs), and physics‑informed neural networks—with strong emphasis on open, reproducible science.

---

## 🎯 Course Goals & Learning Outcomes
By the end of the course, students will be able to:
- Apply advanced statistical methods to analyze scientific data and solve physics problems.  
- Work fluently with Python scientific libraries for **time series and scientific images**.  
- Use **Fourier analysis** and **Monte Carlo** techniques in physical modeling.  
- Understand and implement **AI/ML** approaches (supervised/unsupervised, CNNs, autoencoders, generative models).  
- Integrate physics + ML concepts into **research‑grade projects** and communicate results in technical reports/papers.

---

## 🧭 Course Structure (Units & Timeline)
**Unit 1 (Weeks 1–3):** Dimensionality reduction & time series  
- PCA, SVD, t‑SNE, UMAP, **autoencoders**; feature extraction; Fourier/wavelets; ARIMA & autocorrelation.  

**Unit 2 (Weeks 4–8):** Simulation & core ML  
- Monte Carlo (random walks, diffusion), supervised/unsupervised learning, cross‑validation, CNNs, AEs for images.  

**Unit 3 (Weeks 9–13):** Advanced models & applications  
- **PINNs** for PDEs with boundary conditions, scientific image segmentation, **VAE/GAN**, transfer learning.  

**Unit 4 (Weeks 14–16):** Scientific communication & final project  
- Paper structure & writing, reproducibility (Overleaf/GitHub), manuscript prep, presentations & defense.

---

## 📝 Assessment & Deliverables
- **Weekly participation & formative tasks:** 20%  
  - Class participation (10%), mini technical reports & autonomous tasks (10%).  
- **Midterm (Week 8):** 30%  
  - **Midterm report** (20%) + **partial results presentation** (10%).  
- **Final (Weeks 14–16):** 50%  
  - **Final project**: draft of a scientific paper (30%) + **final presentation & defense** (20%).  
- Recovery follows graduate regulations if final grade < 7.5 (at instructor’s discretion).

---

## 🧪 Repository Layout

```
.
├── notebooks/
│   ├── 01_intro/
│   ├── 02_dimensionality_reduction/      # PCA, SVD, t‑SNE, UMAP, AE latents
│   ├── 03_time_series_fourier_wavelets/
│   ├── 04_monte_carlo/
│   ├── 05_ml_basics_cv/
│   ├── 06_cnns_autoencoders_images/
│   ├── 07_pinns_pdes/
│   ├── 09_segmentation_embeddings/
│   └── 10_generative_vae_gan_transfer/
├── src/                                   # reusable Python modules
├── data/
│   ├── raw/                               # (excluded from repo if large)
│   ├── interim/
│   └── processed/
├── reports/
│   ├── midterm/
│   └── final/
├── env/                                   # environment files
│   ├── environment.yml
│   └── requirements.txt
├── CITATION.cff
├── LICENSE
└── README.md
```

> **Tip:** Large data should be stored via Git LFS or referenced by download scripts (see `data/README.md`).

---

## ⚙️ Environment & Setup

### Option A — Conda (local)
```bash
# Create environment
conda create -n mfff-ml python=3.10 -y
conda activate mfff-ml

# Core scientific stack
pip install -r env/requirements.txt
```

**`env/requirements.txt` (example)**
```
numpy
scipy
pandas
matplotlib
seaborn
scikit-learn
umap-learn
pywavelets
sympy
jupyter
ipykernel

# Deep learning (choose one stack or both as needed)
# Uncomment the appropriate lines for your platform
# torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
# tensorflow

# PINNs and extras
deepxde
```

### Option B — Google Colab
Open notebooks in Colab; GPU is optional but recommended for CNNs/AEs/VAEs/GANs. Ensure the correct runtime (GPU) under **Runtime → Change runtime type**.

---

## ▶️ How to Run

```bash
# 1) Activate environment
conda activate mfff-ml

# 2) Launch Jupyter
jupyter lab  # or jupyter notebook

# 3) Open notebooks under notebooks/02_dimensionality_reduction and run cells
```

---

## 📚 Datasets

- Small demo datasets are fetched automatically by scikit‑learn (e.g., digits).  
- Physics‑oriented examples (images/time series/PDEs) are referenced in each notebook with reproducible download cells.  
- Place larger datasets under `data/raw/` and use provided preprocessing scripts to create `data/processed/`.

---

## 🔬 Reproducibility & Good Practices
- Use **GitHub Issues** for task tracking; each PR must include:
  - Clear description, checklist, and links to related notebook cells.
  - Reproducibility note (random seeds, environment hash).
- Use **Overleaf** for writing the midterm/final manuscripts and keep a synced PDF under `reports/`.  
- Document data provenance (source, license), and set random seeds for stochastic methods (t‑SNE/UMAP/NNs).

---

## 👥 Collaboration & Office Hours
- Teamwork is expected; cite all shared components clearly in notebooks and reports.  
- **Office hours:** Monday–Thursday, 19:00–20:00 (local).

---

## 🤖 Academic Integrity & AI Use
- AI tools may assist **learning** (e.g., coding hints) **only with explicit attribution**.  
- For **evaluations** (exams/reports/projects), generating text/code/results with AI **without proper attribution** is a serious offense. Maintain originality, transparency, and data integrity.

---

## 🧾 Licensing & Citation
- Code is released under the repository’s **LICENSE** (see file).  
- If you use these materials in academic work, please cite the course and include a link to this repository.  
- Course alignment and official information are based on the PHYMSCFUN02 syllabus.

---

## 🗺️ Roadmap (selected)
- [ ] Expand **02_dimensionality_reduction** with side‑by‑side PCA vs. SVD vs. UMAP diagnostics.  
- [ ] Add **PINNs** baseline notebook (Poisson/heat equation) with boundary conditioning.  
- [ ] Provide scripts for reproducible **Monte Carlo** experiments (diffusion, first‑passage).  
- [ ] Integrate dataset cards with licenses and checksums.

---

**Instructor:** Dr. Hernán Andrés Morales‑Navarrete  
**Program:** Master’s in Physics with a focus on Fundamental Physics — **Second Semester 2025**.
