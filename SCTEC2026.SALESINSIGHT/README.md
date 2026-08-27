# SalesInsight

## Sobre o projeto

O **SalesInsight** é um projeto de análise e visualização de dados de vendas desenvolvido em **Python**.

O projeto carrega, limpa, transforma, agrega e visualiza um dataset de vendas, gerando métricas por período, produto, categoria e região. Também realiza uma segmentação de clientes por faixa de gasto e uma projeção de tendências futuras.

Além disso, o projeto demonstra conceitos de **Orientação a Objetos**, incluindo herança, e utiliza cálculos de percentis para análise estatística.

## O que o projeto analisa

* Receita total e volume de vendas por mês e por trimestre
* Top produtos e categorias por receita
* Desempenho por região
* Segmentação de clientes por nível de gasto: **Bronze, Prata e Ouro**
* Relação entre quantidade vendida e receita por transação
* Projeção de receita futura utilizando média móvel
* Percentis (quartis) da receita total
* Relatório de limpeza de dados
* Exportação de relatórios em **CSV e JSON**
* Exportação de gráficos em **PNG**

## Conceitos aplicados

### Lógica e fundamentos

* Variáveis, tipos e operadores
* Estruturas condicionais
* Listas, tuplas e dicionários
* Funções, parâmetros e retorno
* Docstrings
* Lambda e funções de ordem superior
* Leitura e escrita de arquivos CSV e JSON
* Módulo `datetime`
* Expressões regulares com `re`

### Pandas

* Series e DataFrames
* Filtros
* `groupby`
* Transformações
* `merge`
* `pivot`

### NumPy

* Arrays
* Operações vetorizadas
* Broadcasting
* Cálculo de percentis

### Visualização de dados

Utilização de **Matplotlib** e **Seaborn** para criação de:

* Gráficos de linha
* Gráficos de barras
* Gráficos de dispersão
* Histogramas
* Subplots
* Gráficos de barras agrupados
* Exportação de gráficos

### Orientação a Objetos

* Classes
* Construtor
* Atributos
* Métodos
* Herança
* Utilização de `super()`

### Versionamento

* Git e GitHub
* Branches
* Commits
* GitFlow simplificado

## Como executar

### Google Colab — recomendado

1. Abra o notebook `salesinsight.ipynb` no **Google Colab**.
2. Faça o upload do arquivo `.ipynb` ou abra-o diretamente caso ele já esteja disponível no Google Drive.
3. No menu superior, acesse **Ambiente de execução (Runtime)**.
4. Selecione **Executar tudo (Run all)**.

O notebook irá gerar o dataset fictício, realizar o processamento dos dados, gerar os gráficos e exportar os resultados para a pasta `outputs/`.

### Localmente com VS Code

1. Instale o **Python 3.10+** e o **Visual Studio Code**.
2. Instale as dependências:

```bash
pip install pandas numpy matplotlib seaborn
```

3. Execute o script Python:

```bash
python salesinsight.py
```

## Estrutura do projeto

```text
SCTEC2026.SALESINSIGHT/
│
├── salesinsight.ipynb       # Notebook principal com o fluxo completo
├── salesinsight.py          # Versão Python exportada do notebook
├── image/
│   └── background.png
├── README.md                # Documentação do projeto
│
└── outputs/
    ├── metricas_por_mes.csv
    ├── segmentacao_clientes.csv
    ├── estatisticas_gerais.json
    │
    └── graficos/
        ├── receita_por_mes.png
        ├── top_produtos.png
        ├── quantidade_vs_receita.png
        ├── painel_resumo.png
        ├── histograma_receita.png
        └── receita_vs_meta_regiao.png
```

## Decisões técnicas

Uma decisão técnica importante foi remover os registros com `data_venda` inválida e valores nulos críticos, como `quantidade` e `preco_unitario`.

Embora fosse possível tentar imputar esses valores, a remoção foi escolhida para garantir a **integridade dos cálculos de receita e das análises temporais**, evitando a introdução de vieses ou distorções causadas por dados sintéticos ou incompletos.

A precisão dessas métricas é fundamental para apoiar decisões de negócio.

## Melhorias futuras

Foram identificados alguns pontos que podem ser aprimorados em versões futuras do projeto:

* Melhorar o tratamento de dados nulos
* Aprimorar o tratamento de datas inválidas
* Padronizar os nomes dos clientes
* Implementar testes automatizados

Essas melhorias contribuiriam para aumentar a qualidade, confiabilidade e robustez da análise.

## Ferramentas utilizadas

* **Python 3.10+**
* **Google Colab**
* **Visual Studio Code**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **re**
* **json**
* **datetime**
* **os**
* **random**
* **Git**
* **GitHub**

## Vídeo de demonstração

🎥 **Apresentação do projeto:**
(https://drive.google.com/file/d/1cFDK6NRcI5Opo9SOYwyjIFd8FxUTwasc/view?usp=sharing)

## Autor

**Otávio Augusto Reis Nascimento**

Projeto desenvolvido como parte das atividades acadêmicas do curso.
