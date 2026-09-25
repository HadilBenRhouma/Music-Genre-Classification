# Music Genre Classification 🎵

School AI project (ENIS, 2023): predicting the genre of a music track from its audio, using MFCC features and a K-Nearest Neighbours classifier.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=black)

## Result

**64.8 % accuracy** on the test set (K = 5, random 66 / 34 train–test split) across 10 genres:
blues, classical, country, disco, hip-hop, jazz, metal, pop, reggae, rock.

## How it works

1. **Dataset** — [GTZAN](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification): 1,000 tracks of 30 seconds, 100 per genre.
2. **Features** — for each track, MFCCs are extracted with `python_speech_features`; the track is summarised by the **mean vector** and **covariance matrix** of its MFCCs.
3. **Distance** — two tracks are compared with a distance between their MFCC distributions (mean + covariance).
4. **Classification** — K-Nearest Neighbours with a majority vote among the 5 closest tracks.

## Notebooks

| Notebook | Purpose |
|---|---|
| `train_knn.ipynb` | Extracts features from GTZAN into `my.dat`, splits train / test, evaluates the classifier |
| `predict.ipynb` | Loads `my.dat` and predicts the genre of a new `.wav` file |

## Run it

The notebooks were written for Google Colab.

1. Download GTZAN and put `genres_original/` in your Google Drive.
2. Update the Drive paths at the top of `train_knn.ipynb`, run it to generate `my.dat`.
3. Run `predict.ipynb` on any `.wav` file.

## Possible improvements

- Stratified split and cross-validation for a more stable score
- Compare with an SVM or a CNN on mel-spectrograms, which usually score higher on GTZAN

## Author

**Hadil Ben Rhouma** — [Portfolio](https://portfilio-gules-three.vercel.app/?utm_source=github) · [LinkedIn](https://www.linkedin.com/in/hadil-benrhouma/)
