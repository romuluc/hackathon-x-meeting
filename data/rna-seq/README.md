# GSE249950 — Perfis Transcriptômicos de Células Epiteliais Mamárias Bovinas Sob Estresse Térmico e Durante a Recuperação

## Visão Geral

Este dataset contém dados de RNA-seq gerados a partir da linhagem celular epitelial mamária bovina **MAC-T**, submetida a diferentes condições de diferenciação, estresse térmico (*heat stress*, HS) e recuperação pós-estresse.

O objetivo do estudo foi caracterizar os mecanismos moleculares envolvidos na resposta ao estresse térmico e nos processos de recuperação celular após exposição aguda ao calor, fornecendo uma visão abrangente das alterações transcriptômicas associadas à homeostase celular, síntese de leite, metabolismo, apoptose, proteostase e adaptação ao estresse.

O conjunto de dados é particularmente relevante para estudos envolvendo:

- Estresse térmico em bovinos leiteiros
- Biologia da glândula mamária
- Lactação
- Diferenciação de células epiteliais mamárias
- Resposta ao choque térmico
- Heat Shock Proteins (HSPs)
- Recuperação celular pós-estresse
- Transcriptômica funcional
- Redes regulatórias
- Descoberta de biomarcadores
- Adaptação às mudanças climáticas
- Pecuária de precisão

---

# Informações Gerais

| Campo | Informação |
|----------|----------|
| GEO Series | GSE249950 |
| Título | Transcriptomic Profiles of Bovine Mammary Epithelial Cells Under Heat Stress and During Subsequent Recovery |
| Organismo | *Bos taurus* |
| Tipo de Experimento | Expression profiling by high throughput sequencing |
| Plataforma | GPL26012 — Illumina NovaSeq 6000 |
| Modelo Experimental | Células epiteliais mamárias bovinas MAC-T |
| Status | Público desde 11 de dezembro de 2025 |
| BioProject | PRJNA1051168 |
| Assembly | ARS-UCD1.3 |

---

# Contexto Científico

O estresse térmico é um dos principais fatores ambientais responsáveis por perdas econômicas na indústria leiteira mundial. Além da redução da ingestão alimentar, o calor afeta diretamente a biologia da glândula mamária, comprometendo processos celulares essenciais para a síntese e secreção do leite.

Embora os impactos produtivos do estresse térmico sejam amplamente conhecidos, os mecanismos moleculares responsáveis pela resposta celular ao calor e pelos processos de recuperação ainda permanecem parcialmente compreendidos.

Neste estudo, células epiteliais mamárias bovinas MAC-T foram utilizadas como modelo experimental para investigar:

- Processos de diferenciação lactogênica;
- Respostas imediatas ao estresse térmico;
- Alterações transcriptômicas induzidas pelo calor;
- Mecanismos de recuperação celular após remoção do estressor;
- Potenciais reguladores transcricionais envolvidos na adaptação ao calor.

Foram identificados **1.668 genes diferencialmente expressos (DEGs)** entre os grupos experimentais.

Os principais achados incluem:

- Supressão de programas de diferenciação celular durante o estresse térmico;
- Ativação robusta de genes da família Heat Shock Protein (HSP);
- Alterações em vias relacionadas à síntese lipídica do leite;
- Ativação de mecanismos de dobramento proteico mediado por chaperonas;
- Regulação de apoptose durante a recuperação inicial;
- Enriquecimento de vias associadas à homeostase celular e estresse oxidativo após recuperação prolongada;
- Identificação de potenciais fatores de transcrição reguladores da resposta ao calor.

---

# Desenho Experimental

## Linhagem Celular

| Campo | Informação |
|----------|----------|
| Linhagem | MAC-T |
| Tipo Celular | Epitélio mamário bovino |
| Espécie | *Bos taurus* |

---

## Grupos Experimentais

As células foram divididas em seis condições experimentais.

| Grupo | Descrição |
|----------|----------|
| NHSUD | Não submetidas ao estresse térmico e não diferenciadas |
| NHSD | Não submetidas ao estresse térmico e diferenciadas |
| HSUD | Submetidas ao estresse térmico e não diferenciadas |
| HSD | Submetidas ao estresse térmico e diferenciadas |
| D2R | Diferenciadas, submetidas ao estresse térmico e recuperadas por 2 horas |
| D6R | Diferenciadas, submetidas ao estresse térmico e recuperadas por 6 horas |

---

## Condições de Cultivo

### Meio Basal (Não Diferenciado)

- DMEM alta glicose
- 10% FBS
- 1% Penicilina/Estreptomicina
- 1% L-Glutamina
- 5 μg/mL Insulina
- 1 μg/mL Hidrocortisona

### Meio Lactogênico (Diferenciado)

- Meio basal
- 5% FBS
- 5 μg/mL Prolactina ovina
- 10 μg/mL Dexametasona

---

## Tratamentos de Estresse Térmico

| Condição | Temperatura | Tempo |
|----------|----------|----------|
| Controle | 37°C | 4 dias |
| Heat Stress | 42°C | 1 hora |
| Recuperação D2R | 37°C | 2 horas após HS |
| Recuperação D6R | 37°C | 6 horas após HS |

---

# Amostras

