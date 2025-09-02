A qualidade de um sinal proveniente de um satélite e recebido por uma antena GNSS tem um impacto crucial no desempenho de uma estação GNSS. Existem vários factores que podem influenciar a qualidade do sinal e que são apresentados nas secções seguintes.

## Visibilidade do Céu

As estações GNSS devem estar localizadas em locais com obstruções mínimas acima do horizonte local. Acima de 10° de elevação, a estação não deve apresentar obstruções. O recetor deve ser configurado para rastrear todos os satélites dentro de uma máscara de elevação de 0°.

## Multitrajetos

A interferência por multitrajetos ocorre quando um sinal GNSS chega à antena por diferentes caminhos. O sinal chega uma vez directamente do satélite e adicionalmente após ter sido reflectido noutras superfícies.
As fontes de multitrajetos podem ser naturais ou artificiais. A lista seguinte apresenta possíveis fontes conhecidas por gerar multitrajetos fortes.

Fontes Artificiais:

- Painéis e sinais metálicos
- Telhados
- Paredes de edifícios
- Vedações
- Painéis solares

Fontes Naturais:

- Árvores (especialmente húmidas)
- Superfícies de água como lagos, rios, etc.

Evite estes elementos reflectores nas estações GNSS. As fontes suspeitas de multitrajetos devem estar a pelo menos 20 metros da antena GNSS e abaixo de 5° de elevação.

## Fontes de Interferência de Radiofrequência

Fontes comuns de Interferência de Radiofrequência (RFI) incluem:

- Emissores de rádio, televisão e redes móveis,
- Ligações de dados por micro‑ondas,
- Linhas de energia,
- Transformadores.

Transmissores direccionais, especialmente ligações por micro‑ondas apontadas em direcção à estação CORS, podem causar interferência significativa. Entre outros parâmetros, o efeito da RFI é função da frequência, da potência radiada e da distância à fonte. O efeito da RFI aumenta significativamente quando a RFI é uma harmónica de uma frequência de sinal GNSS.

Portanto, é difícil definir uma distância de segurança relativamente a uma fonte de RFI. A RFI pode ser difícil de confirmar e pode ser necessário o aconselhamento de especialistas se houver suspeita de RFI. Se a RFI for confirmada e não puder ser mitigada numa estação CORS proposta, deve ser considerado um local alternativo.

!!! note "Nota"

As fontes de RFI não afectam apenas os sinais GNSS recebidos na antena, mas também a transmissão sem fios (rádio ou rede móvel) dos dados da estação. Quando uma estação CORS transmite dados por uma ligação rádio, a transmissão em si pode ser uma fonte de RFI nos sinais GNSS da antena.

Antes da instalação final de um monumento, recomenda‑se testar o ambiente de multitrajetos e verificar se existem fontes de RFI no local. Isto pode ser feito instalando temporariamente o equipamento GNSS num tripé e investigando a qualidade dos dados.
