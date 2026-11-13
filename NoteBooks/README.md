# Análisis de puntos de calor para identificación de incendios forestales

## Descripción del proyecto
Este proyecto analiza un conjunto de datos de puntos de calor para identificar zonas específicas donde se registran incendios forestales o eventos de calor anómalo. El objetivo principal es transformar datos crudos en información útil para detectar patrones por departamento, municipio, paisaje y fecha, así como para apoyar la toma de decisiones en temas de prevención y monitoreo ambiental.

El dataset utilizado corresponde a registros geoespaciales de detecciones de calor, con información como coordenadas, fecha de adquisición, tipo de instrumento, entidad territorial, tipo de paisaje y clasificación asociada al evento.

## Problema de investigación
En Colombia y en regiones tropicales, los puntos de calor pueden ser indicadores tempranos de incendios forestales, deforestación o presiones sobre ecosistemas sensibles. Sin embargo, estos registros suelen presentarse como datos crudos y dispersos, difíciles de interpretar sin un proceso previo de limpieza, parseo y análisis.

El problema central es responder la siguiente pregunta:

¿En qué ubicaciones geográficas, fechas y categorías se concentran los puntos de calor, y cuáles de estos podrían estar asociados a incendios forestales o riesgo ambiental?

## Objetivo general
Realizar un análisis exploratorio de puntos de calor a partir del archivo CSV para identificar patrones espaciales, temporales y temáticos que permitan reconocer zonas con mayor incidencia de incidentes de fuego.

## Objetivos específicos
- Explorar la estructura del dataset y validar columnas, tipos de datos y valores faltantes.
- Parsear y limpiar los datos para convertir fechas, coordenadas y variables categóricas a formatos útiles para análisis.
- Identificar la distribución geográfica de los puntos de calor por departamento, municipio y paisaje.
- Analizar la evolución temporal de las detecciones por fecha de adquisición.
- Detectar zonas con mayor frecuencia de eventos y relacionarlas con categorías institucionales o ambientales.
- Preparar la información para análisis posteriores, visualización y posibles modelos predictivos.

## Alcance
Este proyecto tiene un alcance analítico y exploratorio. Se enfoca en:

- Lectura, limpieza y parseo del archivo CSV de puntos de calor.
- Identificación de patrones por ubicación y tiempo.
- Evaluación de valores faltantes y duplicados.
- Organización de los datos para análisis descriptivo y visualización.

No incluye, en esta fase, un modelo de predicción avanzada ni análisis de satélite de alta resolución, aunque la base de datos puede servir como insumo para estudios posteriores de machine learning o análisis geoespacial.

## Dataset
El conjunto de datos se encuentra en el archivo:

PuntosCalor.csv

### Variables principales
El dataset incluye información como:

- X: coordenada espacial X
- Y: coordenada espacial Y
- objectid: identificador del registro
- latitude: latitud
- longitude: longitud
- acq_date: fecha de adquisición del dato
- instrument: sensor o instrumento responsable de la detección
- fecha_date: fecha de procesamiento o registro asociado
- paisaje: tipo de paisaje o cobertura
- departamen: departamento
- municipio: municipio
- car: corporación ambiental o entidad territorial
- sigla_elt: sigla de la entidad o clasificación asociada
- leyenda: texto descriptivo relacionado con el evento
- acq_col: fecha de colección o captura del dato
- confidence_modis: valor de confianza para datos MODIS
- confidence: nivel de confianza o categoría asociada

## Metodología propuesta
1. Carga del archivo CSV con pandas.
2. Inspección de columnas, dtypes y valores faltantes.
3. Parseo de fechas y normalización de texto.
4. Detección y eliminación de duplicados.
5. Imputación de valores faltantes según el tipo de variable.
6. Análisis descriptivo por departamento, municipio, fecha y paisaje.
7. Visualización de resultados y preparación del dataset para trabajo adicional.

## Resultado esperado
Se espera obtener una base de datos ordenada y analizable que permita responder preguntas como:

- ¿Qué departamentos tienen mayor cantidad de puntos de calor?
- ¿Qué municipios concentran más eventos?
- ¿Existen meses o temporadas con mayor frecuencia de detecciones?
- ¿Hay correlación entre paisaje y número de puntos de calor?
- ¿Qué zonas requieren mayor atención por riesgo de incendio?

## Conclusión preliminar
La lectura del archivo indica que se trata de un conjunto de datos de detecciones térmicas asociadas a incendios forestales o eventos de calor anómalo. El análisis de estos registros permite convertir observaciones geográficas crudas en una evidencia útil para la identificación de focos de riesgo y el diseño de estrategias de prevención ambiental.

## 9. Criterios de la lectura inicial y del prototipo
El prototipo de la Evaluación 1 no exige un modelo final. Sí exige evidencia de que el equipo:

- eligió un dataset y definió problema, objetivos y alcance;
- puede leer el archivo de forma reproducible;
- parsea tipos en lugar de dejar todo como texto;
- depura con reglas de dominio, no con borrado automático de atípicos;
- justifica qué se elimina y qué no;
- si imputa, distingue relleno por media de una imputación que no destruye la distribución;
- deja un primer resultado funcional (tabla limpia, descriptivos o figura) generado por código.

## 10. Definición del problema (plantilla del equipo)
Completar en esta sección o en un documento enlazado:

- Problema: identificar la distribución espacial y temporal de los puntos de calor para detectar zonas con mayor riesgo de incendios forestales y apoyar la priorización de monitoreo ambiental.
- Objetivos: leer y limpiar el dataset, parsear sus tipos, depurar inconsistencias, imputar valores faltantes sin distorsionar la distribución, y generar un primer análisis descriptivo por fecha, departamento, municipio, paisaje y coordenadas.
- Alcance (qué entra y qué no): entra la lectura, limpieza, parseo, exploración descriptiva y visualización preliminar de los puntos de calor; no entra un modelo predictivo complejo, ni análisis satelital avanzado ni validación operativa in situ.
- Dataset: PuntosCalor.csv, fuente de detecciones de calor, número de filas y columnas según lectura inicial del archivo; formato CSV con registros geoespaciales y atributos asociados.
- Variable(s) de interés: X, Y, latitude, longitude, acq_date, fecha_date, departamen, municipio, paisaje, leyenda, confidence, confidence_modis.
- Limitaciones conocidas del dato: solo se usa la información disponible en la fecha y hora cuando se puede, además de las coordenadas (X, Y, latitud, longitud), municipio, departamento, paisaje y leyenda; no se asume una validación completa de cada punto como incendio confirmado, sino como detección de calor que requiere análisis contextual.

## Observaciones de dominio
El análisis se centra en registros de detecciones térmicas asociadas a incendios forestales, especialmente en zonas de interés ambiental como el Amazonas y otros territorios con alta sensibilidad ecológica. La variable de interés principal es la localización geográfica del punto de calor, junto con la fecha de adquisición y la clasificación de la detección.


