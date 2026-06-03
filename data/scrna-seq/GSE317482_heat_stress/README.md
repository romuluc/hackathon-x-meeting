# 🔬 GSE317482 — Atlas Single-Nucleus da Glândula Mamária Bovina Sob Estresse Térmico

snRNA-seq · **Bos taurus** · Glândula mamária bovina · Resolução celular

---

## 📖 Visão Geral

Este dataset contém dados de **single-nucleus RNA sequencing (snRNA-seq)** obtidos a partir de biópsias de glândula mamária bovina coletadas sob condições de:

* Termoneutralidade (TN)
* Estresse térmico (HS — *Heat Stress*)
* Pair-Fed (PF)

O objetivo do estudo foi caracterizar, em resolução celular, como o estresse térmico altera programas transcricionais, estados celulares, trajetórias de diferenciação, comunicação intercelular e redes regulatórias na glândula mamária bovina.

O dataset fornece um atlas celular abrangente das populações epiteliais, imunes e estromais envolvidas na resposta ao calor e nos mecanismos associados à redução da produção leiteira.

---

## 🎯 Relevância para o Hackathon

Este dataset pode ser utilizado para:

| Aplicação                | Objetivo                                          |
| ------------------------ | ------------------------------------------------- |
| 🔬 Anotação Celular      | Identificação de tipos celulares mamários         |
| 🧬 Expressão Diferencial | Resposta celular ao estresse térmico              |
| 🥛 Lactação              | Regulação de genes associados à produção de leite |
| 📈 Trajetórias Celulares | Diferenciação e pseudotempo                       |
| 🔗 Comunicação Celular   | Interações ligante-receptor                       |
| 🧠 Redes Regulatórias    | Inferência de fatores de transcrição              |
| 🌡️ Heat Stress          | Biomarcadores de adaptação térmica                |
| 🔄 Integração Multiômica | Integração com RNA-seq, ATAC-seq e BS-seq         |

---

## 📋 Informações Gerais

| Campo               | Informação                                         |
| ------------------- | -------------------------------------------------- |
| GEO Series          | GSE317482                                          |
| Organismo           | *Bos taurus*                                       |
| Tipo de experimento | Expression profiling by high throughput sequencing |
| Tecnologia          | Single-Nucleus RNA Sequencing (snRNA-seq)          |
| Plataforma          | Illumina NovaSeq X Plus                            |
| Status              | Público desde 18/05/2026                           |
| Assembly            | ARS-UCD1.2                                         |
| Pré-publicação      | BioRxiv                                            |

---

## 🧬 Contexto Biológico

O estresse térmico é um dos principais fatores que limitam a produtividade da pecuária leiteira mundial.

Embora os impactos fisiológicos sejam amplamente conhecidos, os mecanismos celulares específicos envolvidos na resposta mamária ao calor permanecem pouco compreendidos.

Utilizando snRNA-seq, este estudo investigou:

* Alterações de estados celulares induzidas pelo calor;
* Remodelamento da diferenciação epitelial;
* Alterações em programas secretores;
* Respostas de proteostase;
* Comunicação célula-célula;
* Ativação de fatores de transcrição específicos;
* Mudanças em vias associadas à lactação.

---

## 🔬 Desenho Experimental

Após os tratamentos experimentais, biópsias mamárias foram coletadas do quarto posterior direito de vacas leiteiras.

Os núcleos celulares foram isolados dos tecidos e submetidos ao sequenciamento de RNA nuclear.

### Grupos Experimentais

| Grupo | Descrição                       |
| ----- | ------------------------------- |
| TN    | Condição termoneutra            |
| HS    | Estresse térmico                |
| PF    | Pair-Fed (controle nutricional) |

---

## 📂 Correspondência das Amostras

| GEO Sample | Descrição                                        |
| ---------- | ------------------------------------------------ |
| GSM9472939 | Glândula mamária bovina — Termoneutralidade (TN) |
| GSM9472940 | Glândula mamária bovina — Estresse térmico (HS)  |
| GSM9472941 | Glândula mamária bovina — Pair-Fed (PF)          |

