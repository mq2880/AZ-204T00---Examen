# Module 8 Implement API Management

## Lab: Creating a multi-tier solution by using services in Azure

1. **Nombres y apellidos:** Francisco Javier Moreno Quevedo
2. **Fecha:** 17/01/2021
3. **Resumen del Ejercicio:** Crear una Web App y un API como proxy para otros servicios con un header personalizado
4. **Dificultad o problemas presentados y como se resolvieron:** Ninguna



### Exercise 1: Creating an Azure App Service resource by using a Docker container image

Crear una **Web App**

![](./img/Captura1.jpg)

Probar desde el Swagger



![](./img/Captura2.jpg)

### Exercise 2: Build an API proxy tier by using Azure API Management

Crear un **API Management**

![](./img/Captura3.jpg)

Crear una nueva API

![](./img/Captura4.jpg)



Añadir una nueva **Operation**

![](./img/Captura5.jpg)



Añadir un nuevo Header

![](./img/Captura6.jpg)



Actualizar el Backend

![](./img/Captura7.jpg)

Probar

![](./img/Captura8.jpg)

Añadir una nueva **operation** 

![](./img/Captura9.jpg)



Probar

![](./img/Captura10.jpg)



Añadir un OutBoun Personalizado 

```
<outbound>
    <base />
    <xml-to-json kind="direct" apply="always" consider-accept-header="false" />
</outbound>
```

![](./img/Captura11.jpg)

Comprobar que el nuevo resultado es un Json

![](./img/Captura12.jpg)

Usar  **Trace** para ver la peticion enviada al servicio de BackEnd

![](./img/Captura13.jpg)

![](./img/Captura14.jpg)