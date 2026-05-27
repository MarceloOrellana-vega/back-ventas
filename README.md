# 🛒 Innovatech Chile - API Backend Ventas

Este repositorio contiene el microservicio encargado de procesar las órdenes de venta del sistema **Innovatech Chile**, estructurado para ser desplegado como contenedor Docker en una arquitectura Cloud (AWS).

## 🚀 Tecnologías Utilizadas

- **Lenguaje/Framework:** Java 17, Spring Boot
- **Construcción:** Maven
- **Base de Datos:** MySQL
- **Contenedorización:** Docker & Docker Compose
- **Automatización:** GitHub Actions (CI/CD)

## 🏗️ Funcionamiento en la Arquitectura

El servicio se ejecuta en la capa de aplicación (instancia `ec2-app` en subred privada). Su función principal es recibir las solicitudes de venta generadas desde el Frontend, procesar la lógica de negocio y registrar las transacciones de manera segura en el contenedor de Base de Datos (`ec2-datos`).

## ⚙️ Persistencia de Datos

Se implementa persistencia mediante **Named Volumes** en Docker. Esto previene la pérdida de datos transaccionales de ventas, separando el ciclo de vida del contenedor del ciclo de vida de los datos almacenados.

## 🛠️ Cómo ejecutar el proyecto localmente

1. Clona el código fuente:
   ```bash
   git clone [https://github.com/MarceloOrellana-vega/back-ventas.git](https://github.com/MarceloOrellana-vega/back-ventas.git)
   ```
