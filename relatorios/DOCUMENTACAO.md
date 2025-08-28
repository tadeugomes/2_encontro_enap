# Documentação do Projeto de Análise de Dados RAIS

## Visão Geral

Este projeto tem como objetivo analisar dados da RAIS (Relação Anual de Informações Sociais) com foco em padrões salariais por ocupação (CBO), gênero e região. O projeto utiliza a base de dados do basedosdados para extrair, processar e analisar informações sobre trabalhadores de diferentes áreas.

## Estrutura do Projeto

```
2_encontro_enap/
├── baixar_dados_por_CBO.py          # Script para download de dados filtrando por CBOs
├── analisar_salarios.py             # Análise inicial de salários
├── analisar_padroes.py              # Análise detalhada de padrões
├── DOCUMENTACAO.md                  # Esta documentação
├── RELATORIO_ANALISE.md             # Relatório de análise
├── cbos_estudo_comparativo.csv      # Arquivo com CBOs para análise
├── dados/                           # Pasta com dados baixados e resultados
│   ├── rais_todos_cbos.csv          # Dados brutos baixados
│   ├── dicionario_rais_todos_cbos.csv
│   ├── *.png                        # Gráficos gerados
│   └── *.csv                        # Arquivos de análise
└── dicionario/                      # Dicionários e referências
    └── cnaes_ti_export.csv
```

## Scripts Desenvolvidos

### 1. baixar_dados_por_CBO.py

**Objetivo**: Baixar dados da RAIS filtrando por CBOs específicos do arquivo `cbos_estudo_comparativo.csv`

**Características**:
- Lê CBOs do arquivo CSV
- Filtra dados para o ano de 2023
- Inclui CBOs das áreas de Tecnologia da Informação, Administração e Saúde
- Salva dados em `dados/rais_todos_cbos.csv`

**CBOs incluídos**:
- 2124-05: Analista de desenvolvimento de sistemas (TI)
- 3172-10: Técnico de suporte ao usuário de TI (TI)
- 2521-05: Administrador (Administração)
- 3513-05: Técnico em administração (Administração)
- 2251-25: Médico clínico (Saúde)
- 3222-05: Técnico de enfermagem (Saúde)

### 2. analisar_salarios.py

**Objetivo**: Análise inicial de padrões salariais

**Análises realizadas**:
- Salário médio por CBO
- Salário médio por CBO e gênero
- Salário médio por região
- Salário médio por região e gênero
- Distribuição de trabalhadores por UF

### 3. analisar_padroes.py

**Objetivo**: Análise detalhada com visualizações

**Resultados**:
- Gráficos de salários por CBO
- Comparação de gênero por ocupação
- Salários por região
- Distribuição de salários por região
- Arquivos CSV detalhados com todas as análises

## Principais Descobertas

### Salários por Ocupação
1. Médico clínico: R$10.486,47
2. Analista de desenvolvimento de sistemas: R$9.562,41
3. Administrador: R$6.454,97
4. Técnico em administração: R$5.673,69
5. Técnico de suporte ao usuário de TI: R$2.909,88
6. Técnico de enfermagem: R$3.004,51

### Diferenças Salariais por Gênero
As maiores diferenças percentuais foram:
1. Administração: Homens ganham 25,9% mais
2. Técnico em administração: Homens ganham 22,9% mais
3. Técnico de suporte ao usuário de TI: Homens ganham 12,2% mais

### Salários por Região
1. Centro-Oeste: R$6.263,41
2. Sudeste: R$5.888,07
3. Sul: R$5.550,39
4. Nordeste: R$3.875,90
5. Norte: R$3.557,64

## Recomendações sobre Agrupamento

Após análise dos dados, foi possível concluir que:
- Todos os estados possuem dados suficientes para análise individual (>1000 registros)
- **Recomendação**: É viável analisar os dados por UF individualmente

## Como Executar

### Pré-requisitos
```bash
pip install basedosdados pandas numpy matplotlib seaborn
```

### Passo a passo
1. Executar o script de download:
```bash
python baixar_dados_por_CBO.py
```

