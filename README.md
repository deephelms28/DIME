## Dataset: CLEVR_v1.0

Download and extract the CLEVR dataset and accompanying DIME annotations:

```bash
# Download and unzip the CLEVR dataset
wget https://dl.fbaipublicfiles.com/clevr/CLEVR_v1.0.zip
unzip CLEVR_v1.0.zip
rm CLEVR_v1.0.zip

# Download and unzip DIME-specific annotations
wget -O clevr_annotations.zip https://zenodo.org/record/4721981/files/clevr_annotations.zip?download=1
unzip clevr_annotations.zip
rm clevr_annotations.zip
```

---

## Setting Up Environment for DIME

DIME requires Python 3.7. We recommend using [`pyenv`](https://github.com/pyenv/pyenv) to manage Python versions.

### 1. Install `pyenv`

```bash
curl -fsSL https://pyenv.run | bash

# Add pyenv to shell startup script
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init - bash)"' >> ~/.bashrc

# Restart your shell to apply changes
exec "$SHELL"
```

### 2. Install Python 3.7 and setup environment

```bash
pyenv install 3.7.11
pyenv local 3.7.11

# Upgrade pip
pip install --upgrade pip
```

---

## Running DIME

Open the Jupyter notebook and follow the cells.  
Make sure to update the dataset paths to match your local directory structure.
