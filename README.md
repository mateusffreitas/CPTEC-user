[![Logo](https://github.com/framework-CPTEC/_static/blob/main/framework.png)](https://www.cptec.inpe.br/)


### Framework-CPTEC 

É um pacote in Python para a distribuição de dados brutos dos Modelos Numéricos de forma segmentada/particionada. Com esse pacote o usuário não necessita fazer o Download de todo o volume bruto o pacote auxilia a manipular somente a sua necessidade.

support Python >= 3.10.

## Instalação 

- Criar ambiente conda

conda create -n cptec python=3.10

conda activate cptec

- Instalar Pacotes

conda install -c conda-forge matplotlib pycurl cfgrib netCDF4 pynio xarray dask esmpy scipy mpi4py xesmf

- Instalar Pacote

### Via pip

pip install -i https://test.pypi.org/simple/ cptec-model

### Via fonte

git clone https://github.com/framework-CPTEC/CPTEC-user.git  

cd CPTEC-user 

python setup.py install

## Uso

import cptecmodel.CPTEC_BAM as BAM

bam = BAM.model()

date = '2023010800'

vars = ['t', 'u10m']

levels = [1000, 850]

steps = 3

f = bam.load(date=date, var=vars,level=levels, steps=steps)

## Exemplos Python

## Exemplos Jupyter Notebook

conda install -c anaconda ipykernel

pip install jupyter

jupyter notebook

