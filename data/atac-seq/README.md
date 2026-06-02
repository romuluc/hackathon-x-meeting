# `atacseq/` — Dados de acessibilidade cromatínica

> 🔒 **NDA e confidencialidade.** Os dados disponibilizados foram selecionados,
> curados e pré-processados no contexto do desafio.
>
> Use estes arquivos exclusivamente para as análises autorizadas. Não redistribua,
> publique ou compartilhe os datasets, metadados ou resultados intermediários fora
> dos canais permitidos.

Esta pasta contém resultados de **ATAC-seq** para identificação de regiões de
cromatina acessível no genoma bovino. A análise foi realizada com o genoma de
referência **Bos taurus ARS-UCD2.0**.

## Conteúdo da pasta

| Pasta    | Conteúdo                               | Uso típico                                                                         |
| -------- | -------------------------------------- | ---------------------------------------------------------------------------------- |
| `peaks/` | Arquivos de peaks chamados por amostra | Análise de acessibilidade cromatínica, integração com genes e regiões regulatórias |

Estrutura esperada:

```text id="7sbabh"
atacseq/
└── peaks/
    ├── SRRXXXXXXX_peaks.narrowPeak
    ├── SRRXXXXXXX_peaks.xls
    └── SRRXXXXXXX_summits.bed
```

## Arquivos principais

| Arquivo                    | Descrição                                     | Uso típico                                                           |
| -------------------------- | --------------------------------------------- | -------------------------------------------------------------------- |
| `peaks/*_peaks.narrowPeak` | Regiões genômicas chamadas como peaks         | Interseção com genes, promotores e outras regiões regulatórias       |
| `peaks/*_peaks.xls`        | Tabela detalhada dos peaks chamados pelo MACS | Estatísticas por amostra, ranking por significância e enriquecimento |
| `peaks/*_summits.bed`      | Ponto de maior sinal dentro de cada peak      | Análise de motivos e janelas centradas no summit                     |

## Referência genômica

A análise utilizou:

```text id="djsaj7"
Bos taurus ARS-UCD2.0
GCF_002263795.3_ARS-UCD2.0_genomic.fna
```

## Pipeline resumido

Os dados foram processados a partir de arquivos FASTQ paired-end. As principais
etapas foram:

1. **Controle de qualidade e trimming** com `fastp`
2. **Alinhamento** ao genoma ARS-UCD2.0 com `Bowtie2`
3. **Ordenação, indexação e filtragem** com `SAMtools`
4. **Remoção de duplicatas** com `sambamba`
5. **Filtragem por qualidade de mapeamento** (`MAPQ >= 30`)
6. **Remoção de reads mitocondriais** associadas ao contig `NC_006853.1`
7. **Chamada de peaks** com `MACS2` ou `MACS3`

## Interpretação

Os peaks representam regiões do genoma com maior acessibilidade cromatínica.
Essas regiões podem indicar:

* promotores ativos;
* enhancers;
* elementos regulatórios abertos;
* possíveis sítios de ligação de fatores de transcrição;
* regiões de cromatina menos compactada.

Os arquivos `peaks/*_peaks.narrowPeak` e `peaks/*_peaks.xls` descrevem as regiões
acessíveis completas, enquanto `peaks/*_summits.bed` informa o ponto de maior
sinal dentro de cada peak.

## Dicas de uso

* Trate os arquivos originais como **somente leitura**.
* Gere resultados derivados via scripts em `src/`, garantindo reprodutibilidade.
* Confirme que todas as camadas multiômicas usam a mesma build de referência
  (**Bos taurus ARS-UCD2.0**).
* Para integração com RNA-seq, associe peaks a genes próximos ou regiões
  promotoras.
* Para integração com BS-seq, compare acessibilidade cromatínica com regiões
  diferencialmente metiladas.
* Para análise regulatória, use os summits como entrada para busca de motivos de
  fatores de transcrição.

