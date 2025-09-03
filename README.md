


























Este trabajo construye, limpia y explora un dataset masivo de aplicaciones de Google Play (≈2.316.533 filas y 24 columnas al ingresar) para generar insight de mercado y, finalmente, entrenar un modelo de clasificación binaria que predice si una app tendrá calificación alta (≥4.5). A continuación se sintetizan objetivos, proceso, hallazgos clave, resultados del modelo y oportunidades de mejora.

Los resúmenes describen centralidad y dispersión: Rating con media ~2.20 y máximo 5; Installs con asimetría extrema (apps de Google dominan los rangos altos). Entre las vistas:
-Top por instalaciones: Google Play Services (~1e10), Google Photos, YouTube, Google Drive, Gmail, Maps, Chrome, Hangouts, etc., confirman una concentración de mercado en apps nativas/ecosistema Google.
-Top por popularidad ajustada (Installs×Rating): el ranking repite la hegemonía de Google, reforzando que poder de distribución + experiencia percibida elevan ese indicador.
-Gratuitas vs de pago: promedio de Rating ligeramente superior en apps de pago (~4.15) respecto de las gratuitas (~4.10); la brecha es pequeña y su relevancia práctica debe contrastarse con tamaño de efecto y distribución.
-Contenido “Everyone”: apps marcadas como “Everyone” tienen rating medio apenas mayor (~4.10 vs ~4.09 en no-Everyone), diferencia marginal.
-Instalaciones: distribución altamente sesgada con “colas pesadas”; conviene trabajar con escalas logarítmicas o “buckets” finos.
-Matriz de correlación (Rating, Rating Count, Installs, etc.): confirma relaciones esperables (p.ej., installs con máximos/mínimos), sin grandes sorpresas; la relación directa de Rating con “volumen” suele ser más débil.
-Conteo por tipo de contenido: la mayoría se concentra en “Everyone”/“Teen”, útil para segmentar posicionamientos y ASO familiar.
ANALISIS
-El mercado muestra ultra-concentración en apps nativas del ecosistema Google en descargas absolutas y “popularidad ajustada”. Para competidores, el foco debe ser nichos donde el ecosistema nativo no es dominante o donde la propuesta de valor es claramente diferenciada.
-La diferencia de rating entre gratuitas y de pago es pequeña; monetización directa no penaliza necesariamente la percepción si el valor percibido es claro.
-Segmentación por contenido (“Everyone”, “Teen”, etc.) no muestra grandes brechas de calidad percibida; la ventaja competitiva probablemente provenga de UX, utilidad y reputación del desarrollador más que del sello de contenido.



