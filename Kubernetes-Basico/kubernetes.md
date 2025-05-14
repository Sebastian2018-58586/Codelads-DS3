# Introducción Práctica a Kubernetes

En esta guía aprenderás paso a paso cómo desplegar y gestionar una aplicación en Kubernetes. Usare imágenes ilustrativas para comprender cada proceso.

## Preparar el entorno

En esta sección configuraremos el entorno necesario para comenzar a trabajar con Kubernetes.

![Preparar el entorno - Minikube iniciado](./Imagenes/kube1.PNG)  
*Minikube iniciado correctamente.*

![Preparar el entorno - Verificación del clúster](./Imagenes/kube2-1.png)  
*Verificación de que el clúster está funcionando.*


## Desplegando nuestra primera aplicación

Ahora crearemos y desplegaremos nuestra primera aplicación en Kubernetes utilizando un deployment.

![Crear el deployment - archivo yaml](./Imagenes/kube3-1.png)  
*Definimos el archivo de configuración del deployment.*

![Crear el deployment - aplicación desplegada](./Imagenes/kube4-1.png)  
*Aplicación desplegada correctamente con `kubectl apply`.*

![Crear el deployment - ver pods](./Imagenes/kube5-1.png)  
*Verificamos los pods en ejecución.*

![Crear el deployment - verificar servicios](./Imagenes/kube6-1.png)  
*Comprobamos que el servicio está creado y funcionando.*


### Accedemos desde el navegador

Abrimos la aplicación en el navegador utilizando la URL proporcionada por Minikube o el servicio NodePort.

![Acceder desde el navegador - vista en navegador](./Imagenes/kube7.PNG)  
*La aplicación se muestra correctamente en el navegador.*


### Escalamos la aplicación

Aumentamos la cantidad de réplicas para escalar horizontalmente la aplicación.

- Aumentamos el número de réplicas a 3 con el siguiente comando:

![Aumentar el número de replicas](./Imagenes/kube8-1.png)