2. Executar análise inicial:
```bash
python analisar_salarios.py
```

3. Executar análise detalhada:
```bash
python analisar_padroes.py
```

## Arquivos Gerados

### Dados Brutos
- `dados/rais_todos_cbos.csv`: Dados principais (1.770.700 registros)
- `dados/dicionario_rais_todos_cbos.csv`: Dicionário de dados

### Resultados de Análise
- `dados/salario_medio_por_cbo.csv`: Salários por ocupação
- `dados/diferenca_genero_por_cbo.csv`: Diferenças de gênero
- `dados/salario_medio_por_regiao.csv`: Salários por região
- `dados/distribuicao_por_regiao_cbo.csv`: Distribuição por região e ocupação

### Visualizações
- `dados/salario_por_cbo.png`: Gráfico de salários por ocupação
- `dados/comparacao_genero_cbo.png`: Comparação de gênero por ocupação
- `dados/salario_por_regiao.png`: Salários por região
- `dados/distribuicao_salarios_regiao.png`: Distribuição de salários por região

## Metodologia

### Fonte de Dados
Os dados foram obtidos através da plataforma basedosdados, utilizando a tabela `br_me_rais.microdados_vinculos` com os seguintes filtros:
- Vínculo ativo em 31/12 (`vinculo_ativo_3112 = '1'`)
- Ano 2023 (`ano = 2023`)
- CBOs específicos das áreas de interesse

### Tratamento de Dados
- Remoção de registros com UF inválida
- Mapeamento de códigos para nomes descritivos
- Agrupamento por diferentes dimensões (CBO, região, gênero)
- Cálculo de médias e diferenças percentuais

## Limitações

1. Os dados representam vínculos formais registrados na RAIS
2. Não incluem trabalhadores informais ou autônomos
3. Os salários são médios e podem não refletir a totalidade da remuneração
4. A classificação por CBO pode não capturar todas as nuances das funções

## Próximos Passos

1. Análise mais detalhada por faixas salariais
2. Correlação com nível de instrução
3. Análise temporal comparando diferentes anos
4. Estudo das representatividades proporcionais por gênero em cada área
5. Cruzamento com dados de CNAE para análise setorial mais detalhada

## Contato

Para dúvidas ou sugestões sobre este projeto, entre em contato com a equipe responsável.
## Análise de Diferenças Salariais por Categoria Profissional (CBO)

Esta análise examina especificamente as diferenças salariais entre homens e mulheres em diferentes categorias profissionais (CBOs), permitindo identificar padrões setoriais e ocupacionais.

### Metodologia

A análise utiliza os dados agregados da RAIS já processados, comparando os salários médios de homens e mulheres em cada categoria profissional selecionada. As categorias foram escolhidas para representar diferentes áreas de atuação e níveis de formação.

### Principais Resultados

1. **Diferença salarial média**: 13.94% em favor dos homens
2. **Maior diferença**: Administrador (25.91%)
3. **Menor diferença**: Técnico de enfermagem (5.22%)

### Análise por Área de Atuação

- **Administração**: 24.40% de diferença salarial média
- **Tecnologia da Informação**: 11.44% de diferença salarial média
- **Saúde**: 5.99% de diferença salarial média

### Análise por Características de Gênero

As ocupações com maior predominância feminina mostraram menor diferença salarial:
- **Tradicionalmente feminina**: 5.22%
- **Tradicionalmente masculina**: 9.88%
- **Equilibrada**: 22.89%

### Interpretação

Os resultados sugerem que mesmo em ocupações predominantemente femininas, a desigualdade salarial ainda existe, embora em menor magnitude. As áreas de administração mostram as maiores diferenças salariais, independentemente da característica de gênero da ocupação.

### Limitações

Esta análise é descritiva e não controla por fatores como experiência, carga horária, tamanho da empresa ou localização geográfica. Uma análise mais aprofundada utilizando técnicas como a decomposição Oaxaca-Blinder seria necessária para isolar os componentes explicados e não explicados da diferença salarial.
