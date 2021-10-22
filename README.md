create env

```bash
conda create -n wineq python=3.7 -y
```

activate env

```bash
conda activate wineq
```

created a req file

install the req

```bash
pip install -r requirements.txt
```

make template.py script #to develop folder structure needed for models (similar to cookiecutter structure)

download the data from

https://drive.google.com/drive/folders/18zqQiCJVgF7uzXgfbIJ-04zgz1ItNfF5?usp=sharing


python template.py


```bash
git init
```

```bash
dvc init 
```

```bash
dvc add data_given/winequality.csv
```

```bash
git add .
```

```bash
git commit -m "first commit"
```

oneliner updates  for readme

```bash
git add . && git commit -m "update Readme.md"
```

create a new github repository

```bash
git remote add origin https://github.com/olufemiolajide/dvc-demo-v1.git
git branch -M main
git push origin main
```



git add . && git commit -m "params added"  # to update params

git push origin main  # to push updated params


##develop get_data.py script in src folder

python src\get_data.py  # for windows folder

git add . && git commit -m "add get_data"

git push origin main


##develop load_data.py script in src folder

python src\load_data.py


#develop dvc.yaml script in src folder

dvc repro

git add . && git commit -m "stage 1 complete"

git push origin main


#develop split_data.py in src folder

dvc repro

git add . && git commit -m "stage 2 complete"

git push origin main


#develop train_and_evaluate.py in src folder

dvc repro

git add . && git commit -m "stage 3 complete"

git push origin main


mkdir report

#Develop params.json and scores.json in report folder

dvc repro

dvc metrics show

dvc metrics diff

git add . && git commit -m "tracker added"

git push origin main


#Create tox.ini file

mkdir tests

create conftest.py and test_config.py files in tests folder

create__init__.py in tests folder

create setup.py

pip install -e .

pip freeze  #to check what packages are installed


git add . && git commit -m "setup done" && git push origin main


# Create load_data.py in src

tox command -

```bash
tox
```

for rebuilding -

```bash
tox -r 
```

pytest command

```bash
pytest -v
```

setup commands -

```bash
pip install -e . 
```

build your own package commands-

```bash
python setup.py sdist bdist_wheel
```
