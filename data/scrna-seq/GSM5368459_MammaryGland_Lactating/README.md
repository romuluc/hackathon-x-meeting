# MammaryGland_Lactating (GSM5368459)

## Referência Transcriptômica Single-Cell da Glândula Mamária Bovina em Lactação

Dataset GEO **GSE176512** · Amostra **GSM5368459** · scRNA-seq · *Bos taurus*

---

## 🧬 Visão Geral

Este repositório contém o dataset **MammaryGland_Lactating (GSM5368459)**, pertencente à série GEO **GSE176512**, um estudo de transcriptômica de célula única (*single-cell RNA sequencing*, scRNA-seq) que gerou um atlas celular de tecidos metabólicos-chave de vacas leiteiras em lactação.

Embora o estudo original tenha analisado múltiplos tecidos bovinos, este repositório é focado exclusivamente na **glândula mamária em lactação**, fornecendo uma referência transcriptômica celular de alta qualidade para aplicações em:

* Produção e composição do leite
* Biologia da lactação
* Fisiologia da glândula mamária
* Anotação de tipos celulares
* Resposta ao estresse térmico (*heat stress*)
* Mastite e imunologia mamária
* Integração multiômica
* Genômica funcional bovina
* Descoberta de biomarcadores
* Inteligência artificial aplicada à agropecuária

O dataset representa tecido mamário bovino saudável em lactação e pode ser utilizado como atlas de referência para análises comparativas e integrativas.

---

## 🐄 Contexto Científico

A glândula mamária bovina é um órgão altamente especializado responsável pela síntese, secreção e regulação imunológica associadas à produção de leite.

A lactação depende da interação coordenada entre diferentes populações celulares, incluindo:

* Células epiteliais luminais
* Células secretoras alveolares
* Células mioepiteliais
* Fibroblastos
* Células endoteliais
* Macrófagos
* Linfócitos T
* Linfócitos B
* Outras populações estromais e imunológicas

Tecnologias de transcriptômica single-cell permitem caracterizar essas populações em resolução celular, possibilitando investigar:

* Heterogeneidade celular
* Programas transcricionais específicos
* Estados funcionais celulares
* Redes regulatórias
* Comunicação intercelular
* Mecanismos associados à produção de leite

Este dataset pode ser utilizado como referência para estudos envolvendo condições fisiológicas, desafios ambientais, infecções, estresse térmico e integração multiômica.

---

## 📋 Informações Gerais

| Campo                | Informação                              |
| -------------------- | --------------------------------------- |
| GEO Series           | GSE176512                               |
| GEO Sample           | GSM5368459                              |
| Título               | MammaryGland_Lactating                  |
| Organismo            | *Bos taurus*                            |
| Raça                 | Holstein                                |
| Tecido               | Glândula Mamária                        |
| Estágio Fisiológico  | Lactação                                |
| Tipo de Experimento  | Single-cell RNA-seq                     |
| Plataforma           | GPL26012 — Illumina NovaSeq 6000        |
| Tecnologia           | 10x Genomics Chromium Single Cell 3' v3 |
| Molécula Analisada   | RNA total                               |
| Genoma de Referência | *Bos taurus* Ensembl v99                |
| Processamento        | Cell Ranger v3.1.0                      |
| Status GEO           | Público desde 04/05/2022                |

---

## 🔬 Desenho Experimental

O estudo original gerou aproximadamente **88 mil células individuais** provenientes de diferentes tecidos metabólicos de vacas leiteiras.

Neste repositório é utilizada exclusivamente a seguinte amostra:

| GEO Sample | Descrição                           |
| ---------- | ----------------------------------- |
| GSM5368459 | Glândula mamária bovina em lactação |

---

## 🧪 Processamento do Tecido

Após a coleta, o tecido mamário passou por um protocolo de dissociação celular para obtenção de uma suspensão unicelular.

### Fluxo Experimental

1. Remoção do tecido adiposo
2. Lavagem em PBS + 5% FBS
3. Incubação com EDTA 20 mM
4. Dissociação enzimática
5. Filtragem em filtros de:

   * 70 μm
   * 30 μm
6. Lavagem e centrifugação
7. Preparação para construção das bibliotecas

---

## 📚 Preparação das Bibliotecas

As bibliotecas foram construídas utilizando:

**10x Genomics Chromium Single Cell 3' Reagent Kits v3**

### Etapas

1. Isolamento celular
2. Encapsulamento individual das células
3. Barcoding molecular
4. Síntese de cDNA
5. Amplificação
6. Construção das bibliotecas
7. Sequenciamento em plataforma Illumina

---

## 🧬 Informações de Sequenciamento

| Campo      | Valor                 |
| ---------- | --------------------- |
| Plataforma | Illumina NovaSeq 6000 |
| Tecnologia | 10x Genomics Chromium |
| Estratégia | scRNA-seq             |
| Biblioteca | 3' Gene Expression    |
| Molécula   | RNA Total             |

---

## ⚙️ Processamento Bioinformático

### Ferramentas Utilizadas

