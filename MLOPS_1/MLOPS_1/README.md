# Dataset Versioning using DVC

## Aim
To practice dataset versioning using Git and DVC.

## Tools
- Git
- DVC
- Python
- VS Code / terminal

## Dataset
`data/student.csv` — student records used for the dataset-versioning practical.

## Practical work performed
- Initialized Git and DVC in the project.
- Tracked the dataset with DVC (`data/student.csv.dvc`).
- Created multiple dataset versions and restored earlier versions.
- Configured a DVC remote and practiced pushing/pulling data.

## Repository contents
- `data/`: current dataset and DVC tracking metadata.
- `.dvc/`: DVC project configuration (DVC cache is intentionally excluded).
- `dvc-storage/`: local DVC remote data bundled to make this lab copy portable.
- `Screenshots/`: practical evidence.
- `A1_MLOPS.docx`: reflection/Q&A document from the practical.

## Reproducibility note
For this assignment's portable demonstration, the local DVC remote is included in this repository. This is suitable for a small lab dataset, but a real project should keep DVC remote storage outside Git (for example, cloud/object storage).

## Basic recovery
Install Git and DVC, clone this repository, then from the repository root run:

```bash
dvc pull
```

The configured remote is the bundled `dvc-storage` folder. Dataset version metadata should be committed in Git; use Git history to select a version, then run `dvc checkout` to restore the corresponding data.