## Tabela de Correspondência das Amostras

| ID na Matriz | Nome Completo |
|----------|----------|
| NHSUD1 | Não Estressada, Não Diferenciada — Réplica 1 |
| NHSUD2 | Não Estressada, Não Diferenciada — Réplica 2 |
| NHSUD3 | Não Estressada, Não Diferenciada — Réplica 3 |
| NHSD1 | Não Estressada, Diferenciada — Réplica 1 |
| NHSD2 | Não Estressada, Diferenciada — Réplica 2 |
| NHSD3 | Não Estressada, Diferenciada — Réplica 3 |
| HSUD1 | Estresse Térmico, Não Diferenciada — Réplica 1 |
| HSUD2 | Estresse Térmico, Não Diferenciada — Réplica 2 |
| HSUD3 | Estresse Térmico, Não Diferenciada — Réplica 3 |
| HSD1 | Estresse Térmico, Diferenciada — Réplica 1 |
| HSD2 | Estresse Térmico, Diferenciada — Réplica 2 |
| HSD3 | Estresse Térmico, Diferenciada — Réplica 3 |
| D2R1 | Recuperação 2h Pós-Estresse Térmico — Réplica 1 |
| D2R2 | Recuperação 2h Pós-Estresse Térmico — Réplica 2 |
| D2R3 | Recuperação 2h Pós-Estresse Térmico — Réplica 3 |
| D6R1 | Recuperação 6h Pós-Estresse Térmico — Réplica 1 |
| D6R2 | Recuperação 6h Pós-Estresse Térmico — Réplica 2 |
| D6R3 | Recuperação 6h Pós-Estresse Térmico — Réplica 3 |

---

# Extração de RNA e Preparação das Bibliotecas

## Material Biológico

| Campo | Informação |
|----------|----------|
| Molécula extraída | polyA RNA |
| Estratégia | RNA-Seq |
| Fonte da biblioteca | Transcriptômica |
| Seleção da biblioteca | cDNA |
| Plataforma | Illumina NovaSeq 6000 |

---

## Extração de RNA

O RNA total foi isolado utilizando:

- TRIzol Reagent (Invitrogen)
- Phasemaker Tubes (Invitrogen)
- RNeasy Mini Kit (Qiagen)

Controle de qualidade:

- NanoDrop 1000
- Agilent 2100 Bioanalyzer

Critérios utilizados:

- Razão 260/280 ≈ 2
- Razão 260/230 ≈ 2
- RIN > 9

---

## Construção das Bibliotecas

Realizada pela Novogene (Sacramento, CA).

Etapas principais:

1. Seleção de mRNA por Poly-T
2. Fragmentação do mRNA
3. Síntese de cDNA
4. Ligação de adaptadores
5. Seleção de fragmentos
6. Amplificação por PCR
7. Sequenciamento paired-end em plataforma Illumina

---

# Processamento Bioinformático

## Controle de Qualidade

| Ferramenta | Versão |
|----------|----------|
| fastp | v0.23.2 |

---

## Alinhamento

| Ferramenta | Versão |
|----------|----------|
| STAR | v2.7.9a |

Genoma de referência:

**ARS-UCD1.3 (Bos taurus)**

---

## Quantificação

| Ferramenta | Versão |
|----------|----------|
| FeatureCounts | v2.0.3 |

---

## Normalização e Estatística

| Ferramenta | Função |
|----------|----------|
| DESeq2 | Normalização e DEGs |
| limma | Remoção de batch effect |
| ClusterGVis | Clustering e GO |
| clusterProfiler | Enriquecimento KEGG |
| ShinyGO | Análise de fatores de transcrição |

---

## Critérios para DEGs

Genes diferencialmente expressos foram definidos como:

- |Fold Change| > 1,5
- p-valor ajustado < 0,1

---

# Aplicações Potenciais

## Resposta ao Estresse Térmico

- Heat Shock Proteins (HSPs)
- Proteostase
- Estresse oxidativo
- Hipóxia celular

## Lactação

- Síntese de lipídios do leite
- Diferenciação mamária
- Produção leiteira

## Redes Regulatórias

- Fatores de transcrição
- Regulação gênica
- Resposta ao calor

## Desenvolvimento de Biomarcadores

- Resiliência térmica
- Eficiência produtiva
- Saúde mamária

## Integração Multiômica

Integração potencial com:

- RNA-seq bulk
- snRNA-seq
- scRNA-seq
- ATAC-seq
- Metilação de DNA
- Metabolômica

---

# Estrutura dos Arquivos

O arquivo inclui:

- Matrizes de contagem gênica bruta


Formatos comuns:

```text
counts_matrix.tsv
metadata.tsv
sample_information.tsv
```

---

# Referências

## GEO Series

**GSE249950**

Transcriptomic Profiles of Bovine Mammary Epithelial Cells Under Heat Stress and During Subsequent Recovery

## BioProject

**PRJNA1051168**

---

# Contribuidores

- Yu X
- Harman RM
- Danev N
- Li G
- Fang Y
- Van de Walle GR
- Duan JE

---

# Contato

**Guangsheng Li**

Department of Animal Science  
Cornell University  
Ithaca, NY, USA

E-mail: gl357@cornell.edu