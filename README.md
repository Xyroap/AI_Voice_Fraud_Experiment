# Voice Fraud Detection Experiment

An academic machine learning project exploring whether an audio
recording is **genuine or synthetically generated/manipulated**. The
experiment focuses on audio deepfake detection using signal-processing
features and a deep learning classifier.

> **Project type:** University coursework / experimental project\
> **Task:** Binary audio classification --- Real vs. Fake

## Overview

Voice cloning and synthetic speech can be misused to impersonate people.
This project investigates how audio features can help a model
distinguish genuine speech from fake audio. It is an experimental
coursework project and is not intended to serve as a production
fraud-detection system.

## Dataset

The experiment uses the **In-The-Wild Audio Deepfake** dataset obtained
from Kaggle:

-   **Dataset:** [In The Wild (audio Deepfake) ---
    Kaggle](https://www.kaggle.com/datasets/abdallamohamed312/in-the-wild-audio-deepfake)
-   **Original dataset information:** [In-the-Wild Dataset ---
    Fraunhofer
    AISEC](https://deepfake-demo.aisec.fraunhofer.de/in_the_wild)

The dataset contains real and fake speech recordings collected from
publicly available online sources. It was created to evaluate audio
deepfake detection under more realistic conditions than studio-only
datasets. Please refer to the dataset page and its accompanying
documentation for the latest details, terms, and attribution
requirements.

**Important:** The audio dataset is not included in this repository.
Download it from the source and follow its license and usage conditions.

## Methodology

The experiment explores an audio-classification pipeline:

1.  **Audio preparation** --- load audio files and prepare them for
    feature extraction.
2.  **Feature extraction** --- derive time-frequency representations
    such as Mel-Frequency Cepstral Coefficients (MFCCs) and
    Linear-Frequency Cepstral Coefficients (LFCCs).
3.  **Model training** --- use a CNN-BiLSTM-based deep learning approach
    to learn local spectral patterns and temporal relationships in the
    audio features.
4.  **Evaluation** --- assess the model using classification metrics and
    detection-oriented measures.
5.  **Result analysis** --- review model performance and consider
    limitations when generalizing to unseen voices, recording
    conditions, or synthesis methods.

The exact preprocessing settings, data split, and training configuration
should be taken from the experiment's source code and notebook.

## Reported Experimental Results

The experiment's reported results were:

  Metric                     Result
  ------------------------ --------
  Accuracy                   97.35%
  ROC-AUC                    0.9995
  Equal Error Rate (EER)      1.27%

These values describe the reported experiment only. Results may vary
depending on data splits, preprocessing, model configuration, and
evaluation procedure; they should not be interpreted as a guarantee of
real-world performance.

## Technologies

-   Python
-   Deep learning with CNN and BiLSTM
-   Audio feature extraction with MFCC and LFCC
-   Machine learning model evaluation

## Reproducing the Experiment

1.  Clone or download this repository.
2.  Download the dataset from the Kaggle link above.
3.  Install the dependencies specified by the project's environment or
    notebook.
4.  Update dataset paths in the code to match your local setup.
5.  Run the preprocessing, training, and evaluation steps in the order
    described by the notebook or scripts.

This README does not specify installation commands or exact file paths
because they depend on the final repository structure and environment
configuration.

## Limitations

-   The experiment is intended for academic exploration, not as a
    standalone fraud-verification service.
-   Performance on one dataset does not guarantee performance on unseen
    speakers, languages, codecs, background noise, or newly developed
    voice-generation systems.
-   Model predictions should not be treated as definitive evidence that
    a person did or did not say something.
-   Dataset licensing, privacy, consent, and source-media rights should
    be considered before redistribution or further use.

## References

1.  Abdalla Mohamed, [In The Wild (audio Deepfake) dataset on
    Kaggle](https://www.kaggle.com/datasets/abdallamohamed312/in-the-wild-audio-deepfake).
2.  Nicolas M. Müller, Pavel Czempin, Franziska Dieckmann, Adam
    Froghyar, and Konstantin Böttinger, ["Does Audio Deepfake Detection
    Generalize?"](https://arxiv.org/abs/2203.16263), Interspeech 2022.
3.  [Fraunhofer AISEC --- In-the-Wild
    Dataset](https://deepfake-demo.aisec.fraunhofer.de/in_the_wild).

------------------------------------------------------------------------

**Disclaimer:** This project was developed for educational purposes as
part of university coursework.
