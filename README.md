# 📊 Análise Exploratória de Dados (EDA) - Churn de Clientes

Este projeto apresenta uma análise exploratória completa de dados de churn de clientes de uma empresa de telecomunicações, utilizando Python e técnicas estatísticas para identificar padrões e fatores que influenciam o abandono de clientes.

## 🎯 Objetivos

- Analisar o comportamento de churn de clientes
- Identificar variáveis que mais influenciam o abandono
- Realizar análises estatísticas para validar hipóteses
- Detectar e tratar outliers nos dados
- Automatizar a geração de relatórios de EDA

## 📁 Estrutura do Projeto

```
analise/
├── eda_churn.ipynb          # Notebook principal com análise completa
├── datasets_aula/           # Dados originais
│   ├── churn_customers.csv  # Dados dos clientes
│   ├── churn_services.csv   # Dados dos serviços
│   └── churn_contracts.csv  # Dados dos contratos
├── Pipfile                  # Dependências do projeto
├── Pipfile.lock            # Versões fixas das dependências
└── README.md               # Este arquivo
```

## 🔍 Principais Análises Realizadas

### 1. **Preparação e Limpeza dos Dados**

- Carregamento e unificação de 3 datasets (customers, services, contracts)
- Tratamento de valores ausentes e conversão de tipos de dados
- Renomeação e padronização de colunas

### 2. **Análise Univariada**

- Distribuição da variável target (Churn)
- Análise de frequências e percentuais
- Medidas de posição e dispersão
- Visualizações com histogramas e gráficos de barras

### 3. **Análise Bivariada**

- Tabelas de contingência entre variáveis categóricas
- Testes de hipótese Chi-Square (Qui-Quadrado)
- Correlações entre variáveis numéricas (Pearson e Spearman)
- Validação de hipóteses de negócio

### 4. **Tratamento de Outliers**

- Detecção usando método IQR (Tukey)
- Detecção usando Z-Score
- Visualizações com Box Plots

### 5. **Automação de EDA**

- Relatório automatizado usando ydata-profiling
- Geração de insights abrangentes

## 🧪 Principais Descobertas

### Hipóteses Validadas:

✅ **Clientes com contrato mensal são mais propensos ao churn**

- 88% dos clientes que abandonaram tinham contrato mensal
- Qui² alto indica forte correlação (p-value < 0.05)

✅ **Clientes com menos de 6 meses são mais propensos ao churn**

- Correlação estatisticamente significativa (p-value < 0.05)
- Menor força de correlação comparado ao tipo de contrato

✅ **Faixa etária tem associação com churn**

- Correlação estatisticamente significativa mas com relação baixa
- Clientes seniores apresentam comportamento diferenciado

### Insights Importantes:

- Forte correlação positiva entre tempo de contrato e valor total pago
- Concentração de churn nos primeiros meses de contrato
- Padrões distintos entre diferentes tipos de contrato

## 🛠️ Tecnologias Utilizadas

- **Python 3.11+**
- **Pandas** - Manipulação e análise de dados
- **NumPy** - Computação numérica
- **Matplotlib** - Visualizações básicas
- **SciPy** - Testes estatísticos
- **ydata-profiling** - Relatórios automatizados de EDA
- **Jupyter Notebook** - Ambiente de desenvolvimento

## ⚙️ Configuração do Ambiente

### Pré-requisitos

- Python 3.11 ou superior
- pipenv (recomendado) ou pip

### Instalação

1. **Clone o repositório:**

```bash
git clone <url-do-repositorio>
cd analise
```

2. **Instale as dependências:**

```bash
# Usando pipenv (recomendado)
pipenv install
pipenv shell

# Ou usando pip
pip install pandas numpy matplotlib scipy ydata-profiling jupyter ipywidgets
```

3. **Execute o notebook:**

```bash
jupyter notebook eda_churn.ipynb
```

## 📈 Como Usar

1. **Execute as células sequencialmente** para reproduzir toda a análise
2. **Modifique os parâmetros** nas análises conforme necessário
3. **Use a célula de ProfileReport** para gerar relatório automático
4. **Explore as visualizações** para insights adicionais

## 🔧 Resolução de Problemas

### Erro: "ImportError: Numba needs NumPy 2.1 or less"

```bash
pip install "numpy<2.1" ydata-profiling
```

### Erro: "ModuleNotFoundError: No module named 'ipywidgets'"

```bash
pip install --upgrade jupyter ipywidgets
```

### Problemas com ProfileReport

- Use a célula alternativa que salva o relatório em HTML
- Verifique se todas as dependências estão instaladas

## 📊 Resultados

Os resultados desta análise fornecem insights valiosos para:

- **Estratégias de retenção** focadas em clientes de alto risco
- **Políticas de contrato** mais atrativas
- **Programas de fidelização** para novos clientes
- **Modelos preditivos** de churn mais precisos

## 👨‍💻 Autor

**Daniela Medeiros Batista**

---

📌 **Nota:** Este projeto foi desenvolvido como parte de estudos em análise de dados e machine learning, demonstrando técnicas fundamentais de EDA e análise estatística aplicadas a problemas reais de negócio.

