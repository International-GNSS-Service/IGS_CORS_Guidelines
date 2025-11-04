Los metadatos GNSS son información del sitio, incluida la propiedad del sitio, detalles de contacto, información del monumento, las coordenadas de la estación y un historial del equipo instalado. Los metadatos confiables y actualizados son fundamentales para la gestión y el uso de una estación GNSS, y son responsabilidad del operador de la estación.

## Archivo IGS Log de la estación/GeodesyML

El IGS requiere que cada estación CORS registre y mantenga sus metadatos en un archivo del sitio "log file IGS" (ASCII) o GeodesyML (Geodesy Markup Language) y que los metadatos estén disponibles para el IGS y para todos los usuarios. El IGS utiliza una [aplicación web](https://slm.igs.org) para mantener los metadatos de la estación.

Es obligatorio que todas las estaciones CORS completen y publiquen los metadatos, proporcionando un método coherente de distribución de información relevante del sitio a los centros de análisis y a los usuarios. Es posible que un operador de CORS necesite ingresar metadatos adicionales del sitio para ayudar a la gestión y operación internas.

Todas las estaciones IGS se identifican mediante una abreviatura única de nueve caracteres. Los primeros cuatro caracteres deben ser únicos a nivel mundial y el nombre generalmente se elige para representar el suburbio, ciudad o localidad del sitio. El operador GNSS debe verificar con el Coordinador de la red IGS que el identificador de cuatro caracteres propuesto para una nueva CORS no esté ya en uso. Además, se debe solicitar para cada estación IGS CORS el [número identificatorio "IERS DOMES"](domes-request). Será necesario verificar que el código de cuatro caracteres previsto no se haya utilizado previamente para otras técnicas geodésicas consultando la [lista de números IERS DOMES](domes-list).

## Encabezados de archivos RINEX

Los encabezados de los archivos RINEX deben coincidir con los metadatos registrados en el archivo log del sitio IGS. Los archivos RINEX se volverán a enviar en caso de discrepancias en los metadatos. Toda la información del encabezado del RINEX debe estar codificada en ASCII. El uso de caracteres de otros estándares de codificación (por ejemplo, UTF-8) pueden provocar un cambio de los elementos del encabezado durante la decodificación, por ejemplo, mediante el uso de signos diacríticos (tilde, diéresis). La tabla siguiente enumera los elementos que se deben proporcionar obligatoriamente en el encabezado para cada archivo RINEX.

| Elementos del encabezado RINEX | Recomendaciones | Ejemplo |
| ------------------------------ | --------------- | ------- |
| `MARKER NAME`                  | <ul><li>Se recomienda utilizar el código de estación de nueve caracteres.</li><li>Alternativamente, se puede utilizar el código de estación de 4 caracteres.</li><li>Todas las letras deben escribirse en mayúsculas.</li></ul> | OUS200NZL<br>OUS2 |
| `MARKER NUMBER`                | Número otorgado por el IERS a la estación (Domes number). Todas las letras deben escribirse en mayúsculas. | 50212M002 |
| `MARKER TYPE`                  | Debe configurarse en GEODETIC. ||
| `OBSERVER`                     | Se recomienda proporcionar una dirección de correo electrónico genérica. El número máximo de caracteres es 20. | gnss@agency.org |
| `AGENCY`                       | Se recomienda proporcionar las abreviaturas de las agencias como se indica en las secciones 11 y 12 del IGS log file del sitio. Si se refieren varias agencias, deben estar separadas por una barra ("/"). El número máximo de caracteres es 60. | OUSD/GFZ |
| `REC # / TYPE / VERS`          | Toda la información del receptor debe ser idéntica a los metadatos indicados en el log file del sitio IGS. ||
| `ANT # / TYPE`                 | Toda la información de la antena debe ser idéntica a los metadatos indicados en el log file del sitio IGS. ||
| `APPROX POSITION XYZ`          | Las coordenadas aproximadas deberán coincidir con una precisión de 1 m con respecto a las indicadas en el archivo log del sitio IGS. ||
| `ANTENNA: DELTA H/E/N`         | Las excentricidades de la antena deben coincidir con las indicadas en el registro del log file del sitio IGS. ||

## Fotografías Digitales

Para cada estación CORS se deben proporcionar fotografías de la instalación de la antena, del monumento y sus alrededores, tomadas desde la dirección de los cuatro puntos cardinales (preferiblemente 8 fotografías cada 45°). Deben actualizarse después de cada evento o cambio de hardware en el sitio.
Las imágenes deben etiquetarse y nombrarse según la siguiente convención de nomenclatura de archivos:

`SSSSMRCCC_YYYYMMDD_D[D].fff`

La tabla siguiente describe los elementos de esta convención. Todos los elementos están separados por un guión bajo ("_").

| Componente  | Descripción | Ejemplo |
| ----------  | ----------- | ------- |
| `SSSSMRCCC` | Código de la estación de 9-caracteres. | NYA200NOR |
| `YYYYMMDD`  | Fecha de admisión de la fotografía (año, mes, día) sin separación y con relleno de ceros. | 20210131 |
| `D[D]`      | <ul><li>Dirección Cardinal: N, E, S, W y combinación bidireccional de ellos</li><li>Número de serie de la Antena: AS</li><li>Montaje de antena: AM</li><li>Receptor: R</li><li>Monumento: M</li></ul> | N (North)<br>SE (South-East) |
| `fff`       | El formato del archivo gráfico. Se admiten JPEG y PNG. | .jpg |

Alternativamente, las fotografías pueden ponerse a disposición en un sitio web alojado por el operador de la estación o de la organización matriz.

## Calibraciones individuales de antena 

Aunque no es obligatorio, se recomienda proporcionar calibraciones de antena individuales. Son útiles para actividades e investigaciones para diferentes grupos de trabajo de IGS (por ejemplo, Grupo de Trabajo de Antenas). El fichero ANTEX correspondiente deberá ponerse a disposición del Coordinador de la Red IGS.

## Cumplimiento de la protección de datos

La Unión Europea y otros países implementaron regulaciones sobre la protección de datos personales. Dado que el IGS es una organización voluntaria sin una fuerte representación legal, no le interesa abordar las sutilezas que trae consigo cada una de las regulaciones.

Por lo tanto, solicitamos que toda la información personal en los metadatos (registros del sitio IGS/GeodesyML) y en el encabezado RINEX (nombres completos y direcciones de correo electrónico) se reemplacen por nombres genéricos y listas de correo electrónico, por ejemplo:

- IGS Site Log/GeodesyML:
    - Nombre de Contacto: "Agencia" Operador de Red
    - E-Mail: gnss@agency.org
- Encabezado del archive RINEX:
    - Observador: gnss@agency.org
    - Comentarios con información de descargo de responsabilidad.

Las estaciones propuestas al IGS deberán seguir estas reglas antes de su aceptación. A los operadores de estaciones que estén actualizando los metadatos de sus estaciones también se les pedirá que utilicen información de contacto que cumpla con la protección de datos.

[domes-request]: https://itrf.ign.fr/en/network/domes/request
[domes-list]: https://itrf.ign.fr/en/network/list
