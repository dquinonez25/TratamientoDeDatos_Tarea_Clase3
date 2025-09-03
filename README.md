Documentación del trabajo.

Descripición del propósito del dataset: El dataset para analizar se descargó desde www.kaggle.com con nombre Google Play Store Apps fue muy interesante, debido a que es una plataforma digital que permite a los usuarios de dispositivos Android acceder a una amplia variedad de aplicaciones, juegos, películas, libros electrónicos, entre otros. El propósito fue realizar procesamiento de datos (limpieza, transformación y adaptación) para el análisis, posterior realizar análisis exploratorio de datos (EDA) y visualización de datos donde fue generado gráficos informativos y estéticamente atractivos utilizando herramientas apropiadas las cuales fueron efectuadas de manera exitosa.

Explicación de los pasos de limpieza y transformación: Se importaron las librerías necesarias para las ejecuciones, se validó información de nombres, números de valores no nulos, filas y columnas del DataFrame y sus tipos de datos. Se generó resumen estadístico de los datos de las columnas numéricas y distribución percentiles. Mediante línea de código se eliminó filas duplicadas del DataFrame, se eliminó filas con muchos nulos, se limpió y convirtió los datos de columnas eliminando caracteres + y , dando como resultado lo que aún es texto en número decimal float para poder hacer cálculos. Se reasignó columnas con nuevos valores limpios y convertidos. 
Se convirtió tamaños de archivos como 19M o 1.2G a a valores numéricos en bytes. Se convirtió columnas de fechas que están en formato de texto en un formato de fecha y hora. Se asignó un precio de 0 a todas las filas del DataFrame donde la columna Free indicaba que la app es gratuita. Se filtró y limpió el DataFrame eliminando las filas donde el número mínimo de instalaciones era mayor que el número máximo, para evitar muestre un error lógico en los datos. Se eliminaron apps o registros que no habían sido instalados ni calificados, lo cual probablemente no tenían actividad real para no dar conflictos en los análisis. 
Se codificó y convirtió cada categoría en una columna binaria 0 o 1, y se limpió filas y columnas para evitar redundancia en modelos lineales. Se normalizó el texto en columnas para evitar errores y duplicados al trabajar con datos categóricos o hacer comparaciones. Se eliminó columnas innecesarias o irrelevantes. Se limpió y preparó datos eliminando apps que no habían sido instaladas ni calificadas, probablemente no tenían uso real o eran datos vacíos. Se validó limpieza y transformación del procesamiento de datos.

Principales hallazgos del análisis: Se agrupó por categoría de contenido y calculó el promedio de califiación para las apps marcadas como everyone lo cual da hallazgo que apto para todo público tuvo una calificación promedio ligeramente más alta (4.102) que los que no lo están (4.092).
Se agrupó para validar y mostrar promedio de calificaciones (Rating) según si una app o contenido es gratuito (Free) o no, dando hallazgo que apps de pago tienen una calificación promedio ligeramente más alta (≈4.15) que gratuitas (≈4.10).
Se agrupó y validó que apps de pago y no aptas para todos tienen la calificación más alta (≈4.17), y apps gratuitas y no aptas para todos tienen la calificación más baja (≈4.09). Se tuvo hallazgo en que usuarios valoran más las apps de pago, especialmente si están dirigidas a un público más específico y las apps gratuitas tienen una calificación más baja, por expectativas más bajas o menor calidad percibida.
Se comprobó hallazo de las 10 apps más populares según el número de instalaciones y mejor valoradas en donde destacaron google text-to-speech, hangouts, google drive, whatsapp messenger, android accessibility suite las cuales destacan por ofrecer a los usuarios convertir texto escrito en voz hablada, escuchar contenido mientras hacen otras cosas como conducir o entrenar, combinar mensajería instantánea, llamadas de voz y videollamadas en una sola plataforma, incluso ayuda para personas con discapacidad visual, auditiva o motora.
Mediante visualización entre variables numéricas en un heatmap se validaron correlaciones positivas y negativas lo cual da hallazgo que una correlación positiva fuerte, indica que las apps más descargadas tienden a recibir más calificaciones; una correlación débil o moderada, sugiere que una app muy descargada no necesariamente tiene mejor calificación; y que correlación negativa o cercana a cero, indicó que las apps más populares no siempre son las mejor valoradas.

Cualquier insight o información relevante: Se puede detallar que analizar éste dataset nos conectó con el ámbito real de los consumidores, al mismo tiempo dio una emoción saber que no existe status económico o edad específica para el uso de apps, unos con un enfoque mas especifico por temas de estudio, negocio, personales o labores profesionales, y otros por temas de apoyarse con la inteligencia artificial, incluso conocer que personas con discapacidad han tenido un espacio muy importante en el uso de apps que les brindan un acompañamiento digital en sus rutinas diarias y un apoyo en su estilo de vida.



























Conclusión y resultados:

Con éste detallado análisis se identificó que hay un campo muy abierto que cada día crece a pasos agigantados permitiendo a las empresas tomar decisiones estratégicas y de gran valor para sus marcas. Pero más que todo permitiendo a los usuarios poder probar varias alternativas que se ajusten a su necesidad y estar en su decisión lo que consumen si es gratis o con pago, teniendo presente que cada ámbito les generará una experiencia diferente de satisfacción. 
Adicional la implementación de análisis de machine learning con Scikit-learn sirvió para transformar datos en conocimiento útil, automatizar toma de decisiones y descubre patrones ocultos entre los que destacan predicción de resultados, segmentación de clientes y análisis de sentimientos, e incluso gráficos que proyectan estadísticas e información a usuarios que comprenden mejor así, los cuales son fundamentales para alcanzar objetivos en los proyectos.
