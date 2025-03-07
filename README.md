# Monitorización de recursos con Grafana y Prometheus

Este proyecto implementa un sistema de monitorización de recursos utilizando **Grafana** y **Prometheus**. El proyecto visualiza métricas del uso de CPU, memoria y carga del sistema a través de dashboards en Grafana. Además, se utiliza Docker para contenedores y WSL2 para ejecutar en Windows.  


## Tecnologías utilizadas

- **Grafana**: Herramienta para visualizar métricas.
- **Prometheus**: Sistema de monitoreo y recolección de métricas.
- **Docker**: Contenedores para ejecutar Prometheus, Grafana y Node Exporter.
- **WSL2**: Ejecutar los contenedores en un entorno Linux sobre Windows.
- **Node Exporter**: Exportador para recolectar métricas del sistema operativo.


## Instalación

1. Instalar **WSL2** en Windows:

   ```bash
   wsl --install
   ```
2. Inicia **Ubuntu**
   ```bash
   wsl.exe -d Ubuntu
   ```
4. Instala **Docker**
   ```bash
   sudo apt install docker.io -y
   ```
5. Ejecuta los contenedores:
   ```bash
   docker-compose up
   ```
Después de ejecutar esto, accede a Grafana en ```http://localhost:3000``` y Prometheus en ```http://localhost:9090```  


## Configuración

- En **Prometheus**: Usé un archivo `prometheus.yml` para configurar los targets (Grafana, node_exporter).
  
![image](https://github.com/user-attachments/assets/2b4dda32-401e-4114-9d72-2e49407afc53)  

- **Docker Compose:** Para desplegar los servicios de Grafana, Prometheus y Node Exporter, utilizamos el archivo `docker-compose.yml`.
![image](https://github.com/user-attachments/assets/606f8425-19b2-48ea-90c6-0fee50df3718)

- En **Grafana**: Agregué el origen de datos de Prometheus para visualizar las métricas.

## Dashboard

He creado un dashboard en Grafana que visualiza las siguientes métricas:

- Uso de **CPU**
- Uso de **Memoria**
- Carga del **Sistema**


## Imágenes del Dashboard

A continuación se muestra cómo se ven las métricas en Grafana:

![Uso de CPU](https://github.com/user-attachments/assets/1dd04719-0eba-4628-ae78-945c213dd91e)
![Uso de Memoria](https://github.com/user-attachments/assets/00deda92-1feb-4e45-a72b-f562e0bbd69b)  


## Conclusión

Este proyecto me ha permitido aplicar mis conocimientos sobre **monitorización** de sistemas y el uso de **Docker** para la automatización de la infraestructura. Además, me ha permitido aprender más sobre herramientas como **Prometheus** y **Grafana** para la visualización de datos.

