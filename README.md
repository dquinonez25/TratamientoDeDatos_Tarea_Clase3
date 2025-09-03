Documentación del trabajo.

Descripición del propósito del dataset: El dataset para analizar se descargó desde www.kaggle.com con nombre Google Play Store Apps que es muy interesante, por ser una plataforma digital que permite a los usuarios de dispositivos Android acceder a una amplia variedad de aplicaciones, juegos, películas, libros electrónicos, entre otros. El propósito fue realizar procesamiento de datos (limpieza, transformación y adaptación) para el análisis, posterior realizar análisis exploratorio de datos (EDA) y visualización de datos donde sea generado gráficos informativos y estéticamente atractivos utilizando herramientas apropiadas para encontrar varios hallazgos de manera positiva.

Explicación de los pasos de limpieza y transformación: Se importaron las librerías necesarias para sus respectivas ejecuciones, se validaron información de nombres, números de valores no nulos, filas y columnas del DataFrame y sus tipos de datos. Se generó resumen estadístico de datos de columnas numéricas y distribución percentiles. Mediante línea de código se eliminó filas duplicadas, se eliminó filas con muchos nulos, se limpió y convirtió datos de columnas eliminando caracteres + y , dando como resultado lo que aún es texto convertirlo en número decimal float para poder hacer cálculos. Se reasignó columnas con nuevos valores limpios y convertidos. 
Se convirtió tamaños de archivos como 19M o 1.2G a a valores numéricos en bytes. Se convirtió columnas de fechas que están en formato de texto en un formato de fecha y hora. Se asignó un precio de 0 a todas las filas del DataFrame donde la columna Free indicaba que la app es gratuita. 
Se filtró y limpió el DataFrame eliminando las filas donde el número mínimo de instalaciones era mayor que el número máximo, para evitar muestre un error lógico en los datos. 
Se eliminaron apps o registros que no habían sido instalados ni calificados, lo cual probablemente no tenían actividad real para no dar conflictos en los análisis. Se codificó y convirtió cada categoría en una columna binaria 0 o 1, y se limpió filas y columnas para evitar redundancia en modelos lineales. Se normalizó el texto en columnas para evitar errores y duplicados al trabajar con datos categóricos o al hacer comparaciones, y se validó limpieza y transformación del procesamiento de datos de manera exitosa.

Principales hallazgos del análisis: Se agrupó por categoría de contenido y calculó el promedio de califiación para las apps marcadas como everyone lo cual da hallazgo que apto para todo público tuvo una calificación promedio ligeramente más alta (4.102) que los que no lo están (4.092). Se agrupó para validar y mostrar promedio de calificaciones (Rating) según si una app o contenido es gratuito (Free) o no, dando hallazgo que apps de pago tienen una calificación promedio ligeramente más alta (≈4.15) que gratuitas (≈4.10). Se agrupó y validó que apps de pago y no aptas para todos tienen la calificación más alta (≈4.17), y apps gratuitas y no aptas para todos tienen la calificación más baja (≈4.09). 
Se tuvo hallazgo en que usuarios valoran más las apps de pago, especialmente si están dirigidas a un público más específico y las apps gratuitas tienen una calificación más baja, por expectativas más bajas o menor calidad percibida. Se comprobó hallazo de las 10 apps más populares según el número de instalaciones y mejor valoradas en donde destacaron google text-to-speech, hangouts, google drive, whatsapp messenger, android accessibility suite las cuales destacan por ofrecer a los usuarios convertir texto escrito en voz hablada, escuchar contenido mientras hacen otras cosas como conducir o entrenar, combinar mensajería instantánea, llamadas de voz y videollamadas en una sola plataforma, incluso ayuda para personas con discapacidad visual, auditiva o motora. 
Mediante visualización entre variables numéricas en un heatmap se validaron correlaciones positivas y negativas lo cual da hallazgo que una correlación positiva fuerte, indica que las apps más descargadas tienden a recibir más calificaciones; una correlación débil o moderada, sugiere que una app muy descargada no 
necesariamente tiene mejor calificación; y que correlación negativa o cercana a cero, indicó que las apps más populares no siempre son las mejor valoradas.

Cualquier insight o información relevante: Se puede detallar que analizar éste dataset nos conectó con el ámbito real de los consumidores, al mismo tiempo dio una emoción saber que no existe status económico o edad específica para el uso de apps, unos con un enfoque mas especifico por temas de estudio, negocio, personales o labores profesionales, y otros por temas de apoyarse con la inteligencia artificial, incluso conocer que personas con discapacidad han tenido un espacio muy importante en el uso de apps que les brindan un acompañamiento digital en sus rutinas diarias y un apoyo en su estilo de vida.

Descripción del dataset: El conjunto de datos Google Play Store Apps es un repositorio que contiene información sobre las aplicaciones de Google Play, se incluye detalles de las aplicaciones como su nombre, categoría, valoración, número de reseñas, tamaño, tipo (gratis/pago), contenido de calificación y género. Este conjunto de datos se utiliza para realizar un Análisis Exploratorio de Datos para descubrir patrones, tendencias y relaciones en el mercado de aplicaciones móviles, ayudando a los desarrolladores y profesionales a comprender las preferencias de los usuarios y el rendimiento de las apps. 

