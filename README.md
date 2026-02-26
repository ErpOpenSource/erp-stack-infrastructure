# ERP Infrastructure Stack

Este repositorio gestiona la infraestructura necesaria para el funcionamiento del ERP, utilizando un enfoque de **Infraestructura como Código (IaC)**.

## 🛠 Tecnologías Principales
* **Base de Datos:** PostgreSQL (Persistencia de datos)
* **Caché/Queues:** Redis (Rendimiento y mensajería)
* **Orquestación:** [Pendiente decidir: Docker Compose / Kubernetes]

## 🏗 Arquitectura de Escalabilidad
Para garantizar que el ERP crezca sin fricciones:
1. **PostgreSQL:** Configuración pensada para futuras réplicas de lectura.
2. **Redis:** Implementación preparada para modo Cluster o Sentinel.

## 🚀 Despliegue Rápido
(Aquí añadiremos los comandos conforme definamos las herramientas en el siguiente paso).
