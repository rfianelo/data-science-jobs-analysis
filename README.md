# data-science-jobs-analysis

Limpeza e análise de vagas de ciência de dados do Glassdoor com Python (pandas e NumPy), com dashboard em Power BI.

**🔗 [Acessar o dashboard interativo](https://app.powerbi.com/view?r=eyJrIjoiYWZjZmYyYzAtYzQ5Ny00ODcxLTlhNDktZWIzZTBhNzFiMjY1IiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)**

<a href="https://app.powerbi.com/view?r=eyJrIjoiYWZjZmYyYzAtYzQ5Ny00ODcxLTlhNDktZWIzZTBhNzFiMjY1IiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9">
  <img width="1593" height="854" alt="Preview do dashboard" src="https://github.com/user-attachments/assets/ef3869c2-73b7-454a-9f76-db8b885ea584" />
</a>

---

## Sobre o projeto

Primeiro projeto do portfólio, com foco em praticar **limpeza e tratamento de dados com Python**.

Parti de uma base bruta de vagas de ciência de dados publicadas no Glassdoor, com salários em texto, cargos escritos de formas diferentes e localizações em campo único. O resultado final foi uma base estruturada, pronta para análise e visualização.

Depois da limpeza, realizei uma análise exploratória para tirar as primeiras conclusões sobre a distribuição dos dados e, posteriormente, construí um dashboard em Power BI com os resultados.

## Dados

- **Fonte:** dataset *Uncleaned DS Jobs* (Kaggle) — `rashikrahmanpritom/data-science-job-posting-on-glassdoor`
- **Volume:** 672 vagas, 15 colunas na base bruta
- **Escopo:** Estados Unidos
- **Saída:** base tratada com 21 colunas, exportada em CSV

## Ferramentas

`Python` · `pandas` · `NumPy` · `Google Colab` · `Power BI`

## O que foi feito na limpeza

- Substituição dos valores faltantes codificados como `-1` por nulos
- **Padronização de cargos:** a base trazia dezenas de variações para o mesmo cargo, agrupadas em 6 categorias
- **Extração de senioridade** a partir do título da vaga, usando um dicionário de prefixos comuns (Jr, Sr, Lead, Principal...)
- **Tratamento de salários:** o campo vinha como texto (`$79K-$131K (Glassdoor est.)`) e foi convertido em valores numéricos de mínimo, máximo e média
- **Separação de localização** em cidade, estado e país, tanto da vaga quanto da sede da empresa
- Agrupamento do número de funcionários em 4 categorias de porte
- **Enriquecimento geográfico:** merge com uma base pública de coordenadas de cidades americanas para permitir o mapa no dashboard — 92% das vagas encontraram correspondência

## Principais achados

**Data Scientist domina o mercado.** Dos cargos identificados, 455 são de Data Scientist — quase 10x mais que Data Analyst e Data Engineer, empatados em 47 vagas.

**O estado da Califórnia concentra as vagas**, com 163 posições, e a região de Washington DC (Virgínia + Maryland + DC) também chama atenção com 136 vagas somadas.

**Salário médio de US$ 123,7 mil por ano**, com metade das vagas entre US$ 103 mil e US$ 136 mil. A faixa vai de US$ 43,5 mil a US$ 271,5 mil.

**TI lidera as contratações** (188 vagas), seguido por Serviços Empresariais (120) e Biotecnologia e Farmacêutica (66).

**Avaliação da empresa não tem relação com salário.** A correlação entre o rating no Glassdoor e o salário médio ficou em 0,02 — ou seja, empresas bem avaliadas não pagam mais que as outras nesta base.

## Limitações

- O dataset tem pouquíssimas vagas remotas (6 no total), então não é possível comparar salários de remoto e presencial com segurança
- A senioridade só pôde ser identificada em cerca de 17% das vagas, já que a maioria dos títulos não traz essa informação
- Os salários são estimativas do Glassdoor, não valores informados pelas empresas

---

**Felipe Rossigalli Ianelo**
[LinkedIn](https://www.linkedin.com/in/felipe-ianelo/) · [GitHub](https://github.com/rfianelo)
