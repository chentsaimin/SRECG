# SRECG 1.1

**SRECG** is an ECG signal super-resolution framework for improving low-resolution ECG signals used in cardiac arrhythmia classification.

This repository update is the **SRECG 1.1 manual-upload version**. It is intentionally limited to three root-level files:

1. `README.md`
2. `SRECG.ipynb`
3. `requirements.txt`

No generated result folders or auxiliary files are required for this lightweight GitHub update. Existing repository files and folders such as `comparison/`, `LICENSE`, or prior benchmark artifacts should be left unchanged unless you explicitly choose to regenerate and upload new outputs later.

## What changed in 1.1

- Rewrites the end-to-end experiment notebook as a **PyTorch** workflow.
- Keeps the project centered on the single executable notebook: `SRECG.ipynb`.
- Adds Kaggle/local path discovery for the CPSC2018 dataset.
- Uses memory-mapped NumPy cache handling to reduce RAM pressure during repeated ECG loading.
- Keeps the 10-fold evaluation workflow in the notebook.
- Updates `requirements.txt` to a minimal runtime dependency list instead of an environment-specific full freeze.

## Repository layout after manual upload

Only the following root files need to be uploaded/replaced for this 1.1 update:

```text
SRECG/
├── README.md
├── SRECG.ipynb
├── requirements.txt
├── comparison/          # existing folder; no manual upload required for this lightweight update
├── LICENSE              # existing file; keep unchanged
└── ...                  # other existing repository files remain unchanged
```

## Dataset expectation

The notebook expects the CPSC2018 dataset in the same structure used by the original experiment:

```text
CPSC2018Dataset/
├── REFERENCE.csv
├── TrainingSet1/
├── TrainingSet2/
└── TrainingSet3/
```

The notebook automatically searches common local and Kaggle paths, including:

```text
./CPSC2018Dataset
../input/CPSC2018Dataset
/kaggle/input/CPSC2018Dataset
/kaggle/input/cpsc2018dataset
```

If your Kaggle dataset path is different, edit the dataset path setting near the top of `SRECG.ipynb`.

## Installation

Install the runtime dependencies with:

```bash
python -m pip install -r requirements.txt
```

Then open and run:

```text
SRECG.ipynb
```

## Important runtime switches

The notebook exposes key configuration variables near the top:

| Variable | Default | Purpose |
|---|---:|---|
| `FAST_DEV_RUN` | `False` | Use `True` only for a small smoke test. |
| `REUSE_EXISTING_CHECKPOINTS` | `True` | Reuse trained checkpoints if available. |
| `REBUILD_DATA_CACHE` | `False` | Rebuild the memory-mapped data cache when needed. |
| `WRITE_REQUIREMENTS` | `False` | Avoid overwriting the lightweight `requirements.txt` during normal runs. |
| `SRECG_BATCH_SIZE` | `64` | Optional environment override for batch size. |
| `SRECG_EPOCHS` | `100` | Optional environment override for training epochs. |
| `SRECG_DETERMINISTIC` | `0` | Set to `1` for stricter deterministic behavior at the cost of speed. |

## GitHub notebook preview note

`SRECG.ipynb` in this manual-upload package is saved as a GitHub-renderable notebook: code and Markdown are preserved, but saved cell outputs are cleared before upload. This avoids GitHub preview failures such as `Unable to render code block` caused by large embedded notebook outputs.

This does **not** change the experiment source code or runtime logic. Running the notebook regenerates the outputs from the same cells.

## Manual GitHub upload procedure

Use GitHub's web interface to replace exactly these three files at the repository root:

```text
README.md
SRECG.ipynb
requirements.txt
```

Recommended commit message:

```text
Release SRECG v1.1 manual notebook update
```

Do not upload the entire ZIP file into the repository. Extract it first, then upload the three files individually.

## Notes on reproducibility

This manual-upload version updates the runnable notebook and dependency declaration only. It does not upload regenerated plots, CSV summaries, NumPy result arrays, fold-index files, checkpoints, or cache files. Those artifacts should be treated as notebook-generated outputs and can be regenerated later if needed.

## References

1. Chen et al., *SRECG: ECG Signal Super-Resolution Framework for Portable/Wearable Devices in Cardiac Arrhythmias Classification*.
2. CPSC2018 ECG dataset workflow as used by the original SRECG experiment.

## License

This repository retains the original GPL-3.0 license.
