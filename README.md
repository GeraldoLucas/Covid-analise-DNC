# Covid-analise-DNC
Doenças Neurológicas Crônicas: análise dos dados em pacientes com Covid;


# Importação de bibliotecas necessárias
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

pd.set_option('display.max_columns', None)
pd.set_option('display.width', None)
pd.set_option('display.max_colwidth', 0)


# Importar dos dados sobre Doenças Neurológicas Crônicas em pacientes com Covid para um DataFrame
uri = r"C:/Users/geral/Dropbox/geraldolucas/Python/Python Machine Learning/Analise de dados/INFLUD-15-03-2021.csv"
dF = pd.read_csv(uri, sep=';',
                 error_bad_lines=True,
                 warn_bad_lines=True,
                 engine="python",
                 encoding='UTF-8')

print(f"Número total de Casos considerados: {dF.shape[0]}")


# Removendo colunas desconsideradas na análise
