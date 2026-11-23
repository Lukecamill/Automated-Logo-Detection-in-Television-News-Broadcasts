# Automated-Logo-Detection-in-Television-News-Broadcasts

LogoSpotter — ARI3129

Automated, single-class logo detection in television news footage.

## Team

Five members, as agreed with the professor. Team accounts: @Lukecamill, @nathanvella019, @Tristin28, @JakeDesira, @kurtabela06. Confirm the Person 2–5 mapping before replacing their labels.

| Member | Shared responsibility | Individual detector |
| --- | --- | --- |
| Person 1 | Dataset preparation, Roboflow, splits and annotation quality | YOLO11 |
| Person 2 | Exploratory data analysis | Faster R-CNN |
| Person 3 | Shared evaluation and detection analytics | RetinaNet |
| Person 4 | Model comparison | RF-DETR |
| Person 5 | Documentation and repository organisation | SSD |

Every member manually annotates their allocated 300 images, trains and evaluates their own detector, and contributes to the technical report and AI usage journal.

## Repository

- `notebooks/1_EDA.ipynb`: shared dataset analysis.
- `notebooks/2_<Architecture>_<StudentName>.ipynb`: one detector notebook per member. Rename `PersonN` to your name before starting.
- `notebooks/3_results_comparison.ipynb`: shared model comparison.
- `data/README.md`: dataset access, version and partition records.
- `data/splits/`: shared split manifests once agreed.
- `configs/`: reproducible experiment configurations.
- `results/`: small metrics files and plots, organised by detector.
- `reports/`: report contributions and individual AI journal entries.
- `CONTRIBUTING.md`: group workflow.

## Dataset

Public Roboflow project: **pending creation — Person 1 will add the URL**.
Project name: `LogoSpotter-G[N]` (replace `[N]` with the group number).
Class: `Logo`. All models must use the same original training, validation and test partitions.
Annotations are manual. Exclude digital broadcast overlays; retain null frames as background examples. Apply augmentation only to training data.

## Getting started

1. Accept the repository collaborator invitation.
2. Clone the repository and create a branch for your work; see `CONTRIBUTING.md`.
3. Create a Python environment and install the notebook tools:

   ```sh
   python3 -m venv .venv
   source .venv/bin/activate
   python -m pip install -r requirements.txt
   jupyter lab
   ```

4. Install your detector's dependencies in your own environment and record their exact versions with your experiment. Model frameworks are not installed by the shared requirements file.
5. Download the agreed dataset version using `data/README.md` once populated.
6. Run notebooks from top to bottom and record the actual results.

## Reproducibility

Record the dataset version, split manifest, seed, pretrained weights, model size, software versions, hardware, image resolution, preprocessing, augmentation and training configuration for every experiment. Use validation data for model selection and the held-out test set for final comparison. Save metrics and small plots under `results/<detector>/`; keep datasets and model checkpoints outside Git.

## Submission

Deadline in the supplied brief: 11 January 2027. Group deliverables: a technical report (maximum 20 pages), AI usage journal (maximum 10 pages), public Roboflow dataset and public GitHub repository. The notebooks currently contain outlines only; no training or evaluation has been performed.
