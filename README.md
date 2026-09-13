# ChandraAlign
Multi-modal, Sun angle and scale invariant image correspondence using Chandrayaan-2 optical images (OHRC, TMC and IIRS)

# Potential Structure
```
lunar-image-registration/
│
├── README.md
├── LICENSE
├── .gitignore
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
├── pyproject.toml
│
├── docs/
│   ├── problem-statement.md
│   ├── system-architecture.md
│   ├── algorithm-research.md
│   ├── dataset.md
│   └── experiments.md
│
├── data/
│   ├── raw/
│   │   ├── ohrc/
│   │   ├── tmc2/
│   │   ├── iirs/
│   │   ├── lro/
│   │   └── selene/
│   │
│   ├── processed/
│   │
│   └── samples/
│
├── notebooks/
│   ├── 01_explore_ohrc.ipynb
│   ├── 02_explore_reference.ipynb
│   ├── 03_sift_baseline.ipynb
│   ├── 04_multimodal_experiments.ipynb
│   └── 05_deep_matching.ipynb
│
├── src/
│   │
│   ├── data/
│   │   ├── loader.py
│   │   ├── metadata.py
│   │   ├── pds4.py
│   │   └── preprocessing.py
│   │
│   ├── features/
│   │   ├── sift.py
│   │   ├── akaze.py
│   │   ├── orb.py
│   │   └── deep_features.py
│   │
│   ├── matching/
│   │   ├── classical.py
│   │   ├── deep.py
│   │   └── filtering.py
│   │
│   ├── registration/
│   │   ├── affine.py
│   │   ├── homography.py
│   │   ├── geometric.py
│   │   └── subpixel.py
│   │
│   ├── evaluation/
│   │   ├── metrics.py
│   │   ├── rmse.py
│   │   ├── inliers.py
│   │   └── visualization.py
│   │
│   ├── pipeline/
│   │   └── register.py
│   │
│   └── config/
│       └── settings.py
│
├── api/
│   ├── main.py
│   ├── routes/
│   │   └── registration.py
│   └── schemas/
│       └── registration.py
│
├── frontend/
│   └── ...
│
├── tests/
│   ├── test_preprocessing.py
│   ├── test_features.py
│   ├── test_matching.py
│   ├── test_registration.py
│   └── test_pipeline.py
│
├── results/
│   ├── registered/
│   ├── matches/
│   ├── metrics/
│   └── visualizations/
│
└── scripts/
    ├── download_data.py
    ├── preprocess.py
    ├── run_registration.py
    └── benchmark.py
```
