# 🐘 Apache Kafka

Este repositorio reúne mis apuntes teóricos, scripts de configuración y ejercicios prácticos (Ejercicios y PostWorks) creados para dominar la arquitectura de **Apache Kafka**.

El código está implementado principalmente en **Python**, abarcando desde la creación de productores y consumidores básicos hasta la gestión de grupos de consumo y despliegue de infraestructura con Docker.

---

## 📚 Contenido

### 1. Arquitectura & Conceptos Core

#### 📘 Teoría

* **Arquitectura del Clúster:** Brokers, Zookeeper y el rol del Controller.
* **Modelo de Datos:** Topics, Particiones (Partitions), Segmentos y Réplicas.
* **Actores:**
    * **Producers:** Estrategias de envío (Fire-and-forget vs. Síncrono/Asíncrono) y Acks.
    * **Consumers:** Consumer Groups, offsets (`__consumer_offsets`) y rebalanceo.
* **Semántica de entrega:** At-most-once, At-least-once y Exactly-once.
* **Infraestructura:** Despliegue de servicios mediante `docker-compose`.
  

### 2. Desarrollo con Python

#### 🧪 Ejercicios Prácticos (`/Ejercicios`)

Scripts enfocados en la implementación base del cliente de Kafka en Python:

* **Configuración del Cliente:** Conexión a Brokers y serialización de datos.
* **Productores (Producers):**
    * Envío de mensajes de texto simple.
    * Uso de claves (`keys`) para garantizar el orden en particiones.
    * Serialización JSON para envío de objetos estructurados.
* **Consumidores (Consumers):**
    * Suscripción a Topics y "polling" de mensajes.
    * Lectura desde el inicio (`earliest`) vs. tiempo real (`latest`).
    * Manejo básico de errores y desconexiones.

#### 🚀 Proyectos de Refuerzo (`/PostWork`)

Casos de uso más avanzados para consolidar el conocimiento:

* **Simulación de Streaming:** Generación de flujos de datos continuos (ej. sensores o transacciones).
* **Consumer Groups:** Levantar múltiples consumidores para procesar una misma partición en paralelo.
* **Transformación en vuelo:** Procesamiento sencillo del dato antes de consumirlo o reenviarlo.


### 🛠 Despliegue Rápido

El repositorio incluye un archivo `docker-compose.yml` para levantar el entorno localmente.

1. **Levantar servicios:**
   ```bash
   docker-compose up -d
