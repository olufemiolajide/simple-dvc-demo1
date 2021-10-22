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


#develop dvc.yaml script

dvc repro

git add . && git commit -m "stage 1 complete"

git push origin main



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
