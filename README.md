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
   ```wsl.exe -d Ubuntu
   ```
3. Instala **Docker**
   ```sudo apt install docker.io -y
   ```
4. Ejecuta los contenedores:
   ```docker-compose up
   ```
Después de ejecutar esto, accede a Grafana en ```http://localhost:3000``` y Prometheus en ```http://localhost:9090```  


## Configuración

- En **Prometheus**: Usé un archivo `prometheus.yml` para configurar los targets (Grafana, node_exporter).
- En **Grafana**: Agregué el origen de datos de Prometheus para visualizar las métricas.
