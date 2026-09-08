# CZAI Summer School 2026 — AI for Enzymes

Hands-on notebooks for the CZAI Summer School lecture *"AI pro enzymy: Jak pochopit chemii přírody – a překonat ji"*.

## 1. Enzyme Function Prediction with CLEAN

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/soldatmat/czai-summer-school-2026/blob/main/CZAI_Summer_School-CLEAN_training.ipynb)

Predicting an enzyme's EC number from its sequence with contrastive learning, in the style of **CLEAN**.

Adapted from Ariane Mora's [AMLD workshop notebook](https://huggingface.co/datasets/arianemora/AMLD_workshop_ML4Enzymes), pointing at the [soldatmat/CZAI_Summer_School-CLEAN_training](https://huggingface.co/datasets/soldatmat/CZAI_Summer_School-CLEAN_training) dataset mirror.

## 2. Machine-Learning-guided Directed Evolution with BOES

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/soldatmat/czai-summer-school-2026/blob/main/CZAI_Summer_School-MLDE_BOES.ipynb)

Active-learning-guided directed evolution: a protein language model embedding plus Bayesian Optimization (**BOES**) sequentially discovers high-fitness protein variants in a real combinatorial fitness landscape (GB1 by default, also PhoQ/TrpB), and is compared round-by-round against a random-selection baseline and a zero-shot PLM-ranking baseline.

Pointing at the [soldatmat/CZAI_Summer_School-MLDE_landscapes](https://huggingface.co/datasets/soldatmat/CZAI_Summer_School-MLDE_landscapes) dataset mirror (cleaned fitness landscapes + precomputed ESM-2 embeddings).

## 3. Protein Backbone Generation with RFdiffusion

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/soldatmat/czai-summer-school-2026/blob/main/CZAI_Summer_School-RFdiffusion.ipynb)

**Needs a GPU runtime.** Diffusion-based protein backbone generation with **RFdiffusion**: unconditional generation of a novel backbone from noise, then motif scaffolding — fixing hen egg-white lysozyme's real catalytic residues (Glu35, Asp52, verified against PDB entry [1LYZ](https://www.rcsb.org/structure/1LYZ)) and designing a new scaffold around them — both with a 3D animation of the denoising trajectory. No training involved; this is inference-time conditioning only.

Adapted from Sergey Ovchinnikov's [ColabDesign RFdiffusion notebook](https://github.com/sokrypton/ColabDesign/blob/main/rf/examples/diffusion.ipynb), pointing at the [soldatmat/CZAI_Summer_School-RFdiffusion_weights](https://huggingface.co/datasets/soldatmat/CZAI_Summer_School-RFdiffusion_weights) checkpoint mirror.

---

Click a badge above, then **File → Save a copy in Drive** if you want to keep your results or changes.

## Citations

<sub>**CLEAN notebook** — Yu, T. et al. *Enzyme function prediction using contrastive learning.* Science 379(6639), 1358-1363 (2023).

**BOES notebook** — Soldát, M. & Kléma, J. *Directed Evolution of Proteins via Bayesian Optimization in Embedding Space.* 2024 IEEE International Conference on Bioinformatics and Biomedicine (BIBM), 91-98 (2024). Reference implementation: [soldatmat/PELLM](https://github.com/soldatmat/PELLM).

GB1 — Wu, N.C. et al. *Adaptation in protein fitness landscapes is facilitated by indirect paths.* eLife 5, e16965 (2016).
PhoQ — Podgornaia, A.I. & Laub, M.T. *Pervasive degeneracy and epistasis in a protein-protein interface.* Science 347(6222), 673-677 (2015).
TrpB — Johnston, K.E. et al. *A combinatorially complete epistatic fitness landscape in an enzyme active site.* PNAS 121(32), e2400439121 (2024).

**RFdiffusion notebook** — Watson, J.L. et al. *De novo design of protein structure and function with RFdiffusion.* Nature 620, 1089–1100 (2023). Code & weights: [RosettaCommons/RFdiffusion](https://github.com/RosettaCommons/RFdiffusion) (BSD License). Notebook adapted from Sergey Ovchinnikov's [ColabDesign](https://github.com/sokrypton/ColabDesign) (`rf/examples/diffusion.ipynb`). Lysozyme structure — Diamond, R. *Real-space refinement of the structure of hen egg-white lysozyme.* J. Mol. Biol. 82, 371-391 (1974); PDB entry [1LYZ](https://www.rcsb.org/structure/1LYZ).</sub>
