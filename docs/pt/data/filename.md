O IGS suporta actualmente três versões principais do padrão RINEX: RINEX v.2, RINEX v.3 e RINEX v.4. Todos os operadores são encorajados a enviar os dados na versão principal/menor mais recente disponível no recetor. Novas CORS IGS propostas devem submeter no mínimo os seus dados em RINEX 3.04.

## RINEX v.4/v.3

Os ficheiros [RINEX v.3](https://files.igs.org/pub/data/format/rinex305.pdf) e [RINEX v.4](https://files.igs.org/pub/data/format/rinex_4.01.pdf) devem ser transmitidos de acordo com a seguinte convenção de nomes:

*Ficheiros de Observação e Ficheiros Meteorológicos*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_FRU_DT.fff.cmp`

*Ficheiros de Navegação*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_DT.fff.cmp`

Todos os elementos do corpo principal do nome do ficheiro devem conter letras maiúsculas ASCII ou números e todos os elementos têm um comprimento fixo e são separados por um sublinhado “_”. Os campos de tipo de ficheiro e de compressão (extensão) utilizam um ponto “.” como separador e devem ser caracteres ASCII minúsculos. Os campos devem ser preenchidos com zeros para completar a largura do campo.
Para reduzir ainda mais o tamanho dos ficheiros de observação, deve ser utilizado o [toolkit de compressão Hatanaka](https://terras.gsi.go.jp/ja/crx2rnx.html).

=== "SSSSMRCCC"
Nome da Estação IGS de nove caracteres

- SSSS: nome da estação com 4 caracteres
- M: número do monumento ou marcador (0‑9)
- R: número do recetor (0‑9)
- CCC: código ISO‑3166 do país ou região (alfa‑3)

Exemplo: POTS00DEU

Nota: Para alinhar com o formato SINEX, números de monumento e marcador diferentes de 0 não são actualmente suportados
                                                                                                                                                               |
=== "S"
Origem dos dados

Suportados: R (do recetor usando software do fornecedor ou outro) e S (RTCM ou outro formato de fluxo)
=== "YYYYDDDHHMM"

Hora de início

- YYYY: ano gregoriano (por exemplo, 2024)
- DDD: dia do ano (por exemplo, 260)
- HHMM: horas e minutos do dia (por exemplo, 1000)

É preferível utilizar a hora nominal de início do ficheiro. No entanto, utilizar a hora real de início do ficheiro é aceitável.

=== "DDU"
Período do ficheiro

- DD: período do ficheiro
- U: unidade do período do ficheiro
- Aceites: 15M, 01H, 01D
=== "FRU"
Frequência dos dados

- FR: frequência dos dados
- U: unidade da frequência
- Aceites: 01S para dados de alta taxa e 30S ou 15S para dados horários/diários

Não é necessário para ficheiros RINEX de navegação
=== "DT"
Tipo de dados

- Dois caracteres representam o tipo
- D: sistema de satélites (permitidos: G, R, E, C, J, S, I e M (mistos))
- T: tipo de ficheiro RINEX (permitidos: O, N, M)

Exemplo: MO
=== "fff"
Formato do ficheiro. Suportados: rnx (RINEX) e crx (RINEX comprimido)

=== "cmp"
Formato de compressão. Suportado: gzip (gz).

## RINEX v.2

Os dados RINEX v.2 (Gurtner, 2007) devem ser transmitidos de acordo com a seguinte convenção de nomes:

`ssssdddf.yyt`

A tabela abaixo descreve cada elemento desta convenção de nomes. As estações que transmitem ficheiros RINEX v.2 são encorajadas a fornecer ficheiros comprimidos em gzip. Mesmo que os ficheiros sejam enviados em compressão Z, os centros de dados IGS irão recomprimi‑los e torná‑los publicamente disponíveis utilizando gzip.

=== "ssss"
O nome da estação IGS de 4 caracteres

Exemplo: pots
=== "ddd"
Dia do ano do primeiro registo

Exemplo: 260
=== "f"
Número ou carácter de sequência do ficheiro dentro do dia

- Ficheiros diários (30 segundos): f=0
- Ficheiros horários (30 segundos):
    - f=a (00:00:00 a 00:59:30),
    - f=b (01:00:00 a 01:59:30), 
    - ...
    - f=x (23:00:00 a 23:59:30)
- Ficheiros de alta taxa (15M, 1 Hz):
    - f=a00 (00:00:00 a 00:14:59)
    - f=a15 (00:15:00 a 00:29:59) ...
    - f=m30 (12:30:00 a 12:44:59) ...
    - f=x45 (23:45:00 a 23:59:59)
=== "yy"
Ano com dois dígitos (por exemplo, 24)

=== "t"
Tipo de ficheiro. Os tipos permitidos são:

- O: ficheiro de observação
- D: ficheiro de observação comprimido Hatanaka
- N: ficheiro de navegação GPS
- G: ficheiro de navegação GLONASS
- M: ficheiro meteorológico
