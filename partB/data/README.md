# Dataset Description — Synthetic Time Series with Planted Motifs

## What is the dataset?

This dataset is a **synthetic sinusoidal time series** with two deliberately planted motif subsequences.  
It is generated programmatically in `task_2_1.ipynb` and saved as `synthetic_stream.npy`.

## How to obtain it

The dataset is fully reproducible from `task_2_1.ipynb`. Run the notebook from top to bottom using:

```bash
jupyter nbconvert --to notebook --execute task_2_1.ipynb --output task_2_1.ipynb
```

This generates `partB/data/synthetic_stream.npy` (a NumPy binary array).

## How it is used in the notebooks

| Notebook | Usage |
|---|---|
| `task_2_1.ipynb` | Dataset generation and exploratory plot |
| `task_2_2.ipynb` | Loaded for streaming motif reproduction |
| `task_2_3.ipynb` | Loaded for result comparison + visualisation |
| `task_3_1.ipynb` | Loaded for ablation experiments |
| `task_3_2.ipynb` | Modified version used for failure mode demonstration |

## Parameters

- **Length**: 500 time steps
- **Subsequence length** (m): 20  
- **Window size** (w): 100  
- **Planted motif**: A 5 Hz sine burst of length 20, injected at positions 50 and 300  
- **Background noise**: Gaussian noise, σ=0.5, seeded at `np.random.seed(42)`
