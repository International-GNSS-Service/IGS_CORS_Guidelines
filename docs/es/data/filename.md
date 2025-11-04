Actualmente, IGS admite tres versiones principales del estándar RINEX: RINEX v.2, RINEX v.3 y RINEX v.4. Se recomienda a todos los operadores de estaciones a transmitir la última versión mayor/menor disponible. Las IGS CORS propuestas recientemente deben enviar sus datos en RINEX 3.04 como mínimo.

## RINEX v.4/v.3

Los datos en [RINEX v.3](https://files.igs.org/pub/data/format/rinex305.pdf) y [RINEX v.4](https://files.igs.org/pub/data/format/rinex_4.01.pdf) deben transmitirse según la siguiente convención de nomenclatura de archivos:

*Archivos de Observación y Archivos Meteorológicos*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_FRU_DT.fff.cmp`

*Archivos de Navegación*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_DT.fff.cmp`

Todos los elementos del cuerpo principal del nombre del archivo deben contener letras o números ASCII en mayúscula y todos los elementos tienen una longitud fija y están separados por un guión bajo "_". El tipo de archivo y los campos de compresión (extensión) utilizan un punto "." como separador y deben ser caracteres ASCII en minúscula. Los campos deben rellenarse con ceros para llenar el ancho del campo. (Consulte la Tabla más abajo)

Para reducir aún más el tamaño de los archivos de observación, se debe utilizar el [conjunto de herramientas de compresión Hatanaka](https://terras.gsi.go.jp/ja/crx2rnx.html).

=== "SSSSMRCCC"
    Nombre de la estación de nueve caracteres

    - SSSS: nombre (existente) de la estación IGS de 4 caracteres 
    - M: número del sitio o monumento (0-9)
    - R: número del receptor (0-9)
    - CCC: código ISO-3166 de país o región (alpha-3)
    
    Ejemplo: POTS00DEU

    Nota: Para alinearse con el formato SINEX, actualmente no se admiten números de sitios y monumentos distintos de 0.

=== "S"
    Fuente de datos

    Se admiten R (desde el receptor que utiliza el software proveedor u otro software) y S (RTCM u otro formato de transmisión)

=== "YYYYDDDHHMM"

    Tiempo inicial

    - YYYY: Año Gregoriano (p.ej., 2024)
    - DDD: Día del año (p.ej., 260)
    - HHMM: Hora y minutos del día (p.ej., 1000)

    Es preferible utilizar la hora de inicio nominal del archivo. Sin embargo, es aceptable utilizar la hora de inicio real de un archivo.

=== "DDU"
    Período del archivo

    - DD: Período del archivo
    - U: Unidad del Período del archivo
    - Los aceptados son: 15M, 01H, 01D

=== "FRU"
    Frecuencia de los datos

    - FR: Frecuencia de los datos
    - U: Unidad de la Frecuencia de los datos
    - Los aceptados son: 01S para datos de alta frecuencia y 30S o 15S para datos horarios/diarios

    No es necesario para archivos RINEX de navegación

=== "DT"
    Tipo de Datos

    - Dos caracteres representan el tipo
    - D: Sistema Satelital (Los aceptados son G, R, E, C, J, S, I y M(ixed))
    - T: tipo de archivos RINEX (los aceptados son O, N, M)

    Ejemplo: MO

=== "fff"
    Formato del archivo. Se admiten rnx (RINEX) y crx (RINEX comprimido)

=== "cmp"
    Formato de Compresión. Se admite gzip (gz).

## RINEX v.2

Los datos RINEX v.2 (Gurtner, 2007) deben transmitirse según la siguiente convención de nomenclatura de archivos:

`ssssdddf.yyt`

La tabla siguiente describe cada elemento de esta convención de nomenclatura de archivos. Se recomienda a las estaciones que transmiten archivos RINEX v.2 que proporcionen archivos comprimidos gzip. Incluso si los archivos se envían en compresión Z, los centros de datos de IGS los recomprimirán y los pondrán a disposición del público mediante gzip.

=== "ssss"
    Los 4-caracteres del nombre de la estación IGS

    Ejemplo: pots

=== "ddd"
    Día del año del primer registro.

    Ejemplo: 260

=== "f"
    Número del archivo secuencial/sesión dentro del día
    
    - Para archivo diario (30 segundos): f=0
    - Para archivos Horarios (30 segundos):
        - f=a (00:00:00 to 00:59:30),
        - f=b (01:00:00 to 01:59:30), 
        - ...
        - f=x (23:00:00 to 23:59:30)
    - Para archivos de alta frecuencia (15M, 1 Hz):
        - f=a00 (00:00:00 to 00:14:59)
        - f=a15 (00:15:00 to 00:29:59) ...
        - f=m30 (12:30:00 to 12:44:59) ...
        - f=x45 (23:45:00 to 23:59:59)

=== "yy"
    Dos-dígitos para el año (p.ej., 24)

=== "t"
    Los tipos de archivos permitidos son:

    - O: Archivo de Observación
    - D: Archivo de Observación comprimido en Hatanaka 
    - N: Archivo de navegación GPS
    - G: Archivo de navegación GLONASS 
    - M: Archivo Meteorológico
