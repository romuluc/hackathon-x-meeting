# 🔥 GSE249950 — Estresse Térmico e Recuperação em Células Mamárias Bovinas (MAC-T)

RNA-seq bulk · **Bos taurus** · Células epiteliais mamárias bovinas (MAC-T)

---

## 📖 Visão Geral

Este dataset contém perfis transcriptômicos obtidos por RNA-seq da linhagem celular bovina **MAC-T**, submetida a diferentes estados de diferenciação, estresse térmico (*heat stress*) e recuperação pós-estresse.

O estudo foi desenvolvido para investigar os mecanismos moleculares associados à:

- diferenciação lactogênica;
- resposta celular ao calor;
- ativação de Heat Shock Proteins (HSPs);
- proteostase;
- apoptose;
- homeostase celular;
- recuperação após estresse térmico.

Foram identificados **1.668 genes diferencialmente expressos (DEGs)** entre os grupos experimentais.

---

## 🎯 Relevância para o Hackathon

Este dataset pode ser utilizado para:

| Aplicação | Objetivo |
|------------|------------|
| 🧬 RNA-seq diferencial | Identificar genes responsivos ao estresse térmico |
| 🥛 Lactação | Investigar vias relacionadas à síntese de leite |
| 🔥 Heat Stress | Caracterizar mecanismos de adaptação ao calor |
| 🧠 Redes regulatórias | Inferir fatores de transcrição associados ao HS |
| 📊 Integração multiômica | Integrar com scRNA-seq, snRNA-seq, ATAC-seq e BS-seq |
| 🐄 Produção animal | Identificar biomarcadores de resiliência térmica |

---

## 📋 Informações Gerais

| Campo | Informação |
|---------|---------|
| GEO Series | GSE249950 |
| BioProject | PRJNA1051168 |
| Organismo | *Bos taurus* |
| Tipo de experimento | Expression profiling by high throughput sequencing |
| Plataforma | Illumina NovaSeq 6000 |
| Status | Público desde 11/12/2025 |

---

## 🧫 Modelo Experimental

### Linhagem Celular

| Campo | Informação |
|---------|---------|
| Linhagem | MAC-T |
| Tipo celular | Epitélio mamário bovino |
| Espécie | *Bos taurus* |

---

## 🔬 Desenho Experimental

As células foram divididas em seis condições experimentais.

| Grupo | Descrição |
|---------|---------|
| NHSUD | Não estressada e não diferenciada |
| NHSD | Não estressada e diferenciada |
| HSUD | Estresse térmico e não diferenciada |
| HSD | Estresse térmico e diferenciada |
| D2R | Recuperação por 2h após estresse térmico |
| D6R | Recuperação por 6h após estresse térmico |

### Condições Experimentais

| Tratamento | Temperatura | Duração |
|------------|------------|------------|
| Controle | 37°C | 4 dias |
| Heat Stress | 42°C | 1 hora |
| Recuperação D2R | 37°C | 2 horas |
| Recuperação D6R | 37°C | 6 horas |

---

## 🧪 Composição dos Meios

### Meio Basal

- DMEM alta glicose
- 10% FBS
- 1% Penicilina/Estreptomicina
- 1% L-Glutamina
- 5 μg/mL Insulina
- 1 μg/mL Hidrocortisona

### Meio Lactogênico

- Meio basal
- 5% FBS
- 5 μg/mL Prolactina ovina
- 10 μg/mL Dexametasona

---

## 📂 Correspondência das Amostras

### Nomes encontrados na matriz

| Amostra | Descrição |
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

## 🧬 Extração de RNA

### Material Biológico

| Campo | Informação |
|---------|---------|
| Molécula extraída | polyA RNA |
| Estratégia | RNA-Seq |
| Biblioteca | cDNA |
| Plataforma | Illumina NovaSeq 6000 |

### Controle de Qualidade

Critérios utilizados:

- RNA Integrity Number (RIN) > 9
- Razão 260/280 ≈ 2
- Razão 260/230 ≈ 2

Ferramentas utilizadas:

- NanoDrop 1000
- Agilent 2100 Bioanalyzer

---

## ⚙️ Processamento Bioinformático

### Pipeline

| Etapa | Ferramenta |
|---------|---------|
| QC | fastp v0.23.2 |
| Alinhamento | STAR v2.7.9a |
| Quantificação | FeatureCounts v2.0.3 |
| Normalização | DESeq2 |
| Correção de Batch | limma |



### Critérios para DEGs

```text
|Fold Change| > 1.5
Adjusted p-value < 0.1
```

---

## 🚀 Possíveis Análises

### Expressão Diferencial

- NHSD vs NHSUD
- HSD vs NHSD
- HSD vs D2R
- HSD vs D6R

### Enriquecimento Funcional

- GO
- KEGG
- Reactome

### Redes Regulatórias

- Heat Shock Factors (HSFs)
- HSPs
- Reguladores da lactação

### Integração Multiômica

Integração potencial com:

- RNA-seq bulk
- scRNA-seq
- snRNA-seq
- ATAC-seq
- BS-seq
- Metabolômica

---

## 📁 Estrutura dos Arquivos

```text
data/
└── RNA/
    ├── GSE249950_MACT_count.txt
    └── README.md
```

---

## 📚 Referência

### GEO Series

**GSE249950**

Transcriptomic Profiles of Bovine Mammary Epithelial Cells Under Heat Stress and During Subsequent Recovery

### BioProject

**PRJNA1051168**

---

## 👥 Contribuidores

- Yu X
- Harman RM
- Danev N
- Li G
- Fang Y
- Van de Walle GR
- Duan JE

---

## 📧 Contato

**Guangsheng Li**  
Department of Animal Science  
Cornell University  
Ithaca, New York, USA

E-mail: gl357@cornell.edu