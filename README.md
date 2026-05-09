# 🚲 Estudo de Caso Cyclistic: Estratégias de Conversão Baseadas em Dados

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-Public-lightblue?logo=tableau&logoColor=white)

Projeto de conclusão do **Certificado Profissional de Análise de Dados do Google**. Este repositório contém o código, a documentação e os resultados da análise de dados de uma empresa fictícia de compartilhamento de bicicletas, a Cyclistic.

## 🎯 O Desafio de Negócios (Fase Ask)

A diretoria de marketing da Cyclistic identificou que membros com assinatura anual são muito mais lucrativos do que usuários casuais (que pagam por viagens avulsas).

**A pergunta central do projeto:** Como os membros anuais e os ciclistas casuais usam as bicicletas da Cyclistic de forma diferente?  
**O Objetivo:** Extrair insights comportamentais dos dados para embasar uma nova estratégia de marketing focada em converter usuários casuais em membros anuais.

## 🛠️ Ferramentas Utilizadas

* **Python (Pandas, Matplotlib, Seaborn):** Limpeza, manipulação, transformação, agregação de dados e visualizações.
* **Jupyter Notebook:** Documentação e execução do código passo a passo.
* **Tableau Public:** Dashboard interativo para apresentação executiva.
* **PowerPoint / PDF:** Apresentação final de recomendações.

## 📁 Estrutura do Projeto

```
cyclistic-share-analysis/
├── notbooks/
│   └── analise.ipynb        # Análise completa: limpeza, EDA e visualizações
├── apresentacao/
│   └── analise-cyclistic.pdf  # Apresentação executiva
├── dados/
│   └── fonte_dos_dados.md   # Instruções de download dos dados originais
├── requirements.txt          # Dependências Python
└── README.md
```

## ⚙️ Como Executar

**1. Instale as dependências:**
```bash
pip install -r requirements.txt
```

**2. Baixe os dados originais:**  
Veja as instruções em [`dados/fonte_dos_dados.md`](dados/fonte_dos_dados.md).

**3. Configure os caminhos no notebook:**  
Abra `notbooks/analise.ipynb` e atualize as duas primeiras variáveis da célula de configuração:
```python
CAMINHO_2019 = r"caminho/para/Divvy_Trips_2019_Q1.csv"
CAMINHO_2020 = r"caminho/para/Divvy_Trips_2020_Q1.csv"
```

**4. Execute o notebook:**
```bash
jupyter notebook notbooks/analise.ipynb
```

## 📊 O Dashboard Interativo (Fase Share)

As visualizações completas deste estudo foram publicadas no Tableau Public.  
👉 **[Clique aqui para acessar o Dashboard Interativo](https://public.tableau.com/app/profile/ygor.prado.chagas/viz/analise-cyclistic/Painelestudodecaso)**

## 🧹 Preparação e Limpeza de Dados (Fases Prepare & Process)

Os dados originais compreendem o primeiro trimestre de 2019 e 2020. Para garantir a precisão da análise, o seguinte processo de limpeza foi executado em Python:

* **Padronização de Arquitetura:** As colunas exclusivas de 2019 (dados demográficos, duração em texto) e de 2020 (geolocalização) foram removidas para permitir a concatenação das duas bases.
* **Unificação de Nomenclatura:** Descobriu-se uma mudança no banco de dados entre os anos. A categoria histórica `Subscriber` foi atualizada para `member` e `Customer` para `casual`, padronizando o dataset.
* **Feature Engineering:** As colunas de tempo (strings) foram convertidas para `DateTime`. A partir delas, foram criadas as colunas calculadas `ride_length` (duração em segundos) e `day_of_week` (dia da semana).
* **Remoção de Anomalias:** Filtrei o dataset para excluir viagens com duração negativa ou igual a zero (geradas por erros de sistema ou testes de manutenção), garantindo a integridade das médias.

## 💡 Principais Descobertas (Fase Analyze)

A análise exploratória revelou a existência de duas personas completamente distintas utilizando o mesmo serviço:

| | Membro Anual | Usuário Casual |
|---|---|---|
| **Volume** | 91% das viagens | 9% das viagens |
| **Duração média** | ~13 min | ~85 min |
| **Padrão semanal** | Pico seg–sex | Pico sáb–dom |
| **Perfil de uso** | Deslocamento diário | Lazer e passeios |

## 🚀 Recomendações Estratégicas

Com base na descoberta de que o usuário casual não utiliza o serviço para a rotina diária, o plano anual tradicional não atende às suas necessidades. Recomenda-se:

1. **Criar o "Plano Anual de Fim de Semana":** Um novo produto desenhado sob medida para o padrão de uso exclusivo aos sábados e domingos.
2. **Marketing Geofocalizado:** Direcionar anúncios e promotores físicos para as estações mais movimentadas (orlas e parques) estritamente aos finais de semana, atacando o usuário no momento exato do lazer.
3. **Gamificação de Retenção:** Implementar recompensas no aplicativo para viagens acima de 60 minutos exclusivas para membros, oferecendo um benefício imediato ao comportamento natural do usuário casual caso ele faça a assinatura.

---
### 👨‍💻 Ygor Prado Chagas
