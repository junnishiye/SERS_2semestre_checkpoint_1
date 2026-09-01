# SERS — Checkpoint 1 do 2º semestre

Projeto acadêmico de análise exploratória de dados energéticos. O trabalho reúne tratamento de dados, cálculo de indicadores, identificação de períodos de alta demanda ou geração, visualizações e elaboração de relatórios.

## Sobre a entrega

> Este repositório contém **dois códigos principais**, ambos em notebooks Jupyter (`.ipynb`).  
> Os demais arquivos são **bases de dados auxiliares em CSV**, necessárias para executar corretamente as análises do primeiro notebook. Eles não representam códigos ou entregas independentes.

## Notebooks

### 1. Análise de seis bases de energia

[**Datasets_1_2_3_4_5_6.ipynb**](./Datasets_1_2_3_4_5_6.ipynb)

Concentra a exploração e a análise de seis conjuntos de dados:

1. consumo de energia de eletrodomésticos;
2. consumo de energia na indústria siderúrgica;
3. consumo de energia da cidade de Tetuão;
4. geração de energia solar por planta;
5. produção de energia eólica e solar;
6. consumo elétrico residencial.

O notebook inclui inspeção dos dados, tratamento de valores ausentes, estatísticas descritivas, definição de critérios de alto consumo ou geração, cálculos percentuais, gráficos e interpretações dos resultados.

[Executar no Google Colab](https://colab.research.google.com/github/junnishiye/SERS_2semestre_checkpoint_1/blob/main/Datasets_1_2_3_4_5_6.ipynb)

### 2. Análise da carga elétrica pela API do ONS

[**Desafio_Final_Energia_ONS_API_Unificado.ipynb**](./Desafio_Final_Energia_ONS_API_Unificado.ipynb)

Analisa a carga elétrica de São Paulo entre **1º e 7 de agosto de 2025**, a partir da API pública do Operador Nacional do Sistema Elétrico (ONS). O notebook reúne os Desafios 1 a 9:

- obtenção, construção e inspeção do DataFrame;
- organização e tratamento dos dados;
- cálculo de mínimo, máximo, média, mediana e amplitude;
- identificação de alta demanda e do momento de pico;
- comparação de critérios;
- criação e interpretação de gráficos;
- síntese dos resultados;
- geração de relatório com o modelo **GPT-4o mini**;
- validação crítica e apresentação do relatório final revisado.

[Executar no Google Colab](https://colab.research.google.com/github/junnishiye/SERS_2semestre_checkpoint_1/blob/main/Desafio_Final_Energia_ONS_API_Unificado.ipynb)

## Estrutura do repositório

| Arquivo | Tipo | Finalidade |
|---|---|---|
| `Datasets_1_2_3_4_5_6.ipynb` | Código principal | Análise exploratória das seis bases locais |
| `Desafio_Final_Energia_ONS_API_Unificado.ipynb` | Código principal | Análise da API do ONS e relatório com GPT-4o mini |
| `Appliences_Energy_Prediction_Sample.csv` | Dado auxiliar | Base de consumo de eletrodomésticos |
| `Steel_Industry_Energy_Consumption_Sample.csv` | Dado auxiliar | Base de consumo da indústria siderúrgica |
| `Power_Consumption_of_Tetouan_City.csv` | Dado auxiliar | Base de consumo da cidade de Tetuão |
| `amostra_geracao_planta.csv` | Dado auxiliar | Base de geração de uma planta solar |
| `Wind_&_Solar_Energy_Production_Sample.csv` | Dado auxiliar | Base de produção eólica e solar |
| `Individual_Household_Eletric_Power_Consumption_Sample.csv` | Dado auxiliar | Base de consumo elétrico residencial |

## Outputs disponíveis

Os dois notebooks foram salvos **com os resultados visíveis**, permitindo que o conteúdo seja avaliado diretamente pelo GitHub ou pelo Google Colab sem uma nova execução.

| Notebook | Células de código executadas | Saídas salvas | Gráficos salvos | Outputs de erro |
|---|---:|---:|---:|---:|
| `Datasets_1_2_3_4_5_6.ipynb` | 43 de 43 | 55 | 4 | 0 |
| `Desafio_Final_Energia_ONS_API_Unificado.ipynb` | 19 de 19 | 26 | 2 | 0 |

No segundo notebook, o relatório produzido pelo GPT-4o mini também está preservado nos outputs. Portanto, **não é necessário possuir uma chave da OpenAI apenas para visualizar e avaliar os resultados já salvos**.

## Como executar

### Opção recomendada

Clone o repositório para manter os notebooks e seus arquivos auxiliares no mesmo diretório:

```bash
git clone https://github.com/junnishiye/SERS_2semestre_checkpoint_1.git
cd SERS_2semestre_checkpoint_1
```

Depois, abra o notebook desejado no Jupyter ou no Google Colab e execute as células em ordem.

### Arquivos CSV

O notebook `Datasets_1_2_3_4_5_6.ipynb` utiliza caminhos relativos. Por isso, os seis arquivos CSV devem permanecer na mesma pasta do notebook — ou ser enviados para o diretório de execução da sessão do Colab.

O notebook `Desafio_Final_Energia_ONS_API_Unificado.ipynb` não depende desses CSVs: os dados são consultados diretamente na [API pública de carga verificada do ONS](https://apicarga.ons.org.br/prd/cargaverificada).

### Chave da OpenAI

A chave **não está armazenada no repositório**. Ela só é necessária caso seja feita uma nova execução da etapa que gera o relatório com o GPT-4o mini.

No Google Colab, adicione a chave em **Segredos** com o nome:

```text
OPENAI_API_KEY
```

O notebook recupera esse segredo de forma segura com `google.colab.userdata`.

## Tecnologias utilizadas

- Python;
- Jupyter Notebook / Google Colab;
- pandas;
- Matplotlib;
- Seaborn;
- Requests;
- API pública do ONS;
- API da OpenAI com GPT-4o mini.

## Observação final

Para avaliação, basta abrir os dois notebooks no GitHub: códigos, tabelas, indicadores, relatórios e gráficos já estão registrados nos próprios arquivos. Uma nova execução só é necessária para reproduzir ou atualizar os resultados.
