Esta secção apresenta uma visão geral das recomendações obrigatórias e desejáveis que uma CORS deve cumprir para aderir à rede IGS. Destinam‑se a ser aplicáveis tanto às estações IGS actualmente activas como às estações propostas. O cumprimento integral destas Diretrizes é claramente desejado pelo IGS; contudo, quando as diretrizes não puderem ser integralmente cumpridas, pede‑se aos operadores das estações que consultem a Comissão de Infraestruturas do IGS. Informações detalhadas sobre as recomendações apresentadas podem ser encontradas nos capítulos seguintes destas Diretrizes.

!!! info "Legenda"

:material-check-bold: Esta característica é requisito mínimo.

:fontawesome-solid-triangle-exclamation: Esta característica é encorajada mas não é obrigatória.

:x: Esta característica não é recomendada.

## Geral


| Recomendação                                                                                          | Classificação                          |
| ------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| A estação pertence a uma rede geodésica nacional ou regional                                         | :fontawesome-solid-triangle-exclamation: |
| Estação planeada e instalada para operação contínua e permanente                                   | :material-check-bold:                    |
| A agência operadora da estação mantém total capacidade para reparar, atualizar e manter a estação | :material-check-bold:                    |

## Fundação e Localização


| Recomendação                                                    | Classificação       |
| ----------------------------------------------------------------- | --------------------- |
| Base de rocha sólida ou betão maciço                           | :material-check-bold: |
| Montada em edifícios ou estruturas semelhantes[^2]               | :x:                   |
| Vista de céu desobstruída com poucas obstruções acima de 10° | :material-check-bold: |
| Local livre de obstruções de sinal ou interferências de RF     | :material-check-bold: |
| Local livre de materiais reflectores                              | :material-check-bold: |

## Monumentação e Montagem


| Recomendação                                                                                                                 | Classificação       |
| ------------------------------------------------------------------------------------------------------------------------------ | --------------------- |
| Monumentos em pilar de betão ou suportes (tri‑, quad‑, ...)-pod                                                             | :material-check-bold: |
| (Suportes de aço) fixados ao edifício                                                                                        | :x:                   |
| O suporte fixa a antena no lugar para manter a orientação e o nível                                                         | :material-check-bold: |
| O suporte permite que a antena seja removida e recolocada dentro de 0.5 mm e 1° da sua localização e orientação originais | :material-check-bold: |

## Energia e Comunicação


| Recomendação                                                               | Classificação                          |
| ---------------------------------------------------------------------------- | ---------------------------------------- |
| Garantir o funcionamento contínuo de todos os dispositivos de comunicação | :fontawesome-solid-triangle-exclamation: |
| Garantir acesso remoto controlado ao recetor                                | :material-check-bold:                    |

## Recetor


| Recomendação                                                                                                                      | Classificação                          |
| ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| Rastreamento de código e fase da portadora para todos os sinais GNSS[^3]                                                           | :material-check-bold:                    |
| Registo contínuo de dados GNSS brutos                                                                                              | :fontawesome-solid-triangle-exclamation: |
| Transmissão de dados em tempo real (RTCM)                                                                                          | :fontawesome-solid-triangle-exclamation: |
| Rastreamento de todos os satélites visíveis (saudáveis e não saudáveis) com uma elevação mínima de 5° (0° é recomendado) | :material-check-bold:                    |
| Desactivação da suavização de pseudo‑distância e fase                                                                         | :material-check-bold:                    |
| Desactivação da mitigação de multitrajetos                                                                                      | :material-check-bold:                    |
| Capacidade de armazenar uma quantidade razoável de dados brutos (dependendo das circunstâncias locais)                            | :material-check-bold:                    |

## Antena


| Recomendação                                                                                                                    | Classificação                          |
| --------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| Uso de uma antena com centro de fase absoluto calibrado pelo IGS (calibração média) conforme incluído no ANTEX oficial do IGS | :material-check-bold:                    |
| Centro de fase absoluto da antena calibrado individualmente                                                                       | :fontawesome-solid-triangle-exclamation: |
| Antena nivelada e orientada dentro de 5° para o Norte verdadeiro                                                                 | :material-check-bold:                    |
| Protecção por radome da antena                                                                                                  | :x:                                      |

## Dados


| Recomendação                                                                                                     | Classificação       |
| ------------------------------------------------------------------------------------------------------------------ | --------------------- |
| Os dados devem ser fornecidos em formato RINEX[^4]                                                                 | :material-check-bold: |
| ^^Os dados em tempo real devem estar disponíveis^^<br>RTCM 3 MSM5 *stream* para aplicações em tempo real[^6] | :material-check-bold: |
| Os dados devem ser reenviados aos centros de dados após uma interrupção de comunicação                        | :material-check-bold: |
| Os dados RINEX devem ser gerados no recetor ^^ou^^ a partir do ficheiro binário nativo                            | :material-check-bold: |
| Mínimo de completude do ficheiro                                                                                  | 99%                   |

### Ficheiros RINEX de Alta Taxa


| Recomendação     |             | Classificação                          |
| ------------------ | ----------- | ---------------------------------------- |
| Disponibilização |             | :fontawesome-solid-triangle-exclamation: |
| Latência          | < 5 minutos | :material-check-bold:                    |
| Taxa de amostragem | 1 Hz        | :material-check-bold:                    |
| Duração          | 15 minutos  | :material-check-bold:                    |

### Ficheiros RINEX Horários


| Recomendação     |             | Classificação                          |
| ------------------ | ----------- | ---------------------------------------- |
| Disponibilização |             | :fontawesome-solid-triangle-exclamation: |
| Latência          | < 5 minutos | :material-check-bold:                    |
| Taxa de amostragem | 30 segundos | :material-check-bold:                    |

### Ficheiros RINEX Diários


| Recomendação     |              | Classificação       |
| ------------------ | ------------ | --------------------- |
| Disponibilização |              | :material-check-bold: |
| Latência          | < 30 minutos | :material-check-bold: |
| Taxa de amostragem | 30 segundos  | :material-check-bold: |

## Metadados


| Recomendação                                                                                                | Classificação       |
| ------------------------------------------------------------------------------------------------------------- | --------------------- |
| Metadados completos e actualizados no formato de registo de estação IGS/GeodesyML                           | :material-check-bold: |
| Identificador único de nove caracteres da estação aprovado pelo IGS                                        | :material-check-bold: |
| Atribuição de um número único DOMES do IERS                                                               | :material-check-bold: |
| Actualização do registo de estação IGS no prazo de 24 horas após as alterações efectuadas na estação | :material-check-bold: |
| O cabeçalho RINEX corresponde à informação no registo de metadados do IGS                                 | :material-check-bold: |
| Disponibilização de fotografias da instalação da antena nas 4 direcções cardeais (N, E, S, O)           | :material-check-bold: |

[^1]: Obrigatório para CORS regionais no âmbito da APREF, EPN e SIRGAS.
    
[^2]: Dispensas podem ser concedidas após revisão pelo SPC.
    
[^3]: As novas estações devem rastrear todos os códigos de frequência e fases de portadora disponíveis.
    
[^4]: Para novas estações: RINEX 3.04 é a versão mínima aceite. RINEX 2.11 não é aceite.
    
[^5]: As novas estações são fortemente encorajadas a fornecer fluxos em tempo real.
    
[^6]: MSM7 é preferível.
