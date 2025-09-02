Os metadados GNSS são a informação sobre o local, incluindo a propriedade, contactos, informações sobre o monumento, as coordenadas do local e um historial do equipamento instalado. Metadados fiáveis e actualizados são essenciais para a gestão e utilização de uma estação GNSS e são da responsabilidade do operador da estação.

## Registo de Estação IGS/GeodesyML

O IGS exige que as CORS registem e mantenham os seus metadados num registo de estação IGS (ASCII) ou em formato GeodesyML, e que os metadados sejam disponibilizados ao IGS e a todos os utilizadores. O IGS utiliza uma [aplicação web](https://slm.igs.org) para manter os metadados das estações.

É obrigatório que os metadados sejam completos e publicados para todas as CORS, a fim de fornecer um método consistente de distribuição das informações relevantes do local aos centros de análise e aos utilizadores. Um operador de CORS pode necessitar de manter metadados adicionais do local para ajudar na gestão e operação internas.

Todas as estações IGS são identificadas por um código único de nove caracteres. Os primeiros quatro caracteres devem ser globalmente únicos, e o nome é geralmente escolhido para indicar o subúrbio, a cidade ou a localidade. O operador GNSS deve verificar com o Coordenador da Rede IGS que o identificador de quatro caracteres proposto para uma nova CORS não está já em uso. Além disso, cada CORS IGS precisa de solicitar um [número DOMES do IERS](domes-request). Certifique‑se de que o código de quatro caracteres pretendido não foi já utilizado para outras técnicas geodésicas consultando a [lista de números DOMES](domes-list).

## Cabeçalhos RINEX

Os cabeçalhos RINEX devem corresponder às informações registadas no registo de estação IGS. Os ficheiros RINEX devem ser reenviados em caso de discrepâncias nos metadados. Todas as informações no cabeçalho RINEX devem ser codificadas em ASCII. A utilização de caracteres de outros padrões de codificação (por exemplo, diacríticos em UTF‑8) pode levar a um deslocamento dos elementos do cabeçalho durante a descodificação. A tabela abaixo lista os elementos de cabeçalho RINEX obrigatórios fornecidos para cada ficheiro RINEX.


| Elemento de Cabeçalho RINEX | Recomendações                                                                                                                                                                                                                                  | Exemplo           |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------- |
| `MARKER NAME`                | <ul><li>Recomenda‑se utilizar o código de nove caracteres da estação.</li><li>Em alternativa, pode utilizar o código de quatro caracteres.</li><li>Todas as letras devem estar em maiúsculas.</li></ul>                                    | OUS200NZL<br>OUS2 |
| `MARKER NUMBER`              | Número DOMES do IERS. Todas as letras devem estar em maiúsculas.                                                                                                                                                                               | 50212M002         |
| `MARKER TYPE`                | Deve ser definido como GEODETIC.                                                                                                                                                                                                                 |                   |
| `OBSERVER`                   | Recomenda‑se fornecer um endereço de e‑mail genérico. O número máximo de caracteres é 20.                                                                                                                                                 | gnss@agency.org   |
| `AGENCY`                     | Recomenda‑se fornecer as abreviaturas da agência, conforme indicadas nas secções 11 e 12 do registo de estação IGS. Se várias agências forem listadas, devem ser separadas por uma barra (“/”). O número máximo de caracteres é 60. | OUSD/GFZ          |
| `REC # / TYPE / VERS`        | Todas as informações do recetor devem ser idênticas às metadados indicadas no registo de estação IGS.                                                                                                                                      |                   |
| `ANT # / TYPE`               | Todas as informações da antena devem ser idênticas às metadados indicadas no registo de estação IGS.                                                                                                                                       |                   |
| `APPROX POSITION XYZ`        | As coordenadas aproximadas devem concordar até 1m com as indicadas no registo de estação IGS.                                                                                                                                                 |                   |
| `ANTENNA: DELTA H/E/N`       | As excentricidades da antena devem corresponder às indicadas no registo de estação IGS.                                                                                                                                                       |                   |

## Fotografias Digitais

Cada CORS IGS deve fornecer fotografias da instalação da antena nas quatro direcções cardeais (de preferência 8 fotografias a cada 45°), do monumento e da sua proximidade. Devem ser actualizadas após cada evento ou alteração de hardware no local.
As fotografias devem ser rotuladas e nomeadas de acordo com a seguinte convenção:

`SSSSMRCCC_YYYYMMDD_D[D].fff`

A tabela abaixo descreve os elementos desta convenção. Todos os elementos são separados por um sublinhado (“_”).


| Componente  | Descrição                                                                                                                                                                                       | Exemplo                   |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| `SSSSMRCCC` | O código de nove caracteres da estação.                                                                                                                                                        | NYA200NOR                 |
| `YYYYMMDD`  | Data de admissão (ano, mês, dia) sem separação e preenchida com zeros.                                                                                                                        | 20210131                  |
| `D[D]`      | <ul><li>Direcção cardinal: N, E, S, W e uma combinação de duas destas</li><li>Número de série da antena: AS</li><li>Suporte de antena: AM</li><li>Recetor: R</li><li>Monumento: M</li></ul> | N (Norte)<br>SE (Sudeste) |
| `fff`       | O formato do ficheiro gráfico. São suportados JPEG e PNG.                                                                                                                                       | .jpg                      |

Em alternativa, as fotografias podem ser disponibilizadas num sítio web hospedado pelo operador da estação ou pela organização-mãe.

## Calibrações Individuais de Antenas

Embora não seja obrigatório, recomenda‑se fornecer calibrações individuais de antena. São úteis para actividades e investigações de diferentes grupos de trabalho do IGS (por exemplo, o Grupo de Antenas). O ficheiro ANTEX correspondente deve ser disponibilizado ao Coordenador da Rede IGS.

## Conformidade com a Protecção de Dados

A União Europeia e outros países implementaram regulamentos sobre a protecção de dados pessoais. Uma vez que o IGS é uma federação voluntária sem uma representação jurídica, não é do interesse do IGS lidar com as subtilezas de cada um destes regulamentos.
Por conseguinte, solicitamos que toda a informação pessoal nos metadados (registos de estação IGS/GeodesyML) e nos cabeçalhos RINEX (nomes completos e endereços de e‑mail) seja substituída por nomes genéricos e listas de e-mails, por exemplo:

- Registo de Estação IGS/GeodesyML:
  - Nome de contacto: “Instituição”
  - E‑Mail: gnss@agency.org
- Cabeçalho RINEX:
  - Observador: gnss@agency.org
  - Comentários com informação de aviso

As estações propostas ao IGS terão de seguir estas regras antes da aceitação. Os operadores que actualizem os metadados das suas estações também serão convidados a utilizar informações de contacto conformes à protecção de dados.

[domes-request]: https://itrf.ign.fr/en/network/domes/request
[domes-list]: https://itrf.ign.fr/en/network/list
