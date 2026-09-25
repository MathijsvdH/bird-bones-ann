# Bird bones neural network

A Keras neural network that predicts a bird's ecological group from 10 bone measurements. It also tests how the learning rate and network size affect training.

Dataset: [Birds' Bones and Living Habits](https://www.kaggle.com/datasets/zhangjuefei/birds-bones-and-living-habits) (Zhang, n.d.). It has 420 birds and 6 classes: SW (swimming), W (wading), T (terrestrial), R (raptors), P (scansorial) and SO (singing).

## Results

| | |
|---|---|
| Model | 10 → 32 → 16 → 6, Adam, lr 0.01, EarlyStopping |
| Split | 70 / 15 / 15, stratified |
| Test accuracy | 0.903 (56/62) |
| Macro F1 | 0.857 |

- **Learning rate** (0.01 / 0.001 / 0.0001): 0.01 converges about 6× faster with the same accuracy as 0.001. 0.0001 doesn't converge within 2000 epochs.
- **Network size** (8 / 32-16 / 128-64): the single 8-neuron layer underfits. 32-16 and 128-64 reach the same accuracy.
- Most test errors stay within one size group (small: SO, P, T; large: SW, W, R). Wading birds get confused with swimming birds most often.

Each setting ran with 3 seeds and is reported as mean ± std. See the notebook for the learning curves, the confusion matrix and the reflection.

## Files

- `ann.ipynb`: the notebook with outputs
- `ann.html`: HTML export of the notebook, readable without Jupyter
- `data/bird.csv`: local copy of the dataset, used when the Kaggle download fails

## Run

Python 3.12, TensorFlow/Keras, pandas, scikit-learn, matplotlib, seaborn, kagglehub.

```
uv add tensorflow pandas scikit-learn matplotlib seaborn kagglehub ipykernel
uv run jupyter notebook ann.ipynb
```

Random seed 1 is used throughout for reproducibility.
