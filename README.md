# TimesFM Model Test Repository

This repository is dedicated to testing and experimenting with the [TimesFM Model](https://github.com/google-research/timesfm). TimesFM (Time-series Foundation Model) is a decoder-only attention-based architecture designed for zero-shot time-series forecasting. Inspired by advances in large language models, TimesFM is trained on a mixture of real-world and synthetic time-series data to provide out-of-the-box predictions with minimal fine-tuning.

---

## About TimesFM
TimesFM is designed to handle diverse forecasting scenarios across varying time horizons, granularities, and domains. It achieves near state-of-the-art zero-shot accuracy compared to supervised models while being significantly smaller and computationally efficient (200M parameters). Key features include:
- **Decoder-only architecture**: Enables efficient training and inference using input patching techniques.
- **Diverse pretraining dataset**: Combines data from Google Trends, Wikimedia pageviews, and synthetic time-series.
- **Scalability**: Handles varying input and output lengths, making it versatile across applications like energy demand forecasting, traffic predictions, and retail planning.

For more details, refer to the [official paper](https://arxiv.org/pdf/2310.10688.pdf).

---

## Project Setup

### Python Version
This project uses **Python 3.10**. Ensure you have this version installed to avoid compatibility issues.

---

### Environment Setup

#### Using Conda
- **Export Environment**:
   If you modify the environment and want to save it for future use:
   ```bash
   conda env export | sed '/prefix:/d' > environment.yml
   ```

- **Import Environment**: 
  To recreate the environment from an environment.yml file:
  ```bash
  conda env create -f environment.yml && conda activate timesfm_env
  ```


#### Using Pip
- **Export Requirements**: To save the current environment to a requirements.txt file:

```bash
pip freeze > requirements.txt
```

- **Import Requirements**: To recreate the environment:

```bash
python3 -m venv timesfm_env
source timesfm_env/bin/activate  # On Windows: timesfm_env\Scripts\activate
pip install -r requirements.txt
```

### Repository Contents
- `TimesFM_Test.ipynb`: A Jupyter Notebook to explore and test the TimesFM model.
- `environment.yml`: Conda environment file for setting up the environment.
- `requirements.txt`: Pip requirements file for setting up the environment.