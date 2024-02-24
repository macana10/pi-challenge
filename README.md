# PI Challenge

Este proyecto hace referencia a un challenge realizado para Pi. 

##  El problema

Un proceso ETL toma datos de un archivo y lo deposita en la tabla dbo.Unificado.
Por algún error en estos archivos, aparecieron registros duplicados en la tabla.
Consultando con el cliente, nos cuenta que es posible que estas cosas sucedan como consecuencia de errores en el sistema que genera estos archivos, pero que siempre tomemos el ultimo registro que fue copiado, considerando que un registro será duplicado si los campos [ID], [MUESTRA] y [RESULTADO] son iguales en dos filas distintas.

## Consignas

a. Montar el backup de la base de datos (SQL Server - .bak)
b. Descargar programaticamente el archivo csv con el link de abajo. Hacelo teniendo en cuenta que este archivo en el origen cambia semana a semana con datos nuevos para integrar a la base de datos.
c. Desarrollar un proceso que inserte las filas del archivo .csv en la tabla Unificado. Tener en cuenta que la columna FECHA_COPIA esta vacia en el archivo, y hay que agregarle la fecha en la cual estas insertando las nuevas filas a la base de datos.
d. Testearlo y verificar que no haya perdida de información. Documentar.
e. Dejar de algún modo programado ese proceso para que se ejecute los lunes de cada semana, a las 5:00 AM.
f. Mejorar el proceso para que guarde logs en cada ejecución con la información que creas necesaria (cantidad de filas afectadas, fecha del proceso, instancia de base de datos, etc).
