# Requerimientos Kubernetes

Necesito ayuda con el siguiente requerimiento: Crear los siguientes recursos en kubernetes:

✅ Crear un namespace (donde desplegará sus workloads) y establecer en este un default request and limits.

✅ Crear 3 workloads de tipo Deployment para desplegar el frontend, el backend y la base de datos de una aplicación cualquiera.

✅ Definir un resource quota de tal manera que no se puedan generar, en el namespace definido previamente, más deployments, que los generados en el paso anterior. Además, deberá limitar la creación de secrets, configMaps y services.

✅ Con la finalidad de aislar el ciclo de vida de la data del ciclo de vida del pod, el contenedor de base de datos deberá utilizar un volumen de tipo ReadWriteOnce que se mapee contra un path del host, para ello deberá definir un PV y un PVC.

✅ Implementar health checks de tipo livenessProbe y redinessProbe para el contenedor del backend.

✅ Crear un HPA para poder escalar dinámicamente, de acorde al consumo promedio de CPU, a un máximo de 10 pods y un mínimo de 2 para el backend.

✅ Crear 2 secretos para proteger la información sensible (credenciales de base de datos) y referenciar estos valores tanto en pod del backend como en el de base de datos.

✅ Crear 2 configMap para establecer propiedades adicionales que se puedan necesitar en el backend y frontend.

✅ Crear 3 servicios tipo clusterIP, para lograr la comunicación entre los pods desplegados en los pasos anteriores.

✅ Crear 1 ingress y 1 NGINX Ingress controller para enrutar el acceso a la aplicación de frontend.

✅ Definir en el archivo config, de kubectl, un usuario que tenga permisos únicamente para visualizar los objetos del namespace en el cual fueron desplegados los recursos de las preguntas anteriores, para ello deberá definir un contexto, un rol y un rolebinding adecuados.

✅ Se requiere que la aplicación de backend obtenga información del api-server, para ello deberá definir un service acount y especificar un rol que obtenga únicamente la lista de pods de todos los namespaces.
