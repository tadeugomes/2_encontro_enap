# Análise de Padrões Salariais por CBO, Gênero e Região

## Principais Descobertas

### 1. Salários por Ocupação (CBO)
- Médico clínico: R$10.486,47 (maior salário médio)
- Analista de desenvolvimento de sistemas: R$9.562,41
- Administrador: R$6.454,97
- Técnico em administração: R$5.673,69
- Técnico de suporte ao usuário de TI: R$2.909,88
- Técnico de enfermagem: R$3.004,51 (menor salário médio)

### 2. Diferenças de Gênero
As maiores diferenças salariais entre homens e mulheres foram encontradas em:
1. Administração: Homens ganham 25,9% mais que mulheres
2. Técnico em administração: Homens ganham 22,9% mais que mulheres
3. Técnico de suporte ao usuário de TI: Homens ganham 12,2% mais que mulheres
4. Analista de desenvolvimento de sistemas: Homens ganham 10,6% mais que mulheres
5. Médico clínico: Homens ganham 6,8% mais que mulheres
6. Técnico de enfermagem: Homens ganham 5,2% mais que mulheres

### 3. Salários por Região
- Centro-Oeste: R$6.263,41 (maior salário médio regional)
- Sudeste: R$5.888,07
- Sul: R$5.550,39
- Nordeste: R$3.875,90
- Norte: R$3.557,64 (menor salário médio regional)

### 4. Recomendação sobre Agrupamento
Com base na análise:
- Todos os estados (exceto um com dados insuficientes) possuem mais de 1.000 registros
- A maioria dos estados tem dados suficientes para análise individual
- **Recomendação**: Pode-se analisar por UF individualmente, pois a maioria tem dados suficientes

### 5. Análise Detalhada por Categoria Profissional (CBO)

#### 5.1. Resultados da Análise de Diferenças Salariais por CBO

| Ocupação | Código CBO | Salário Médio Homens | Salário Médio Mulheres | Diferença Salarial |
|----------|------------|---------------------|------------------------|-------------------|
| Administrador | 252105 | R$ 7.317,85 | R$ 5.811,94 | 25,91% |
| Técnico em administração | 351305 | R$ 6.357,20 | R$ 5.173,03 | 22,89% |
| Técnico de suporte ao usuário de TI | 317210 | R$ 2.979,33 | R$ 2.654,62 | 12,23% |
| Analista de desenvolvimento de sistemas | 212405 | R$ 9.766,16 | R$ 8.826,88 | 10,64% |
| Médico clínico | 225125 | R$ 10.818,07 | R$ 10.133,35 | 6,76% |
| Técnico de enfermagem | 322205 | R$ 3.137,05 | R$ 2.981,36 | 5,22% |

#### 5.2. Análise por Área de Atuação

1. **Administração**: 24,40% de diferença salarial média
2. **Tecnologia da Informação**: 11,44% de diferença salarial média
3. **Saúde**: 5,99% de diferença salarial média

#### 5.3. Análise por Nível de Formação

1. **Superior**: 14,44% de diferença salarial média
2. **Operacional**: 13,45% de diferença salarial média

#### 5.4. Análise por Características de Gênero

1. **Equilibrada com tendência feminina**: 25,91%
2. **Equilibrada**: 22,89%
3. **Tradicionalmente masculina**: 9,88%
4. **Tradicionalmente feminina**: 5,22%

## Arquivos Gerados
1. `salario_por_cbo.png` - Gráfico de salários por ocupação
2. `comparacao_genero_cbo.png` - Comparação de gênero por ocupação
3. `salario_por_regiao.png` - Salários médios por região
4. `distribuicao_salarios_regiao.png` - Distribuição de salários por região
5. `salario_medio_por_cbo.csv` - Dados detalhados de salários por CBO
6. `diferenca_genero_por_cbo.csv` - Análise de diferenças salariais por gênero
7. `salario_medio_por_regiao.csv` - Salários médios por região
8. `distribuicao_por_regiao_cbo.csv` - Distribuição de trabalhadores por região e ocupação
9. `analise_diferencas_salariais_por_cbo_resumo.csv` - Resumo da análise de diferenças salariais por CBO
10. `analise_diferencas_salariais_por_cbo.csv` - Dados detalhados da análise de diferenças salariais por CBO
11. `relatorio_diferencas_salariais_por_cbo.md` - Relatório detalhado da análise por CBO
12. `diferencas_salariais_por_cbo.png` - Gráfico de diferenças salariais por CBO
13. `comparacao_salarios_cbo.png` - Comparação de salários homens vs mulheres por CBO
14. `diferencas_salariais_por_area.png` - Diferenças salariais por área de atuação
15. `diferencas_salariais_por_genero.png` - Diferenças salariais por características de gênero

## Conclusões

1. Existe uma diferença salarial significativa entre homens e mulheres em todas as ocupações analisadas
2. As maiores diferenças são encontradas nas áreas de administração
3. As regiões Centro-Oeste, Sudeste e Sul apresentam salários mais elevados
4. As áreas de saúde (médicos) e tecnologia da informação (analistas) apresentam os maiores salários
5. **As maiores desigualdades salariais** ocorrem nas áreas de administração, mesmo em ocupações consideradas equilibradas em termos de gênero
6. **As menores desigualdades** são encontradas nas ocupações predominantemente femininas, como o técnico de enfermagem
7. **A área de saúde** apresenta as menores diferenças salariais, sugerindo maior equidade de gênero nesse setor
8. **A área de tecnologia** mostra diferenças moderadas, com maior desigualdade nas posições operacionais

## Recomendações

1. Investigue fatores estruturais nas áreas de administração que contribuem para as altas diferenças salariais
2. Promova políticas de transparência salarial para identificar e corrigir disparidades
3. Analise a progressão de carreira de homens e mulheres nas diferentes ocupações para entender os pontos de divergência
4. Realize uma análise mais aprofundada com técnicas estatísticas avançadas, como a decomposição Oaxaca-Blinder, para isolar os componentes explicados e não explicados da diferença salarial
5. Considere a realização de estudos qualitativos para complementar os achados quantitativos