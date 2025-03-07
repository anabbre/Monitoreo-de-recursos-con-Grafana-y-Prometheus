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
- En **Grafana**: Agregué el origen de datos de Prometheus para visualizar las métricas.

## Dashboard

He creado un dashboard en Grafana que visualiza las siguientes métricas:

- Uso de **CPU**
- Uso de **Memoria**
- Carga del **Sistema**


## Imágenes del Dashboard

A continuación se muestra cómo se ven las métricas en Grafana:

![image](https://github.com/user-attachments/assets/adefddc0-f605-49cb-b3e4-dfee6196e5af)
![image](https://github.com/user-attachments/assets/8dacfa31-5f16-4b5e-b037-c810f374c9a6)
