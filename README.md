# FakeReviewDetection

A feature-ablation study of RoBERTa-based models to diagnose cross-domain failures in fake-review detection (Amazon -> Yelp).

## Contents

- `FakeReviewDetectionPipeline.ipynb` — primary analysis and modeling notebook.
- Datasets: `Amazon Cleaned Dataset.url`, `YelpChi Cleaned Dataset.url`

## Requirements

- The notebook is intended to be run in Google Colab (no local environment required).

### Run the notebook in Google Colab

1. Open Colab in your browser and either:

	- Use **File -> Upload notebook** to upload `FakeReviewDetectionPipeline.ipynb`, or
	- Since the repo is public, open the notebook via **File -> Open notebook -> GitHub** and paste the repo URL.

2. Install packages: run the notebook's top cells which include the required `!pip install` commands (these set up `transformers`, `tensorflow`, and other dependencies).

3. Mount Google Drive and extract datasets — the notebook already contains the Drive-mount and extraction cells at the top, so just run those top cells:

```python
from google.colab import drive
drive.mount('/content/drive')
# extraction cells follow in the notebook; run the top cells to perform them
```

4. Run cells in Colab as usual. Note that Colab has limited runtime storage and memory — upload data or keep it on Drive, and consider using smaller samples or Colab Pro+ (or an equivalent high-RAM machine) for longer/more memory-intensive runs.

Important: extracting and processing the full Amazon dataset used in this project required about 160 GB of RAM during embedding extraction and training. For full-scale runs we recommend Colab Pro+ or an equivalent high-RAM machine.

Tips:

- Run the notebook's top cells first — they install dependencies and mount Drive where needed.


