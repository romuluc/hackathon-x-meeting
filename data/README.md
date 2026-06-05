# `data/` — Dados do desafio

> 🔒 **NDA e confidencialidade (Regulamento §06).** Os dados de origem são
> públicos, mas os arquivos disponibilizados para o hackathon foram selecionados,
> curados, organizados e/ou pré-processados pela organização.
>
> Esses arquivos devem ser usados exclusivamente no contexto do desafio. É
> proibido redistribuir, publicar ou compartilhar os datasets pré-processados,
> metadados, anotações ou materiais internos fora dos canais autorizados.

## Acesso aos dados

Os arquivos de dados **não são versionados neste repositório**.

Para evitar consumo de Git LFS e manter o repositório leve, os dados oficiais do
desafio estão disponíveis exclusivamente no Google Drive:

**Link do Drive:** https://drive.google.com/drive/folders/1gNulDlA7ZU1UepV2P1OPRTRdg66LvqTy?usp=drive_link

Após baixar os dados, os participantes devem organizar os arquivos localmente de
acordo com a estrutura disponibilizada no Drive.

## Camadas ômicas do desafio

O desafio envolve a integração de quatro camadas de dados:

| Camada              | O que informa                                                                | Análises típicas                                               |
| ------------------- | ---------------------------------------------------------------------------- | -------------------------------------------------------------- |
| 🧬 **RNA-seq bulk** | Genes mais/menos expressos no tecido como um todo (**âncora** da integração) | Expressão diferencial, enriquecimento de vias, co-expressão    |
| 🔬 **sc/snRNA-seq** | Quais genes são expressos em **cada tipo celular**                           | Clustering, anotação de tipos celulares, deconvolução do bulk  |
| 📊 **ATAC-seq**     | Regiões do genoma **acessíveis** e elementos regulatórios                    | Picos, acessibilidade diferencial, motivos de TF, peak-to-gene |
| 🔩 **BS-seq**       | Regiões com marcas de **metilação** de DNA                                   | DMRs, correlação metilação ↔ expressão                         |

Cada camada captura uma dimensão diferente do sistema; integradas, geram hipóteses
mais robustas sobre produção e composição do leite.

## Dados externos

Dados públicos externos usados para validação, comparação ou enriquecimento das
análises podem ser utilizados, desde que a equipe documente:

* fonte;
* versão;
* data de acesso;
* link ou identificador público;
* justificativa de uso no contexto da solução.

## Boas práticas

* Não envie arquivos grandes para o GitHub.
* Não adicione datasets, arquivos `.fastq`, `.fq`, `.bam`, `.sam`, `.cram`,
  `.bed`, `.bigWig`, `.bw`, `.vcf`, `.csv`, `.tsv`, `.h5ad`, `.rds`, `.zip`,
  `.tar.gz`, `.gz` ou similares ao repositório.
* Trate os dados originais como **somente leitura**.
* Gere resultados sempre por código, de forma reproduzível.
* Confirme a **build do genoma de referência** (*Bos taurus*) e use a mesma em
  todas as camadas.
* A integração das camadas é o objetivo central do desafio — é onde a solução se
  diferencia.

## Observação sobre Git LFS

Este repositório não deve depender de Git LFS para distribuição dos dados do
desafio. O GitHub deve conter apenas código, documentação, instruções e arquivos
leves.
