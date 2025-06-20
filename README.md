# High-Dimensional Text Data Visualization

Streamlit-based application for exploring and visualizing high-dimensional text data from the [News
Category Dataset](https://www.kaggle.com/datasets/rmisra/news-category-dataset). We use DistilBERT
text vector embeddings and visualize data using dimensionality reduction techniques such as UMAP,
t-SNE, PaCMAP, and TriMAP to create intuitive 2D and 3D plots. We also integrate topic modeling to
allow users to interactively explore topic prevalence and evolution over time, enabling dynamic
insights into large text corpora.

You can read more (in Polish) [here](docs/preliminary.pdf).

---

First create virtual environment and install the required dependencies

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

To download the used [News Category
Dataset](https://www.kaggle.com/datasets/rmisra/news-category-dataset) simply run the following
command. It will download and extract the dataset into `data/` directory.

```bash
python3 scripts/download.py
```

---

To compute the vector embeddings required for visualization simply run

```bash
python3 scripts/bert_embeddings.py
```

---

To run the application

```bash
streamlit run app.py
```

## Running inside docker container

With docker running you can build and run the app using the following two commands

```bash
docker build -t news-viz .
docker run --rm -p 8501:8501 news-viz
```
