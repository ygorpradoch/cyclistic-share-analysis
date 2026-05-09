# Fonte dos Dados

Os dados utilizados nesta análise são disponibilizados publicamente pela **Motivate International Inc.** (operadora do sistema Divvy de Chicago) sob licença de uso público.

## Datasets Utilizados

| Arquivo | Período | Registros |
|---|---|---|
| `Divvy_Trips_2019_Q1.csv` | Jan–Mar 2019 | 365.069 viagens |
| `Divvy_Trips_2020_Q1.csv` | Jan–Mar 2020 | 426.887 viagens |

## Download

Os arquivos podem ser baixados diretamente do portal oficial:

🔗 **https://divvy-tripdata.s3.amazonaws.com/index.html**

Procure pelos arquivos:
- `Divvy_Trips_2019_Q1.zip`
- `Divvy_Trips_2020_Q1.zip`

## Como Configurar

Após o download, extraia os CSVs e atualize os caminhos no início do notebook `notbooks/analise.ipynb`:

```python
CAMINHO_2019 = r"caminho/para/Divvy_Trips_2019_Q1.csv"
CAMINHO_2020 = r"caminho/para/Divvy_Trips_2020_Q1.csv"
```

## Licença dos Dados

Os dados são disponibilizados pela Lyft Bikes and Scooters, LLC ("Bikeshare") sob a [Divvy Data License Agreement](https://divvybikes.com/data-license-agreement).

> Os dados são anonimizados — não contêm informações pessoais identificáveis dos usuários.
