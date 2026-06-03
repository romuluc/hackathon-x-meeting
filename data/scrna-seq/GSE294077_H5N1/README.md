# GSE294077 — Resposta Imune de Células Somáticas do Leite Bovino à Infecção por Influenza Aviária H5N1

Dataset GEO **GSE294077** · scRNA-seq · *Bos taurus* · HPAIV bovine-H5N1

---

## 🧬 Visão Geral

Este repositório contém o dataset **GSE294077**, um estudo de transcriptômica de célula única (*single-cell RNA sequencing*, scRNA-seq) que investigou as respostas imunológicas de células somáticas do leite bovino (*Bovine Milk Somatic Cells – bMSCs*) após infecção experimental por Influenza Aviária Altamente Patogênica (**HPAIV H5N1**) isolada de bovinos leiteiros.

O estudo foi motivado pelo surto ocorrido em 2024 nos Estados Unidos, quando o vírus H5N1 foi detectado em vacas leiteiras, causando mastite, alterações na produção de leite e sinais respiratórios, levantando preocupações importantes para a saúde pública e para a indústria leiteira.

Utilizando scRNA-seq, os autores caracterizaram as alterações celulares e imunológicas induzidas pela infecção viral, identificando mudanças na composição celular, ativação de vias inflamatórias e remodelamento da resposta imune mamária.


---

## 🦠 Contexto Científico

O surto de HPAIV H5N1 em bovinos leiteiros ocorrido em 2024 representou um evento sem precedentes, demonstrando que o vírus pode infectar a glândula mamária bovina e ser detectado diretamente no leite.

Diferentemente das infecções por Influenza A anteriormente descritas em bovinos, que geralmente apresentavam caráter subclínico, a infecção por H5N1 resultou em:

* Mastite clínica
* Alterações na produção de leite
* Sintomas respiratórios
* Elevada carga viral no leite

Para compreender os mecanismos celulares envolvidos nessa resposta, os autores realizaram análises de scRNA-seq em células somáticas do leite infectadas in vitro.

---

## 📋 Informações Gerais

| Campo               | Informação                        |
| ------------------- | --------------------------------- |
| GEO Series          | GSE294077                         |
| Organismo           | *Bos taurus*                      |
| Tipo de Experimento | Single-cell RNA-seq               |
| Plataforma          | GPL23055 — Illumina NextSeq 500   |
| Status GEO          | Público desde 08/04/2025          |
| BioProject          | PRJNA1248006                      |
| Tecnologia          | 10x Genomics Single Cell          |
| Tipo Celular        | Bovine Milk Somatic Cells (bMSCs) |

---

## 🧪 Desenho Experimental

As células somáticas foram isoladas a partir de leite cru proveniente de três vacas Holstein-Friesian multíparas.

Após o isolamento, as células foram submetidas a infecção experimental in vitro utilizando:

```text
A/dairy cattle/Kansas/5/2024 (HPAIV bovine-H5N1)
```

O período de infecção foi de:

```text
24 horas
```

Posteriormente as células foram processadas por scRNA-seq.

---

## 🐄 Amostras

| GEO Sample | Descrição                       |
| ---------- | ------------------------------- |
| GSM8898337 | Controle não infectado          |
| GSM8898338 | Infectado com HPAIV bovine-H5N1 |

---

## ⚙️ Estrutura dos Arquivos

```text
hackathon-x-meeting/
└── data/
    └── scrna-seq/
        └── GSE294077_H5N1/
            ├── GSE294077_Final.cloupe
            ├── GSE294077_Final.cloupe.gz
            └── README.md
```

---

## 📄 Descrição dos Arquivos

### Arquivo Principal

| Arquivo                   | Descrição                                                            |
| ------------------------- | -------------------------------------------------------------------- |
| GSE294077_Final.cloupe    | Projeto Cell Ranger Loupe Browser contendo os resultados processados |
| GSE294077_Final.cloupe.gz | Versão compactada do projeto Loupe                                   |

---

## 🧬 Sobre o Arquivo `.cloupe`

O formato `.cloupe` é um arquivo nativo do **10x Genomics Loupe Browser**.

Ele normalmente contém:

* Matriz de expressão gênica
* Clusters celulares
* UMAP
* t-SNE
* PCA
* Metadados celulares
* Marcadores celulares
* Resultados de agrupamento

Para visualizar os dados:

1. Instale o Loupe Browser
2. Abra o arquivo:

```text
GSE294077_Final.cloupe
```

O software permite explorar interativamente:

* Populações celulares
* Expressão gênica
* Clustering
* Genes marcadores
* Distribuição das amostras

---

## 🧫 Populações Celulares Identificadas

O estudo identificou 10 agrupamentos celulares distintos.

Entre os principais tipos celulares observados:

### Células Epiteliais

* Epitélio luminal produtor de leite
* Subtipos epiteliais secretores
* Células associadas à homeostase mamária

### Células Imunes

* Linfócitos T
* Macrófagos
* Células dendríticas

### Outras Populações

* Células somáticas presentes no leite
* Estados celulares associados à resposta antiviral

---

## 🚀 Integração Multiômica Potenciais

Possível integração com:

* GSE176512 (glândula mamária em lactação)
* GSE249950 (estresse térmico em MAC-T)
* GSE317482 (snRNA-seq de estresse térmico)
* ATAC-seq
* Metilação de DNA


---

## 📖 Publicação Associada

> Singh G, Kafle S, Assato P, Goraya M et al.
>
> Single-Cell Analysis of Host Responses in Bovine Milk Somatic Cells (bMSCs) Following HPAIV Bovine H5N1 Influenza Exposure.
>
> Viruses. 2025.

**PMID:** 40573402

---

## 🔗 Origem dos Dados

| Campo       | Identificador          |
| ----------- | ---------------------- |
| GEO Series  | GSE294077              |
| BioProject  | PRJNA1248006           |
| Plataforma  | GPL23055               |
| GEO Samples | GSM8898337, GSM8898338 |

---

## 👥 Contribuidores

* Singh G
* Kafle S
* Assato P
* Goraya M
* Colaboradores

---

## 📧 Contato

**Gagandeep Singh**

Kansas State University
Manhattan, Kansas, USA

E-mail: [gdsdhol@vet.k-state.edu](mailto:gdsdhol@vet.k-state.edu)

---

*Dataset organizado para utilização no BovOmics Challenge — X-Meeting 2026.*
