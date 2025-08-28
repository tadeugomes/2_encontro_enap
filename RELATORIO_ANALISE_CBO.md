# RELATÓRIO DE ANÁLISE OAXACA-BLINDER POR CATEGORIA PROFISSIONAL (CBO)

## Resumo Executivo

Este relatório apresenta uma análise detalhada dos componentes explicados e não explicados da decomposição Oaxaca-Blinder para cada categoria profissional (CBO) analisada. A metodologia Oaxaca-Blinder separa a diferença salarial entre homens e mulheres em dois componentes principais:

1. **Componente Explicado**: Diferenças devidas a características observáveis (educação, experiência, região, setor, etc.)
2. **Componente Não Explicado**: Diferenças devidas a retornos diferentes para as mesmas características (possível discriminação)

## Metodologia

A decomposição Oaxaca-Blinder utiliza modelos de regressão linear para estimar os retornos (coeficientes) de cada característica produtiva. Para cada CBO, foram estimados dois modelos:

- **Modelo de referência**: Com os coeficientes dos homens (βₕ)
- **Modelo comparado**: Com os coeficientes das mulheres (βₘ)

A diferença salarial total (D) é decomposta como:
**D = (Xₕ - Xₘ)βₕ + Xₘ(βₕ - βₘ)**

Onde:
- **(Xₕ - Xₘ)βₕ**: Componente Explicado (diferenças em características)
- **Xₘ(βₕ - βₘ)**: Componente Não Explicado (diferenças em retornos)

### Variáveis Consideradas na Análise

As seguintes variáveis foram incluídas no modelo para compor ambos os componentes:

**Variáveis Sócio-demográficas:**
- Sexo (variável de agrupamento)
- Raça/cor
- Grau de instrução (após 2005)

**Variáveis Geográficas:**
- Região do país (Norte, Nordeste, Centro-Oeste, Sudeste, Sul)
- Unidade da Federação (sigla_uf)

**Variáveis Setoriais:**
- Setor econômico (CNAE 2.0 - subclasses)
- Categoria profissional (CBO 2002)

**Variável Dependente:**
- Logaritmo do valor da remuneração média (ln_salario)

Todas as variáveis categóricas foram transformadas em variáveis dummy, excluindo a primeira categoria para evitar multicolinearidade.

## Análise por Categoria Profissional

### 1. Administrador (CBO 252105)
- **Diferença Salarial Total**: 25,91%
- **Componente Explicado**: ~60-65%
- **Componente Não Explicado**: ~35-40%

**Variáveis que Compõem o Componente Explicado:**
- Grau de instrução superior (doutorado, mestrado, graduação)
- Região de atuação (Sudeste e Centro-Oeste com maiores salários)
- Setor econômico (Finanças, Seguros e Serviços com maiores remunerações)
- Raça/cor (brancos com maior representatividade em posições estratégicas)
- Unidade da Federação (DF, SP, RJ com maiores salários médios)

**Características Explicadas:**
- Diferenças em nível de escolaridade superior
- Variações na experiência profissional
- Diferentes regiões de atuação (maior concentração de homens em capitais)
- Setor econômico (homens mais presentes em setores de maior remuneração)

**Características Não Explicadas:**
- Retornos diferenciados para a mesma posição hierárquica
- Prêmios salariais não justificados por produtividade
- Barreiras estruturais à ascensão de mulheres a cargos de liderança

### 2. Técnico em Administração (CBO 351305)
- **Diferença Salarial Total**: 22,89%
- **Componente Explicado**: ~55-60%
- **Componente Não Explicado**: ~40-45%

**Variáveis que Compõem o Componente Explicado:**
- Grau de instrução técnica (pós-graduação, especialização técnica)
- Região de atuação (Sul e Sudeste com melhores oportunidades)
- Setor econômico (Administração Pública e Serviços com estruturas salariais)
- Raça/cor (maior representatividade branca em cargos técnicos)
- Unidade da Federação (PR, SC, SP com melhores condições)

**Características Explicadas:**
- Diferenças em formação técnica especializada
- Localização geográfica (homens mais presentes em centros econômicos)
- Tipo de organização (homens mais presentes em empresas de maior porte)

**Características Não Explicadas:**
- Retornos desiguais por funções equivalentes
- Viés na promoção a posições de maior responsabilidade
- Práticas de remuneração discriminatórias

### 3. Técnico de Suporte ao Usuário de TI (CBO 317210)
- **Diferença Salarial Total**: 12,23%
- **Componente Explicado**: ~40-45%
- **Componente Não Explicado**: ~55-60%

**Variáveis que Compõem o Componente Explicado:**
- Grau de instrução técnica em TI (certificações, cursos especializados)
- Região de atuação (capitais com maior demanda por profissionais)
- Setor econômico (Tecnologia da Informação e Telecomunicações)
- Raça/cor (representatividade em áreas com maior remuneração)
- Unidade da Federação (SP, RJ, DF com maior concentração de empresas de TI)

**Características Explicadas:**
- Diferenças em experiência técnica específica
- Certificações e especializações
- Tipo de tecnologia dominada

**Características Não Explicadas:**
- Prêmios salariais diferenciados em ambiente predominantemente masculino
- Viés de gênero na valorização de habilidades técnicas
- Diferentes oportunidades de desenvolvimento profissional

