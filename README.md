# Monitorización de recursos con Grafana y Prometheus

Este proyecto implementa un sistema de monitoreo de recursos utilizando **Grafana** y **Prometheus** para visualizar métricas de uso de CPU, memoria y carga del sistema a través de dashboards. Utiliza Docker para desplegar los servicios y WSL2 para ejecutar el entorno Linux sobre Windows.  

  
## Tecnologías utilizadas

- **Grafana**: Plataforma para visualizar y analizar métricas en tiempo real a través de dashboards.
- **Prometheus**: Sistema de monitoreo y recolección de métricas, se integra con Grafana para graficar los datos.
- **Docker**: Contenedores que facilitan la ejecución de los servicios de Prometheus, Grafana y Node Exporter de forma aislada.
- **WSL2**: Proporciona un entorno Linux sobre Windows, ideal para ejecutar contenedores Docker en un sistema Windows.
- **Node Exporter**: Herramienta que recoge métricas sobre el hardware y el sistema operativo, usada por Prometheus.


## Instalación

1. Instalar **WSL2** en Windows:
   ```bash
   wsl --install
   ```
2. Inicia **Ubuntu** con:
   ```bash
   wsl.exe -d Ubuntu
   ```
4. Instala **Docker**. Una vez dentro de Ubuntu, instala Docker con: 
   ```bash
   sudo apt install docker.io -y
   ```
5. Ejecuta los contenedores. Navega al directorio del proyecto y ejecuta los contenedores con: 
   ```bash
   docker-compose up
   ```
Esto descargará las imágenes necesarias y pondrá en marcha Prometheus y Grafana.  

  
![image](https://github.com/user-attachments/assets/ebb2de9b-c3ca-411e-9956-b89040cdf7bf)


  
Accede a Grafana en ```http://localhost:3000``` y Prometheus en ```http://localhost:9090```  


## Configuración

- En **Prometheus**: Se utiliza el archivo prometheus.yml para configurar los targets, que incluyen Prometheus, Grafana y Node Exporter.
  
![image](https://github.com/user-attachments/assets/116a7060-c608-4f19-83b3-3fa2ba2a5305)

- **Docker Compose:** Usamos el archivo docker-compose.yml para gestionar la orquestación de los servicios de Grafana, Prometheus y Node Exporter. Esto simplifica la ejecución de los contenedores.

![image](https://github.com/user-attachments/assets/ce152a7a-033f-4606-8d12-e771ea405775)  


- En **Grafana**: Configuramos el origen de datos de Prometheus para permitir la visualización de las métricas. A continuación, se explica cómo se configuran los servicios.

  
## Dashboard en Grafana

Este proyecto incluye varios dashboard en Grafana que visualiza tres métricas clave para el monitoreo del sistema:  


- Uso de **CPU** Visualiza la carga del procesador en tiempo real.
- Uso de **Memoria** Muestra la memoria total utilizada y disponible en el sistema.
- Carga del **Sistema** Indica la carga del sistema a lo largo del tiempo.


## Imágenes del Dashboard

A continuación se muestra cómo se ven las métricas en Grafana:

![Uso de CPU](https://github.com/user-attachments/assets/1dd04719-0eba-4628-ae78-945c213dd91e)
![Uso de Memoria](https://github.com/user-attachments/assets/00deda92-1feb-4e45-a72b-f562e0bbd69b)  


## Conclusión

Este proyecto me ha permitido aplicar mis conocimientos sobre **monitoreo de sistemas**, el uso de **Docker** para la automatización de la infraestructura y la gestión de recursos. Además, me ha ayudado a profundizar en herramientas de monitoreo como **Prometheus** y **Grafana**, ampliando mi capacidad para gestionar y visualizar métricas de un sistema de manera efectiva. 

