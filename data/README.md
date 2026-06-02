# `data/` — Dados do desafio

> ⚠️ **NDA (Regulamento §06).** Os datasets da JBS são de **uso exclusivo e
> restrito** ao período do hackathon. É **proibido baixar, copiar, compartilhar
> ou publicar** esses dados fora do ambiente controlado. **Nada aqui dentro vai
> para o Git** — o `.gitignore` versiona só a estrutura de pastas, não os dados.

Coloque os arquivos recebidos da JBS na pasta da camada correspondente. Cada
camada captura uma dimensão diferente do sistema; integradas, geram hipóteses
mais robustas sobre produção e composição do leite.

## As 4 camadas

| Pasta | Camada | O que informa | Análises típicas |
|---|---|---|---|
| `rna-seq/` | 🧬 **RNA-seq bulk** | Genes mais/menos expressos no tecido como um todo (**âncora** da integração) | Expressão diferencial, enriquecimento de vias, co-expressão |
| `scrna-seq/` | 🔬 **sc/snRNA-seq** | Quais genes são expressos em **cada tipo celular** | Clustering, anotação de tipos celulares, deconvolução do bulk |
| `atac-seq/` | 📊 **ATAC-seq** | Regiões do genoma **acessíveis** (elementos regulatórios) | Picos, acessibilidade diferencial, motivos de TF, peak-to-gene |
| `bs-seq/` | 🔩 **BS-seq** | Regiões com marcas de **metilação** de DNA | DMRs, correlação metilação ↔ expressão |

Dados públicos externos (validação cross-cohort) podem ir em `data/external/` —
crie a pasta se for usar e **documente a fonte, versão e data** (§07).

## Dicas

- Trate os dados originais como **somente leitura**; gere resultados sempre via
  código em `src/` para que tudo seja reproduzível.
- Confirme a **build do genoma de referência** (*Bos taurus*) e use a mesma em
  todas as camadas, para que coordenadas (ATAC/BS-seq) e genes (RNA-seq) batam.
- A integração das camadas é o objetivo central do desafio — é onde a solução se
  diferencia.
