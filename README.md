# Prueba_ToolBox
Pruebas de api ToolBox con Postman para ejecutar en Newman

El archivo collection corresponde a la colección creada en postman y el enviroment, al ambiente.
Se realiza un pedido GET a "https://echo-serv.tbxnet.com/v1/system/ping" y GET a "https://echo-serv.tbxnet.com/v1/echo?text=test" 

Para ejecutar los casos de prueba contenidos en estos archivos, se debe hacer por Newman, ejecutando desde la consola
newman run -e ToolBox_Tests.postman_environment.json ToolBox.postman_collection.json newman

Los casos de prueba evalúan :  

Que la respuesta sea válida (código 200), que contenga body y un json
Que el content Type sea válido
Que la respuesta sea menor a 200 ms
Que el esquema sea válido