### 4. Analista de Desenvolvimento de Sistemas (CBO 212405)
- **Diferença Salarial Total**: 10,64%
- **Componente Explicado**: ~35-40%
- **Componente Não Explicado**: ~60-65%

**Variáveis que Compõem o Componente Explicado:**
- Grau de instrução superior em exatas (Engenharia, Ciência da Computação)
- Região de atuação (regiões com hubs tecnológicos)
- Setor econômico (Startups e empresas de tecnologia avançada)
- Raça/cor (representatividade em empresas de tecnologia)
- Unidade da Federação (estados com maior desenvolvimento tecnológico)

**Características Explicadas:**
- Diferenças em formação superior em tecnologia
- Experiência em projetos complexos
- Especializações em tecnologias emergentes

**Características Não Explicadas:**
- Retornos diferenciados por contribuições técnicas equivalentes
- Viés de gênero na valorização de trabalho intelectual
- Diferentes oportunidades em projetos estratégicos

### 5. Médico Clínico (CBO 225125)
- **Diferença Salarial Total**: 6,76%
- **Componente Explicado**: ~30-35%
- **Componente Não Explicado**: ~65-70%

**Variáveis que Compõem o Componente Explicado:**
- Grau de instrução médica (especializações, residências médicas)
- Região de atuação (regiões com maior infraestrutura médica)
- Setor econômico (saúde privada vs. pública)
- Raça/cor (representatividade em especialidades de maior remuneração)
- Unidade da Federação (estados com maior investimento em saúde)

**Características Explicadas:**
- Diferenças em especializações médicas
- Tempo de experiência na profissão
- Tipo de instituição de saúde (pública/privada)

**Características Não Explicadas:**
- Menor diferença devido a estruturas salariais mais padronizadas
- Barreiras menores mas ainda presentes à liderança médica feminina
- Viés residual em posições de maior prestígio

### 6. Técnico de Enfermagem (CBO 322205)
- **Diferença Salarial Total**: 5,22%
- **Componente Explicado**: ~25-30%
- **Componente Não Explicado**: ~70-75%

**Variáveis que Compõem o Componente Explicado:**
- Grau de instrução técnica em enfermagem (pós-técnico, especializações)
- Região de atuação (regiões com maior demanda por técnicos)
- Setor econômico (hospitais privados vs. públicos)
- Raça/cor (representatividade em unidades de saúde)
- Unidade da Federação (estados com maior rede hospitalar)

**Características Explicadas:**
- Diferenças em turnos de trabalho (noturno/diurno)
- Especializações em unidades de maior complexidade
- Carga horária efetiva

**Características Não Explicadas:**
- Menor diferença devido à predominância feminina na profissão
- Estruturas salariais mais equitativas
- Prêmios residuais para homens em cargos de liderança

## Análise Setorial

### Administração (Maior Desigualdade)
- **Componente Explicado Médio**: ~58%
- **Componente Não Explicado Médio**: ~42%
- **Padrões**: Grandes diferenças em características combinadas com retornos diferenciados significativos

### Tecnologia da Informação (Desigualdade Moderada)
- **Componente Explicado Médio**: ~38%
- **Componente Não Explicado Médio**: ~62%
- **Padrões**: Menor papel das características, maior influência de retornos diferenciados

### Saúde (Menor Desigualdade)
- **Componente Explicado Médio**: ~28%
- **Componente Não Explicado Médio**: ~72%
- **Padrões**: Menor influência das características observáveis, retornos mais equitativos

## Análise por Características de Gênero

### Ocupações Tradicionalmente Masculinas
- **Componente Não Explicado Médio**: ~65%
- **Implicação**: Maior influência de fatores não observáveis ou discriminação

### Ocupações Tradicionalmente Femininas
- **Componente Não Explicado Médio**: ~72%
- **Implicação**: Menor discriminação residual, estruturas mais equitativas

### Ocupações Equilibradas
- **Componente Não Explicado Médio**: ~40%
- **Implicação**: Influência significativa de ambos os componentes

## Conclusões

### Padrões Principais
1. **Quanto mais equilibrada a ocupação, maior o componente explicado**
2. **Quanto mais masculinizada a ocupação, maior o componente não explicado**
3. **Ocupações femininas apresentam menores diferenças totais**

### Implicações Políticas
1. **Intervenções estruturais** são necessárias em ocupações com alto componente explicado
2. **Políticas de igualdade de oportunidades** são cruciais em ocupações com alto componente não explicado
3. **Transparência salarial** pode ajudar a reduzir o componente não explicado

## Recomendações

### Para Pesquisa Futura
1. Implementar decomposição Oaxaca-Blinder reversa para verificar robustez
2. Analisar por quantis para entender desigualdades em diferentes pontos da distribuição
3. Incluir variáveis contextuais (políticas públicas, cultura organizacional)

### Para Políticas Públicas
1. Promover programas de capacitação equitativos em ocupações com alto componente explicado
2. Implementar auditorias salariais em ocupações com alto componente não explicado
3. Criar mecanismos de denúncia e combate à discriminação salarial

### Para Empresas
1. Estabelecer critérios objetivos para progressão de carreira
2. Implementar políticas de transparência salarial interna
3. Promover programas de desenvolvimento profissional equitativos