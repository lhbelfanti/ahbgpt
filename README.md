<p align="center">
  <img src="media/ahbgpt-logo.png" width="100" alt="Repository logo" />
</p>
<p align="center">AHB GPT<p>
<p align="center">
    <img src="https://img.shields.io/github/repo-size/lhbelfanti/ahbgpt?label=Repo%20size" alt="Repo size" />
    <img src="https://img.shields.io/github/license/lhbelfanti/ahbgpt?label=License" alt="License" />
</p>

---

# AHB GPT
The idea behind this repository is to use the OpenAI API to classify tweets related to AHB issues (see more in [AHBCC](https://github.com/lhbelfanti/ahbcc/blob/main/README.md)), specifically the **"Illicit drug use"** problem.

## Corpus
The tweets of the [corpus](data/raw/corpus.csv) were retrieved using [GoXCrap](https://github.com/lhbelfanti/goxcrap).

The manual categorization of the tweets was done using [Binarizer](https://github.com/lhbelfanti/binarizer).

And finally, the corpus was created with [AHBCC](https://github.com/lhbelfanti/ahbcc).


## Set up & usage 

### Installation
1. Clone this repository:
    ```bash
    git clone https://github.com/lhbelfanti/ahbgpt.git
    cd ahbgpt
    ```

2. Create and activate a virtual environment (recommended):
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    ```

3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
   
4. Set your OpenAI API Key as an environment variable, replacing <API-KEY> with your actual key:
    ```bash
    export OPENAI_API_KEY=<API-KEY>       # macOS/Linux
    setx OPENAI_API_KEY "<API-KEY>"       # Windows (PowerShell)
    ```

### Usage

1. Launch Jupyter Notebook:
    ```bash
    jupyter notebook 
    ```

2. Open the notebook:
    ```bash
    ahb_gpt.ipynb
    ```

3. Run all cells to reproduce the results.

---

## License

[MIT](https://choosealicense.com/licenses/mit/)

### Logo License

Generated with AI

### Matplotlib style

The [style.mplstyle](./style.mplstyle) file was obtained from the following [repository](https://github.com/DataForScience/Networks/blob/master/d4sci.mplstyle) 