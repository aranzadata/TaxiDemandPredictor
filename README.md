# TaxiDemandPredictor

La compañía Sweet Lift Taxi ha recopilado datos históricos sobre pedidos de taxis en los aeropuertos. Para atraer a más conductores durante las horas pico, se contruye un modelo para predecir la cantidad de pedidos de taxis para la próxima hora.

Se empieza por analizar las tendencias generales de los datos, para lo cual se calculan el número de órdenes por hora y por día. Para estas dos muestras se obtienen sus componetes de tendencia, estacionalidad y residuo y se grafican.

Para el número de total de órdenes al día, se observa una tendencia creciente en el número de órdenes. El periodo de la componente estacional parece ser una semana. La amplitud de la componente residual es mayor a la componente estacional.

Para el número de total de órdenes por hora, la componente de tendencia también es creciente, pero parece también tener oscilaciones. Por otro lado la componente estacional tiene una clara periodicidad de un día.

En base al análisis exploratorio se añaden las siguientes características:

Número de mes, de 1 a 24
Día del mes, de 1 a 31
Día de la semana, de 0 a 6
Hora, de 0 a 23
Número del día del año
Para las primeras características se hace una codificación periódica, que consiste en hacer un mapeo a dos componentes: seno y coseno. Esto ayuda a suavizar el valor de las características a través del tiempo y a su vez ayuda a escalar los datos.

