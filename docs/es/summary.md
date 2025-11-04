Esta sección presenta una descripción general de los requisitos obligatorios y deseables que debe cumplir una CORS para integrarse a la red IGS. Se pretende que sean aplicables tanto a las estaciones IGS activas actualmente como a las estaciones propuestas. El IGS desea claramente el pleno cumplimiento de estas Directrices; sin embargo, cuando no se pueda cumplir con las directrices, se pide a los operadores de estaciones que consulten con el Comité de Infraestructura. Se puede encontrar información más detallada sobre las recomendaciones en los capítulos siguientes de esta guía.

!!! info "Leyenda"

    :material-check-bold: Esta característica es el mínimo requerido.

    :fontawesome-solid-triangle-exclamation: Esta característica se recomienda pero no es obligatoria.

    :x: Esta característica no se recomienda.

## General

| Recomendación | Clasificación  |
| ------------- | -------------- |
| La estación pertenece a una red geodésica nacional/regional[^1]                                              | :fontawesome-solid-triangle-exclamation: |
| La estación es planificada e instalada para operación continua y permanente                                  | :material-check-bold: |
| La agencia operativa de la estación mantiene plena capacidad para reparar, actualizar y mantener la estación | :material-check-bold: |

## Fundación y Localización

| Recomendación | Clasificación  |
| ------------- | -------------- |
| Base en roca u hormigón macizo | :material-check-bold: |
| Montaje en edificios o estructuras similares[^2] | :x: |
| Vista del cielo despejado con obstrucciones limitadas por encima de 10° | :material-check-bold: |
| El sitio debe estar libre de obstrucciones de señal o RFI | :material-check-bold: |
| El sitio debe estar libre de material reflectante | :material-check-bold: |

## Monumentación y Montaje

| Recomendación | Clasificación  |
| ------------- | -------------- |
| Pilar de hormigón o arriostrado (armado) (tri-, quad-, …) | :material-check-bold: |
| (Acero) soportes fijados al edificio | :x: |
| El soporte bloquea la antena en su lugar para mantener la orientación y el nivel | :material-check-bold: |
| El soporte permite retirar la antena y volver a colocarla con una precisión de 0,5 mm de su ubicación original y 1° de su orientación | :material-check-bold: |

## Potencia y Comunicación

| Recomendación | Clasificación  |
| ------------- | -------------- |
| Garantizar el funcionamiento continuo de todos los dispositivos de comunicación | :fontawesome-solid-triangle-exclamation: |
| Garantizar el acceso remoto controlado al receptor | :material-check-bold: |

## Receptor

| Recomendación | Clasificación  |
| ------------- | -------------- |
| Seguimiento de código multifrecuencia y fase de portadora para todos los GNSS[^3] | :material-check-bold: |
| Registro continuo de datos crudos sin procesar (raw) GNSS | :fontawesome-solid-triangle-exclamation: |
| Transmisión de datos en tiempo real (RTCM) | :fontawesome-solid-triangle-exclamation: |
| Seguimiento de todos los satélites visibles (en buen estado y en mal estado) con una elevación mínima de 5° (se recomienda 0°) | :material-check-bold: |
| Deshabilitar el pseudorange y el suavizado de fase | :material-check-bold: |
| Deshabilitar la mitigación de trayectorias múltiples (multipath) | :material-check-bold: |
| Capacidad para almacenar una cantidad razonable de datos sin procesar (dependiendo de las circunstancias locales) | :material-check-bold: |

## Antena

| Recomendación | Clasificación  |
| ------------- | -------------- |
| Uso de antenas que dispongan de calibración absoluta de su centro de fase (calibración media) del IGS, como se incluye en el archivo oficial [IGS ANTEX](https://files.igs.org/pub/station/general/igs20.atx) | :material-check-bold: |
| Centro de fase de antena con calibración absoluta individualmente | :fontawesome-solid-triangle-exclamation: |
| Antena nivelada y orientada dentro de 5° al norte verdadero | :material-check-bold: |
| Radome protector de antena | :x: |

## Datos

| Recomendación | Clasificación  |
| ------------- | -------------- |
| Los datos deben proveerse en formato RINEX[^4] | :material-check-bold: |
| ^^ Si está disponible la transmisión en Tiempo Real[^5]:^^<br>Transmisión RTCM 3 MSM5 para aplicaciones en tiempo real[^6] | :material-check-bold: |
| Los datos deben volver a enviarse a los centros de datos después de una interrupción de la comunicación | :material-check-bold: |
| Los datos RINEX deben generarse en el receptor ^^o^^ desde un archivo binario nativo | :material-check-bold: |
| Objetivo de integridad del archivo | 99% |

### Archivos RINEX de alta frecuencia

| Recomendación     |              | Clasificación  |
| ----------------- | ------------ | -------------- |
| Disponibles       |              | :fontawesome-solid-triangle-exclamation: |
| Latencia          | < 5 minutos  | :material-check-bold: |
| Tasa de grabación | 1 Hz         | :material-check-bold: |
| Duración          | 15 minutos   | :material-check-bold: |

### Archivos RINEX horarios

| Recomendación     |              | Clasificación  |
| ----------------- | ------------ | -------------- |
| Disponibles       |              | :fontawesome-solid-triangle-exclamation: |
| Latencia          | < 5 minutos  | :material-check-bold: |
| Tasa de grabación | 30 segundos  | :material-check-bold: |

### Archivos RINEX diarios

| Recomendación     |              | Clasificación  |
| ----------------- | ------------ | -------------- |
| Disponibles       |              | :material-check-bold: |
| Latencia          | < 30 minutos | :material-check-bold: |
| Tasa de grabación | 30 segundos  | :material-check-bold: |

## Metadatos

| Recomendación  | Clasificación  |
| -------------- | -------------- |
| Metadatos completos y actualizados en el archivo de registro del sitio, formato IGS site log/GeodesyML | :material-check-bold: |
| Identificador único de estación de nueve caracteres aprobado por IGS | :material-check-bold: |
| Asignado con el número único de IERS (IERS DOMES number) | :material-check-bold: |
| Actualización del registro del sitio IGS dentro de las 24 horas posteriores a los cambios de estación aplicados | :material-check-bold: |
| El encabezado del archivo RINEX debe coincidir con la información del registro de metadatos del IGS | :material-check-bold: |
| Suministro de fotografías de la instalación de la antena en los 4 puntos cardinales (N, E, S, W) | :material-check-bold: |

[^1]: Obligatoria para las CORS regionales en la zona de APREF, EPN y SIRGAS.
[^2]: Se pueden conceder exenciones después de la revisión por parte del SPC.
[^3]: Las nuevas estaciones deben rastrear todos los códigos de frecuencia disponibles y las fases de la portadora.
[^4]: Para nuevas estaciones: RINEX 3.04 es la mínima versión aceptada. RINEX 2.11 ya no se acepta.
[^5]: Se recomienda encarecidamente que las nuevas estaciones proporcionen transmisiones en tiempo real.
[^6]: Se sugiere MSM7.
