# 📊 Análise e Inserção de Dados Totvs

Este projeto visa realizar o tratamento e análise de dados com informações de clientes e histórico de propostas da TOTVS.

---

## ⚙️ Tecnologias Utilizadas

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- SQLAlchemy
- PyOD (para detecção de outliers)
- Jupyter Notebook

---

## 📁 Estrutura dos Dados

### 1. `dados_clientes.csv`

Contém informações de clientes da base Totvs.

**Principais etapas de tratamento:**

- Classificação de produtos em nichos com base em palavras-chave
- Conversão de tipos de dados para categorias, strings, datas e floats
- Identificação e Tratamento de valores nulos
- Identificação e Tratamento de outliers

### 2. `historico.csv`

Contém o histórico de propostas e vendas.

**Principais etapas de tratamento:**

- Conversão de tipos de dados para categorias, strings, datas e floats
- Identificação e Tratamento de valores nulos
- Identificação de outliers, utilizando o K-Nearest Neighbors (KNN) para detecção
- Tratamento de outliers por Winsorização

---

## 📈 Análises Realizadas

- Boxplots por nicho de produtos e por variáveis financeiras
- Cálculo de limites para outliers com IQR
- Comparação de valores antes e depois da remoção de outliers
- Análise exploratória com gráficos descritivos

---

## 🗄️ Conexão e Inserção no Banco de Dados

No final do processo, os DataFrames tratados (`df_clientes_varejo_att`, `df_historico`) são preparados para inserção em um banco de dados SQL utilizando a biblioteca `SQLAlchemy`. A string de conexão é montada com `urllib.parse`, e os dados são enviados com o método `to_sql()` do pandas.

> ⚠️ **Atenção:** A conexão ao banco exige credenciais seguras e não estão incluída diretamente no notebook por motivos de privacidade.

---

## 🚀 Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/bonett1/totvs-analise.git
   cd totvs-analise
   ```

2. Crie um ambiente virtual e ative:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   venv\\Scripts\\activate  # Windows
   ```

3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

4. Execute o notebook no Jupyter:
   ```bash
   jupyter notebook
   ```

---

## 📌 Autores

[LinkedIn Pedro Bonetti](https://www.linkedin.com/in/pedro-bonetti/) – Estagiário de Business Intelligence do Freto
[LinkedIn Gabriel Zaki](https://www.linkedin.com/in/gabrielzaki/) - Assistende de Negócios da SuperSim
[LinkedIn Rafael da Guia](https://www.linkedin.com/in/rafadaguia/) - Cientista de Dados da Minsait
[LinkedIn Arthur Colombo](https://www.linkedin.com/in/arthurcolombomello/) - Analista de Business Intelligence da Soul Trade Marketing
[LinkedIn Júlio César](https://www.linkedin.com/in/julio-cesar-data/) - Estudante de Ciência de Dados

*Todos os autores são alunos do curso de Ciência de Dados da FIAP*