### Importância do Grupo Pair-Fed

O grupo PF foi incluído para separar:

* efeitos diretos do estresse térmico;
* efeitos indiretos decorrentes da redução da ingestão alimentar.

Essa estratégia permite identificar alterações verdadeiramente associadas ao calor.

---

## 🧫 Populações Celulares Identificadas

O estudo identificou **14 clusters celulares distintos**, incluindo:

### Populações Epiteliais

* Células luminais
* Células alveolares
* Células hormone-sensing
* Estados secretores intermediários

### Populações Imunes

* Macrófagos
* Linfócitos
* Outras células imunes residentes

### Populações Estromais

* Fibroblastos
* Células do microambiente mamário

---

## 🧬 Material Biológico e Sequenciamento

| Campo                 | Informação                              |
| --------------------- | --------------------------------------- |
| Molécula extraída     | RNA nuclear                             |
| Estratégia            | RNA-Seq                                 |
| Fonte da biblioteca   | Transcriptômica single-cell             |
| Seleção               | cDNA                                    |
| Tecnologia            | 10x Genomics Chromium Single Cell 3' v4 |
| Plataforma            | Illumina NovaSeq X Plus                 |
| Tipo de leitura       | Paired-End                              |
| Comprimento das reads | 150 bp                                  |

---

## ⚙️ Preparação das Bibliotecas

As biópsias congeladas pertencentes ao mesmo tratamento foram agrupadas (*pooled*) antes do isolamento nuclear.

Fluxo experimental:

1. Isolamento de núcleos celulares;
2. Encapsulamento e barcode pelo sistema 10x Genomics;
3. Síntese de cDNA;
4. Amplificação do cDNA;
5. Construção das bibliotecas;
6. Controle de qualidade por Bioanalyzer;
7. Sequenciamento Illumina.

---

## 💻 Processamento Bioinformático

### Pipeline

| Etapa                  | Ferramenta        |
| ---------------------- | ----------------- |
| Processamento primário | CellRanger v9.0.1 |
| Parâmetros             | Default           |
| Assembly               | ARS-UCD1.2        |

### 📁 Estrutura dos Dados

```text
data/
└── scrna-seq/
    └── GSE317482_heat_stress/
        ├── README.md
        │
        ├── GSM9472939_thermoneutrality/
        │   ├── GSM9472939_barcodes.tsv.gz
        │   ├── GSM9472939_features.tsv.gz
        │   └── GSM9472939_matrix.mtx.gz
        │
        ├── GSM9472940_HS_heatstress/
        │   ├── GSM9472940_HS_barcodes.tsv.gz
        │   ├── GSM9472940_HS_features.tsv.gz
        │   └── GSM9472940_HS_matrix.mtx.gz
        │
        └── GSM9472941_pairfed/
            ├── GSM9472941_PF_barcodes.tsv.gz
            ├── GSM9472941_PF_features.tsv.gz
            └── GSM9472941_PF_matrix.mtx.gz
```

#### Descrição dos Arquivos

Cada condição experimental contém uma matriz de expressão gênica gerada por single-nucleus RNA sequencing (snRNA-seq), armazenada no formato padrão do ecossistema 10x Genomics.

| Arquivo           | Descrição                                             |
| ----------------- | ----------------------------------------------------- |
| `barcodes.tsv.gz` | Lista de núcleos/células identificados no experimento |
| `features.tsv.gz` | Lista de genes anotados na matriz                     |
| `matrix.mtx.gz`   | Matriz esparsa de contagens gênicas (genes × núcleos) |

---

#### Condições Experimentais

