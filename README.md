# Análisis exploratorio de datos sobre tiempos de entrega de pedidos

# Descripción del Proyecto

En este proyecto se realiza un análisis exploratorio de datos para tener un primer acercamiento a las fechas de los diferentes pasos en el proceso de entrega de pedidos de una empresa ficticia.

## Pregunta de estudio

¿Que parte del proceso podemos mejorar para reducir los tiempos de entrega de pedidos?
______
## Creación de valores dummy

Si deseas crear valores dummy para utilizar el código mostrado ingresa al notebook *create_dummy_data* y genera tu fuente de datos, este archivo cuenta con las siguientes funciones:

* **generate_dummy_df** Genera un dataframe con valores aleatorios y congruentes
* **add_outliers** Agrega outliers al dataframe
* **introduce_missing_values** Intriduce valores vacíos al dataframe

*No olvides guardar tu archivo en CSV corriendo la ultima celda del notebook*

En caso de que tengas datos reales asegúrate que tengan el siguiente formato:

| ID_pedido | Fecha_pedido | Fecha_picking | Fecha_factura | Fecha_entrega |
|-----------|--------------|--------------|--------------|--------------|
| 1         | DD/MM/YYYY   | DD/MM/YYYY   | DD/MM/YYYY   | DD/MM/YYYY   |
____
## Ver el análisis

Para ver el proceso del análisis utiliza en archivo eda.ipynb corriendo linea por linea

# Resumen de resultados

* Se observan algunos valores vacíos 
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/37386c13-c2dd-4472-bfad-89933d71b947/1bdf63a1-712c-4ffd-9085-baa0305196a7/Untitled.png)

* No se observa una alta correlación sobre la falta de valores en las variables
* Se observan algunos outliers que al ser pocos, se procede a eliminar
* Se observa que los días entre el pedido y la factura no tienen tanta variablilidad, como los dias de la factura a la entrega
* No se observa correlación entre estas 3 variables
* Con los gráficos de cajas y bigotes se puede observar la media y desviación de las 3 variables
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/37386c13-c2dd-4472-bfad-89933d71b947/d5184a2f-12b6-4586-bfd1-c9eaac387886/Untitled.png)

* Viendo las medias se puede observar que los días entre la factura y la entrega representan la mayor parte de los días del proceso de envíos
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/37386c13-c2dd-4472-bfad-89933d71b947/06cef8b3-48da-4f15-88b3-c709a53669de/Untitled.png)
______
## Conclusión

En base al análisis exploratorio de los datos se puede observar que el proceso en el que debemos enfocarnos para mejorar los tiempos de entrega es el transporte hacia el cliente, que es lo que sucede entre la factura y la entrega, pues esto representa el 58% del tiempo total del proceso.
______
# Referencias

https://altair-viz.github.io/index.html
https://matplotlib.org


Este proyecto se realizó utilizando la version 3.11.2 de python