Explicación de los pasos de limpieza y transformación: Se importa la librería Matplotlib, se utiliza para crear visualizaciones estáticas, animadas e interactivas en Python.La biblioteca Seaborn permite visualizar datos de Python basada en matplotlib. Proporciona una interfaz de alto nivel para crear gráficos estadísticos atractivos e informativos.

Principales hallazgos del análisis: Aunque las aplicaciones de categorías como juegos, redes sociales y comunicación son las que tienen mayor número de instalaciones, valoraciones y reseñas, refleja  la tendencia actual que tienen los usuarios que utilizan el sistema Android, estas no se encuentran entre las cinco aplicaciones más caras de la tienda que están conformadas por aplicaciones de finanzas o estilo de vida. Esto permite que la tendencia actual en el mercado Android sea para aplicaciones de asistencia, comunicación o entretenimiento.

Otro dato importante que se encuentra en la base es el tamaño de las aplicaciones. La mayoría de las aplicaciones instaladas no superan los 200 megabytes, por lo que la mayoría de los consumidores no quieren descargar aplicaciones que ocupen demasiado espacio en el almacenamiento de sus dispositivos. Además, Google solo permite aplicaciones de menos de 500 MB.

La regresión logística obtuvo una precisión mayor al 90%para el análisis del modelo, por lo que se convierte en un algortimo más eficaz en este contexto. Esta alta
precisión indica que la regresión logísitca puede predecir de forma fiable el sentimiento de los usuarios basándose en los atributos de la aplicación, lo que proporciona a los desarrolladores información útil para la optimización de la aplicación.

Este trabajo construye, limpia y explora un dataset masivo de aplicaciones de Google Play (≈2.316.533 filas y 24 columnas al ingresar) para generar insight de mercado y, finalmente, entrenar un modelo de clasificación binaria que predice si una app tendrá calificación alta (≥4.5). A continuación se sintetizan objetivos, proceso, hallazgos clave, resultados del modelo y oportunidades de mejora.

Los resúmenes describen centralidad y dispersión: Rating con media ~2.20 y máximo 5; Installs con asimetría extrema (apps de Google dominan los rangos altos). Entre las vistas: -Top por instalaciones: Google Play Services (~1e10), Google Photos, YouTube, Google Drive, Gmail, Maps, Chrome, Hangouts, etc., confirman una concentración de mercado en apps nativas/ecosistema Google. -Top por popularidad ajustada (Installs×Rating): el ranking repite la hegemonía de Google, reforzando que poder de distribución + experiencia percibida elevan ese indicador. -Gratuitas vs de pago: promedio de Rating ligeramente superior en apps de pago (~4.15) respecto de las gratuitas (~4.10); la brecha es pequeña y su relevancia práctica debe contrastarse con tamaño de efecto y distribución. -Contenido “Everyone”: apps marcadas como “Everyone” tienen rating medio apenas mayor (~4.10 vs ~4.09 en no-Everyone), diferencia marginal.

Instalaciones: distribución altamente sesgada con “colas pesadas”; conviene trabajar con escalas logarítmicas o “buckets” finos. -Matriz de correlación (Rating, Rating Count, Installs, etc.): confirma relaciones esperables (p.ej., installs con máximos/mínimos), sin grandes sorpresas; la relación directa de Rating con “volumen” suele ser más débil. -Conteo por tipo de contenido: la mayoría se concentra en “Everyone”/“Teen”, útil para segmentar posicionamientos y ASO familiar. 

ANALISIS -El mercado muestra ultra-concentración en apps nativas del ecosistema Google en descargas absolutas y “popularidad ajustada”. Para competidores, el foco debe ser nichos donde el ecosistema nativo no es dominante o donde la propuesta de valor es claramente diferenciada. -La diferencia de rating entre gratuitas y de pago es pequeña; monetización directa no penaliza necesariamente la percepción si el valor percibido es claro. -Segmentación por contenido (“Everyone”, “Teen”, etc.) no muestra grandes brechas de calidad percibida; la ventaja competitiva probablemente provenga de UX, utilidad y reputación del desarrollador más que del sello de contenido.


Conclusión y resultados:

Con éste detallado análisis se identificó que hay un campo muy abierto que cada día crece a pasos agigantados permitiendo a las empresas tomar decisiones estratégicas y de gran valor para sus marcas. Pero más que todo permitiendo a los usuarios poder probar varias alternativas que se ajusten a su necesidad y estar en su decisión lo que consumen si es gratis o con pago, teniendo presente que cada ámbito les generará una experiencia diferente de satisfacción. 
Adicional la implementación de análisis de machine learning con Scikit-learn sirvió para transformar datos en conocimiento útil, automatizar toma de decisiones y descubre patrones ocultos entre los que destacan predicción de resultados, segmentación de clientes y análisis de sentimientos, e incluso gráficos que proyectan estadísticas e información a usuarios que comprenden mejor así, los cuales son fundamentales para alcanzar objetivos en los proyectos.
















