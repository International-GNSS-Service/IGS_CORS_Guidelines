La calidad de la señal satelital que llega a una antena GNSS tiene un impacto crucial en el rendimiento de una estación GNSS. Hay una variedad de factores que pueden influir en la calidad de la señal. Se describen en las siguientes secciones.

## Visibilidad al Cielo (horizonte despejado)

Las estaciones GNSS deben ubicarse en sitios con obstrucciones mínimas sobre el horizonte local. Por encima de los 10° de elevación, la estación no debe presentar ninguna obstrucción. El receptor se deberá configurar para rastrear todos los satélites dentro de una máscara de elevación de 0° (ver también la Sección 4.1).

## Multi trayecto (multipath)

La interferencia por trayectos múltiples se produce cuando una señal de satélite GNSS llega a la antena por caminos diferentes. La señal llega una vez, directamente desde el satélite y además reflejándose en otras superficies.

Las fuentes de trayectorias múltiples pueden ser naturales o artificiales. La tabla siguiente enumera posibles fuentes que se sabe generan fuertes Multipath.

Fuentes Artificiales:

- Paneles y letreros metálicos
- Techos
- Paredes de edificios
- Mallas de cierres (cercos o cierres perimetrales)
- Paneles solares

Fuentes Naturales:

- Árboles (especialmente los mojados)
- Superficies de agua como lagos, ríos, etc.

Evite estos cuerpos reflectantes en emplazamientos GNSS en cualquier momento. Las fuentes sospechosas de trayectorias múltiples deben estar a una distancia mínima de 20 metros de la antena GNSS y por debajo de 5° de elevación.

## Fuentes de radio-interferencia

Las fuentes comunes de interferencia de radiofrecuencia (RFI) incluyen:

- Radio, televisión y transmisores de teléfonos móviles,
- Enlaces de datos por microondas,
- Líneas eléctricas,
- Transformadores.

Los transmisores direccionales, particularmente los enlaces de datos de microondas que apuntan hacia el sitio CORS, pueden causar RFI significativa.

Entre otros parámetros, el efecto de la RFI es función de la frecuencia, la potencia radiada y la distancia a la fuente. El efecto de la interferencia aumenta significativamente cuando el RFI es un armónico de una frecuencia de señal GNSS.

Por lo tanto, es difícil definir una distancia operativa segura desde una fuente de RFI. La RFI puede ser difícil de confirmar y puede ser necesario el asesoramiento de un especialista si se sospecha de una RFI. Si se confirma la RFI y no se puede mitigar en el sitio CORS propuesto, se debe considerar un sitio CORS alternativo.

!!! note "Nota"

    Las fuentes de RFI no solo afectan las señales GNSS recibidas en la antena, sino también la transmisión inalámbrica (red de radio o telefonía móvil) de los datos del sitio. Cuando un sitio CORS transmite datos a través de un enlace de radio, la transmisión de radio puede ser en sí misma una fuente de RFI en las señales GNSS en la antena.

Antes de la instalación final de un monumento, se recomienda probar el entorno de rutas múltiples y verificar si hay fuentes de RFI presentes en el sitio GNSS. Esto podría hacerse instalando el equipo GNSS en un trípode temporalmente e investigando la calidad de los datos.