| Diretório                     | GEO Sample | Condição               |
| ----------------------------- | ---------- | ---------------------- |
| `GSM9472939_thermoneutrality` | GSM9472939 | Termoneutralidade (TN) |
| `GSM9472940_HS_heatstress`    | GSM9472940 | Estresse térmico (HS)  |
| `GSM9472941_pairfed`          | GSM9472941 | Controle Pair-Fed (PF) |

---

#### Correspondência dos Grupos Experimentais

| Sigla | Descrição                                                                                              |
| ----- | ------------------------------------------------------------------------------------------------------ |
| TN    | Vacas mantidas em condição termoneutra                                                                 |
| HS    | Vacas submetidas ao estresse térmico                                                                   |
| PF    | Grupo Pair-Fed utilizado para controlar os efeitos da redução do consumo alimentar induzida pelo calor |

---

#### Formato dos Dados

As matrizes seguem o formato padrão da plataforma 10x Genomics e podem ser carregadas diretamente em ferramentas amplamente utilizadas para análise de transcriptômica de célula única:

##### R / Seurat

```r
library(Seurat)

tn <- Read10X("GSM9472939_thermoneutrality/")
hs <- Read10X("GSM9472940_HS_heatstress/")
pf <- Read10X("GSM9472941_pairfed/")
```

##### Python / Scanpy

```python
import scanpy as sc

adata_tn = sc.read_10x_mtx(
    "GSM9472939_thermoneutrality",
    var_names="gene_symbols"
)

adata_hs = sc.read_10x_mtx(
    "GSM9472940_HS_heatstress",
    var_names="gene_symbols"
)

adata_pf = sc.read_10x_mtx(
    "GSM9472941_pairfed",
    var_names="gene_symbols"
)
```

---

#### Observações

* Os dados foram gerados utilizando a plataforma Illumina NovaSeq X Plus.
* O dataset contém núcleos isolados de tecido mamário bovino (snRNA-seq).
* As matrizes representam contagens gênicas brutas.
* Recomenda-se realizar filtragem de qualidade, remoção de dupletos, normalização e integração entre condições antes das análises comparativas.
* O grupo Pair-Fed (PF) permite distinguir efeitos metabólicos decorrentes da redução de ingestão alimentar daqueles causados diretamente pelo estresse térmico.


---

## 🚀 Possíveis Análises

### Identificação de Tipos Celulares

* Clustering
* UMAP
* t-SNE
* Anotação celular

### Expressão Diferencial

Comparações possíveis:

* HS vs TN
* HS vs PF
* PF vs TN

### Pseudotempo

Ferramentas recomendadas:

* Monocle3
* Slingshot
* scVelo

### Comunicação Intercelular

* CellChat
* CellPhoneDB
* LIANA

### Redes Regulatórias

* SCENIC
* pySCENIC
* DoRothEA

### Integração Multiômica

Integração potencial com:

* RNA-seq bulk
* scRNA-seq
* ATAC-seq
* BS-seq
* Metabolômica

---

## 🛠️ Ferramentas Recomendadas

### Ecossistema R

* Seurat
* SingleCellExperiment
* Monocle3
* CellChat
* SCENIC
* clusterProfiler

### Ecossistema Python

* Scanpy
* scvi-tools
* Squidpy
* CellPhoneDB
* PySCENIC
* scVelo

---

## 📚 Referências

### GEO Series

**GSE317482**

Single-nucleus RNA sequencing reveals cell type-specific response to heat stress in bovine mammary gland

### Preprint

Yu X et al.

Single-nucleus RNA sequencing reveals cell type-specific response to heat stress in bovine mammary gland.

BioRxiv (2026)

---

## 👥 Contribuidores

* Yu X
* Shambhvi F
* A. Ceballos D
* M. Ferreira M
* Zapata A
* Seneviratne N
* Pokharel S
* Fang Y
* Li G
* Leal-Yepes F
* W. McFadden J
* Duan J

---

## 📧 Contato

**Jingyue (Ellie) Duan**

Cornell University
Ithaca, New York, USA

E-mail: [jd774@cornell.edu](mailto:jd774@cornell.edu)
