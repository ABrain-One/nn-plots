# <img src='https://abrain.one/img/lemur-nn-icon-64x64.png' width='32px'/> Neural Network Performance Analysis
<sub><a href='https://pypi.python.org/pypi/nn-stat'><img src='https://img.shields.io/pypi/v/nn-stat.svg'/></a><br/>short alias <a href='https://pypi.python.org/pypi/lmurs'>lmurs</a></sub>

The original version of the NN Stat project was created by <strong>Waleed Khalid</strong> at the Computer Vision Laboratory, University of Würzburg, Germany.

<img src='https://abrain.one/img/lemur-nn-stat-whit.jpg' width='25%'/>

<h3>Overview 📖</h3>

<p>Automated conversion of <a href="https://github.com/ABrain-One/nn-dataset" target="_blank" rel="noopener noreferrer">LEMUR</a> data into Excel format with statistical visualizations. It is developed to support the <a href="https://github.com/ABrain-One/nn-dataset">NN Dataset</a> and <a href="https://github.com/ABrain-One/nn-gpt">NN GPT</a> projects.</p>

## Installation with the LEMUR Dataset

```bash
source .venv/bin/activate
pip install nn-stat[dataset]
```

## Usage

```bash
source .venv/bin/activate
python -m ab.stat.export
```
Data and statistics are stored in the <strong>stat</strong> directory in Excel files and PNG/SVG plots.

## Update of NN Dataset
Remove old version of the LEMUR Dataset and its database:
```bash
source .venv/bin/activate
pip uninstall nn-dataset -y
rm -rf db
```
Installing the stable version:
```bash
source .venv/bin/activate
pip install nn-dataset --upgrade --extra-index-url https://download.pytorch.org/whl/cu124
```
Install from GitHub to get the most recent code and statistics updates:
```bash
source .venv/bin/activate
pip install git+https://github.com/ABrain-One/nn-dataset --upgrade --force --extra-index-url https://download.pytorch.org/whl/cu124
```


## Environment for NN Stat Contributors
### Pip package manager
Create a virtual environment, activate it, and run the following command to install all the project dependencies:
```bash
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt --extra-index-url https://download.pytorch.org/whl/cu124
```

### Docker
All versions of this project are compatible with <a href='https://hub.docker.com/r/abrainone/ai-linux' target='_blank'>AI Linux</a> and can be run inside a Docker image:
```bash
docker run -v /a/mm:. abrainone/ai-linux bash -c "PYTHONPATH=/a/mm python -m ab.stat.export"
```

#### The idea of Dr. Dmitry Ignatov
