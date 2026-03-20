# 🚲 Estudo de Caso Cyclistic: Estratégias de Conversão Baseadas em Dados

Bem-vindo ao meu projeto de conclusão do Certificado Profissional de Análise de Dados do Google. Este repositório contém o código, a documentação e os resultados da análise de dados de uma empresa fictícia de compartilhamento de bicicletas, a Cyclistic.

## 🎯 O Desafio de Negócios (Fase Ask)
A diretoria de marketing da Cyclistic identificou que membros com assinatura anual são muito mais lucrativos do que usuários casuais (que pagam por viagens avulsas). 

**A pergunta central do projeto:** Como os membros anuais e os ciclistas casuais usam as bicicletas da Cyclistic de forma diferente?
**O Objetivo:** Extrair insights comportamentais dos dados para embasar uma nova estratégia de marketing focada em converter usuários casuais em membros anuais.

## 🛠️ Ferramentas Utilizadas
* **Python (Pandas):** Limpeza, manipulação, transformação e agregação de dados.
* **Jupyter Notebook:** Documentação e execução do código passo a passo.
* **Tableau Public:** Criação do dashboard interativo e visualização de dados.
* **PowerPoint / PDF:** Apresentação executiva de recomendações.

## 📊 O Dashboard Interativo (Fase Share)
As visualizações completas deste estudo foram publicadas no Tableau Public. 
👉 **[CLIQUE AQUI PARA ACESSAR O DASHBOARD INTERATIVO]** *https://public.tableau.com/views/analise-cyclistic/Estudodecasocyclistic?:language=pt-BR&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link*

## 🧹 Preparação e Limpeza de Dados (Fases Prepare & Process)
Os dados originais compreendem o primeiro trimestre de 2019 e 2020. Para garantir a precisão da análise, o seguinte processo de limpeza foi executado em Python:

* **Padronização de Arquitetura:** As colunas exclusivas de 2019 (dados demográficos, duração em texto) e de 2020 (geolocalização) foram removidas para permitir a concatenação perfeita das duas bases.
* **Unificação de Nomenclatura:** Descobriu-se uma mudança no banco de dados entre os anos. A categoria histórica `Subscriber` foi atualizada para `member` e `Customer` para `casual`, padronizando o dataset.
* **Feature Engineering:** As colunas de tempo (strings) foram convertidas para `DateTime`. A partir delas, foram criadas as colunas calculadas `ride_length` (duração da viagem em segundos) e `day_of_week` (dia da semana).
* **Remoção de Anomalias:** Filtrei o dataset para excluir viagens com duração negativa ou igual a zero (geradas por erros de sistema ou testes de manutenção), garantindo a integridade das médias.

## 💡 Principais Descobertas (Fase Analyze)
A análise exploratória revelou a existência de duas personas completamente distintas utilizando o mesmo serviço:

1. **O Comutador (Membro Anual):** * Representa o volume massivo da empresa (91% das viagens).
   * Realiza viagens curtas (média de 13 minutos).
   * O uso atinge o pico de segunda a sexta-feira, caracterizando o uso utilitário (deslocamento para o trabalho/estudos).

2. **O Turista / Lazer (Usuário Casual):**
   * Representa uma parcela menor do volume (9%), mas com altíssima retenção por viagem.
   * Pedala por um tempo quase 6x maior (média de 89 minutos).
   * O uso domina o fim de semana (sábados e domingos), caracterizando uso voltado para passeios e recreação.

## 🚀 Recomendações Estratégicas
Com base na descoberta de que o usuário casual não utiliza o serviço para a rotina diária, o plano anual tradicional não atende às suas necessidades. Recomenda-se:

1. **Criar o "Plano Anual de Fim de Semana":** Um novo produto desenhado sob medida para o padrão de uso exclusivo aos sábados e domingos.
2. **Marketing Geofocalizado:** Direcionar anúncios e promotores físicos para as estações mais movimentadas (orlas e parques) estritamente aos finais de semana, atacando o usuário no momento exato do lazer.
3. **Gamificação de Retenção:** Implementar recompensas no aplicativo para viagens acima de 60 minutos exclusivas para membros, oferecendo um benefício imediato ao comportamento natural do usuário casual caso ele faça a assinatura.

---
### 👨‍💻**Ygor Prado Chagas**

