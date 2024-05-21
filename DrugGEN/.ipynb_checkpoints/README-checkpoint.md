# Group9 reimplement toturial
# how to training

# set up the environment (installs the requirements):

conda env create -f DrugGEN/dependencies.yml

# activate the environment:

conda activate druggen

```

Here is with pip using virtual environment:

```bash
python -m venv DrugGEN/.venv
./Druggen/.venv/bin/activate
pip install -r DrugGEN/requirements.txt
```


### Training the model

```
# Download input files:

cd DrugGEN/data

bash dataset_download.sh

cd

# Default DrugGEN model can be trained with the one-liner:

python DrugGEN/train.py --submodel="DrugGEN" --raw_file="DrugGEN/data/chembl_train.smi" --dataset_file="chembl45_train.pt" --drug_raw_file="DrugGEN/data/akt_train.smi" --drug_dataset_file="drugs_train.pt" --max_atom=45
```