| Ferramenta  | Versão |
| ----------- | ------ |
| Cell Ranger | 3.1.0  |

### Alinhamento

O processamento foi realizado utilizando os parâmetros padrão do Cell Ranger.

**Genoma de referência**

```text
Bos_taurus Ensembl v99
```

---

## 📁 Estrutura dos Arquivos

```text
data/
└── scrna-seq/
    └── GSE176512_mammary_lactating/
        ├── GSM5368459_MammaryGland_Lactating_barcodes.tsv.gz
        ├── GSM5368459_MammaryGland_Lactating_genes.tsv.gz
        ├── GSM5368459_MammaryGland_Lactating_matrix.mtx.gz
        ├── GSM5368459_MammaryGland_cells_Rdata.rds.gz
        └── README.md
```

---

## 📁 Estrutura dos Arquivos

```text
hackathon-x-meeting/
└── data/
    └── scrna-seq/
        └── GSM5368459_MammaryGland_Lactating/
            ├── GSM5368459_MammaryGland_cells_Rdata.rds.gz
            ├── GSM5368459_MammaryGland_Lactating_barcodes.tsv.gz
            ├── GSM5368459_MammaryGland_Lactating_genes.tsv.gz
            ├── GSM5368459_MammaryGland_Lactating_matrix.mtx.gz
            └── README.md
```

---

## 📄 Descrição dos Arquivos

### Arquivos de Entrada (10x Genomics)

| Arquivo                                             | Descrição                                               |
| --------------------------------------------------- | ------------------------------------------------------- |
| `GSM5368459_MammaryGland_Lactating_matrix.mtx.gz`   | Matriz esparsa contendo as contagens gênicas por célula |
| `GSM5368459_MammaryGland_Lactating_genes.tsv.gz`    | Lista de genes presentes na matriz de expressão         |
| `GSM5368459_MammaryGland_Lactating_barcodes.tsv.gz` | Identificadores únicos das células sequenciadas         |

Esses três arquivos correspondem ao formato padrão de saída do **10x Genomics Cell Ranger** e podem ser importados diretamente em ferramentas como:

* Seurat (R)
* Scanpy (Python)
* Bioconductor
* Pegasus
* Cell Ranger

---

## 🧫 Tipos Celulares Esperados

As populações celulares presentes na glândula mamária podem incluir:

### Células Epiteliais

* Células epiteliais luminais
* Células secretoras alveolares
* Células progenitoras mamárias

### Células Estruturais

* Células mioepiteliais
* Fibroblastos
* Endoteliais
* Pericitos

### Células Imunes

* Macrófagos
* Monócitos
* Linfócitos T
* Linfócitos B
* Células dendríticas
* Neutrófilos

A validação das identidades celulares deve ser realizada utilizando genes marcadores específicos.

---

## 🚀 Aplicações Potenciais

### Biologia da Lactação

* Produção de proteínas do leite
* Genes de caseína
* Metabolismo lipídico
* Atividade secretora mamária

### Fisiologia Mamária

* Heterogeneidade celular
* Organização tecidual
* Estados celulares funcionais

### Estudos Comparativos

* Estresse térmico (*heat stress*)
* Mastite
* Infecções virais
* Adaptação ambiental
* Resiliência fisiológica

### Integração Multiômica

Possível integração com:

* RNA-seq bulk
* scRNA-seq
* snRNA-seq
* ATAC-seq
* Metilação de DNA
* Transcriptômica espacial
* Metabolômica

### Ciência de Dados e IA

* Classificação celular
* Transferência de anotação celular
* Anotação automática
* Predição de estados celulares
* Benchmarking de algoritmos
* Integração de datasets single-cell

---

## ⚠️ Limitações

* Apenas uma condição fisiológica (lactação saudável)
* Ausência de desafio infeccioso
* Ausência de estresse térmico experimental
* Possível sub-representação de populações celulares frágeis
* Dados provenientes de uma única amostra mamária

---

## 📖 Publicação Associada

> Wu JJ, Zhu S, Gu F, Valencak TG et al.
>
> Cross-tissue single-cell transcriptomic landscape reveals the key cell subtypes and their potential roles in the nutrient absorption and metabolism in dairy cattle.
>
> *Journal of Advanced Research*. 2022;37:1–18.

**PMID:** 35499046

**DOI:** https://doi.org/10.1016/j.jare.2022.04.003

---

## 🔗 Origem dos Dados

| Campo      | Identificador |
| ---------- | ------------- |
| GEO Series | GSE176512     |
| GEO Sample | GSM5368459    |
| BioSample  | SAMN19647896  |
| SRA        | SRX11105220   |

---

## 👥 Contribuidores

* Wu J
* Zhu S
* Gu F
* Sun H

---

## 📧 Contato

**Jiajin Wu**

Zhejiang University
Hangzhou, Zhejiang, China

E-mail: [wujj@zju.edu.cn](mailto:wujj@zju.edu.cn)

---

*Dataset derivado da série GEO GSE176512 e organizado para utilização no BovOmics Challenge — X-Meeting 2026.*
